lambdaについて<br>

lambdaとは無名関数と日本語では呼ばれています。一般的な関数defは名前をつけて、<br>
その関数を定義する必要がありますが、lambdaは名前をつけなくてもいいため、<br>
無名関数と呼ばれています。<br>

それでは、二つの数の足し算を行うlambdaを使って、実際に使い方を見てみましょう。<br>

>>>lambda a, b: a+b <br>

このlambdaは ":" （コロン）の左側のaとbが引数、右側がその戻り値を表しています。 <br>
例えば、<br>

>>>l = lambda a, b: a+b <br>

>>>print(l(2,3)) <br>
とすると、"5"が表示されます。 <br>

この場合、一見lambdaをlと定義されているように見えますが、 <br>
"l　= "の右側は変数であり、この後、<br>
"l = 3" や "l = lambda a,b: a*2 + b*3"のように定義しなおすことが可能です。 <br>
これはdefを使った場合、例えば <br>

>>>def l(a,b) <br>
>>>  return a+b; <br>

のような関数の場合l(a,b)を再定義することはできません。 <br>
これがdefとlambdaの違いです。 <br>

しかし、正直なところ、lambdaを使わずにもPythonでコードを書くことはできます。 <br>
lambdaでできることはdefを使い関数として表すことができるからです。 <br>
では、いつlambdaを使うのか。主に二つの場合に使うことが多いです。 <br>

1.一度しか使わない <br>
2.定義したい関数が簡単なものである（ex. いくつかの数の和など）<br>

<br>
また、lambdaがよく使われるケースにmap関数があります。map関数のシンタックスは以下のようになっており、 <br>
sequenceの中の数字をfuntionを使って変えることができます。 <br>

>>>map(function, sequence) <br>

lambda, sequenceをそれぞれ以下のように定義すると、 <br>

>>>sqr = lambda x: x**2 <br>
>>>primes = [2, 3, 5, 7, 11] <br>

>>>list(map(sqr, primes)) <br>
[4, 9, 25, 49, 121] <br>

となります。 <br>
また、lambdaを定義することなく、 <br>2_

>>>list(map(lambda x: x**2, primes)) <br>

と、表すことも可能です。 <br>
