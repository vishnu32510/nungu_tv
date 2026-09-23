## 2026-09-14 - [Flutter Ripple Obscured by Container]
**Learning:** Wrapping a colored `Container` inside an `InkWell` causes the background color to paint over the `InkWell`'s splash ripple, completely hiding the tap feedback.
**Action:** Use a `Material` widget as the ancestor to provide the background color and borders, and wrap the `Padding` with the `InkWell`.
## 2026-10-27 - [GestureDetector vs InkWell for Accessibility]
**Learning:** `GestureDetector` lacks native keyboard focus and visible tap feedback (splash ripples) which is a significant accessibility issue, especially on the web.
**Action:** Replace `GestureDetector` with `InkWell` for clickable elements. When styling is needed, use `Material` as the ancestor and `Ink` to provide decorations like gradients or borders to avoid obscuring the splash ripple.
