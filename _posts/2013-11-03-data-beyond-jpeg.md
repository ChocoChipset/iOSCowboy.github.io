---
layout: post
title: The data beyond the JPEG 
---

JPEG files from a digital camera include lots of information beyond the actual picture. Camera settings, serial numbers, flash setups and more are included in one of many formats like Exif, IPTC, JFIF or TIFF.

To simplify the extraction and reading of all those properties, I've programmed **[Bravo](https://github.com/Hecktorzr/Bravo)**, an Objective-C library that extracts all the metadata available from a JPEG image and compiles it under a single NSDictionary object.

It's use requires calling a single method to call: 

```obj-c
NSDictionary *metadataProperties = [[BRavoExifManager sharedManager] extractMetadataFromJPEG:imageData];
```

and is available under the MIT License.
