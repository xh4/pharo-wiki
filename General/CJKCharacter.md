# Using CJK (Chinese, Japanese, and Korean) characters

Pharo's default font settings for code (Source Code Pro) and UI (Source Sans Pro) are unable to handle [CJK characters](https://en.wikipedia.org/wiki/CJK_characters). 



Operating systems may come with fonts that support those characters, but as far as I know, none of them are monospaced, which is not good for displaying code. If you need to display CJK characters in Pharo, you are recommended to install a monospace font which also covers CJK characters. Some of them are [`Noto Sans Mono CJK`](https://www.google.com/get/noto/) , `Microsoft YaHei Mono`, [`WenQuanYi Zen Hei Mono`](http://wenq.org).



Note that on Windows 10, you may need to manually copy font files to `C:\Windows\Fonts\`.

Here is a code sample:

```Smalltalk
StandardFonts 
	defaultFont: (LogicalFont familyName: 'Noto Sans CJK SC' pointSize: 9);
	codeFont: (LogicalFont familyName: 'Microsoft YaHei Mono' pointSize: 10);
	listFont: (LogicalFont familyName: 'Noto Sans CJK SC' pointSize: 9);
	menuFont: (LogicalFont familyName: 'Noto Sans CJK SC' pointSize: 9);
	buttonFont: (LogicalFont familyName: 'Noto Sans CJK SC' pointSize: 9);
	windowTitleFont: (LogicalFont familyName: 'Noto Sans CJK SC' pointSize: 10);
	balloonFont: (LogicalFont familyName: 'Noto Sans CJK SC' pointSize: 8);
	haloFont: (LogicalFont familyName: 'Noto Sans CJK SC' pointSize: 8).
```

Related links:

https://www.samadhiweb.com/blog/2019.02.22.windows.multilingual.html  
http://forum.world.st/Japanese-Fonts-td4928056.html  
http://forum.world.st/im-using-pharo-7-with-linux-env-but-cannot-input-korean-td5095342.html