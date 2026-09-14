in kiro** using claude sonnet 4

make a three js scene with even lighting looking down at the origin. i want to setup a game world. make a grid of tiles. setup the game architecture so that the rows of the game will each be defined by their ground type. for now, just define rhe first ground type as grass (there will be more), and define each row as grass. grass is just a flat pale green color.

add super thin black lines running through the rows and white lines thru the cols

the lines seem to be offest by half a tile down and half a tile right

add a little white cube that starts in the center of the 5th row. the character can move it around the board by htting wasd. its centered in the center of the tile it stands on

how are the rows counted? i want row 0 to be the row closest to the camera at aspawn ( coming from positive z direction)

add a number at the rightmost tile of each row labeling which row it is numerically

make it so the first row is 0. if the user goes backwards past row 5, the board stays in place. otherwise it functions as is

currently theres still a row -1 and -2. make the first row 0

make it spawn on row 4. and make it so the board always has 15 rows visible

when the square gets past 5 the board starts moving. the board should never move

add a new ground type, street. street is grey, and rows of type street dont spawn until row 8. then rows of roads and grass start randowmly alternating

add rectangular prisms that are a little smaller than 2x1 tiles and half a tile tall that spawn on road rows that appear on one side of the row and dissapear on the otherside. on each row, all "cars" can only drive one direction, decided randomly.

make it so cars cant spawn on eachother . only have 5 cars on a road on a row at once. make them spawn less often

when the game starts, there should already be cars on the board.

if the character hits a car, they die

right now, the player seems to die when they are within a tile of the car. they should only be considered to have touched if they are on the same row, and col at the same time

switched to claude in browser**

make it so in this crossyroad style game, the payer cant backtrack once they have progressed forwards. if they pass the 5th relative row, the visible map shifts one row. if they go backwards, the map wont move

ok, close. right now, if the user tries to go back, they cant move. i want the map to be static if they try to move back, but the player themselves can transverse the parts of the map that are visible to them. its just that the map's rows wont change. if the player passes the 5th relative row again, the map progresses as before

add a button toggle on the side to enable and disable the row col markers plus the row numbers on the side

