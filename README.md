# dictionaries
# various independent examples of creating and calling dictionaries

# basic dictionary functions
sample_dict = {'weather': 'beautiful', 'tea': 'iced', 'age': 29}
print(sample_dict['weather'])

# updating dictionary values, printing individual values, deleting an item(key and value)
stock = {'oranges': 10, 'apples': 5, 'pears': 10}
print(stock)
stock['oranges'] = 13
stock['apples'] = 9
stock['pears'] = 14
print(stock)
stock['pears'] += 1
print(stock)
print(stock['pears'])
print(stock['apples'])
del stock['oranges']
print(stock)
stock['cherries'] = 4
print(stock)
# when printed:
beautiful
{'oranges': 10, 'apples': 5, 'pears': 10}
{'oranges': 13, 'apples': 9, 'pears': 14}
{'oranges': 13, 'apples': 9, 'pears': 15}
15
9
{'apples': 9, 'pears': 15}
{'apples': 9, 'pears': 15, 'cherries': 4}


# checking for membership inside a dictionary
stock = {'oranges': 10, 'apples': 5, 'pears': 10}
print('apples' in stock)
print('grapes' in stock)
print('lollipop' not in stock)

# sell some oranges
stock['oranges'] -= 2
print(stock)
# add 3 apples to the stock
stock['apples'] += 3
print(stock)
# we are out of pears
del stock['pears']
print(stock) 
# is there pizza in stock ?
print('pizza' in stock)
# when printed:
True
False
True
{'oranges': 8, 'apples': 5, 'pears': 10}
{'oranges': 8, 'apples': 8, 'pears': 10}
{'oranges': 8, 'apples': 8}
False

# let's create a list of all the keys and values and pairs as well from the dictionary
stock = {'oranges': 10, 'apples': 5, 'pears': 10}
fruits = stock.keys()
print(fruits)
number_available = stock.values()
print(number_available)
together = stock.items()
print(together)
# when printed:
dict_keys(['oranges', 'apples', 'pears'])
dict_values([10, 5, 10])
dict_items([('oranges', 10), ('apples', 5), ('pears', 10)])

# converting a dictionary into a list and a list into a dictionary
stock = {'oranges': 10, 'apples': 5, 'pears': 10}
print(list(sorted(stock.keys())))
# when printed:
['apples', 'oranges', 'pears']

# more ditionary functions:
def fillable(stock, merch, n):
  if n <= stock[merch]:
    return True
  if n >= stock[merch]:
    return False
stock = {'apples': 12, 'bananas': 14, 'oranges': 6}
print(fillable(stock, 'apples', 14))
print(fillable(stock, 'bananas', 12))
fillable(stock, 'oranges', 12)
# when called:
False
True
False

# turning a list into a dictinoary
def user_contacts(lst):
  dictionary = {}
  for person in lst:
    name = person[0]
    if len(person) > 1:
      code = person[1]
    else:
      zip_code = None
    dictionary[name] = code
  return dictionary 

lst = [["Grae Drake", 98110], ["Bethany Kok"], ["Alex Nussbacher", 94101], ["Darrell Silver", 11201]]
user_contacts(lst)
# when called:
{'Alex Nussbacher': 94101,
 'Bethany Kok': 98110,
 'Darrell Silver': 11201,
 'Grae Drake': 98110}
 
 
