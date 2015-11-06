## cljs.core/vector-seq



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1211"><img valign="middle" alt="[+] 0.0-1211" title="Added in 0.0-1211" src="https://img.shields.io/badge/+-0.0--1211-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__vector-seq__ v offset)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r1211/src/cljs/cljs/core.cljs#L2510-L2528):

```clj
(defn vector-seq [v offset]
  (let [c (-count v)]
    (when (pos? c)
      (reify
        IPrintable
        (-pr-seq [vseq opts] (pr-sequential pr-seq "(" " " ")" opts vseq))
        ISequential
        IEquiv
        (-equiv [vseq other] (equiv-sequential vseq other))
        ASeq
        ISeq
        (-first [_] (-nth v offset))
        (-rest [_]
          (let [offset (inc offset)]
            (if (< offset c)
              (vector-seq v offset)
              ())))
        ISeqable
        (-seq [vseq] vseq)))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1211
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:2510-2528](https://github.com/clojure/clojurescript/blob/r1211/src/cljs/cljs/core.cljs#L2510-L2528)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/vector-seq` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/vector-seq.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core/vector-seq.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "vector-seq",
 :type "function",
 :signature ["[v offset]"],
 :source {:code "(defn vector-seq [v offset]\n  (let [c (-count v)]\n    (when (pos? c)\n      (reify\n        IPrintable\n        (-pr-seq [vseq opts] (pr-sequential pr-seq \"(\" \" \" \")\" opts vseq))\n        ISequential\n        IEquiv\n        (-equiv [vseq other] (equiv-sequential vseq other))\n        ASeq\n        ISeq\n        (-first [_] (-nth v offset))\n        (-rest [_]\n          (let [offset (inc offset)]\n            (if (< offset c)\n              (vector-seq v offset)\n              ())))\n        ISeqable\n        (-seq [vseq] vseq)))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1211",
          :filename "src/cljs/cljs/core.cljs",
          :lines [2510 2528]},
 :full-name "cljs.core/vector-seq",
 :full-name-encode "cljs.core/vector-seq",
 :history [["+" "0.0-1211"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/vector-seq"]))
```

-->