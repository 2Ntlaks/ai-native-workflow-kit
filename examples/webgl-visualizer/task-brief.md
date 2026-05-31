# Task Brief: WebGL Visualizer

## Objective

Correct aspect-ratio handling in a WebGL teaching visualizer so shapes do not stretch when the browser window or device pixel ratio changes.

## Background

The visualizer is used for teaching graphics concepts. Distorted output makes lessons about projection and transforms harder to explain.

## Scope

In scope:

- Inspect canvas resize code, viewport setup, and projection matrix calculation.
- Update resize handling for CSS size and device pixel ratio.
- Add a small regression check if render math is testable.
- Document any manual screenshot check.

Out of scope:

- Replacing WebGL with a new rendering library.
- Redesigning controls or shaders unrelated to aspect ratio.

## Autonomy Level

A2.

## Acceptance Criteria

- [ ] Canvas backing size matches displayed size and device pixel ratio.
- [ ] `gl.viewport` updates after resize.
- [ ] Projection aspect ratio uses current canvas dimensions.
- [ ] Manual resize check shows circles remain circular or grid squares remain square.

## Verification

```bash
npm test
```

Manual check: resize the browser from wide to narrow and capture before/after evidence.

## Human Review Focus

Confirm the fix teaches the projection concept clearly and does not hide the math in an unnecessary abstraction.
