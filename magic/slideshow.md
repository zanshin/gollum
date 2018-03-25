## Make slideshow from `jpg` files

    for p in *.jpg ; do ffmpeg -loop_input -f image2 -i $p -t 3 -r 4 -s 1080x720 -f avi - >> slides.avi ; done

For **OS X**

    `ffmpeg -f image2 -r 1/.5  -pattern_type glob -i '*.JPG' -c:v libx264 -r 30 -pix_fmt yuv420p out.mp4`

The value of `-r` is a ratio. `1/1` ia one second per frame, `1/5` is five seconds. `1/.5` is a half second.

From: https://trac.ffmpeg.org/wiki/Create%20a%20video%20slideshow%20from%20images