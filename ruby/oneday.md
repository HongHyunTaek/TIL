# Ruby



### 0.개요

- 루비는 순수 객체 지향 언어이다.
- 모든것이 객체
- Ruby on Rails 프레임워크 등장으로 유명해짐 



### 1.puts vs print

```ruby
3.times { print "hello"} # => hellohellohello
3.times { puts "hello"} # => hello
					  # => hello
					  # => hello

```

puts는 개행문자 포함 



### 3. p vs puts

```ruby
string = "hello"
puts string # hello => nil
p string => # "hello" => "hello"
```

### 4. Naming conventions

- 변수

  - snake_case

- 상수

  - CONSTANT

- 클래스

  - CamelCase

  

  

## 5.pry

- 설치

  ```ruby
  gem install pry
  ```

  

- 실행

  ```ruby
  pry
  ```

  





## 6. Inline statement

```ruby
# if문
puts "a=0" if a==0 
# "a=0"

puts "a=0" if a==1
# 출력안됨

# while문
c = 0
result = c+=2 while c < 50
put result 
# 50
    
puts "hi" if 0 
# hi
# 0 은 true!!!

```



## 7. case

```ruby
case name
	when "hyuntaek" then puts "hi hyuntaek"  
	when "tak" then puts "hi tak"  
	else puts "hi"  
end  
#hi hyuntaek
```



## 8. method

- 대부분의 언어
  - 클래식 밖  : function
  - 클래스 안 :  method
- 루비에서는 모든 function은 method

```ruby
#루비에서의 method 선언
def simple
    puts"simples!!"
end  

# 루비에서의 method는 괄호를 선택적으로 사용 
def asdf()
	puts "asdf"
end  
```

```ruby
# 리턴이 없을경우에 마자막문장값을 리턴합니다.
def add(a,b)
	return a+b
end  

def add2(a,b)
	a+b
end  

add 3,4
=> 7


#return을 선택적으로 사용할수가 있습니다.
def divide(a,b)
	return "I dont think so" if b == 0
	 a/b
end  


```



- 기본 매개변수

- ```ruby
  def factorial(n)
      n == 0 ? 1 : n * 
      factorial(n-1)
  end
  
  factorial # 에러 -> 매개변수 1개를 기대했으나 아무것도 주지않았다. 
  
  def factorial_d(n=5)
      n == 0 ? 1 : n * factorial_d(n-1)
  end
  factorial_d #120
  
  ```

## 9. BLOCK

```ruby
3.times do |asdf| # asdf에 인덱스 값을 넣어준다 
 	puts asdf
 end  # do - end가 블럭임 

3.times {puts "hello"}


```

```ruby
 def hihi
	 return "No block" unless block_given?
	 yield
end  

hihi # => "No block"
hihi {puts "hihi"} # hihi 

```

## 10.String



```ruby
a = "안녕하세요 \n 멋사입니다."
b = '안녕하세요 \n 멋사입니다.'

puts a 
#안녕하세요
#멋사입니다

puts b
#안녕하세요. \n 멋사입니다.

name = "taek2"
a = "#{name}님안녕하세요"
b = '#{name}님안녕하세요'
```













