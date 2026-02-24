# plexus

Particle Plexus
An animated particle network simulation where floating particles connect with lines when in proximity.

# How it Works
150 particles are spawned at random positions and drift across a 1080×1080 canvas with random velocities. Each frame, every particle checks its distance to every other particle — if two particles are within 75 pixels of each other, a blue line is drawn between them. Particles wrap around the edges of the canvas so they never disappear.

# Configuration
Adjust these variables in the code to customize the output:

num — number of particles (default: 150)
d < 75 — connection distance threshold (default: 75px)
random(-1, 1) — particle speed range (default: -1 to 1)
ellipse(..., 5, 5) — particle size (default: 5px)
fill(0, 0, 255) — particle and line color (default: blue)

# Saving Frames

To export frames as images, uncomment the following line at the bottom of draw():

"javasaveFrame("out/plexus_###.png");"

Make sure an out/ folder exists in your sketch directory before running.

# License
MIT
