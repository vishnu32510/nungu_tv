## 2026-09-14 - [Flutter Ripple Obscured by Container]
**Learning:** Wrapping a colored `Container` inside an `InkWell` causes the background color to paint over the `InkWell`'s splash ripple, completely hiding the tap feedback.
**Action:** Use a `Material` widget as the ancestor to provide the background color and borders, and wrap the `Padding` with the `InkWell`.

## 2026-09-14 - [Flutter GestureDetector Lacks Feedback]
**Learning:** `GestureDetector` on its own lacks native keyboard focus and visual feedback when interacted with.
**Action:** For accessibility and visual feedback, replace it with a `Material` widget ancestor, an `Ink` widget for background/borders, and `InkWell` to ensure native keyboard focus and visible splash ripples.
