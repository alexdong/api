## <img width="48px" valign="middle" src="http://i.imgur.com/Hi20huC.png"> cljs.core/while

 <table border="1">
<tr>
<td>macro</td>
<td><a href="https://github.com/cljsinfo/api-refs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
imported [<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/while</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/while)
</td>
</tr>
</table>

 <samp>
(__while__ test & body)<br>
</samp>

```
Repeatedly executes body while test expression is true. Presumes
some side-effect will cause test to become false/nil. Returns nil
```

---

 <pre>
clojure @ clojure-1.4.0
└── src
    └── clj
        └── clojure
            └── <ins>[core.clj:5598-5606](https://github.com/clojure/clojure/blob/clojure-1.4.0/src/clj/clojure/core.clj#L5598-L5606)</ins>
</pre>

```clj
(defmacro while
  [test & body]
  `(loop []
     (when ~test
       ~@body
       (recur))))
```


---

```clj
{:ns "cljs.core",
 :name "while",
 :signature ["[test & body]"],
 :history [["+" "0.0-927"]],
 :type "macro",
 :full-name-encode "cljs.core_while",
 :source {:code "(defmacro while\n  [test & body]\n  `(loop []\n     (when ~test\n       ~@body\n       (recur))))",
          :filename "clojure/src/clj/clojure/core.clj",
          :lines [5598 5606],
          :link "https://github.com/clojure/clojure/blob/clojure-1.4.0/src/clj/clojure/core.clj#L5598-L5606"},
 :full-name "cljs.core/while",
 :clj-symbol "clojure.core/while",
 :docstring "Repeatedly executes body while test expression is true. Presumes\nsome side-effect will cause test to become false/nil. Returns nil"}

```