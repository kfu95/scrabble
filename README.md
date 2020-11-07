What will make up scrabble:

Can think of dividing it in ways of more games than just scrabble to make it more extensible since all games have diff rules
and diff logic flow but want to make it as extensible as possible

Player:
    Properties: int Score, string name
    Methods: getScore, getName

ScrabblePlayer:
    Property: String[] lettersHeld

PlayerController:
    Methods: addToScore(int num, Player currPlayer), addToHand(), skipTurn(), removeFromHand()
 
Board:
    array[][] boardTiles
    int SizeOfBoard, addTile

    Properties: int SizeOfBoard, Array[][] boardTiles, Players[] players
    Methods: CreateBoard(Array[][] boardTiles)
//business logic, aka word checking
Board Controller:

    Methods: AddWord, AddScoreToPlayer, EndGame, validWordCheck, computeScore
    

BoardTiles: 

    Properties: ENUM: mathPropertyToDo (0 -> valueOfTile, 1 -> valueOfTile * 2, 2-> valueOfTile *3, 3-> allWords *2  , 4-> allWords *3) 

LetterBag:

    Properties: HashMap of Letters, int lettersLeft
    Methods: removeFromBag(Char[] letterToRemove) -> return char + remove, addToBag(String letterToAdd)

LetterBagController

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
    - But when information gets more complicated, you can split up the responsibility along that line, So you can have a Board class that holds information about the board and supports very elementary operations and a "BoardController" class that makes business logic level actions on the "Board"
    - Board interface  "addTile()
    - while the BoardController can implement "addWord()"

Side Notes:
    - What else can use a controller, what else can be more complex than it seems. Board controller can also check for valid Moves
    - Player controller too. can also control things players do 