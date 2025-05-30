# HelpViewer

A simple reader for ZIP archives containing markdown files, intended to serve as a help file viewer similar to those found in older Windows systems - [HTML Help Viewer][HTMLHW] and [WinHelp][WinHlp32] - with single-file deployment.

## How does it works

1. You will open **HelpViewer.htm** file in your browser.
2. Then you will populate parameter **?d=X** where X will be your ZIP file path where all markdown files for your help file are present.

## Troubleshooting

- The solution is implemented using pure JavaScript. Please ensure that JavaScript is enabled in your browser to ensure proper functionality.

### Page not reading ZIP content - check if your browser is blocking content because of CORS policy

You need to run your browser in mode with bypass CORS policy:
- Firefox:
  > Address bar: 
  about:config
  > 
  > search:
  privacy.file_unique_origin
  > 
  > set to:
  false
  
- Chrome:
  > Run in CLI:
  > chrome.exe --disable-site-isolation-trials --disable-web-security --user-data-dir="C:\temp"

## Data files structure

- [Metadata structure description][Structure]

## Used 3rd party products

- [JSZip library][JSZIP]
- [Marked][Marked]

## Future plans

- HLP file browsing will not be supported (at least not for now).
- Support old help CHM file format with defined conversion steps.

## About AI Assistance

Some parts of this project were developed with assistance from:

- ChatGPT, 
- Copilot

, an AI-powered advisor. 
While AI helped generate suggestions, the final code and design decisions were made by the project author.

Please note that any use of third-party code generated or suggested by AI is subject to the original licenses of that code.

[HTMLHW]: https://learn.microsoft.com/en-us/previous-versions/windows/desktop/htmlhelp/about-the-html-help-viewer "HTML Help Viewer"
[WinHlp32]: https://blog.butras.cz/2013/11/jiz-od-verze-windows-vista-jiz-neni.html "WinHlp32"
[JSZIP]: http://jszip.org/ "JSZip JavaScript library"
[Marked]: https://marked.js.org/ "Marked JavaScript library"
[Structure]: FileMetadata.md "File metadata"