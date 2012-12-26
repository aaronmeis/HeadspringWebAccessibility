# Web Accessibility

Making a site accessible is intended to make your site useable by the broadest set of user's possible.

## Major Standards

1. [WAI-ARIA](http://www.w3.org/WAI/PF/aria-practices/)
2. [WCAG 2.0](http://www.w3.org/TR/WCAG20/)
3. [Section 508](http://www.section508.gov/)

## Requirements for an Accessible Site

* full keyboard support
* high contrast page elements
* text-based versions of non-text elements

### Checklist

1. The language in the header must be correct as it is the default used by screenreaders `<html lang="en">`
2. Search and autocomplete widget results must be keyboard accessible
3. Search and autocomplete widget results must be exposed to assistive technology
4. All images should have explanatory text via the 'alt' attribute

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

### Widgets

#### Autocomplete Widgets

An autocomplete widget should be keyboard accessible.

## Accessibility Tools

### Screen Readers

* Windows
  * JAWS
  * NVDA
  * Window Eyes
* Mac OS X and iOS
  * VoiceOver
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


References
* [Kendo UI Accessibility Overview](http://docs.kendoui.com/tutorials/accessibility/accessibility-overview)
* [Rough Guide: browsers, operating systems and screen reader support](http://www.paciellogroup.com/blog/2012/02/rough-guide-browsers-operating-systems-and-screen-reader-support/)
* [Screen Reader User Survey #4 Results](http://webaim.org/projects/screenreadersurvey4/)

Interesting Links
* [jQuery UI Accessibility Test](http://hanshillen.github.com/jqtest/#goto_slider)
* [Sim Daltonism](http://michelf.ca/projects/sim-daltonism/)
* 

