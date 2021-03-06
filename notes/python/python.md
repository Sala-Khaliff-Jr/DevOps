# Python

[Python CheatSheet](https://github.com/aneagoie/ztm-python-cheat-sheet)

List

    list.sort modifies the list being sorted
    x = sorted(list) creates a new sorted list 

    Unpacking
    a, b, *other, d = [1,2,3,4,5]
    # a = 1, b= 2, other = [3,4] d = 5



Dictionary

    Instead of using dictionary['key'] use dictionary.get['key',default_value], because if a key is not found it doesn't throw error instead returns None or default value


Short Circuting

    Python doesn't check entire if statements based on "and" or "or", If a value of determined to take action it skips the rest of the if checking and continues.

DocStrings


    ''' ''' include inside a function to provide documentation about the function

    print(func_name) will print the docstring

    magic method

        print(funcname.__doc__) also prints

Arguments vs Parameters

    #parameter
    def greet(name,age):
        print(f'Hello {name} of {age} years old')

    #argument
    greet('steve',20)


@classmethod

    decorator that is used to access method in a class without creating an instane

    eg:

    @classmethod
    def method_name(cls,param1,..)
        return cls('param')

@staticmethod 

    same as classmethod, but cls param not required

    @staticmethod
    def mehtod1(param1,..):

Dunder / Magic Methods

        __method__

Method Resolution Order

    in multiple inheritance
        calssname.mro() returns the order which the class uses to resolve methods

[Wheel](https://realpython.com/python-wheels/)
