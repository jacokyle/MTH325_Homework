# Kyle Jacobson
# Professor Taylor
# MTH 325 - 02
# 23 March 2020

# The following function takes two inputs: one a graph, 
# and the other a coloring of the vertices, 
# and determines whether or not the coloring is a 
# proper vertex-coloring of the given graph.

def is_proper(pairs, coloring):
    # Loops through order.
    for vertex in pairs:
      
        # Iterates through the max range of the pairs graph.
        for x in range(len(pairs[vertex])):
          
            # Checks if the vertex coloring value is equal to coloring of the pairs.
            if coloring[vertex] == coloring[pairs[vertex][x]]:
                return False

    return True

# This function takes two inputs: one a graph, 
# and the other an ordering of the vertices as a list, 
# and returns the proper vertex-coloring produced by the 
# greedy algorithm over the ordering in the list. 
    
def greedy(pairs, coloring):
    color = {}
  
    # Loops through order.
    for vertex in coloring:
      
        # Assign the first dictionary with color "1".
        color[vertex] = 1

        # Adds connected vertices to a list and colors them.
        nearbyColors = []
        
        # Iterates through the adjacent vertices in the graph.
        for adjacent in pairs[vertex]:
          
            # If a vertex is next to another vertex, add it to nearbyColors.
            if adjacent in color:
                nearbyColors.append(color[adjacent])
                
        # While current color is the same as the adjacent vertices,
        # increments that vertex color by 1.
        while(color[vertex] in nearbyColors):
            color[vertex] += 1
    
    # Outputs the proper vertex-coloring using a greedy algorithm.
    print(color)
