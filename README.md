# Git---Issue-Tab-Opener

This is a very simple javascript bookmarklet that is able to open all issues on a GitHub Issues page in it's own tab. 

## How to Use

1) In your browser create a bookmark. Instead of "URL" use the code below:

```javascript
javascript:(function(e,a,g,h,f,c,b,d)%7Bif(!(f%3De.jQuery)%7C%7Cg>f.fn.jquery%7C%7Ch(f))%7Bc%3Da.createElement("script")%3Bc.type%3D"text/javascript"%3Bc.src%3D"http://ajax.googleapis.com/ajax/libs/jquery/"%2Bg%2B"/jquery.min.js"%3Bc.onload%3Dc.onreadystatechange%3Dfunction()%7Bif(!b%26%26(!(d%3Dthis.readyState)%7C%7Cd%3D%3D"loaded"%7C%7Cd%3D%3D"complete"))%7Bh((f%3De.jQuery).noConflict(1),b%3D1)%3Bf(c).remove()%7D%7D%3Ba.documentElement.childNodes%5B0%5D.appendChild(c)%7D%7D)(window,document,"1.3.2",function(%24,L)%7B%24(".table-list-issues").find(".js-navigation-open").each(function()%7Bwindow.open(%24(this).attr("href"), "_blank")%7D)%7D)%3B
```

2) Navigate to GitHub Issues page
3) Click the newly created bookmark
4) You'll probably have to allow opening popups on *.github domain (icon in the right corner of the URL address bar)

TA DAAAA - issues open in its own tab. No more right-clicking around

## Compatibility, details

The bookmark uses jQuery, however it makes sure it is available before it runs the script. 
The original code looks like this:
```javascript
$(".table-list-issues").find(".js-navigation-open").each(function(){window.open($(this).attr("href"), "_blank")})
```

## Thanks to
Created by tremendous [Ben Alamn's Bookmarklet Generator](http://benalman.com/projects/run-jquery-code-bookmarklet/)
