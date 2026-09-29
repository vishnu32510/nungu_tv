## 2026-09-14 - [Flutter Ripple Obscured by Container]
**Learning:** Wrapping a colored `Container` inside an `InkWell` causes the background color to paint over the `InkWell`'s splash ripple, completely hiding the tap feedback.
**Action:** Use a `Material` widget as the ancestor to provide the background color and borders, and wrap the `Padding` with the `InkWell`.

## 2024-06-25 - Replace GestureDetector with Material/Ink/InkWell
**Learning:** GestureDetector lacks native keyboard focus and visible splash ripple.
**Action:** Always replace GestureDetector with Material, Ink, and InkWell for native keyboard focus and visible splash ripple feedback.
