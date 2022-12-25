# sys Module

The sys module in **Python provides** various functions and __variables that__ are used to manipulate different parts of the Python `runtime environment`. 
It allows operating on the interpreter as it provides access to the variables and functions that interact strongly with the interpreter.

```python
import sys
print(sys.version)

sys.version_info
release levels: 'alpha', 'beta', 'candidate', 'final'
```

### Typical python print

```python
print('%d %s cost $%.2f' % (6, 'bananas', 1.74))
```

### python f_string print
```python
print(f"{6} {'bananas'} ")

number = 6
text = 'bananas'
number2 = 132.23423876
print(f"{number} kjsdfhkjds :\n{text} \n number2 {number2:.3f} ")
```

#### sample use case for date time
```python
import datetime
today = datetime.datetime.now()
print(f"{havij:%B %d, %Y}") # November 30, 2022
print(f"{havij:%Y-%m-%d}") # 2022-11-30
print(f"Today is\n havij day \t {havij:%Y-%m-%d %H:%M}") # 2022-11-30 14:29


Today = datetime.date.today()
day_n_past = (Today-datetime.timedelta(days=5)).strftime('%Y%m%d') 
```
#### sample use case for query string building
```python
for i in range(5):#date_list:
    day_n_past = (Today-datetime.timedelta(days=i)).strftime('%Y%m%d')
    temp_query = '''SELECT *
    FROM table
    WHERE date_key = {day_n_past:%Y-%m-%d} '''
    
    # do something on "temp_query"
```

### making file_name with date_key in YYYY-MM_DD label 
```python
file_name = f'report_ITO_{today:%Y-%m-%d}.csv' # 2022-11-30

file_name2 =f'{self.transFile_name_pattern}_{datetime.strptime(temp_day, "%Y%m%d"):%Y%m%d}.csv' 

```


### Goood reference
[Python OS libraray reference](https://docs.python.org/3.9/library/os.html)
[30-useful-methods-from-python-os-module](https://www.analyticsvidhya.com/blog/2021/05/30-useful-methods-from-python-os-module/?)


[ormatted-string-literals-f-strings-python](https://www.geeksforgeeks.org/formatted-string-literals-f-strings-python)
[Google search page](www.google.com)

 ```python 
import numpy as np

for file in files:
    print(' time + file_name ')

#### old style
a = ['foo', 'bar', 'baz']
'{0[0]}, {0[2]}'.format(a)

'foo, baz'

'{my_list[0]}, {my_list[2]}'.format(my_list=a)

d = {'key1': 'foo', 'key2': 'bar'}
d['key1']

'{0[key1]}'.format(d)

d['key2']

'{my_dict[key2]}'.format(my_dict=d)


quantity = 6
item = 'bananas'
price = 1.74
print(f'{quantity} {item} cost ${price}')


quantity, item, price = 6, 'bananas', 1.74
print(f'Price per item is ${price/quantity}')


print(f' {10:#_b} , {10:#_x}')

import numpy as np

n = 28

def divisors(n):
    divisors = []
    for i in range(2, int(np.floor(np.sqrt(n)))):
        if n % i == 0:
            # print(i)
            print(f'n:{n}, i :{i}, n/i: {n/i}')
            divisors.append(i)
        # else:

        #     # print(i)
        #     print(f'n:{n}, i:{i}, n/i:{n/i}')

    return divisors

divisors(n)

```
