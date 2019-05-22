# Week 7 & 8 Project: WordPress Pentesting

Time spent: 8 hours spent in total

> Objective: Find, analyze, recreate, and document 3 vulnerabilities affecting an old version of WordPress

## Pentesting Report

1. WordPress 3.3-4.7.4 - Large File Upload Error XSS
	- Summary:
		- Vulnerability type: XSS
		- Tested in version: 4.2
		- Fixed in version: 4.2.15
	- Steps to recreate:
		- [Source](https://hackerone.com/reports/203515)
	- Affected source code:
		- [wpincludes/script-loader.php](https://core.trac.wordpress.org/browser/tags/4.2/src/wp-includes/script-loader.php) 
		- [wpincludes/js/plupload/handlers.js](https://core.trac.wordpress.org/browser/tags/4.2/src/wp-includes/js/plupload/handlers.js)
	- GIF Walkthrough:  
	![](https://media.giphy.com/media/TLCmTIRxjpzR6gwDnl/giphy.gif)
	
2. WordPress 3.6.0-4.7.2 - Authenticated Cross-Site Scripting (XSS) via Media File Metadata
	- Summary:
		- Vulnerability type: XSS
		- Tested in version: 4.2
		- Fixed in version: 4.2.13
	- Steps to recreate:
		- [Source](https://seclists.org/oss-sec/2017/q1/563)
	- Affected source code:
		- [wp-includes/js/mediaelement/wp-playlist.js](https://core.trac.wordpress.org/browser/tags/4.2/src/wp-includes/js/mediaelement/wp-playlist.js)
	- GIF Walkthrough:  
	![](https://media.giphy.com/media/ic0VPYcZBjPfMJA8nK/giphy.gif)

3. WordPress <= 4.2 - Unauthenticated Stored Cross-Site Scripting (XSS)
	- Summary:
		- Vulnerability type: XSS
		- Tested in version: 4.2
		- Fixed in version: 4.2.1
	- Steps to recreate:
		- [Source](https://klikki.fi/adv/wordpress2.html)
	- GIF Walkthrough:  
	![](https://media.giphy.com/media/iGG27wJ18L8vISmXZb/giphy.gif)

## Resources
- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## License

    Copyright [2019] [Sai Kumar Juguru]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.