# module3_4hard.py
def green(numbers):
    sum=0
    for i in numbers:
         if isinstance(i, int):
            sum+=i
         elif isinstance(i,str):
            sum+=len(i)
         elif isinstance(i,dict):
              sum+=green(i.keys())
              sum+=green(i.values())
         else:
             sum+=green(i)
    return sum
data_structure = [
[1, 2, 3],
{'a': 4, 'b': 5},
(6, {'cube': 7, 'drum': 8}),
"Hello",
((), [{(2, 'Urban', ('Urban2', 35))}])
]
result = green(data_structure)
print(result)
