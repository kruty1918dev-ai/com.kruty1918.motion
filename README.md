# com.kruty1918.motion

Reusable motion primitives extracted from Moyva: `MotionEaseKind`/`MotionEaseEvaluator`,
`EntityMotion` (slot-based position/yaw/scale/punch/custom motions on a
MonoBehaviour), `PathTraversalMotion` (waypoint traversal).

## Install (Unity Package Manager)

Package Manager → **+** → **Add package from git URL**:

```
https://github.com/kruty1918dev-ai/com.kruty1918.motion.git
```

or in `Packages/manifest.json`:

```json
"com.kruty1918.motion": "https://github.com/kruty1918dev-ai/com.kruty1918.motion.git#v0.1.0"
```

The repository is private — Git credentials (PAT / Git Credential Manager)
are required on every machine that resolves the package.

## API surface

| Type | Purpose |
|---|---|
| `MotionEaseKind` / evaluator | Named easing curves evaluated without DOTween |
| `EntityMotion` | Slot-based motion component — concurrent position/yaw/scale/punch/custom channels |
| `PathTraversalMotion` | Waypoint/path traversal for world entities |

## Model

No game-specific dependencies; compose via your own installer/DI. Slots let a
unit play "walk to tile" and "hit-punch" simultaneously without overriding
each other.
