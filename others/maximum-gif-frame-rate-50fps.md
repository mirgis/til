# Limitation of a GIF

One day, I was working on a simple countdown animation and exported the final result as a GIF. I set the frame rate to 60 frames per second (FPS), which translates to a 1/60-second delay between frames, or roughly 16.7 milliseconds. However, the resulting countdown animation played slightly slower than real-time. After some investigation, I discovered an inconvenient **limitation of the GIF** in web browsers: it caps the **maximum frame rate at 50 frames per second**. You can read more about this limitation in the article below[^1], which says:

> ...no web browser out there right now (in 2020) supports displaying gifs higher than 50FPS...

### References
[^1]: [Buttery Smooth "10fps"](https://wunkolo.github.io/post/2020/02/buttery-smooth-10fps/) by Wunk
