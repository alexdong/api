## <img width="48px" valign="middle" src="http://i.imgur.com/Hi20huC.png"> cljs.core/array

 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/api-refs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
</table>

 <samp>
(__array__ var-args)<br>
</samp>

```
Creates a new javascript array.
@param {...*} var_args
```

---

 <pre>
clojurescript @ r1552
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:90-94](https://github.com/clojure/clojurescript/blob/r1552/src/cljs/cljs/core.cljs#L90-L94)</ins>
</pre>

```clj
(defn array
  [var-args]            ;; [& items]
  (.call (.-slice (.-prototype js/Array)) (js* "arguments")))
```


---

 <pre>
clojurescript @ r1552
└── src
    └── clj
        └── cljs
            └── <ins>[core.clj:985-992](https://github.com/clojure/clojurescript/blob/r1552/src/clj/cljs/core.clj#L985-L992)</ins>
</pre>

```clj
(defmacro array [& rest]
  (let [xs-str (->> (repeat "~{}")
                    (take (count rest))
                    (interpose ",")
                    (apply core/str))]
   (concat
    (list 'js* (core/str "[" xs-str "]"))
    rest)))
```

---

```clj
{:ns "cljs.core",
 :name "array",
 :signature ["[var-args]"],
 :shadowed-sources ({:code "(defmacro array [& rest]\n  (let [xs-str (->> (repeat \"~{}\")\n                    (take (count rest))\n                    (interpose \",\")\n                    (apply core/str))]\n   (concat\n    (list 'js* (core/str \"[\" xs-str \"]\"))\n    rest)))",
                     :filename "clojurescript/src/clj/cljs/core.clj",
                     :lines [985 992],
                     :link "https://github.com/clojure/clojurescript/blob/r1552/src/clj/cljs/core.clj#L985-L992"}),
 :history [["+" "0.0-927"]],
 :type "function",
 :full-name-encode "cljs.core_array",
 :source {:code "(defn array\n  [var-args]            ;; [& items]\n  (.call (.-slice (.-prototype js/Array)) (js* \"arguments\")))",
          :filename "clojurescript/src/cljs/cljs/core.cljs",
          :lines [90 94],
          :link "https://github.com/clojure/clojurescript/blob/r1552/src/cljs/cljs/core.cljs#L90-L94"},
 :full-name "cljs.core/array",
 :docstring "Creates a new javascript array.\n@param {...*} var_args"}

```