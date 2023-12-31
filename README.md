#Neanderthal

The purpose of Neanderthal is to allow you to create and modify configuration environments for Android applications at run time. 

This serves a similar purpose to setting build variables for different variants, however the benefit of Neanderthal is that configuration environments can be added, removed or updated live instead of requiring separate builds.

##Usage

1. Add it to your root build.gradle at the end of repositories:

	allprojects {
	
		repositories {
		
			...
			
			maven { url 'https://jitpack.io' }
			
		}
		
	}
	
2. Add `implementation 'com.github.outware.neanderthal:neanderthal:v1.7.1'` to your application's dependencies.
3. Call `Neanderthal.initialise()`` to initialise the library by supplying a Context, an initial list of variants and
the name of the default variant.
4. Once initialised, call `Neanderthal.getConfiguration()`` to get the currently selected configuration (or the
default configuration if none are selected)

For examples of how to do this, refer to `SampleApplication.java` and `MainActivity.java` in the `neanderthal-sample`
module.
	
##License
		The MIT License (MIT)
		
		Copyright (c) 2015 Outware Mobile
		
		Permission is hereby granted, free of charge, to any person obtaining a copy
		of this software and associated documentation files (the "Software"), to deal
		in the Software without restriction, including without limitation the rights
		to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
		copies of the Software, and to permit persons to whom the Software is
		furnished to do so, subject to the following conditions:
		
		The above copyright notice and this permission notice shall be included in all
		copies or substantial portions of the Software.
		
		THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
		IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
		FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
		AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
		LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
		OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
		SOFTWARE.
