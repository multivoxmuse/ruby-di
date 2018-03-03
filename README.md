# ruby-di
Dependency injection in ruby

# Try it out!
`git clone` this repo and run:

```
cd ruby-di
./test.rb return-of-the-jedi
```

Then go read `classes/rotj.rb` and `test.rb` to understand what is happening under the hood


# Using
To use this:
  - put a new file containing a class that has a method `out` into the classes directory
`classes/tesb.rb`
```
class TheEmpireStrikesBack
  def out
    'i am your father'
  end
end
```
  - run `./test.rb name-of-your-new-class`
   
It will:
  - Require your new file, thereby putting your class into the scope
  - It will camelize to `NameOfYourNewClass`
  - It will instantiate it, and call its `out` method
```
$ ./test.rb the-empire-strikes-back
The empire did nothing wrong
```
  
The script will fall back to BaseExample ( see `classes/base_example.rb`) if your class name doesn't match one that exists

```
$ ./test.rb a-nonexisting-class
where is the rebel base
```

