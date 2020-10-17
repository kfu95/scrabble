What will make up scrabble:

Players:

    Properties: int Score, HashSet LettersHeld
    Methods: addToScore(int num),  removeFromHand(char[] word), addToHand(int lengthPut, LetterBag currLetters), skipTurn(), exchangeBag(char[] inHand, LetterBag currLetters)

Board:

    Properties: int SizeOfBoard, Array[][] boardTiles, Players[] players
    Methods: changeTurn(Player turn), drawTurn(), firstTurn(), validMove(), calculateScore(Array boardTilesBefore, boardTileAfter), putOnBoard(Player playerTurn, char[] word, int xCoor, int yCoor)

BoardTiles: 

    Properties: ENUM: mathPropertyToDo (0 -> valueOfTile, 1 -> valueOfTile * 2, 2-> valueOfTile *3, 3-> allWords *2  , 4-> allWords *3) 

LetterBag:

    Properties: HashMap of Letters, int lettersLeft
    Methods: removeFromBag(Char[] letterToRemove) -> return char + remove, addToBag(String letterToAdd)

Letters:

    Properties: int value, char letter

Dictionary:

    Properties: String Language, HashSet AllowedWords
    Methods: AddToAllowed(Char[] wordToAdd), removeFromAllowed(wordToRemove)

Game:

    Properties: Board, List of Players, LetterBag. 
    Methods: 

Notes: 
    - How to make more extensible? Different langauges, wordsAllowed, scoring tiles, num players
    - Game holds board + list of players + letter bag + Dictionary 
    - Don't make it a God Object, consider passing things into each other instead.  also, use Game as the bigger one