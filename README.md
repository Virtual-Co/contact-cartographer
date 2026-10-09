# Contact Cartographer

A static, offline chain reaction puzzle inspired by the local-contact reasoning idea in RiCo. It combines a small 2D polygon collision approximation with a visible contact-to-motion trace and a coarse center-response comparison.

## Run locally

Open `demo/index.html` directly in a modern browser. No build step, server, network access, or external assets are required.

Drag the bodies to arrange them and drag the lime handle to aim and set launch strength. Keyboard: focus the board, press 1–3 to select a body, arrows to move it, Shift+arrows to aim, and +/− to adjust strength. Choose **Launch** to run the puzzle, **Reset** to restore the preset, or **Replay** to rerun the same setup. The comparison toggle switches the launch response to a coarse center-to-center heuristic.

The simulation uses three procedural convex polygons, no more than five bodies, no more than eight vertices per body, a fixed 1/120 second step, at most 600 steps per launch, and a display pixel ratio capped at 2. Those are implementation limits, not accuracy claims.

## Research credit and limits

Inspired by Ruixiang Ouyang, Guanren Qiao, Fansen Meng, Yueci Deng, Ruixing Jin, Kui Jia, and Guiliang Liu, [“RiCo: Neural Simulation of Rigid-Body Interactions via Local Contact Reasoning”](https://arxiv.org/abs/2610.12333) (arXiv:2610.12333).

This is an illustrative 2D approximation, not a RiCo reproduction or validated physics. The response uses polygon overlap axes, a simplified impulse, damping, and a small contact-offset spin effect. The local contact marker is estimated from opposing polygon support vertices; it is not a clipped contact manifold or an exact surface-contact solver. The coarse marker is the center midpoint. It has no learned model, 3D surfaces, physical calibration, or accuracy validation. The coarse mode uses a center-to-center impulse and omits spin. No RiCo code or other third-party code is included.

## License

The original demo code in this repository is available under the MIT License. The paper is cited as research inspiration; no paper text or code is reproduced.

Copyright (c) 2026 Virtual Lab contributors

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
