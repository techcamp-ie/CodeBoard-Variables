Techcamp.js Application Programming Interface
---------------------------------------------

https://github.com/tc-john/TechcampBoard.git

Board
-----
A Board object, called board, is created by default. The default board is 10 squares by 10
squares (numbered 1 t0 10).

Properties:
	- 	squareWidth : the width of each board square in pixels. Default is 50px.
	- 	width : the width of the board in pixels. Default is 500px.
	- 	height : the height of the board in pixels. Default in 500px.

Methods:
	- 	clear() : clears everything off the board
	- 	setBoardConfiguration(aLetter) : pass it a letter and the board will be set up with
		some blue squares in certain positions. e.g. board.setBoardConfiguration('a');
	- 	addCharacter(aCharacter) : adds a character to the board e.g.
			roshan = new Roshan();
			board.addCharacter(roshan);
	- 	add(item) : adds an item to the board e.g.
			var s = new Square();
			board.add(s);
	-	remove(item) :	removes and item from the board e.g.
			var s1 = new Square();
			var s2 = new Square();
			board.add(s1);
			board.add(s2);
			board.remove(s1);
	- 	getItemOnSquare(x,y) : returns the item on the specified square. If there is no
		item on the square it will return null;
	-	getItemUnderCharacter(aCharacter) : given a character will return the board item 
		under it e.g.
			roshan = new Roshan();
			board.addCharacter(roshan);
			roshan.moveRandom();
			board.getItemUnderCharacter(roshan);

Square
------
A Square represents a .... square. Extends createjs.Shape.

To create a Square you can either do: 
	var mySquare;
	mySquare = new Square();

this will create a blue square. Or you can do:
	var myOtherSquare;
	myOtherSquare = new Square("Green");

this will create a green square. The colours you can use are listed here http://www.w3schools.com/html/html_colornames.asp

Properties:
	-	color : returns a String containing the color value of the square e.g. "Green"

Methods:
	-	moveToSquare(x,y) : will move the square to the board square represented by x and y e.g.
			var s = new Square();
			s.moveToSquare(3,2);
	-	moveRandom() : will move the square to a random square on the board
	-	getCurrentSquare() : returns an object that contains the position of the square on the board e.g.
			var s = new Square();
			s.moveToSquare(4,4);

			var boardPos = s.getCurrentSquare();
			var newX = boardPos.xSquare + 1;
			var newY = boardPos.ySquare + 1;

			s.moveToSquare(newX,newY); //square is now on 5,5
	-	setColor(newColor) : changes the color of the square e.g.
			s.setColor("Orange")

Circle
------
A Circle represents a .... circle. Extends createjs.Shape.

To create a Circle you can either do: 
	var myCircle;
	myCircle = new Circle();

this will create a blue circle. Or you can do:
	var myOtherCircle;
	myOtherCircle = new Circle("Green");

this will create a green circle. The colours you can use are listed here http://www.w3schools.com/html/html_colornames.asp

Properties:
	-	color : returns a String containing the color value of the circle e.g. "Green"

Methods:
	-	moveToSquare(x,y) : will move the circle to the board square represented by x and y e.g.
			var c = new Circle();
			c.moveToSquare(3,2);
	-	moveRandom() : will move the circle to a random square on the board
	-	getCurrentSquare() : returns an object that contains the position of the circle on the board e.g.
			var c = new Circle();
			c.moveToSquare(4,4);

			var boardPos = c.getCurrentSquare();
			var newX = boardPos.xSquare + 1;
			var newY = boardPos.ySquare + 1;

			c.moveToSquare(newX,newY); //circle is now on 5,5
	-	setColor(newColor) : changes the color of the circle e.g.
			c.setColor("Orange")

Roshan
------
Roshan is a animated character.

Methods:
	- 	moveToSquare
	-	moveRandom
	-	getCurrentSquare
	-	setSpeed
	-	eat
	-	walkRight
	-	walkLeft
	-	walkUp
	-	walkDown
	-	walkRandom
