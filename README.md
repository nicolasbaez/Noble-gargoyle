# Noble-gargoyle
Boom!

![buh](https://github.com/nicolasbaez/Noble-gargoyle/blob/main/xp023.gif)
```javascript
setup = (_) => createCanvas((w = 500), w, WEBGL);
draw = (_) => {
  rotateX(1);
  rotateY(0.5);
  clear();
  noFill();
  for (i = 0; i < 4 * PI; i += 0.1) {
    stroke(255, map(i, 0, 12, 255, 64), 0);
    push();
    translate(0, 0, map(sin(w + i), -1, 1, -62, 62));
    circle(0, 0, i * 32);
    pop();
  }
  w -= 0.05;
};
keyPressed = (_) => {
  if (key === "s") {
    saveGif("xp023.gif", 251, { delay: 0, units: "frames" });
  }
};
