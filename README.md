What will make up scrabble:

Players:

    Properties: int Score, HashSet LettersHeld
    Methods: addToScore(int num),  removeFromHand(String word), addToHand(int lengthPut), skipTurn(), exchangeBag(char[] inHand)

Board:

    Properties: int SizeOfBoard, Array[][] boardTiles, Players[] players
    Methods: changeTurn(Player turn), drawTurn(), firstTurn(), validMove(), calculateScore(Array boardTilesBefore, boardTileAfter), putOnBoard(Player playerTurn, String word, int xCoor, int yCoor)

BoardTiles: 

    Properties: ENUM: mathPropertyToDo (0 -> valueOfTile, 1 -> valueOfTile * 2, 2-> valueOfTile *3, 3-> allWords *2  , 4-> allWords *3) 

LetterBag:

    Properties: HashMap of Letters, int lettersLeft
    Methods: removeFromBag(String letterToRemove) -> return String + remove, addToBag(String letterToAdd)

Letters:

    Properties: int value, char letter

Dictionary:

    Properties: String Language, HashSet AllowedWords
    Methods: AddToAllowed(String wordToAdd), removeFromAllowed(wordToRemove)


Notes: 
    - How to make more extensible? Different langauges, wordsAllowed, scoring tiles, num players
    - Board is the largest class, takes in Players, boardTiles, LetterBag, Letters, Dictionary