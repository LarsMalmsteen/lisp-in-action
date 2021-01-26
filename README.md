# Lisp in Action
**Lisp İş Başında**

The main language for this repo is Turkish.

This repo contains Lisp codes which are intented to give you an idea of how the Lisp works in reality. This is an attempt to fill the lack of a proper Lisp tutorial in circles where Turkish is being spoken.

Without further due, here is one sample Lisp code:

```
(defparameter *sentence* '(There Is More Than One Way To Do It))

(format t "~{~a~^~} ~%" (mapcar (lambda (x) (symbolize-c (char (symbol-name x) 0))) *sentence*))

(mapc (lambda (x) (format t "~A" (symbolize-c (char (symbol-name x) 0)))) *sentence*)

(defun symbolize-c (char)
  (intern (string char)))

;; Output
"TIMTOWTDI"
```

Here you see the most fundamental building block of Lisp in action: *Symbols* 

In its essence, the Lisp language basically contains only 4 things: An opening paranthesis `(` , space , closing paranthesis `)` and symbols.

Every other things like the `function` `variable` `data structure` `operator`, etc are made using only these 4 ingredients. Simple isn't it?
