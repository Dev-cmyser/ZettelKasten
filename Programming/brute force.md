# brute force

Created at: 2022:08:13 17:02

Tags: #python  #курс_алгоритмы-и-структуры-данных    #
__ 

# метод грубой силы
``` python 

def is_simple_number(x: int) -> bool:

    """this function  true if digit simple else not"""

  

    devizor = 2

    while devizor < x:

        if x % devizor == 0:

            return False

        devizor += 1

    return True

  
  

is_simple_number(5)

print(is_simple_number(5))

  

print(help(is_simple_number))
```

__

### Links
-[[]]
- [[]]
- [[]]
- [[]]
- [[]]
- [[]]
- [[]]
- [[]]