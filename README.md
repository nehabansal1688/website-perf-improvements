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
