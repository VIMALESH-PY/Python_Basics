'''
Author  :    Vimalesh R
Problem :   Rat in the Maze
            A rat need to exit from the Maze(2D - Array) which initial position(index) is (0,0) and exit position is (nxm).
            elements of the given matrix is only '0' and '1', rat can move @ '1'.

'''

maze=[[1,0,0,0],[1,1,1,0],[0,0,1,0,],[0,0,1,1]]

a=maze[:][:] # copy of the Maze

n,m = len(a) -1, len(a[0]) -1 # finding the size of the Matrix

initialpos,path=[0,0],[[0,0]] # Initilizing initial position and path

curpos,prepos=[0,0],[0,0] # Initilizing current position and preivous posiion

def nextpos(curpos): #Function to find next position
    global prepos,n,m
    x,y=curpos
    possiblepos=[[x-1,y],[x,y-1],[x+1,y],[x,y+1]]
    if x==0:
        possiblepos.remove([x-1,y])
    if y==0:
        possiblepos.remove([x,y-1])
    if x==n:
        possiblepos.remove([x+1,y])
    if y==m:
        possiblepos.remove([x,y+1])
    for i in possiblepos:
        if a[i[0]][i[1]]==1:
            curpos=[i[0],i[1]]
            if curpos==prepos:
                continue
            return curpos
    return "No Way"

while (curpos!=[n,m]):
    t = curpos
    curpos=nextpos(curpos)
    if curpos == 'No Way':
        print(curpos)
        break
    prepos = t
    path.append(curpos)
    
print(path)
