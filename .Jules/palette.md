## 2026-09-14 - [Flutter Ripple Obscured by Container]
**Learning:** Wrapping a colored `Container` inside an `InkWell` causes the background color to paint over the `InkWell`'s splash ripple, completely hiding the tap feedback.
**Action:** Use a `Material` widget as the ancestor to provide the background color and borders, and wrap the `Padding` with the `InkWell`.

## 2024-05-18 - Replacing GestureDetector for Accessibility
**Learning:** `GestureDetector` in Flutter lacks native keyboard focus and visible focus/hover states out of the box, breaking accessibility for non-pointer users. It also lacks visual ripple feedback, which can leave users unsure if an action was registered.
**Action:** Always replace `GestureDetector` with an `InkWell` when wrapping actionable UI elements like custom buttons. To retain styled backgrounds or gradients, wrap the `InkWell` in an `Ink` widget, and ensure the entire block has a `Material` widget ancestor (with `color: Colors.transparent` if necessary).
