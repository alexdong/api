## clojure.browser.repl

 <table border="1">
<tr>
<td>namespace</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
</table>

evaluate compiled cljs in a browser. send results back to server

---


Source Docstring:

```
Receive - Eval - Print - Loop

  Receive a block of JS (presumably generated by a ClojureScript compiler)
  Evaluate it naively
  Print the result of evaluation to a string
  Send the resulting string back to the server Loop!
```

---

###### Public Symbols:

 <table>
<thead><tr>
<th>=</th>
<th>Name</th>
<th>Type</th>
<th>History</th>
</tr></thead>
<tr>
<td></td>
<td><samp>[bootstrap](../clojure.browser.repl/bootstrap.md)</samp></td>
<td><samp>function</samp></td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-3115"><img valign="middle" alt="[+] 0.0-3115" title="Added in 0.0-3115" src="https://img.shields.io/badge/+-0.0--3115-lightgrey.svg"></a> </td>
</tr>
<tr>
<td></td>
<td><samp>[connect](../clojure.browser.repl/connect.md)</samp></td>
<td><samp>function</samp></td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
<tr>
<td></td>
<td><samp>[evaluate-javascript](../clojure.browser.repl/evaluate-javascript.md)</samp></td>
<td><samp>function</samp></td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
<tr>
<td></td>
<td><samp>[flush-print-queue!](../clojure.browser.repl/flush-print-queueBANG.md)</samp></td>
<td><samp>function</samp></td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/1.7.48"><img valign="middle" alt="[+] 1.7.48" title="Added in 1.7.48" src="https://img.shields.io/badge/+-1.7.48-lightgrey.svg"></a> </td>
</tr>
<tr>
<td></td>
<td><samp>[get-ua-product](../clojure.browser.repl/get-ua-product.md)</samp></td>
<td><samp>function</samp></td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-3058"><img valign="middle" alt="[+] 0.0-3058" title="Added in 0.0-3058" src="https://img.shields.io/badge/+-0.0--3058-lightgrey.svg"></a> </td>
</tr>
<tr>
<td></td>
<td><samp>[load-queue](../clojure.browser.repl/load-queue.md)</samp></td>
<td><samp>var</samp></td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-3115"><img valign="middle" alt="[+] 0.0-3115" title="Added in 0.0-3115" src="https://img.shields.io/badge/+-0.0--3115-lightgrey.svg"></a> </td>
</tr>
<tr>
<td></td>
<td><samp>[order](../clojure.browser.repl/order.md)</samp></td>
<td><samp>var</samp></td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
<tr>
<td></td>
<td><samp>[print-queue](../clojure.browser.repl/print-queue.md)</samp></td>
<td><samp>var</samp></td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/1.7.48"><img valign="middle" alt="[+] 1.7.48" title="Added in 1.7.48" src="https://img.shields.io/badge/+-1.7.48-lightgrey.svg"></a> </td>
</tr>
<tr>
<td></td>
<td><samp>[repl-print](../clojure.browser.repl/repl-print.md)</samp></td>
<td><samp>function</samp></td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
<tr>
<td></td>
<td><samp>[send-print](../clojure.browser.repl/send-print.md)</samp></td>
<td><samp>function</samp></td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
<tr>
<td></td>
<td><samp>[send-result](../clojure.browser.repl/send-result.md)</samp></td>
<td><samp>function</samp></td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
<tr>
<td></td>
<td><samp>[start-evaluator](../clojure.browser.repl/start-evaluator.md)</samp></td>
<td><samp>function</samp></td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
<tr>
<td></td>
<td><samp>[wrap-message](../clojure.browser.repl/wrap-message.md)</samp></td>
<td><samp>function</samp></td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
<tr>
<td></td>
<td><samp>[xpc-connection](../clojure.browser.repl/xpc-connection.md)</samp></td>
<td><samp>var</samp></td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
</table>


---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/clojure.browser.repl.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files