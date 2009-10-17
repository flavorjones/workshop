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

### Ruby 1.0 released in 1996
### open source 

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

Methods are messages

!SLIDE

    thing.do(4)
    thing.do 4
    thing.send "do", 4

!SLIDE

Operators are Methods

!SLIDE

    1 + 2
    1.+(2)
    1.send "+", 2

!SLIDE

    # is a comment

!SLIDE

#### Ruby aims to be elegant and readable
#### so punctuation and boilerplate are minimal

!SLIDE

You don't need semicolons
 
!SLIDE

Use parens when you need them
   
!SLIDE

    >> "Hello".gsub 'H', 'h' 
    => "hello"

    >> "Hello".gsub("H", "h").reverse 
    => "olleh"

!SLIDE

Variables, symbols, constants

!SLIDE

## :this_is_a_symbol
There is only one representation of a given symbol in memory, so it really
means "the thing named :this_is_a_symbol" to the ruby interpreter. 
In ruby,
we prefer symbols over hardcoded globals or strings. They're very lightweight.

!SLIDE

Collections

!SLIDE

Arrays are sized dynamically and can be of mixed types.
 
!SLIDE

    a = [1, 2, 3]
    a.push "four" #=> [1, 2, 3, "four"]
    a.pop #=> "four"
    a[0] #=> 1

!SLIDE

Hashes are like an associative map

!SLIDE
    states = {"MA" => "Massachusetts", "CA" => "California"}
    states["MA"]

!SLIDE

    my_hash = {:a_symbol => 3, "a string" => 4}
    my_hash[:a_symbol] 
    => 3

!SLIDE

String interpolation

!SLIDE

"string #{ruby code} string"

!SLIDE

    >> a = "world"   
    >> puts "hello #{a}"
    hello world
    >> a = 2
    >> puts "hello #{a}"
    hello 2
    >> a = nil
    >> puts "hello #{a}"
    hello 


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

Classes and methods

!SLIDE

    class Thing
      def return_something
        "something"
      end
    end

!SLIDE

    class Thing
      def do_something(a,b)
        a + b 
      end
    end


!SLIDE
&nbsp;
    var 
    @var
    @@var
    $var
    VAR

!SLIDE
&nbsp;
    var   # could be a local variable
    @var  # instance variable
    @@var # class variable
    $var  # global variable
    VAR   # constant
    
!SLIDE

Methods can take blocks, which are like anonymous functions.

!SLIDE

    my_array = ["cat", "dog", ”world"]
    my_array.each do |item|
      puts "hello " + item
    end

!SLIDE

   def do_something
      yield
   end

!SLIDE

    [1, 2, 3].each do |item|
       puts "#{item} is #{item.even? ? "even" : "odd"}."
    end
 
!SLIDE

Blocks can also return a value. Map translates each item in an array.
 
!SLIDE
 
    >> ["hello", "world"].map{ |string| string.upcase } 
    => ["HELLO", "WORLD"]
 
!SLIDE

#### more neat things about ruby

!SLIDE

#### duck typing
 
!SLIDE

    def print_even_or_odd(array_like_thing)
      array_like_thing.each do |item|
        puts "#{item} is #{item.even? ? "even" : "odd"}."
      end
    end
 
!SLIDE

    print_even_or_odd [1, 2, 3]
    print_even_or_odd 1..3
 
!SLIDE

#### advanced ruby 
 
!SLIDE

#### meta-programming
#### creating Domain-Specific Languages (DSLs)

!SLIDE

#Rails
#Rake
#Cucumber
#Rspec
#etc

!SLIDE

    method_missing

!SLIDE

#### private vs public 

!SLIDE

####Private really just means "please don't come in." 
####&nbsp;
####If someone has access to your runtime environment, they are trusted.
####&nbsp;
####Spend your time writing code (and testing it), not protecting yourself from other programmers.
 
!SLIDE

    class Fixnum
      def even?
        self % 2 == 0
      end
    end
    
    1.even? #=> false

!SLIDE

#### everything is an object

!SLIDE

#### Classes are objects
####&nbsp;
#### class methods are really just methods on the class object. 
####&nbsp;
#### Code evaluated in the scope of a class definition acts on the class object.

!SLIDE

Have fun!
