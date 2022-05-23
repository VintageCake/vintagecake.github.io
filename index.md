## Welcome to my page!

There really isn't that much going on here at the moment, but feel free to check out some of my repositories on my GitHub! I largely just upload some of my school projects on there. 

I've recently gotten into doing a few CTFs with a group that I like, my writeups are over [here](https://github.com/VintageCake/HTB-CTF)!

If you feel like you have any critical input as to what kind of cool stuff I should put here, feel free to do so in the issues section of this page repo.

### C++ shenanigans and highlighted project

Probably one of the nicer things I've done on my GitHub is create a circuit + software solution to measure electric fences, where I meshed these small devices together to get additional range as well. For this to work, I created my own routing protocol based on RIP (but wireless).

One of the nice things you get with C++ is that unions aren't removed, so you can do fun things with picking apart individual bytes of a larger data structure - making it really easy to create fields for a protocol message.

```C++
struct route {
    byte base_flag;
    unsigned int dst_id;
    byte most_rssi;
    byte hop_count;
    unsigned int via_id;
    byte age; // Aging variable, decremented on a timer
};

typedef union route_union {
  route fields = {0x00, 0x0000, 0x00, 0x00, 0x0000, 0x00};
  byte bytes[sizeof(fields)];
} route_union;
```

Anyway, the repo can be found [here](https://github.com/VintageCake/ElectricFenceLoRa).

In addtion to this, I've implemented a few RFC standards for school assignments - I'd like to think of my TFTP server as "pretty good", this can can be found [here](https://github.com/VintageCake/1DV701_pset3), although the [HTTP server](https://github.com/VintageCake/1DV701_pset2) was by far the bigger project out of both of them. Something to note is that these are in Java, since the 1DV701 course is built on the two preceeding Java courses.

### CTFs!

So far, I've only participated in a few CTFs, with HTB being the only CTF having a writeup currently. There will be more to come! :)

### Contact
<lovesamuelsson@outlook.com>
