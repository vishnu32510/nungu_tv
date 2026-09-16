## 2026-09-14 - [Flutter Ripple Obscured by Container]
**Learning:** Wrapping a colored `Container` inside an `InkWell` causes the background color to paint over the `InkWell`'s splash ripple, completely hiding the tap feedback.
**Action:** Use a `Material` widget as the ancestor to provide the background color and borders, and wrap the `Padding` with the `InkWell`.

## 2026-09-16 - [Flutter Accessibility with Material & Semantics]
**Learning:** When making custom container buttons in Flutter, using a `GestureDetector` removes semantic keyboard access and tap ripples.
**Action:** Use `Semantics` wrapping a `Material`, `Ink`, and `InkWell` to gain default hover, ripple states, and screen reader labels. Ensure the `InkWell` handles padding directly to get the cursor states working out of the box.
