## <img width="48px" valign="middle" src="http://i.imgur.com/Hi20huC.png"> cljs.core/chunk-buffer

 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/api-refs/tree/0.0-1424"><img valign="middle" alt="[+] 0.0-1424" src="https://img.shields.io/badge/+-0.0--1424-lightgrey.svg"></a> </td>
</tr>
</table>

 <samp>
(__chunk-buffer__ capacity)<br>
</samp>

```
(no docstring)
```

---

 <pre>
clojurescript @ r1552
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:1872-1873](https://github.com/clojure/clojurescript/blob/r1552/src/cljs/cljs/core.cljs#L1872-L1873)</ins>
</pre>

```clj
(defn chunk-buffer [capacity]
  (ChunkBuffer. (make-array capacity) 0))
```


---

```clj
{:full-name "cljs.core/chunk-buffer",
 :ns "cljs.core",
 :name "chunk-buffer",
 :type "function",
 :signature ["[capacity]"],
 :source {:code "(defn chunk-buffer [capacity]\n  (ChunkBuffer. (make-array capacity) 0))",
          :filename "clojurescript/src/cljs/cljs/core.cljs",
          :lines [1872 1873],
          :link "https://github.com/clojure/clojurescript/blob/r1552/src/cljs/cljs/core.cljs#L1872-L1873"},
 :full-name-encode "cljs.core_chunk-buffer",
 :history [["+" "0.0-1424"]]}

```