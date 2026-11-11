# ASCII Mirror
 
A live webcam mirror that turns you into ASCII art in real time, right in the browser.
 
Every frame from your webcam is shrunk down, and each pixel's brightness is swapped for a text character.

## How it works
 
1. **Camera:** `getUserMedia` asks for webcam access and plays the feed in a hidden `<video>` element.
2. **Shrink:** each frame is drawn onto a tiny hidden `<canvas>`, so one pixel equals one character. The number of rows is halved because characters are about twice as tall as they are wide.
3. **Read pixels:** `getImageData` returns the red, green and blue values of every pixel.
4. **Brightness to character:** each pixel's brightness (0 to 1) picks a character from RAMP string.
5. **Display:** the characters are joined into lines and shown in a `<pre>` element, which keeps spaces and line breaks exactly as written.
6. **Loop:** `requestAnimationFrame` repeats this about 60 times a second.


**Have fun!!!**
<p align="center">
  <img width="750" alt="ASCII Mirror demo" src="https://github.com/user-attachments/assets/79aceca9-bbb3-4b79-90bc-995d07bd5b34" />
</p>

