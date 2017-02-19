# ![Timelined](http://i.imgur.com/DQWLvYk.png) Timelined
Timelined is a customizable CSS-only vertical timeline.

#### Static Demo - http://timelined.betterexperience.site/demo.html

## Quick start

### Grab the compiled code
The [compiled SCSS code](https://github.com/andriussev/timelined/raw/master/css/timeline.min.css) is the `css` directory, which will work fully work without the need of compiling anything. Don't forget to grab the [`demo.html` file](https://github.com/andriussev/timelined/raw/master/demo.html) too, to get the idea of how the tool works.

### Compiling
The styling is done with SCSS and you can compile it with any proper tool (I use [node-sass](https://github.com/sass/node-sass)). There are a couple of variables and other stuff to make the customization faster.

### Usage

#### Basic structure

	<div class="timeline gray-blue"> <!-- Main element container -->
		<div class="timeline-block">	<!-- Single block -->
			<div class="timeline-icon"></div> <!-- Icon on the timeline -->
			<div class="timeline-content"> 
				<p> Any content </p> <!-- Content -->
				<div class="timeline-date">Yesterday</div> <!-- Date -->
			</div>
		</div>
		...
	</div>

##### Additional options
Some additional customization is available by adding additional classes to the main container element `.timeline`:

* `.timeline-left` - The line is on the left while the content is always on the right;
* `.timeline-alternating` - Blocks are alternating between left and right of the line;
* `.timeline-collapsing` - The timeline automatically switches to `timeline-left` mode when the container is small (800px, by default);
* `.timeline-with-arrows` - Includes the arrows towards the line (works with default and left modes).

`.timeline-icon` element options:

* `.timeline-icon-hide-border` - Removes the border from the icon circle.

#### Timeline icons
As of now, Font Awesome icons can be used, as well as images:
	
	<div class="timeline-icon timeline-icon-hide-border"> <!-- Hiding border is optional -->
		<i class="fa fa-github fa-lg"></i>
	</div>
	<!-- Or -->
	<div class="timeline-icon">
		<img src="http://lorempixel.com/100/100/"/>
	</div>
#### Hide timeline content - timeline icon only
If you don't want to show the timeline content in the block, add `.timeline-block-icon-only` class on `timeline-block`. This makes the `.timeline-content` invisible.

Furthermore, if you want to enter text instead of an icon (or an image), add `.timeline-icon-text` to `.timeline-icon` div. You might want to also use `.timeline-icon-hide-border` in addition.
Adding the text content to a `span` container will give it the default background and border.

Basic example of how everything would work:

	<div class="timeline-block timeline-block-icon-only">
		<div class="timeline-icon timeline-icon-text timeline-icon-hide-border">
			<span>This is my important text</span>
		</div>
		<div class="timeline-content"></div>
	</div>



#### Additional schemes

Schemes are a quick way to change the color of the line, icon on the timeline and  border of the block. The names are self-explanitory: `gray-red`, `gray-blue`, `blue-yellow-yellow`, `purple-flirt`,`blue-blue-blue`.
Adding the scheme name as a class on the main container will do the job.

## Static Demo - http://timelined.betterexperience.site/demo.html

## License
The MIT License (MIT)

Copyright (c) 2016 Andrius Ševčenko

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
