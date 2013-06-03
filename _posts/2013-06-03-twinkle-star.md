---
layout: post
title: TwinkleStar
---

[TwinkleStar](https://github.com/Hecktorzr/TwinkleStar) is a small iOS library I wrote to handle device's LED through a convenient singleton.
It supports turning it on and off (again), setting up a strobe frequency and determining if a device counts with an integrated LED. 
All conveniently wrapped in a cool singleton with the following interface:

``` objective-c

@property CGFloat flashFrequency;
@property BOOL isFlashLEDAvailable;

+(HZTwinkleStar *)sharedTwinkleStar;

-(void)turnFlashLEDOn;
-(void)turnFlashLEDOff;

```

To make usage clear I've included an example project.
<center>
![TwinkleStar Example Project](/posts_images/2013-06-03-twinkle-star-00.png)
</center>
