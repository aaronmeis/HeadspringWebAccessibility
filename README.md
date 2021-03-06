# Web Accessibility

Making a site accessible is intended to make your site useable by the broadest set of user's possible.

## Major Standards

1. [WAI-ARIA](http://www.w3.org/WAI/PF/aria-practices/)
2. [WCAG 2.0](http://www.w3.org/TR/WCAG20/)
3. [Section 508](http://www.section508.gov/)

## General Requirements for an Accessible Site

* full keyboard support
* high contrast page elements
* text-based versions of non-text elements

### Checklist

* The language in the header must be correct as it is the default used by screenreaders `<html lang="en">`
* Search and autocomplete widget results must be keyboard accessible
* Search and autocomplete widget results must be exposed to assistive technology
* Images should have explanatory text via the 'alt' attribute when not duplicating information.
* Labels and inputs should use 'for' and 'id' attributes respectively.
* Luminosity contrast must be >= 4.5 to 1 for users with vision impairment

### Most common problematic items

> 1.The presence of inaccessible Flash content  
2.CAPTCHA - images presenting text used to verify that you are a human user  
3.Links or buttons that do not make sense  
4.Images with missing or improper descriptions (alt text)  
5.Screens or parts of screens that change unexpectedly  
6.Complex or difficult forms  
7.Lack of keyboard accessibility  
8.Missing or improper headings  
9.Too many links or navigation items  
10.Complex data tables  
11.Inaccessible or missing search functionality  
12.Lack of "skip to main content" or "skip navigation" links  
http://webaim.org/projects/screenreadersurvey4/

## Elements

### Skip Links



### Hidden Text

Use a hidden css class instead of `display:none;` or `visibility:hidden;`.

```css
   .hidden {
       text-indent: -4000px;
   }
   
   \* kendo ui hidden *\
   .hidden {
        position:absolute;
        left:-10000px;
        top:auto;
        width:1px;
	height:1px;
        overflow:hidden;
    }
```

The best set of css classes for dealing with showing and hiding elements related to screen readers are the css classes in the 
[HTML 5 Boilerplate project](http://html5boilerplate.com/).

```css
    /*
     * Image replacement
     */

    .ir {
        background-color: transparent;
        border: 0;
        overflow: hidden;
        /* IE 6/7 fallback */
        *text-indent: -9999px;
    }

    .ir:before {
        content: "";
        display: block;
        width: 0;
        height: 150%;
    }

    /*
     * Hide from both screenreaders and browsers: h5bp.com/u
     */

    .hidden {
        display: none !important;
        visibility: hidden;
    }

    /*
     * Hide only visually, but have it available for screenreaders: h5bp.com/v
     */

    .visuallyhidden {
        border: 0;
        clip: rect(0 0 0 0);
        height: 1px;
        margin: -1px;
        overflow: hidden;
        padding: 0;
        position: absolute;
        width: 1px;
    }

    /*
     * Extends the .visuallyhidden class to allow the element to be focusable
     * when navigated to via the keyboard: h5bp.com/p
     */

    .visuallyhidden.focusable:active,
    .visuallyhidden.focusable:focus {
        clip: auto;
        height: auto;
        margin: 0;
        overflow: visible;
        position: static;
        width: auto;
    }

    /*
     * Hide visually and from screenreaders, but maintain layout
     */

    .invisible {
        visibility: hidden;
    }
```

### Tables

All tables should have a `<caption>` element to help screen readers.  There are primarily two methods for creating accessible tables.

* Method 1 - Header/ID Combinations  
	<table>
	<caption>A Summary of Upcoming Bootcamps</caption>
	<th id="Course">Course</th>
	<th id="Date">Date</th>
	<th id="Cost">Cost</th>
	<tr>
	<td headers="Course">MVC Bootcamp</td>
	<td headers="Start">April 12</td>
	<td headers="Cost">$2000</td>
	</tr>
	<tr>
	<td headers="Course">RavenDB Bootcamp</td>
	<td headers="Start">March 12</td>
	<td headers="Cost">$1500</td>
	</tr>
	</table>
* Method 2 - Header/Scope Combination  
	<table>
	<caption>A Summary of Upcoming Bootcamps</caption>
	<tbody>
	<tr>
	<th scope="col">Course</th>
	<th scope="col">Date</th>
	<th scope="col">Cost</th>
	</tr>
	<tr>
	<th scope="row">MVC Bootcamp</th>
	<td>April 12</td>
	<td>$2000</td>
	</tr>
	<tr>
	<th scope="row">RavenDB Bootcamp</th>
	<td>March 12</td>
	<td>$1500</td>
	</tr>
	</tbody>
	</table>


### Autocomplete Widgets

An autocomplete widget should be keyboard accessible.

## Accessibility Tools

### Screen Readers

* Windows
  * [JAWS](http://www.freedomscientific.com/products/fs/jaws-product-page.asp)
  * [NVDA](http://www.nvda-project.org/)
  * Window Eyes
* Mac OS X and iOS
  * [VoiceOver](http://www.apple.com/accessibility/voiceover/)
* Linux
  * Orca
* Chrome OS
  * ChromeVox

> <table style="width:70%;text-align:left;margin:auto;">
 <caption>Which of the following is your primary desktop/laptop screen reader?</caption>
	<tr><th>Screen Reader</th><th># of Respondents</th><th>% of Respondents</th></tr>
	<tr><td>JAWS</td><td>853</td><td>49.1%</td></tr>
	<tr><td>Window-Eyes</td><td>214</td><td>12.3%</td></tr>
	<tr><td>VoiceOver</td><td>159</td><td>9.2%</td></tr>
	<tr><td>NVDA</td><td>238</td><td>13.7%</td></tr>
	<tr><td>System Access or System Access To Go</td><td>181</td><td>10.4%</td></tr>
	<tr><td>ZoomText</td><td>49</td><td>2.8%</td></tr>
	<tr><td>ChromeVox</td><td>4</td><td>0.2%</td></tr>
	<tr><td>Other</td><td>38</td><td>2.2%</td></tr>
</table>
http://webaim.org/projects/screenreadersurvey4/

### Developer Tools

1. [Google Chrome - Accessibility Developer Tools](https://chrome.google.com/webstore/detail/accessibility-developer-t/fpkknkljclfencbdbgkenhalefipecmb)
2. [Firefox Ext - WAVE Toolbar](https://addons.mozilla.org/en-us/firefox/addon/wave-toolbar/)
3. [IE Web Accessibility Toolbar](http://www.paciellogroup.com/resources/wat/ie)
4. [Google Chrome - High Contrast Ext](https://chrome.google.com/webstore/detail/high-contrast/djcfdncoelnlbldjfhinnjlhdjlikmph)
  * Google Chrome does not support Windows High Contrast mode out of the box.
5. [Color Contrast Analyzer](http://www.paciellogroup.com/resources/contrastAnalyser)


References
* [Kendo UI Accessibility Overview](http://docs.kendoui.com/tutorials/accessibility/accessibility-overview)
* [Rough Guide: browsers, operating systems and screen reader support](http://www.paciellogroup.com/blog/2012/02/rough-guide-browsers-operating-systems-and-screen-reader-support/)
* [Screen Reader User Survey #4 Results](http://webaim.org/projects/screenreadersurvey4/)
* [Pro HTML5 Accessibility](http://www.apress.com/9781430241942)
* [Accessibility Handbook](http://shop.oreilly.com/product/0636920024514.do)
* [Using JAWS to Evaluate Web Accessibility](http://webaim.org/articles/jaws/)
* [Tips For Creating Accessible Charts With Kendo UI DataViz](http://docs.kendoui.com/tutorials/accessibility/five-tips-for-accessible-charts-with-dataviz)

Interesting Links
* [http://www.ajmcclary.com/configuring-your-website-to-work-with-jaws.html](Configuring Your Website to Work with JAWS)
* [jQuery UI Accessibility Test](http://hanshillen.github.com/jqtest/#goto_slider)
* [Sim Daltonism](http://michelf.ca/projects/sim-daltonism/)


