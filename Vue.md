# About Vue
## ***methods 和 computed 的性能***
&emsp;&emsp;当有需要对一个变量进行多次操作时，既可以使用属性methods来定义一个方法也可以使用属性computed来计算返回值。一般建议使用属性computed来计算，因为当一个变量被赋值后，在一段时间里变量的值并不会被改变时，Web的cookie会自动存储该值，当再次用到这个变量时，并不会再次执行computed里的返回的值，而是直接用cookie储存的值。而methods却不一样，若在methods定义方法获取该变量的值，每次调用都会调用methods的定义的方法，这使性能降低了。当然如果不是经常操作某个变量的值，其实methods和computed都差不多。
