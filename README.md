# fsink
Find sink in js code


https://domgo.at/cxss/sinks
https://www.acunetix.com/blog/articles/finding-source-dom-based-xss-vulnerability-acunetix-wvs/
https://github.com/mozilla/eslint-plugin-no-unsanitized

SURTOUT
https://book.hacktricks.xyz/pentesting-web/xss-cross-site-scripting/dom-xss
https://github.com/wisec/domxsswiki/wiki

> **Source** := JavaScript property that accepts user controlled data (eg `location.search`)

> **Sink** := POtential dangerous JavaScript function or DOM object that can cause indésirable effect if attacker controlled data is pass to it (eg `eval`) 
