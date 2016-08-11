##ruby basic
###Proc vs lambda
```
#lambda 会返回它的调用函数，但 Proc 会结束它所位于的 function
def return_from_proc
  ruby_proc = Proc.new { return "return from a Proc" }
  ruby_proc.call
  return "The function will NOT reach here because a Proc containing a return statement has been called"
end

def return_from_lambda
  ruby_lambda = lambda { return "return from lambda" }
  ruby_lambda.call
  return "The function will reach here"
end

puts return_from_proc # display return from proc
puts return_from_lambda # display The function will reach here
```

