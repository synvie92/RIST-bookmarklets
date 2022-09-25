# RIST Bookmarklets
A bookmarklets random pick a SimplyTranslate instances from bookmarklets

## How To Use
Normal Users :
1. Copy below bookmarklets
2. Add a bookmark on your browsers and give a *Name* ( Example : RIST Bookmarklets)
3. Paste bookmarklets on *URL* fill and Save
4. Enjoy it

Advanced User:
1. Copy/Paste to your text editor
2. Modify it to fit your usecase
3. Add modified bookmarklets to your browsers
4. Enjoy it

```javascript
javascript:(function(window, document, undefined) {
/*
Instances : https://simple-web.org/instances/simplytranslate
Support Engine : google,libre,iciba,reverso,deepl
REMARK :
- Google engine support most instances
*/

/*Customization Area*/
    const instances = [
    'simplytranslate.org',
    'st.tokhmi.xyz',
    'translate.josias.dev',
    'translate.namazso.eu',
    'translate.riverside.rocks',
    'translate.northboot.xyz',
    'translate.tiekoetter.com',
    'tl.vern.cc',
    'translate.slipfox.xyz',
    'st.odyssey346.dev'
    ];

    let engine = 'google';
    let from_language = 'auto';
    let to_language = 'en';

/* Don't Touch if you not understand what you doing */
    let query = window.prompt("", "");
    let URLs = 'https://' + instances[Math.floor(Math.random() * instances.length)] + '/?engine=' + engine + '&sl=' + from_language + '&tl=' + to_language + '&text=' + decodeURIComponent(query);
    
    if (query === '') {
        alert("Errors : Empty Query.");
    }
    else if (query === '/about') {
        window.open("https://github.com/synvie92/RIST-bookmarklets", "_blank");
    }
    else if (query === '/credit')  {
        window.open("https://github.com/synvie92/RIST-bookmarklets/blob/main/credit.md", "_blank");
    }
    else if (query !== '') {
        window.open(URLs, "_blank");
    }
})(window)
```
