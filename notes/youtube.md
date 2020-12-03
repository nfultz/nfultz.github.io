<!-- njnmdoc: title="Youtube snippets" -->

```
console.save(Array.from(document.querySelectorAll("#content > a")).map(x => ({title: x.innerText.trim(), href:x.href})), "wl2.json")
```

```
jq -r '.[] | "\(.title | split("\n") | "\(.[2])\t\(.[3])")\t\(.href)"' wl2.json >wl2.tsv
```
