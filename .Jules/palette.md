## 2026-09-14 - [Flutter Ripple Obscured by Container]
**Learning:** Wrapping a colored `Container` inside an `InkWell` causes the background color to paint over the `InkWell`'s splash ripple, completely hiding the tap feedback.
**Action:** Use a `Material` widget as the ancestor to provide the background color and borders, and wrap the `Padding` with the `InkWell`.

## 2024-03-24 - Accessibility Gap in GestureDetector
**Learning:** In Flutter, `GestureDetector` works well for mouse and touch interactions but inherently lacks built-in keyboard focus management, visual feedback (like hover and splash), and accessibility affordances (like tab-navigation) out of the box.
**Action:** When creating primary call-to-action or navigational tap targets, wrap the target inside a `Material` widget and use `InkWell` (and `Ink` for background decoration) instead of `GestureDetector` + `MouseRegion`. This immediately grants tab focus, enter-key trigger support, and hover/splash visuals for better accessibility.
