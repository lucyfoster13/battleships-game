# Battleships

Battleships is a popular, strategy-type guessing game. It is known worldwide as a pencil and paper game, which dates from World War I. It was published by various companies as a pad-and-pencil game in the 1930s and was released as a plastic board game by Milton Bradley in 1967. The game now also has many electronic versions as video games and mobile apps. 
Play the game [here](https://lucys-battleships-74c7927432db.herokuapp.com/)

## Project Goals

The goal of Battleships is to entertain the player and provide them with an engaging gameplay experience. Battleships is a well-known and loved game where the player must try to sink their opponent's battleships first. In this case, the user will play against the computer and their randomly generated board of five ships.

## Technologies

2. Python - programming language used for the creation of the game.
3. Gitpod - was used as the primary local IDE for coding.
4. GitHub - to store the project's code.
5. Heroku - to deploy the application.

## UX

### Strategy

1. Simplicity: The primary strategy for Battleships is to keep the game simple and intuitive. Users should be able to understand the rules and gameplay mechanics without needing extensive instructions.
2. Engagement: The game has been designed to keep players engaged and entertained throughout the entire gaming session.
3. Accessibility: Battleshisps is accessible to a wide range of players, including those with little to no gaming experience. This is due to designing the game interface with clear and easy-to-understand elements.
4. Feedback: Providing feedback to the player is crucial for a good user experience. The game should give clear feedback on each action taken by the player, such as whether their input was valid, and if their guess was correct or incorrect.

### Scope

1. Gameplay Mechanics: The core gameplay mechanics of Battleships involve guessing sqaures on a grid to see igf the opponent has a ship placed there. The scope of the game includes implementing these mechanics in a user-friendly and enjoyable manner.
2. The visual design of Battleships encompasses elements such as the user and computer's boards, complete with an easy to understand key for when a ship has been hit or missed.
### Structure

Since this game works on the command line, information is displayed to the user gradually and depending on their request.
When the game begins, the user is prompted to place their ships on their board and then to start guessing sections on their opponent's board.
A successful guess incurs results in an X displayed on the board. A miss is marked by a -.

### Surface

Due to this program being built for terminal use, there was not much design. I used basic keyboard letters to keep the game simple and easy to understand.

## Features

### Welcome block

The player is presented with a welcome screen giving them details of the game.

![Welcome](readme_images/welcome.png)

### Game

The user is prompted to start placing their ships on their board. Input validation is implemented in the code to ensure there are no errors and the board is setup correctly.
The user is then prompted to start guessing their opponent's placements. As before, if they guess a row or column outside of the designated scope, or something they have already guessed,they will be alerted and prompted to re-enter the selection.

![Game](readme_images/game.png)

### Finish game

On completion of the game, the user is notififed if they have won or lost and is given the option to play again.

![Win](readme_images/win.png)

![Finish](readme_images/game_over.png)

## Testing

### Manual testing

Extensive manual testing was carried to ensure the controls worked as intended and the game didn't crash in any cases of invalid input.
The game performed as expected. In the earlier iterations of the game, I had the error notifications inside a try except block which did not work. I fixed this error by converting to a simple if else block.

### Python Validation

I validated my run.py file using [Code Institute's Python Linter](https://pep8ci.herokuapp.com/#).

![Validator](readme_images/validator.png)

### Bugs

Bugs and errors encountered during the coding of the project were solved through continued testing throughout the development. Using print statements and the Git terminal with python3 run.py, I tested the code to observe its behavior, identify any errors, and address them.
When I ran my Code through the [PEP8](https://pep8ci.herokuapp.com/#), I found such syntax errors:

- trailing whitespace;
- continuation line under-indented for visual indent;
- expected 2 blank lines, found 1;
- line too long.

All errors have been fixed except for two cases of lines that are too long. I tried to separate the lines and then received areas about indentation. I tried many different levels of indentation and still received the same error. For this deployment, I decided to leave the two instances of longer lines as I knew the indentation was correct and would be read by the terminal. This is something I will continue to troubleshoot in order to receive no errors.

## Deployment

### Version Control
The site was created using the Gitpod code editor and pushed to github to the remote repository ‘camera-club’.

The following git commands were used throughout development to push code to the remote repo:

```git add . ``` - This command was used to add any modifications to the staging area before they were committed.

```git commit -m “commit message”``` - This command was used to commit changes to the local repository queue, ready for the final step.

```git push``` - This command was used to push all committed code to the remote repository on github.

### Creating the Heroku app

This project was deployed using Code Institute's mock terminal for Heroku. Below are the steps I followed to be able to deploy the terminal to the website:

1. Create a new Heroku app on the Heroku website.
2. Create config vars:
   - on the _Settings_ tab click "Reveal Config Vars";
   - in the field for key enter "CREDS", all capital letters;
   - copy the entire creds.json file from our workspace and paste it into the value field;
   - click “Add”;
   - add another config var, key "PORT" and set this to "8000".
3. Add two buildpacks from the _Settings_ tab. The ordering is as follows:
   - `heroku/python`
   - `heroku/nodejs`
4. Connect the Heroku app to the repository on GitHub.
5. Enter the name repository, click Search and click Connect.
6. Click Deploy Branch.

### Clone the Repository Code Locally
Navigate to the GitHub Repository you want to clone to use locally:

- Click on the code drop down button
- Click on HTTPS
- Copy the repository link to the clipboard
- Open your IDE of choice (git must be installed for the next steps)
- Type git clone copied-git-url into the IDE terminal

The project will have been cloned on your local machine and be ready to use. 

## Credits

I watched a number of walkthrough videos on Youtube to get a sense of the layout and structure of the game, such as this series by [Knowledge Mavens](https://www.youtube.com/watch?v=tF1WRCrd_HQ&t=1440s). These videos were very helpful for helping me understand the logic of the code but had a number of syntax errors and Python convention conflicts that I amended to comply with the learning on the course.
