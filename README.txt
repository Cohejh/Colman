Colman Documentation

[ Installation ]
1. Install Python 3.10.6 from https://www.python.org/downloads/release/python-3106/

2. Drag the Colman folder into your desktop.

** Make sure there isn't another folder named "Colman" inside the original "Colman" folder. **

** If there is, then replace the original folder with the identically named one inside. **

3. In the Colman folder, there should be a folder named "engines", and select the right engine for you:

- If you have a Mac with an Intel chip, choose macOS -> Intel
- If you have a Mac with an Apple Chip (e.g. m1/m2 series etc.) choose macOS -> Apple Silicon
- If you have a very modern PC, choose Windows -> Next Gen
- If you have an old, or not so good PC, choose Windows -> General

4. Drag the file named "engine" inside the folder, into the base Colman folder. Then delete the engines folder and all its contents. 

5. ** Windows only ** Right click on the engine file, once it is in the Colman folder and select "Copy as path"

6. Go into the "src" folder, and open the "gui.py" file in a plain text editor - TextEdit for macOS, and Notepad for Windows.

7. Edit line 185, as stated below:

- If you have Windows, remove the text between the speechmarks, while leaving the speechmarks themselves. Then paste the path you copied earlier
imbetween the speechmarks so the line says: self.engine_path = "C:/Users/[UserName]/Desktop/Colman/engine.exe", with [UserName] being your
username

- If you have macOS, replace the text between the speechmarks so that the line says
something like: self.engine_path = "~/Users/[UserName]/Desktop/Colman/engine", ** Remember to replace [UserName] with your username**

8. Save the changes made with CMD + S or CTRL + S.

9. Open Terminal, and type "cd Desktop/Colman"

10. Then type the following:

- Windows: "python -m venv venv"
- macOS: "python3 -m venv venv"

11. Then type the following:

- Windows: "venv\Scripts\pip.exe install -r requirements.txt"
- macOS: "venv/bin/pip3 install -r requirements.txt"

You have finished, congratulations.

[Running the bot]

1. Open Terminal, and type "cd Desktop/Colman"

2. Type the following:

- Windows: "venv\Scripts\python.exe src\gui.py"
- macOS: "venv/bin/python3 src/gui.py"

3. In the window that just popped up, select the chess website (chess.com or lichess.org) and click open browser.

4. Start a game like you normally would, and make sure that the window is not obstructing the board.

5. Then click play and enjoy!

** To stop the bot, just press "2" or click the stop button. **
** Do not move the mouse while the bot is playing **

6. Once a game has finished, and you have set up a new one, click start again, to restart the bot.

[Engine parameters]

** The engine has many parameters that you can customise. **

- Calculation time: How long to give the engine to calculate. Larger values provide better moves, but take longer. 1s (1000ms) is
recommended, but 0.1s (100ms) is recommended for blitz/bullet chess games. Value is 1000 by default, but can go from 10 to 10000.

- Skill level: How good the engine plays. Higher values mean better moves, but you can make the engine weaker. Value is 20 by default,
but can go from 0 to 20.

- Depth Iterations: How many moves the engine thinks ahead. Higher values are better, but your computer may struggle. 20 is recommended for
a good computer, while 15 is for the average computer. VALUES OVER 15 ARE FOR POWERFUL COMPUTERS ONLY. Value is 15 by default, but can go
from 1 to 20.

- Memory: How much computer power to allocate to the engine. Value should be about halkf your processing power. If you have 4GB Ram, set to 2048,
if you have 8GB, set to 4096. If you have 16GB, set to 8192. If you have 32GB or higher, set to 16384. Most computer have 8GB, so it is set to 4096
by default.

- CPU Threads: Very techy stuff, do not touch unless you know what you are doing. If accidentaly changed, value is 1 be default.
