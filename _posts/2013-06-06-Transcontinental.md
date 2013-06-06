---
layout: post
title: Transcontinental 
---

If you've worked with the Core Location class **CLPlacemark**, you might have noticed that despite having properties like 'ISOCountryCode' or 'ocean', there is not a property, nor an easy way to obtain its corresponding **continent**. 

To solve this, I've programmed a small category on CLPlacemark that allows you to obtain its continent with a simple method:


``` objective-c

NSString *continentForPlacemark = [paramPlacemark continent];

```

The continent is retrieved from a table using the ISOCountryCode property of the placemark. Also a simple Country-to-Continent decoder is available:

``` objective-c

NSString *expectedContinent = [continentDecoder continentForCountryCode:@"PL"];

```

The name of this project is **'[Transcontinental](https://github.com/Hecktorzr/Transcontinental)'** and is available as a MIT Licensed repository in Github. It also includes a simple example which should make its use clear as water:

![Transcontinental Example Project](/posts_images/2013-06-06-Transcontinental-00.png)


Enjoy!

