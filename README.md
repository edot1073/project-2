# project-2:  
Pool table with colliding balls.  (See exercise x5)

Three pool balls, each with a different color and a different number on it.  

Balls move around a rectangular pool table,  
bouncing off sides of table (left, top, right, bottom),  
and colliding "elastically" with one another.

In an "elastic" collision, the velocities are exchanged  
(i.e. the DX and DY of one ball become the DX and DY of the other ball!)  

Add a **button** to reset all balls to a position on the right side of the table,  
and give them each a random velocity.



float gravity = 9.0;
float mass = 2.0;

int angle = 0;
void setup() {
  size(180, 180);
  stroke(0);
 
  
  fill(255, 126);

}

void draw () {
  background(255, 64, 0);
  line(80,0, mouseX, mouseY);
 if (mousePressed == true) {
    angle += 1;
   float val = cos(radians(angle)) * 12.0;
 for (int a = 0; a < 360; a += 5) {
  float xoff = cos(radians(a)) * val;
      float yoff = sin(radians(a)) * val;
      fill(175);
      stroke(14,35,355);
      ellipse(mouseX + xoff, mouseY + yoff, val, val);
 fill(250);
 stroke(95,174,9);
    ellipse(mouseX, mouseY, 75, 2);
    
  
  } 
}
 }
