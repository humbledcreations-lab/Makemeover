# MakeMeOver — Live Trace Mode (Android browser prototype)

**Signature feature: Trace Mode.** Glowing dashed makeup placement paths follow facial landmarks from the live front camera. The current version includes three guided trace stages for six eyeliner looks (cat, classic wing, kitten, puppy, thin upper lash line, graphic wing) and five eyeshadow looks (natural, smokey, halo, cut crease, shimmer), plus face-area guides for blush, contour, concealer, foundation, and lips. Trace Mode is turned **on** by default. Use the left/right buttons inside the Trace Mode panel to move through individual application actions. You can also select one eye at a time.

The other features remain: live selfie mirror, makeup preview, adjustable mirror size, zoom, makeup strength, face preparation and foundation/concealer order guidance, and the interactive illustrated brush library.

## Upload and open on Android

1. Sign in to GitHub and open your public **makemeover** repository.
2. Upload **only `index.html`** to the repository root, or replace your existing `index.html` with this latest version. GitHub Pages does not use the ZIP file as the website.
3. Under **Settings → Pages**, choose **Deploy from a branch → main → / (root)** and save.
4. After GitHub Pages publishes, use `https://YOUR-USERNAME.github.io/makemeover/` in Chrome on Android (do not open the local `file://` copy).
5. Tap **Start Mirror** and grant camera permission. Face the camera in even lighting. Advance to **Eyeshadow styles** or **Eyeliner styles**, choose the look, and tap the trace arrows to move between instruction stages.
6. To show only the glowing guide, select **Guides only**. To show a virtual cosmetic preview without tracing, select **Virtual makeup only**. You can toggle Trace Mode off and on.

## Important limitations

- Live face tracking depends on a downloaded MediaPipe model and browser support. The first load needs internet. If it cannot load, the selfie camera may still work without overlays.
- These are **approximate illustration guides**, not calibrated, clinically validated, or millimeter-accurate paths. Eye anatomy, pose, lighting, and camera angle can affect alignment. Avoid applying makeup to the waterline or inside the eye. Do not use the on-screen image as the only safety guide around the eyes.
- The prototype cannot tell whether a user has successfully drawn a line or blended their makeup, and the animated brush demonstration is illustrative only.
- Camera processing is local to your browser in this code, which has no photo upload or saving function. External servers provide the MediaPipe JavaScript and model and may receive normal network requests.
- This is a website, not a compiled Android APK. It has been syntax checked but still needs testing on a real device.
