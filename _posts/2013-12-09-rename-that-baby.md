---
layout: post
title: Rename That Ugly Baby
published:false
---

For both persons and programming variables, a good name is an invitation to a prosperous life.
Luckily for your Objective-C variables, their name is easier than the legal trouble of changing your own name to 'Max Power'. Find out how: 

## 'Edit All In Scope' 

## Xcode's Refactor



## Avoid Breaking Stuff While Renaming Ugly Names

0. The first strategy is not to trust Xcode's refactor by a 100% and run a project-wide search for the soon-to-be-replaced name. Look particularly for occurrences inside strings passed to NSPredicates or used in KVO. 
	
	It's pretty easy to miss those ones just to find them later as an unexpected ```NSUndefinedKeyException```. Not good.

1. To help Xcode's refactor tool, use the function [NSStringFromSelector()](https://developer.apple.com/library/ios/documentation/cocoa/reference/foundation/Miscellaneous/Foundation_Functions/Reference/reference.html#//apple_ref/c/func/NSStringFromSelector). 


	Instead of simply passing a string, 

	```
	self.name = [aDecoder decodeObjectForKey:@"name"];
	```	
	
	NSStringFromSelector gives Xcode a little bit more of context on what that particular string means and a hint to include that occurrence in case of renaming. 
	
	```
	self.name = [aDecoder decodeObjectForKey:NSStringFromSelector(@selector(name))];
	```
	
