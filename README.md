Shortening the Critical Rendering Path for index.html

	1. Inlined and minimized CSS
	2. Added "media='print'" to css/print.css (index.html line 63)
	3. Added async attribute to perfmatters.js (index.html line 67)
	4. Uglified perfmatters.js. New script source is "dist/all.min.js" (index.html line 67)
	5. Replaced old google font api with new javascript google font and moved this script below the footer to speed up rendering (index.html line 123)
	6. Optomized pizzeria image

Main.js updates

	1. Removed the dx variable as well as determinedx from "changePizzaSizes" and replaced them with a switch-case approach to eliminate forced syncronous layout (main.js line 427)
	2. Created a new variable, "scrollCalculate", outside of the for loop for updatePositions. This new variable handles the calculation made by "document.body.scrollTop / 1250" and eliminates the need to continuously recalculate scrollTop. (main.js line 496)

Gulp Additions

	1. Uglified main.js (new file found in views/dist) and linked new main.min.js to pizza.html
	2. Uglified perfmatters.js (new file found in dist) and linked index.html to new all.min file


More Notes

	1. My minified files for views can be found in "views/dist"
	2. My minified files for the index.html can be found in "dist"
