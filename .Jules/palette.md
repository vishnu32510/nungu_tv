## 2026-09-14 - [Flutter Ripple Obscured by Container]
**Learning:** Wrapping a colored `Container` inside an `InkWell` causes the background color to paint over the `InkWell`'s splash ripple, completely hiding the tap feedback.
**Action:** Use a `Material` widget as the ancestor to provide the background color and borders, and wrap the `Padding` with the `InkWell`.
## 2026-09-17 - [Accessibility Semantics & Ink Ripple Interactions]
**Learning:** For users employing screen readers on TV/Desktop, generic interactive containers must be explicitly labeled. Also, implementing visual ripple feedback over a gradient background requires a `Material` -> `Ink` -> `InkWell` structure rather than a simple `Container` to prevent the ripple from being obscured.
**Action:** Always wrap interactive gesture hotspots in `Semantics` with `button: true`. When a background color or gradient is needed alongside an `InkWell`, apply it using the `Ink` widget child of a `Material` widget.
