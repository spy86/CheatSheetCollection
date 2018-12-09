### Ressources

-   [CSS Layouts](http://learnlayout.com/) Introduction
-   Web - Javascript Online IDE: [JSFiddle](http://jsfiddle.net/)
-   External Link Indicators

        // Set for all links
        .content a[href^="//"]:after, 
        .content a[href^="http://"]:after, 
        .content a[href^="https://"]:after {
            content: url(/images/Icon_External_Link.png);
            margin: 0 0 0 5px;
        }

        // Exclude local links
        .content a[href^="//lzone.de/"]:after, 
        .content a[href^="http://lzone.de/"]:after, 
        .content a[href^="https://lzone.de/"]:after {
            content: '';
            margin: 0;
        }

-   Image Inlining

        <img src="data:image/png;base64,[IMAGE_DATA_STRING]" />

-   CSS Pre-Processors
    -   [Less](http://lesscss.org/)
    -   [Sass](http://sass-lang.com/)
    -   [Stylus](https://learnboost.github.io/stylus/)

### Advanced CSS Style Overview
