# DomXssFinder

**Find sources and sinks in js code that could lead DOM XSS**

> **💧 Source** := JavaScript property that accepts user controlled data (eg `location.search`)

> **🚰 Sink** := Potential dangerous JavaScript function or DOM object that can cause indésirable effect if attacker controlled data is pass to it (eg `eval`)

## How ?

***> Find sources in js code:***

```shell
cat [js_code_file] | fsource
```

***> Find sinks in js code:***

```shell
cat [js_code_file] | fsink
```

***💡 Tip:***
To retrieve all js code from an url **~>** [`jse`](https://github.com/ariary/JSextractor):
```shell
export URL=[url]
curl -s $URL -H "Accept: text/html" | jse -u $URL -gather-scr 2>/dev/null
```

Find all related shortcuts: [`bang 💥`](https://github.com/ariary/bang/blob/main/EXAMPLES.md#find-dom-xss)

## Get ready !
```shell
curl -s -lO -L https://github.com/ariary/DomXssFinder/releases/latest/download/fsink 
curl -s -lO -L https://github.com/ariary/DomXssFinder/releases/latest/download/fsource
chmod +x fsink fsource
mv fsink [path in $PATH] && mv fsource [path in $PATH]
```

## Notes

See how to exploit:
 * [hacktricks.xyz](https://book.hacktricks.xyz/pentesting-web/xss-cross-site-scripting/dom-xss)

