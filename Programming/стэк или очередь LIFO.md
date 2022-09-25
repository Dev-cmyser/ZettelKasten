# стэк или очередь LIFO

Created at: 2022:09:11 16:37

Tags: #python  #курс_алгоритмы-и-структуры-данных    #
__ 

##

![[Pasted image 20220911182109.png]]
``` python 

"""
>>> clear()

>>> is_empty()
True
>>> push(1)
>>> push(2)
>>> push(3)
>>> is_empty()
False
>>> pop()
3
>>> pop()
2
>>> pop()
1
>>> is_empty()
True

"""
stack = []


def push(x):
    """
    >>> size = len(stack)
    >>> push(5)
    >>> len(stack) - size
    1
    >>> stack[-1]
    5
    """
    return stack.append(x)


def pop():
    return stack.pop()


def clear():
    stack.clear()


def is_empty():
    return len(stack) == 0


if __name__ == "__main__":
    import doctest

    doctest.testmod(verbose=True)


```

__

### Links

- [[heap(пирамида или куча)]]
- [[]]
- [[]]
- [[]]
- [[]]
- [[]]
- [[]]