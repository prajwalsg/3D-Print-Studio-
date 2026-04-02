# 3D-Print-Studio-
🛠️ Procedural 3D Shape Generation
Text-to-Geometry Parser: Generates basic 3D primitives (cubes, spheres, cylinders, toruses) directly from text prompts (e.g., "hollow cube 10cm", "arch bridge").

2D-to-3D Glyph Extrusion: Uses the HTML5 Canvas API to render letters and numbers in 2D, samples the pixel data, and procedurally extrudes them into 3D voxel-style meshes.

🔍 Real-Time Overhang Analysis
Face-Level Angle Calculation: Uses vector mathematics and cross-products to calculate the normal of every individual triangle on the mesh relative to the Z-up build direction.

Visual Risk Mapping: Dynamically recolors the mesh based on printability risk:

Blue: Safe (self-supported)

Orange: Marginal (35°–45°)

Red: Critical overhang (>45°, requires support)

Customizable Thresholds: Users can manually adjust the critical overhang angle threshold (default is 45°) to simulate different material or printer constraints.

🏗️ Dynamic Support Structure Generation
Smart Placement: Automatically identifies critical overhang faces and calculates optimal coordinate placement for support pillars, using spacing algorithms to prevent overlapping.

Multiple Support Types:

Block: Thick, heavily braced columns for maximum stability.

Lattice: Diagonal cross-struts that provide strong thermal conduction with less material.

Tree: Branching supports that minimize contact area and reduce powder waste.

Adjustable Density: Sliders to control the thickness and density of the generated support geometries.

🔄 Build Orientation Optimizer
Automated Scoring: Tests the object across 6 standard rotational axes (e.g., +X 90°, Flip Y).

Powder Saving Calculation: Compares the overhang surface area of all orientations and automatically recommends the one that requires the least amount of support material.

🖥️ Interactive 3D Workstation (Three.js)
Custom Camera Controls: Orbit (left-click), pan (right-click), and zoom (scroll) built natively.

Raycaster Inspection: Hovering over the mesh uses raycasting to display the exact angle of the specific triangle under the cursor.

Multiple View Modes: Toggle between Solid, Wireframe, Overhang isolation, Support isolation, and X-Ray (translucent) modes.

Layer Simulation: An animated "layer line" effect to visualize the slice progression of the print.

🎨 Zero-Dependency Custom UI
Pure Vanilla CSS: Built entirely without CSS frameworks (no Tailwind or Bootstrap), utilizing CSS Variables, Flexbox, and Grid for a highly responsive, modern dark-mode dashboard.

Real-time Metrics Dashboard: Instantly updates face counts, support estimates, and risk percentages as the user rotates or scales the model.
