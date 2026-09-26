## 2026-09-14 - [Flutter Ripple Obscured by Container]
**Learning:** Wrapping a colored `Container` inside an `InkWell` causes the background color to paint over the `InkWell`'s splash ripple, completely hiding the tap feedback.
**Action:** Use a `Material` widget as the ancestor to provide the background color and borders, and wrap the `Padding` with the `InkWell`.

## 2026-09-26 - [Flutter GestureDetector Accessibility limitations]
**Learning:** In Flutter UI development, `GestureDetector` lacks native keyboard focus and visual feedback. Using `InkWell` provides native keyboard focus and visible splash ripples. However, when placing `InkWell` over colored backgrounds or borders, those styles will paint over the ripple. Wrapping the `InkWell` inside a `Material` widget and an `Ink` widget for background/borders solves this.
**Action:** Use `Material` -> `Ink` -> `InkWell` pattern for accessible interactive areas instead of `GestureDetector`.
