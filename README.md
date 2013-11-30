# Simple-Utility
The collection of simple functions for CommonLisp.  
Almost function is created for just simple notations.  
I separated this library because it repeatedly used for my works.


#### require:
  - [Quicklisp](http://www.quicklisp.org)
  - [ClozureCL](http://www.clozure.com/clozurecl.html) or [SBCL](http://www.sbcl.org)

#### usage:
__\#! reader macro__

	;;clojure style lambda.
	(funcall #!(+ 10 %) 100) => 110
	(funcall #!(- %2 %1) 10 100) => 90

__->__

	(-> (+ 1 2) (* 3) (- 10) (print)) is exapnd to (PRINT (- (* (+ 1 2) 3) 10))

__dup__

	(dup 10 4) => (10 10 10 10)
	(dup #!(+ 100 %) 4) => (100 101 102 103)
	(dup #!(+ 100 %) (list 72 75 79 83)) => (172 175 179 183)

__get-fullpath__

	;; returning absoulte full-pathname of path

__mklist__

	;; If input is list, just return it. else (list input)
	(mklist 1)  => (1)
	(mklist (list 1 2 3))  => (1 2 3)
	(mklist nil) => NIL
	
__rename-package-nicknames__  
__println__  
__partition__  
__cat__  
__do-while__  

	
