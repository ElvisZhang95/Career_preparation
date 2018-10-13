### <span style="color:pink">Python</span>
1. Tree可以借助Tail的方法来保存 tail是自己设的（借用）
2. 如果想要让data structure的remove达到 O(1)的效果，可以借助于dictionary
3. Python Filter(function, iteration) 可以把后面的数组通过function来过滤掉
   e.g. filter(None, [...])即把数组里的None过滤掉
4. join function 即插入...在数组中
   e.g.
   s ='\'
   seq = ['a','b','c']
   s.join(seq) = a\b\cMM
5. zip(* iterable) 类似于reshape
6. any() 就是遍历查找有没有 具体看python built-in function
7. Bit Manipulation
8. Sorted() function
9. LinkedList里面的swap l1, l2 = l2, l1只换value 不换next后面的node
10. Lambda
>The lambda operator or lambda function is a way to create small anonymous functions
>e.g. lambda argument_list: expression
>e.g. complex example:(define a comparison)
>comp=lambda a,b:1 if a+b>b+a else -1 if a+b<b+a else 0
11. filter
>filter(func, sequ)
>filter out all the elements of a sequence, for which the function return True. only the function return true, the element will be produced in the list.
> example: list(filter(lambda x: x%2 =0, sequence))
>
12. Map
> map() is a function which take two arguments
> in python 3, it will return a list
> r = map(func, seq)
> all the element in sequence will apply the function and return the result list
> tips: we can use lambda to define the function
> combine lambda and map (example)
> C = [39.2, 36.5, 37.3, 38, 37.8]
> F = list(map(lambda x: (float(9)/5)*x + 32, C))
>
>a = [1, 2, 3]
> b = [17, 12, 11, 10]
> c = [-1, -4, 5, 9]
> list(map(lambda x, y, z : 2.5*x + 2*y - z, a, b, c))
13. Reduce
>not usual in the python3
>reduce(func, seq), support seq = [s1,s2,s3]
>=func(func(s1,s2), s3)
14. Collection: Counter
> count the frequency of element in a sequence.
> c = collections.Counter(t)
>t is the sequence

15. Enumerate
> for c, value in enumerate(my_list, 1):
>  print(c, value)
> here, c is the index counter start from 1.
> value is the element in the list
