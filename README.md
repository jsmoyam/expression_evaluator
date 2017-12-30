# expression_evaluator
Expression analyzer and evaluator for python

Example:
```
expr = '(a>3 and b<7) and (c=0 or d=1)'
values = {'a': 5, 'b': 5, 'c': 0, 'd': 2}
ev = ExpressionEvaluator(expr)
res = ev.evaluate(values)
```
```
expr = 'length[a]=9 and (not xxx and a contains "hello") and (b<10 or c=6)'
values = {'a': 'hello world', 'b': 8, 'c': 6, 'xxx': False}
ev = ExpressionEvaluator(expr)
res = ev.evaluate(values)
```
```
expr = 'length[a]=9 and (not xxx and a contains "hello") and (b<10 or c=6) and (xxx=False and True=have_passed_time["2017-01-01 00:00:00",60,weeks])'
values = {'a': 'hello world', 'b': 8, 'c': 6, 'xxx': False}
ev = ExpressionEvaluator(expr)
res = ev.evaluate(values)
```
```
expr = '(3+5)*a-4*3+10/5'
values = {'a': 2}
ev = ExpressionEvaluator(expr)
res = ev.evaluate(values)
```
```
expr = 'length[a]=9 and (not xxx and a contains "hello") and (b<10 or c=6) and (xxx=False and True=have_passed_time["2017-01-01 00:00:00",60,weeks]) and ((2*c)<b or (b+c)=50)'
values = {'a': 'hello world', 'b': 8, 'c': 6, 'xxx': False}
ev = ExpressionEvaluator(expr)
res = ev.evaluate(values)
```
