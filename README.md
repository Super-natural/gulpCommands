![alt tag](http://www.wearesupernatural.com/wp-content/uploads/2015/09/supernatural_wood_hipster_about_1900x950_v1.jpg)

# Gulp File for all Super natural Builds

 *  v0.1.0
 *	16/02/2016
 *
 *  Written by Stephen Utting



# Set up
You only need to download the installGulp bash script. When double clicked (at least on a mac) it will ssh the latest files from this repo into a folder called _Gulp. It will then install all required npm dependencies and do a cleanup afterwards.  


# Set up HTML
The .html file script re-routing will look for this in your css tags:
```
<!-- build:css All.min.css -->
  <link rel="stylesheet" href="style.css" type="text/css">
<!-- endbuild -->
```
everything inside the build tags will be compacted into All.min.css, please see example folder for details.

# Set up JS
likewise in js script tags in the html:
```
<!-- build:js All.min.js -->
  <script src="myScript.js" type="text/javascript"></script>
<!-- endbuild -->
```
everything inside the build tags will be compacted into All.min.js, please see example folder for details.



# Terminal
Gulp is launched by this command:
```
  gulp --src ../location/of/my/gulpOpts/json/
```
so long as the .json file is filled out correctly (please see example for details) it should all work.

# Notes
   - For dependencies please refer to package.json
   - Please only have one html file in the root of your project or else the script gets confused..
   - Remember that any scripts or style tags outside of the above html blocks need to be manually copied (there is a section for this in gulpOpts.json)
   - This relies on a default folder structure of
```
   _Gulp
   myProject/
      | myHTMLFile.html
      | js/
      |   | myJSFile.js
      | css/
      |   | myCSSFile.css
      | img/
      |   | myImages.{jpg, gif, png, etc}
      | vid/
      |   | myVideos.{mp4. webm, ogv, etc}
      | font/
      |   | myFonts.{woff, otf, ttf, etc}
   backup/
      | myBackupImg.jpg
```
