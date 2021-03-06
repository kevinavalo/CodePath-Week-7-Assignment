# Project 7 - WordPress Pentesting

Time spent: **9** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) Authenticated Shortcode Tags Cross-Site Scripting (XSS)
  - [X] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.5
  - [X] GIF Walkthrough: <img src='https://imgur.com/kKY2oWQ.gif' title='GIF Walkthrough' width='' alt='GIF Walkthrough' />
  - [X] Steps to recreate: 
          - Create a new post
          - In the text area add the html tag <a> with alert in it, instead of href
  - [ ] Affected source code:
    - [Link 1](https://github.com/WordPress/WordPress/commit/f72b21af23da6b6d54208e5c1d65ececdaa109c8)
2. (Required) Authenticated Stored Cross-Site Scripting (XSS)
  - [X] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.3
  - [X] GIF Walkthrough: <img src='https://imgur.com/bdQFOZQ.gif' title='GIF Walkthrough' width='' alt='GIF Walkthrough' />
  - [X] Steps to recreate: 
          - Create a new post
          - In the text area add tag similar to this: <a href="[caption code=">]</a><a title=" onmouseover=alert('test')  ">link</a>
  - [X] Affected source code:
    - [Link 2](https://core.trac.wordpress.org/browser/branches/4.2?rev=33360)
3. (Required) Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeds
  - [X] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.13
  - [X] GIF Walkthrough: <img src='https://imgur.com/H7V8V1f.gif' title='GIF Walkthrough' width='' alt='GIF Walkthrough' />
  - [X] Steps to recreate:
          - Create a new post
          - In the text area add a spliced youtube link similar to this: https://youtube[.]com/watch?v=abc<svg onload=alert(1)>
  - [X] Affected source code:
    - [Link 3](https://github.com/WordPress/WordPress/commit/419c8d97ce8df7d5004ee0b566bc5e095f0a6ca8)

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [XXXX] [name of copyright owner]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
