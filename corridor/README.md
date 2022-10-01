## Corridor Write Up

Firstly, this relates to the web challenge, so dont need to do a scanning, Let's access to the website

![](https://raw.githubusercontent.com/K3v1ne/ctf-wu/main/corridor/images/2143922241f34517fb68adbc990a4d75.jpg)

The first thing i see is a weird corridor

I was looking for the page source and found some interesting hashes

![](https://raw.githubusercontent.com/K3v1ne/ctf-wu/main/corridor/images/912380337da589474dfd4583e61bd69c.jpg)

So what can i do with a hash?
I tried to crack these hash and this is the result

![](https://raw.githubusercontent.com/K3v1ne/ctf-wu/main/corridor/images/ca3a4fa6f51b1bcd1a9c62576ee01a23.jpg.png)

Oh so that's just the numbers

Now do some IDOR exploit, i wrote a simple md5 generator using python and encrypt the number "0"

![](https://raw.githubusercontent.com/K3v1ne/ctf-wu/main/corridor/images/63ebac50a0051d3f6f920c5522ebadad.jpg)

Now paste the hash into the url endpoint and get the flag

![](https://raw.githubusercontent.com/K3v1ne/ctf-wu/main/corridor/images/6ea8d1d5f7f3545a18b9051a60ce5bda.jpg)
