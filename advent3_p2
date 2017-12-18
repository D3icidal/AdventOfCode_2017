require 'matrix'
puzzleInput = 325489
boardSize = Math.sqrt(puzzleInput).ceil
# arrayBoard = Array.new(boardSize){Array.new(boardSize)} #=> [[nil, nil], [nil, nil], [nil, nil]]

# arrayBoard index represents the number (so skip 0), with the values as polar cord

# row, col, default_value = 5, 4, 0
# arr_2d = Array.new(row){Array.new(col,default_value)}
# => [[0, 0, 0, 0],
#     [0, 0, 0, 0],
#     [0, 0, 0, 0],
#     [0, 0, 0, 0],
#     [0, 0, 0, 0]]
arrayBoard = Array.new(boardSize){Array.new(boardSize,0)}
i=2 #memory space itartes sequanntially
x=1 #counter for movement limit
xi=0 #counter for x
r=(boardSize/2) #starting spot
c=(boardSize/2)+1 #starting spot (C starts on the second spot)

boardSpaces = boardSize*boardSize

arrayBoard[r][c-1] = 1
arrayBoard[r][c] = 2
puts("puzzleInput: \t#{puzzleInput}")
puts("boardSpaces: \t#{boardSpaces}")
puts("#{r}x#{c}=2")
puts("Spaces: #{boardSpaces}")
puts("arrayBoard[r][c-1]: #{arrayBoard[r][c-1]}")
puts("arrayBoard[r][c]: #{arrayBoard[r][c]}\n\n")


while i <= boardSpaces

  while xi < x    # go up
    i+=1
    r-=1
    arrayBoard[r][c] = i
    puts("arrayBoard #{r}x#{c}: #{i}")
    xi+=1
  end
  x+=1
  xi=0


  while xi < x    # go left
    i+=1
    c-=1
    arrayBoard[r][c] = i
    puts("arrayBoard #{r}x#{c}: #{i}")
    xi+=1
  end
  xi=0


  while xi < x    # go down
    i+=1
    r+=1
    arrayBoard[r][c] = i
    puts("arrayBoard #{r}x#{c}: #{i}")
    xi+=1
  end
  x+=1
  xi=0


  while (xi < x)  &&  (i <= boardSpaces)  # go right
    i+=1
    c+=1
    arrayBoard[r][c] = i
    puts("arrayBoard #{r}x#{c}: #{i}")
    xi+=1
  end
  xi=0

end

arrayBoard.last.pop
# # Display board
arrayBoard.each do
  |i| puts("\t#{i.join("\t")}\n\n")
end
# end display board

movesNeeded=0
inputLocation = Matrix[*arrayBoard].index(puzzleInput) #Find cordinates of input puzzle number.
puts("Starting PuzzleLocation: #{inputLocation} \t Goal: [#{(boardSize/2)}, #{(boardSize/2)}]")

puts("#{inputLocation[0] - (boardSize/2)} moves vertically" )
puts("#{inputLocation[1] - (boardSize/2)} moves sideways" )












  #=> [1, 1]
# ret = []
# arrayBoard.each_with_index {|x, i| if x.include?(puzzleInput) then ret << i end }
# puts("#{ret}")
# arrayBoard.each_index { |i| j = arrayBoard[i].index 'S'; p [i, j] if j }
# puts("#{p}")
# c=(boardSize/2)+1 #starting spot (C starts on the second spot)
# boardSpaces = boardSize*boardSize
# arrayBoard[r][c-1] = 1
