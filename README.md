# DomXssFinder

**Find sources and sinks in js code that could lead to DOM XSS**

> **💧 Source** := JavaScript property that accepts user controlled data (eg `location.search`)

> **🚰 Sink** := Potential dangerous JavaScript function or DOM object that can cause indesirable effect if attacker controlled data is pass to it (eg `eval`)

## How ?

***> Find sources in js code:***

```shell
cat [js_file] | fsource
```

***> Find sinks in js code:***

```shell
cat [js_file] | fsink
```

***💡 Tip:***
To retrieve all js code from an url **~>** [`jse`](https://github.com/ariary/JSextractor):
```shell
export URL=[url]
curl -s $URL -H "Accept: text/html" | jse -u $URL -gather-src 2>/dev/null
```

Find all related shortcuts: [`bang 💥`](https://github.com/ariary/bang/blob/main/EXAMPLES.md#find-dom-xss)

***💡 Tip 2:***
Use `-C [NUM]` parameter to get more context when source/sink has been found (Print `[NUM]` lines of output context)
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

