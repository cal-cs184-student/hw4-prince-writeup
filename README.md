# CS184/284A Fall 2026 Homework 4 Write-Up

Report by Dongyang Dai and Zihan Wang, following the English report format used for the previous homework write-ups.

- Main page: `index.html`
- GitHub Pages URL: https://cal-cs184-student.github.io/hw4-prince-writeup/
- Assignment requirements: https://cs184.eecs.berkeley.edu/fa26/hw/hw4/deliverables/
- Implementation repository: https://github.com/cal-cs184-student/hw4-prince

The page uses relative image paths, responsive galleries, and print styles for PDF export. Open `index.html` in a browser, or serve this directory with `python3 -m http.server 8000`. The Inter webfont loads from Google Fonts. The page and its equations also render with local fonts. Use the browser print dialog to save a PDF and inspect that all equations, images, and captions appear.

## Asset and parameter notes

- The GUI displays internal density divided by 10. The default scene value is 150; the GUI shows 15.
- The four Part 4 parameter runs use the original simulator and its Normal shader offscreen. Each run starts from `selfCollision.json` with seed 1 and uses the same camera. The screenshots show frame 60 with 90 frames per second, 30 substeps per frame, and 0.2% damping.
- `high_density_normal.png` shows default GUI density 15, not 150. The density comparison uses `high_density_frame.png`, whose GUI shows 150.
- `high_damping_normal.png` shows default damping 0.2%. The report uses high-damping captures whose GUI shows approximately 0.666667% instead.
- The bump/displacement comparison uses the custom dot map `assets/part5/task4_sphere_heightmap.png` through the texture-2 slot, rather than the starter height map.
- The Iridescent Silk and Blinn–Phong comparison images use the same offscreen camera, default lighting, and frame 360 of `sphere.json` (four simulated seconds).
- The report describes the current code, including the single-bucket self-collision search and the stretch-limit pass over all stored springs.

Repo184 configures GitHub Pages from the repository root. Keep implementation source and private material out of this public write-up repository. The course also requires a PDF submission to Gradescope.
