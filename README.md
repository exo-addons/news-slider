News Slider
===========
Description
--
*Get an animated news slider in 5 steps!*

How to install
--
1. **Cloning the project:** 
  * Go to the GitHub repository [exo-addons/news-slider](http://github.com/exo-addons/news-slider "exo-addons/news-slider") and clone the project.



2. **Adding resources:** 
  * Go to the back-office of eXo Platform (using the File Explorer). 
  * Add a content folder (`NewsFolder` for example) in which you'll store the news items (for example under `/shared`), you may create news using the '`Free Layout Webcontent`' template, try to add an illustration image and fileout a summary, in order to be displayed as a preview of the news in our news silder.  
    _PS: For tests, you can import the artificat `NewsFolder.xml` into your File System_.
  * Upload the CSS file `NewsSlider.css` to any location you want (for example: under `/shared/css`) and copy its path`[1]`.
  * Upload the JS files `jquery.easing.min.js` and `jquery.min.js` (which are the JQuery librairies) to any location you want (for example: under `/shared/js`) and copy its path`[2]`.       


 
3. **Update the resources paths:** 
  * Go to the template file `NewsSliderCLVTemplate.gtmpl` and update the exacte location of the resources, for both JS and CSS files (already saved in `[1]` and `[2]`, if not go back to this files `/shared/js` and `/shared/css`, right click on the file, select the last menu entry  '`Copy URL to clipboard`'  and past it the `src` parameter like below:
                    
            <link rel="stylesheet" type="text/css" href="/rest/jcr/repository/collaboration/sites content/live/shared/css/NewsSlider.css" media="all"/>
            <script type="text/javascript" src="/rest/jcr/repository/collaboration/sites content/live/shared/js/jquery.min.js"></script>
            <script type="text/javascript" src="/rest/jcr/repository/collaboration/sites content/live/shared/js/jquery.easing.1.3.js"></script>
  * Ensure that the path is not a private link in order to make the news viewable for guests (for that, delete `/private` from the path).


4. **Add the template via IDE:** 
  * Go to the IDE, select the `dms-system` workspace, navigate to  `exo:ecm > views > templates > content-list-viewer > list`  .
  * Add a new template.
  * Copy/Past the content of the GTMPL file `NewsSliderCLVTemplate.gtmpl` into this template and save it as `NewsSliderCLVTemplate`.



5. **Add the CLV and configure it:**
  * Now, we are ready to add our news slider into a website.
  * Go to a given website, ACME for example, edit the layout, add a new portlet `(content > content list)` to a given page.
  * Edit this content list portlet, configure it by selecting the news folder path (in our case, '`/shared/NewsFolder`', and selecting our new CLV template `NewsSliderCLVTemplate`
  * It's possible also to configure the slider on terms of amount of news, existence of pagination or not.

**Enjoy!**