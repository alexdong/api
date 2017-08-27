---
name: cljs.core/js->clj
see also:
  - cljs.core/clj->js
---

## Summary

## Details

Recursively transforms JavaScript arrays into ClojureScript vectors, and
JavaScript objects into ClojureScript maps.

With option `{:keywordize-keys true}` will convert object fields from strings to
keywords.

Note that `js->clj` is not optimized for speed and the [transit.cljs] library is
recommended for parsing large amounts of JSON data.

[transit.cljs]:https://github.com/cognitect/transit-cljs

## Examples

Parse a JSON string:

```clj
(def json "{\"foo\": 1, \"bar\": 2, \"baz\": [1,2,3]}")
(def a (.parse js/JSON json))
;;=> #js {:foo 1, :bar 2, :baz #js [1 2 3]}
```

Convert JSON data `a` to ClojureScript data:

```clj
(js->clj a)
;;=> {"foo" 1, "bar" 2, "baz" [1 2 3]}

(js->clj a :keywordize-keys true)
;;=> {:foo 1, :bar 2, :baz [1 2 3]}
```
