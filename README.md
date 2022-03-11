# Website-Launch-Checklist

![](Checklist_Image.png)

A checklist of tasks to do before launching a public website.

<br>

## Table Of Contents
  * [Checklist](#checklist)
    + [Pre-Launch](#pre-launch)
    + [Post-Launch](#post-launch)
    + [Launch](#launch)
    + [Ongoing](#ongoing)
  * [Suggestions](#suggestions)
  * [Copyright and Attribution](#copyright-and-attribution)

<br>



## Checklist

Launch preparation generally takes a day or more. You should also reserve a day for bugfixing after you have wrapped the last feature. Be sure to plan accordingly!

### Pre-Launch
* [ ] <b> Content and Style </b> 
 
    * [ ] <b> Typography and layout	  </b>
 
      * [ ] Check for incorrect punctuation marks, particularly apostrophes, quotation marks and hyphens/dashes	 
 
      * [ ] Check headings for where you could potentially use ligatures	 
 
      * [ ] Check for widow/orphan terms in important paragraphs	 
 
 * [ ] <b> Spelling and grammar	 </b>
 
* [ ] <b> Consistency	 </b>
 
    * [ ]  Capitalisation (especially of main headings)	 
 
    * [ ]  Tense/Style of writing	 
 
    * [ ]  Recurring/common phrases (e.g. ‘More about X’ links)	 
  
   * [ ]   Variations in words (e.g. Websites vs Web Sites, or UK vs US spelling)	 
  
    * [ ]  Treatment of bulleted lists (e.g. periods or commas at end of each item)	 
 
 
 
 * [ ]  Check for hard-coded links to staging domain (i.e. ensure all links will change to ‘live’ URL/domain when site is launched)
 
 * [ ] Ensure no test content on site	 
 
 * [ ] Check how important pages (e.g. content items) print	 
 
 * [ ] For re-designs, ensure important old/existing URLs are redirected to relevant new URLs, if the URL scheme is changing
 
 * [ ] Check all ‘Hidden Copy’ (e.g. alt text, transcriptions, text in JavaScript functions)	 
 
 
 * [ ] <b> Standards and Validation </b>
    * [ ] Accessibility	 
   * [ ]  HTML validation	 
   * [ ]  JavaScript validation	 
   * [ ]  CSS validation	 
 
 
 * [ ] <b> Search Engine Visibility, SEO and Metrics </b>

     * [ ] Disable Indexing On Development Server 
   
     * [ ] Page Titles are important; ensure they make sense and have relevant keywords in them.	
  
    * [ ]  Create metadata descriptions for important pages.	 
  
    * [ ]  Check for canonical domain issues (e.g. variations in links to http://site.com http://www.site.com http://www.site.com/index.html should be reduced to a single   consistent style)	 
  
    * [ ]  Ensure content is marked-up semantically/correctly (h1, etc.)	 
  
     * [ ] Check for target keyword usage in general content	 
  
     * [ ] Check format (user/search engine friendliness) of URLs	 
  
    * [ ]  Set up Analytics, FeedBurner, and any other packages for measuring ongoing success	 
  
    * [ ]  Create an XML Sitemap	 
  
     * [ ] Configure Google Webmaster Console and Yahoo! Site Explorer	 

   
    * [ ] <b> Sharing & Rich Snippets</b>
        * [ ] Create a share card using [Photopea](https://photopea.com/) or a similar tool

        * [ ] Set up Facebook meta tags & validate [here](https://developers.facebook.com/tools/debug/)
        
        * [ ] Set up Twitter meta tags & validate [here](https://cards-dev.twitter.com/validator)
       
    <b> Facebook Tag </b>   
    ```html
    <meta property="og:type" content="website">
    <meta property="og:site_name" content="${SITE_NAME}">
    <meta property="og:description" content="${SITE_DESCRIPTION}">
    <meta property="og:image" content="${SHARE_CARD_URL}">
    <meta property="og:title" content="${PAGE_TITLE}">
    <meta property="og:url" content="${PAGE_URL}">
    ```
    
   <b> Twitter Tag</b>
    ```html
    <meta name="twitter:card" content="summary_large_image">
    <meta name="twitter:site" content="${SITE_NAME}">
    <meta name="twitter:creator" content="${SITE_AUTHOR}">
    <meta name="twitter:description" content="${SITE_DESCRIPTION}">
    <meta name="twitter:image" content="${SHARE_CARD_URL}">
    <meta name="twitter:title" content="${PAGE_TITLE}">
    <meta name="twitter:url" content="${PAGE_URL}">
    ```
 
 * [ ] <b> Functional Testing </b>
    * [ ] Check all bespoke/complex functionality	 
 
    * [ ] Check search functionality (including relevance of results)	 
    
    * [ ] Check on common variations of browser (Internet Explorer, Firefox, Safari, Chrome etc.), version (6, 7, 2.2, 3.1 etc.) and platform (Windows, OSX, Linux)	 
    
    * [ ] Check on common variations of Screen Resolution	 
    
    * [ ] Test all forms (e.g. contact us, blog comments), including anti-spam features, response emails/text, etc.
    	 
    * [ ] Test without JavaScript, Flash, and other plug-ins	
     
    * [ ] Check all external links are valid	 
    
    * [ ] Run the site through Google's [PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights/)

    * [ ] Write a script to load test your site
    - Check out [Locust](https://docs.locust.io/en/stable/) for this. See [LA Metro Councilmatic](https://github.com/datamade/la-metro-councilmatic#load-testing) for a basic example.
  
  * [ ] <b> Printer Friendliness </b> 
  
       Dynamic sizing, dark backgrounds, and interactivity don't play well with printers.

       
    * [ ] <b> Pick one option to solve this: </b>
        * [ ] Make a print stylesheet using a `@media print {}` media query, then add it to your site with `<link rel="stylesheet" type="text/css" href="css/print.css" media="print">`

       - <b> OR </b>

        * [ ] Use your browser's dev tools to remove offending elements (like sticky footers), alter colors where needed, and [screenshot the entire page]  (https://stackoverflow.com/a/14830242).
     
    * [ ] Add a link to the printer-friendly version to your website.
    
 * [ ] <b> Browser and mobile compatibility </b>
    * [ ] Use BrowserStack to confirm that your site is compatible with the browsers you wish to support
    
    * [ ] <b> Using BrowserStack's mobile device emulators and/or your own mobile device, confirm that: </b>
        * [ ] Scrolling is easy
    
        * [ ] Nav bar works
    
        * [ ] Hoverable things are tappable
    
        * [ ] Charts and maps look ok
 
 * [ ] <b> Security/Risk </b>
    * [ ]  Configure backup schedule, and test recovery from backup.	 
 
     * [ ] Protect any sensitive pages (e.g. administration area)	 
 
     * [ ] Use robots.txt where necessary	 
 
 * [ ] <b> Security/Penetration test	</b> 
 
    * [ ]  Turn-off verbose error reporting	 
 
     * [ ] Check disk space/capacity	 
 
     * [ ] Set-up email/SMS monitoring/alerts (e.g. for errors, server warnings); consider internal and external monitoring services	 
 
 
 
 
* [ ] <b> Performance </b>
   * [ ]  Load test	 
 
    * [ ] Check image optimisation	 
 
    * [ ] Check and implement caching where necessary	 
 
    * [ ] Check total page size/download time	 
 
    * [ ] Minify/compress static (JavaScript/HTML/CSS) files	 
 
   * [ ]  Optimise your CSS: use short image paths; make full-use ‘cascading’ nature of CSS, etc.	 
 
    * [ ] Check correct database indexing	 
 
    * [ ] Check configuration at every level (Web server, Database, any other software e.g. Content Management System)	
 
   * [ ]  Configure server-based logging/measurement tools (e.g. database/web server logging)	 
 
 
 * [ ] <b> Finishing Touches </b>
    * [ ] Create custom 404 & 500 & other error pages	

    * [ ] <b> Favicons </b>
        * [ ] Create a favicon
    
        * [ ] Add favicons and Apple touch icons (http://www.favicomatic.com/)
 

<br>

 ### Post-Launch
 * [ ] <b> Marketing </b>
    * [ ] Social Marketing: Twitter, LinkedIn, Digg, Facebook, Stumbleupon, etc.	 
 
    * [ ] Submit to search engines	
 
   * [ ]  Set-up PPC/Google Adwords where necessary	 
 
    * [ ] Check formatting of site results in SERPs	 
 
 <br>

 ### Launch
* [ ] <b> Deployment </b>
    * [ ] Create a production deployment

    * [ ] Double check that production-level resources have been provisioned

    * [ ] Purchase your domain and create the DNS record to point it at your production deployment

    * [ ] Ensure HTTPS / SSL is correctly set.
    
* [ ] <b> Web Search Indexing </b>
    * [ ] Allow indexing of your production site
    
    * [ ] Redirect the www subdomain to your root domain
    
    * [ ] [Set a canonical URL](https://developers.google.com/search/docs/advanced/crawling/consolidate-duplicate-urls) to prevent duplicate search results
 
* [ ] <b> Google Analytics </b>
    * [ ] Create a [Google Analytics](http://www.google.com/analytics/) account (if you do not have one)
    
    * [ ] Add [the Google Analytics script](https://developers.google.com/analytics/devguides/collection/analyticsjs) to your site
    
    * [ ] Set up [Google Webmaster Tools](https://www.google.com/webmasters/tools/home?hl=en) and [verify site](https://support.google.com/webmasters/answer/9008080?hl=en)
    * [ ] Link Webmaster Tools to Google Analytics
   
 
<br>

 ### Ongoing
 * [ ] Monitor and respond to feedback (direct feedback, on Social Media sites, check for chatter through Google, etc.)	 
 
 * [ ] Check analytics for problems, popular pages etc. and adjust as necessary	 
 
 * [ ] Update content
 
 * [ ] <b> Optional: </b> Set up relevant Goals and Funnels in Google Analytics
   
 
<br>

## Suggestions

We'd love to hear 'em. [Open an issue](https://github.com/MarketingPipeline/Website-Launch-Checklist/issues)

## Copyright and Attribution

##### Credits To ; 

Copyright (c) 2022 MarketingPipeline. Released under [Creative Commons Attribution-NonCommercial 4.0 International](https://github.com/MarketingPipeline/Website-Launch-Checklist/blob/main/LICENSE).

<small><i><a href='https://github.com/mapiec/checklist'>Original Author Of This Checklist</a></i></small>

