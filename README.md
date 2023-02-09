# website-perf-improvements
 chrome dev tools -> ligthHouse -> check performance under categories -> analyse page load
 
 
 check the page performance and see the oppurtunities to improve site perf
 
** oppurtunities**
1) Reduce unused JavaScript <br/>
 -  click ctrl shift p and click on show coverage - run coverage and check the percentage 
 -  click on file. red block will be unused code and green will be used one

2) remove unused libs
 - click on ctrl shift p - show n/w request blocking
 - add pattern /lib/*
 - go to network tab and reload page
 - unused libs will be marked in red
 
3) use file compression
 - in node js use compression module
 - app.use(compression())

4) click on perf tab
- start profiler
- 


__Metrics__

Visual Metrics - - how fast stuff is painted on screen (FCP) - first contentful paint, speed index
Intractive Metrics - how quickly site become usable for users- time to be intrective(TTI)

__Events__
DCL - dom contentful loaded event - > FP Firs paint -> FCP -> first contentful paint -> LCP largest contentful paint -> L -> on load Event 

# URL for performance stats of website
__Analysis tools__
__https://pagespeed.web.dev/__
<br/>
__https://www.webpagetest.org/__

__monitoring tools__
<br/>GTmetrix <br/> 
speed Curve<br/>
fireFox performance tab<br />

# Chrome perf tab profiler
* inspect dev tool and click on performance tab -> click on refresh -> stop 
* analyse the profile
* profile is better in dev mode rather than production mode as code is compressed and source map are disabled in prod code
* You can enable screenshot option to see what happens on screen during the profile analysis, intermedaitae state of UI which is usually not visible on load
* yellow color - javascript ctivity, green - repainting, blue - html parsing , purple - style calculation
* network tab in profile shows detailed data of n/w console tab. what happen in that time frame i.e. js request, html ,images loaded
* main tab - we should use this for performace gaps

# Web vitals
- used to identify user experience issues in following area
 1) page loading perf
 2) ease of interraction
 3) visual stability
 
__ Core Web Vitals__
1) LCP - largest contentful paint - good if within 2.5sec
2) FID - first inut delay - when user interact with page ie.e from button click to the response - good if less than 100ms
3) CLS - commulative layout shift -changes in display when the content loads and provides bad exp to user- shd be less than 0.1 - 


 # Use Impactful features
 * async and defer
 normal JS html parse and wherever it sees js it download js and execute it and block rest of te execution
 async - script is executed only once downloading is complete i.e. without blocking
 defer - all the html parsing happens first then script downloading and execution
 * use link rel='preconnect' and prefetch, preload
 * use lazy loading images
 *use CDN
 
 
 # PWA - progresive web app
 * can be installed
 * have push notificatiosn
 
