# DunDun Jewel on Render

This repository contains the completed interactive jewelry page. The
FBX-derived models, reference photos, materials, stone controls and
animations are packaged under public/. Large model and image assets are
separate files so the initial HTML loads quickly and browsers can cache them.

## Render settings

- Type: Static Site
- Name: dundun-jewel
- Build command: test -f public/index.html
- Publish directory: public
- No web server, database, disk or environment secrets are required.
- Static sites have no compute plan; bandwidth and build usage still count
  against the Render workspace allowance.

Connect this repository to Render with a Blueprint (render.yaml), or create a
Static Site with the settings above. Share only the actual HTTPS URL returned
by a successful Render deployment. The service name does not guarantee a URL.

Three.js and web fonts load from their existing external CDNs. Browsers need
WebGL 2 or WebGPU. Material changes and stone placements are local to each
visitor's browser; "保存设计设置" downloads a local JSON file.

To update this package, run build-page.py and prepare-render.py in the source
project, then publish the updated public/ directory.

Official documentation: https://render.com/docs/static-sites
