!SLIDE object_in_ruby transition=scrollUp
# Almost everything in Ruby is an object #
    @@@ ruby
    100.next     #=> 101
    'a'.next     #=> "b"

    100.class    #=> Fixnum
    "Ruby".class #=> String
    [].class     #=> Array
    {}.class     #=> Hash

    5.times { print "Ruby! " }
    #=> Ruby! Ruby! Ruby! Ruby! Ruby!

    5 + 5
    5.+(5) # both are the same

!SLIDE explore_in_ruby transition=scrollUp
# Explore in Ruby #

    * irb (Interactive Ruby Shell)

    * ri (Ruby Index)

    * RDoc

!SLIDE array transition=scrollUp
# Array #
    @@@ ruby
    numbers = ['zero', 'one', 'two', 'three']
    numbers[0]      #=> 'zero'
    numbers.first   #=> 'zero'
    numbers.last    #=> 'three'
    numbers[-1]     #=> 'three'

    list = []
    list << 'first'
    list << 'bar'
    list.pop # can be used as a stack

!SLIDE hash transition=scrollUp
# Hash #

    @@@ ruby
    profile = {
      :name => "Samnang",
      :age => 100 #Who knows :-)
    }

    profile[:name]
    profile[:age]

!SLIDE range transition=scrollUp
# Range #

    @@@ ruby
    range = 1..5
    range.to_a        #=> [1, 2, 3, 4, 5]

    range = 'a'..'z'
    range.to_a # array of strings from a to z

    range = 1...5
    range.to_a        #=> [1, 2, 3, 4]

    range.include? 2  #=> true

    array = [1, 2, 3, 4]
    array[0..2]       #=> [1, 2, 3]
    array[1...-1]     #=> [2, 3]

!SLIDE control_statement transition=scrollUp
# Conditionals and Iterators #

    @@@ ruby
    if something_true?
        do_something
    else
        do_another_thing
    end

    puts "I'll love Ruby" if not absence_today?
    puts "I'll love Ruby" unless absence_today?

    %w{Ruby HTML5 CSS3}.each do |lang|
        puts "#{lang} is so cool!"
    end

!SLIDE classes smaller transition=scrollUp
# Classes #

    @@@ ruby
    class BankAccount
      attr_accessor :name, :account_no
      attr_reader :balance

      def initialize(name)
        @name = name
        @balance = 0
      end

      def deposit(amount)
        @balance += amount
      end

      def withdraw(amount)
        @balance += amount
      end

      def active?
        #is account active or not
      end
    end

    account = BankAccount.new("Samnang")

!SLIDE mixins smaller transition=scrollUp
# Mixins #

    @@@ ruby
    module A
      def say_hello
        puts "Hello"
      end
    end

    module B
      def say_goodbye
        puts "Goodbye"
      end
    end

    class C
      include A
      include B
    end

    obj = C.new
    obj.say_hello
    obj.say_goodbye
