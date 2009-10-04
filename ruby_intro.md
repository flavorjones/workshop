!SLIDE

<img src="img/ruby-logo.jpg" width="250">

!SLIDE

<table width="100%">
<tr>
<td align="center">
<img src="img/ruby-logo.jpg" width="250">
</td>
<td align="center">
<img src="img/rails_logo.jpg">
</td>
</tr>
<tr>
<td align="center">
<span class="big-text">Language</span>
</td>
<td align="center">
<span class="big-text">Framework</span>
</td>
</tr>
</table>
# &nbsp;
# &nbsp;

!SLIDE 

## Matz (Yukihiro Matsumoto)

!SLIDE

####People want to express themselves when they program. 
####&nbsp;
####They don't want to fight with the language. 
####&nbsp;
####Programming languages must feel natural to programmers. 
####&nbsp;
####I tried to make people enjoy programming and concentrate on the fun and creative part of programming when they use Ruby.

!SLIDE

####The Java language is:
* simple, object oriented, and familiar.
* robust and secure.
* architecture neutral and portable.
* high performance.
* interpreted, threaded, and dynamic.

!SLIDE centereverything

## Ruby Language Overview
* Dynamically typed
* Interpreted
* Can be modified at runtime
* Object oriented
* Blocks & lambdas
* Perl-like Regular Expressions

!SLIDE

Let's get started

!SLIDE

IRB: Interactive RuBy

!SLIDE

    >> 4
    >> 4 + 4

!SLIDE

Everything is an object

!SLIDE

    “test”.upcase
    “test”.class
    “test”.methods

!SLIDE

Everything evaluates to something

!SLIDE

    2 + 2
    (2+2).zero?

!SLIDE

Variables, symbols, constants

!SLIDE
&nbsp;
    var 
    @var
    @@var
    $var
    :var
    VAR

!SLIDE
&nbsp;
    var   # could be a local variable
    @var  # instance variable
    @@var # class variable
    $var  # global variable
    :var  # symbol
    VAR   # constant
    
!SLIDE

Collections

!SLIDE

    my_array = ["cat", "dog", ”world"]
    my_hash = { :type => "cat", 
                :name => "Beckett",  
                :breed => "alley cat" }

!SLIDE

Iteration

!SLIDE

    my_array = ["cat", "dog", ”world"]
    my_array.each do |item|
      puts "hello " + item
    end

!SLIDE

    my_hash = { :type => "cat", 
                :name => "Beckett", 
                :breed => "alley cat" }
    my_hash.each do |key, value|
      puts "My " + key.to_s + " is " + value
    end

!SLIDE

Methods are messages

!SLIDE

    thing.do(4)
    thing.do 4
    thing.send "do", 4

!SLIDE

    method_missing

!SLIDE

Classes and methods

!SLIDE

    class MyClass
      def my_method
        puts "Doing something " +
             "REALLY IMPORTANT."
      end
    end

