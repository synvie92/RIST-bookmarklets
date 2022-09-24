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
javascript:
/*
Instances : https://simple-web.org/instances/simplytranslate
Engine : google,libre,iciba,reverso,deepl
REMARK :
Google engine support most instances
*/
/*Customization Area*/
    instances = [
    'simplytranslate.org',
    'st.tokhmi.xyz',
    'translate.josias.dev',
    'translate.namazso.eu',
    'translate.riverside.rocks',
    'simplytranslate.pussthecat.org',
    'translate.northboot.xyz',
    'translate.tiekoetter.com',
    'simplytranslate.esmailelbob.xyz',
    'tl.vern.cc',
    'translate.slipfox.xyz',
    'st.odyssey346.dev'
    ];

    var engine = 'google';
    var from_language = 'auto';
    var to_language = 'en';

/* Don't Touch if not understand what you doing */
    var input = window.prompt("", "");
    var results = 'https://' + instances[Math.floor(Math.random() * instances.length)] + '/?engine=' + engine + '&sl=' + from_language + '&tl=' + to_language + '&text=' + decodeURIComponent(input);
    if (input === '') {
        alert("Errors : Empty Input.");
    }
    if (input !== '') {
        window.open(results);
    }
```
