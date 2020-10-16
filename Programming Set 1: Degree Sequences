# Kyle Jacobson
# Professor Taylor
# MTH 325 - 02
# 24 February 2020

# The following function takes a graph represented by a
# dictionary as input and outputs the degree sequence of
# the graph as a list (in non-increasing order).

def degree_sequence(dict):
  
  # The initiliazed list for the function.
  seq = []
  
  # Parses through each element of the input.
  for vertex in dict:
    
    # Adds values to the list.
    seq.append(len(dict[vertex]))
    
    # Sorts the values of the list.
    seq.sort()
    
    # Reverses the list; the list is in non-increasing order.
    seq.reverse()

  return seq

print(degree_sequence({"A": ["B", "C", "D"], "B":["A", "C", "D"], "C":["A", "B", "D"], "D":["A", "B", "C"]}))

# This function takes a list of non-increasing integers as 
# input and uses the Erdos Gallai conditions to determine 
# whether or not this is the degree sequence of a graph.

def Erdos_Gallai(list):
  
  # The initiliazed list for the function.
  seq = []
  
  # Parses through each element of the input.
  for value in list:
      
    # Adds values to the list.
    seq.append(value)
    
    # Throws an error if any value is negative; return error message.
    if(value < 0):
      return("You cannot have a negative degree!")
  
  # Parses through the current list of values.
  for element in range(len(seq) - 1):
    
    # Checks if the inputted list is in non-increasing order; returns False if not.
    if(seq[element] < seq[element + 1]):
      return False

  # Checks if the list has at least one or more element.
  if(len(seq) >= 1):
    
    # Checks if the sum of the list is even; return True.
    if(sum(seq) % 2 == 0):
      return True
      
    # Checks if the sum of the list is odd; return False.
    else:
      return False

print(Erdos_Gallai([6,5,2,2,2,2,1]))
