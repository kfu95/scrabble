What will make up scrabble:

Players:
    Properties: int Score, HashSet LettersHeld
    Methods: addToScore(int num)

Board: 
    Properties: int SizeOfBoard, Array[][] boardTiles

    Methods: changeTurn(Player turn)

BoardTiles: 
    Properties: int mathPropertyToDo,
    

LetterBag:
    Properties: HashMap of Letters
    Methods: removeFromBag(String wordToRemove), addToBag(String wordToAdd)

Letters:
    Properties: int value, char letter

Dictionary:
    Properties: String Language, HashSet AllowedWords
    Methods: AddToAllowed(String wordToAdd), removeFromAllowed(wordToRemove)