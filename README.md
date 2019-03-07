## 60 minutes of Ruby
### Variable assignment
```
a = 1
=> 1
```

### Flexible typing
```
a = 1
 => 1
a = "Hello"
 => "Hello"
1.to_s
 => "1"
"23".to_f
 => 23.0
"23".to_i
 => 23
```

### Nil/Nothingess
```
2.5.1 :001 > a = nil
 => nil
2.5.1 :002 > a.nil?
 => true
2.5.1 :003 > b = 0
 => 0
2.5.1 :004 > b.nil?
 => false
```

### Strings
```
2.5.1 :001 > greeting = "Hello world!"
 => "Hello world!"
```

### Substrings
```
2.5.1 :002 > greeting[2..5]
 => "llo "
```

### String methods
```
2.5.1 :001 > greeting.chars
 => ["H", "e", "l", "l", "o", " ", "w", "o", "r", "l", "d", "!"]
2.5.1 :002 > greeting.length
 => 12
2.5.1 :003 > "".empty?
 => true
2.5.1 :004 > "Hello world".split(" ")
 => ["Hello", "world"]
```

### String concatenation
```
2.5.1 :001 > name = "Alyssa"
 => "Alyssa"
2.5.1 :002 > "Hello " + name + "!"
 => "Hello Alyssa!"
```

### String interpolation
```
2.5.1 :001 > name = "Alyssa"
 => "Alyssa"
2.5.1 :002 > "Hello #{name}!"
 => "Hello Alyssa!"
```

### Code inside interpolation
```
2.5.1 :001 > "#{'Karma ' * 5}Chameleon"
 => "Karma Karma Karma Karma Karma Chameleon"
```

### Operations
```
2.5.1 :001 > a = 2
 => 2
2.5.1 :002 > b = 3
 => 3
2.5.1 :003 > a + b
 => 5
2.5.1 :004 > a - b
 => -1
2.5.1 :005 > a * b
 => 6
2.5.1 :006 > a / b
 => 0
2.5.1 :007 > a.to_f / b.to_f
 => 0.6666666666666666
2.5.1 :008 > (a.to_f / b.to_f).round(4)
 => 0.6667
2.5.1 :009 > a % b
 => 2
2.5.1 :010 > a ** b
 => 8
2.5.1 :011 > a > 2
 => false
2.5.1 :012 > a >= 2
 => true
2.5.1 :013 > a <= 2
 => true
2.5.1 :014 > a < 2
 => false
2.5.1 :015 > a < 3
 => true
2.5.1 :016 > a > 3
 => false
```

### Method Definitions
```
> def greeting(name)
>    "Hello #{name}!"
> end
 => :greeting
2.5.1 :004 > puts greeting("Alyssa")
Hello Alyssa!
```

### Arrays
```
2.5.1 :001 > arr = [1,2,3,4,5]
 => [1, 2, 3, 4, 5]
2.5.1 :002 > arr.sum
 => 15
2.5.1 :003 > arr.length
 => 5
2.5.1 :004 > arr.first(3)
 => [1, 2, 3]
2.5.1 :005 > arr.last(3)
 => [3, 4, 5]
2.5.1 :006 > arr.push(6)
 => [1, 2, 3, 4, 5, 6]
2.5.1 :007 > arr.pop
 => 6
2.5.1 :008 > arr
 => [1, 2, 3, 4, 5]
2.5.1 :009 > arr.delete(1)
 => 1
2.5.1 :010 > arr
 => [2, 3, 4, 5]
 2.5.1 :011 > arr[2]
 => 4
2.5.1 :012 > arr[-1]
 => 5
```

Arrays are Flexible!
```
[2.5.1 :001 > [1, "two", "3", 4.0]
 => [1, "two", "3", 4.0]
```


### Hashes
```
2.5.1 :001 > h = {a: "Alyssa", g: "Gabriel"}
 => {:a=>"Alyssa", :g=>"Gabriel"}
2.5.1 :002 > h[:a]
 => "Alyssa"
2.5.1 :003 > h[:g]
 => "Gabriel"
2.5.1 :004 > h.keys
 => [:a, :g]
2.5.1 :005 > h.values
 => ["Alyssa", "Gabriel"]
```

### Conditions
```
def water_status(minutes)
  if minutes < 7
    puts "The water is not boiling yet."
  elsif minutes == 7
    puts "It's just barely boiling"
  elsif minutes == 8
    puts "It's boiling!"
  else
    puts "Hot! Hot! Hot!"
  end
end

water_status(4)
=>
  The water is not boiling yet.

water_status(7)
=>
  It's just barely boiling

water_status(8)
=>
  It's boiling!

water_status(9*7)
=>
  Hot! Hot! Hot!
```

### Iterators with numbers
```
2.5.1 :001 > 5.times { puts "hello" }
hello
hello
hello
hello
hello
```

### Blocks: do..end & { .. }
```
def peee_7_times
  song_line = ""
  7.times { song_line += "pee "}
  song_line
end

def mi_7_times
  song_line = ""
  7.times do
    song_line += "mi "
  end
  song_line
end

def sing
  puts "Sa sho-#{peee_7_times}"
  puts "Ang da-#{mi_7_times}"
end

sing
=>
Sa sho-pee pee pee pee pee pee pee
Ang da-mi mi mi mi mi mi mi
```

### Classes and Instances
```
class Student
  attr_accessor :firstname

  def introduction
    puts "Hi, I'm #{firstname}"
    end
  end
end

student_1 = Student.new
student_1.firstname = "Skyler"
student_1.introduction
=>
  Hi, I'm Skyler
```
