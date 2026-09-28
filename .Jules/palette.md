## 2026-09-14 - [Flutter Ripple Obscured by Container]
**Learning:** Wrapping a colored `Container` inside an `InkWell` causes the background color to paint over the `InkWell`'s splash ripple, completely hiding the tap feedback.
**Action:** Use a `Material` widget as the ancestor to provide the background color and borders, and wrap the `Padding` with the `InkWell`.
## 2024-05-18 - Native Ripple Effects on Custom Buttons
**Learning:** Custom UI buttons built with `GestureDetector` lack native visual feedback (splash ripples) and keyboard focus states. Wrapping a `GestureDetector` with `MouseRegion` isn't enough; using Flutter's native `Material`, `Ink`, and `InkWell` is necessary to ensure focus visibility and interactive feedback.
**Action:** When creating custom styled buttons with gradients or borders, replace `GestureDetector` with `Material` -> `Ink` (for styles) -> `InkWell` (for interaction/ripple) instead of standard containers to ensure a11y focus and native interaction feel.
