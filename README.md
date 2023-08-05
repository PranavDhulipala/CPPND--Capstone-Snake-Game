# CPPND: Capstone Snake Game

This starter repo for the Capstone project in the [Udacity C++ Nanodegree Program](https://www.udacity.com/course/c-plus-plus-nanodegree--nd213) was added with a few features mentioned in the section [below](#added-features). The code for this repo was inspired by [this](https://codereview.stackexchange.com/questions/212296/snake-game-in-c-with-sdl) excellent StackOverflow post and set of responses.

<img src="snake_game.gif"/>


## Added Features

The following features have been added to the game:

1. **Bonus Food Object**: A bonus food object now appears whenever the player's score is greater than 0 and is a multiple of 10. The bonus food object grants extra points when collected and decreases the speed of the snake, adding a new challenge to the game.

2. **Timer for Bonus Food**: The bonus food object has a limited appearance time of 10 seconds. After this time, the bonus food disappears from the game.

3. **Restart Option**: When the game is over, a pop-up window appears with an option to restart the game. Players can restart the game by clicking on the "OK" button in the pop-up window.

4. **Score Recording**: The game now keeps track of the player's score and saves it to a text file. This allows players to review their progress and high scores even after closing the game.


## Dependencies for Running Locally
* cmake >= 3.7
  * All OSes: [click here for installation instructions](https://cmake.org/install/)
* make >= 4.1 (Linux, Mac), 3.81 (Windows)
  * Linux: make is installed by default on most Linux distros
  * Mac: [install Xcode command line tools to get make](https://developer.apple.com/xcode/features/)
  * Windows: [Click here for installation instructions](http://gnuwin32.sourceforge.net/packages/make.htm)
* SDL2 >= 2.0
  * All installation instructions can be found [here](https://wiki.libsdl.org/Installation)
  >Note that for Linux, an `apt` or `apt-get` installation is preferred to building from source. 
* gcc/g++ >= 5.4
  * Linux: gcc / g++ is installed by default on most Linux distros
  * Mac: same deal as make - [install Xcode command line tools](https://developer.apple.com/xcode/features/)
  * Windows: recommend using [MinGW](http://www.mingw.org/)

## Basic Build Instructions

1. Clone this repo.
2. Make a build directory in the top level directory: `mkdir build && cd build`
3. Compile: `cmake .. && make`
4. Run it: `./SnakeGame`.

## Rubric followed

### Loops, Functions, I/O

| Success Criteria                                                | Specifications                                                                                          | Usage in Code                                                                                                   |
| -------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| The project demonstrates an understanding of C++ functions and control structures. | - A variety of control structures are used in the project.<br>- The project code is clearly organized into functions.<br>- The project reads data from a file and processes the data, or the program writes data to a file.<br>- The project accepts user input and processes the input. | - Control structures used through out the code.<br>- Functions are used through out the code.<br>- Game scroe is written to a text file at when the game is closed.<br>- User input processed for controlling the snake.             |

### Object-Oriented Programming

| Success Criteria                                                | Specifications                                                                                          | Usage in Code                                                                                                   |
| -------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| The project uses Object-Oriented Programming techniques.       | - The project code is organized into classes with class attributes to hold the data, and class methods to perform tasks.<br>- Classes use appropriate access specifiers for class members.     <br>- Class constructors utilize member initialization lists.       <br>- Classes abstract implementation details from their interfaces.     <br>- Classes encapsulate behavior.       <br>- Classes follow an appropriate inheritance hierarchy.       <br>- Overloaded functions allow the same function to operate on different parameters.       <br>- Derived class functions override virtual base class functions.       <br>- Templates generalize functions in the project.       | - The code uses Classes through out.<br>- Access specifiers are used in the classes.<br>- Member initialization lists are used through out the classes.<br>- All the classes hide implementation.<br>- Behavior encapsulated in all the classes.<br>- Inheritance hierarchy used in the Snake class as it inherits from GameObject class.<br>- Overloaded function Reset in class Snake.<br>- Virtual function Reset override in class Snake.<br>- WriteToFile Function uses template in the main.cpp file.       |
| Memory Management                                              | - The project makes use of references in function declarations.       <br>- The project uses destructors appropriately.       <br>- The project uses scope / Resource Acquisition Is Initialization (RAII) where appropriate.       <br>- The project follows the Rule of 5.       <br>- The project uses move semantics to move data, instead of copying it, where possible.       <br>- The project uses smart pointers instead of raw pointers.       | - References used wherever required, example : in the parameters in the Run function of the class Game.<br>- Destructor used in class Renderer for proper memory release.<br>- RAII pattern applied in the smart pointer used for sdl_render.<br>- Rule of 5 implemented in class Renderer.<br>- Move semantics used in function RunGame in the main.cpp.<br>- Smart pointer used in class Renderer.       |
| Concurrency                                                    | - The project uses multithreading.       <br>- A promise and future are used in the project.       <br>- A mutex or lock is used in the project.       <br>- A condition variable is used in the project.       | - Multithreading used to run the BonusFoodTimer in a seperate thread in the Game Class.<br>- Promise and future used in the main function to get GameResult.<br>- Mutex and unique_lock used in the Game Class methods to protect shared data is_bonus_food_active.<br>- Condition variable in function Update of Game class for thread synchronization.       |

## CC Attribution-ShareAlike 4.0 International


Shield: [![CC BY-SA 4.0][cc-by-sa-shield]][cc-by-sa]

This work is licensed under a
[Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa].

[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png
[cc-by-sa-shield]: https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg
