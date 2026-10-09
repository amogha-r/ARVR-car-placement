# Road Vehicle AR

WebXR + three.js app that places life-size cars, trucks and buses on a real road through your phone camera. One file, no build step, no assets.

## Run locally
```bash
cd ar-road-vehicles
npx serve .          # desktop preview at http://localhost:3000
```
WebXR AR needs **HTTPS**. To test on your phone, use a tunnel: `npx localtunnel --port 3000` (or `ngrok http 3000`).

## Deploy (pick one)
- **GitHub Pages**: push `index.html` to a repo, Settings > Pages > deploy from branch. HTTPS is automatic.
- **Netlify / Vercel / Cloudflare Pages**: drag-and-drop the folder.

## Device support
- Android + Chrome + ARCore (Google Play Services for AR): full AR.
- iOS Safari does not support WebXR immersive-ar. Use the desktop-style preview, or open in a WebXR-capable iOS browser app.
- Desktop: 3D preview with a sample road (drag to orbit, scroll to zoom, click to place).

## Use
1. Tap **Start AR**, grant camera permission.
2. Scan the road slowly until the yellow ring appears.
3. Pick vehicle, set **Heading** (direction) and **Scale** (real size is 1.0×), turn on **Lane guide** to align with the lane.
4. Tap the road to place. **Undo** / **Clear all** to remove.

## Customise
Edit `SPECS` and `buildVehicle()` in `index.html` to change sizes/colours, or swap in a glTF model with `GLTFLoader` (import from `three/addons/loaders/GLTFLoader.js` by adding it to the import map).
