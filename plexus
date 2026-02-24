PVector[] particles;
PVector[] motion;
int num = 150;
PFont font;
void setup() {
  size (1080, 1080);
  noStroke();
  particles = new PVector[num];
  motion = new PVector[num];
  for (int i = 0; i < num; i++) {
    particles[i] = new PVector(random(width), random(height));
    motion[i] = new PVector(random(-1, 1), random(-1, 1));
  }
}
void draw() {
  background(255);
  for (int i = 0; i < num; i++) {
    particles[i].add(motion[i]);
    particles[i].x = (particles[i].x + width) % width;
    particles[i].y = (particles[i].y + height) % height;
    ellipse(particles[i].x, particles[i].y, 5, 5);
    fill(0, 0, 255);
    stroke(0, 0, 255);
    for (int j = 0; j < num; j++) {
      float d = dist(particles[i].x, particles[i].y, particles[j].x, particles[j].y);
      if (d < 75 && d> 1) {
        line(particles[i].x, particles[i].y, particles[j].x, particles[j].y);
      }
    }
  }
  //saveFrame("out/plexus_###.png");
}
