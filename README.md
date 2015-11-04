# watch bug demo

fileset passed to watch task from previous tasks is not merged properly

```
;; cljs-repl and reload modifications lost to tasks after watch
boot cljs-repl reload inspect watch inspect cljs
```

vs.

```
;; modifications done inside watch loop work as expected
boot inspect watch cljs-repl reload inspect cljs
```
