# Flappy Bird AI using NEAT - Train Your Own AI to Play Flappy Bird!

Welcome to the **Flappy Bird AI** project! Here, we’ll explore how to use **NEAT** (NeuroEvolution of Augmenting Topologies) to train an AI to master the famous **Flappy Bird** game. Watch as the AI evolves and gets better over time, flying further and scoring higher without any human help.

This project uses **Python**, **Pygame**, and the **NEAT-Python** library to demonstrate how AI can learn to play games through evolutionary algorithms.

## Project Overview

In this project, we create a fully playable **Flappy Bird** environment using Pygame. The AI, controlled by a neural network, learns to play the game using the **NEAT** algorithm, which evolves the bird's "brain" over generations. The more the AI plays, the better it becomes at avoiding pipes and scoring points.

The goal is to train the AI so that it can survive longer and score higher by optimizing its neural network through evolution.

## Technologies Used
- **Python 3.8+**: Main programming language.
- **Pygame**: For building and rendering the Flappy Bird game.
- **NEAT-Python**: For implementing the NEAT algorithm to evolve the AI.
- **Pickle**: To save the best-performing AI model.

## Key Features
- **Flappy Bird Game**: A Pygame-based version of the popular game.
- **AI Training**: Uses a genetic algorithm (NEAT) to teach the bird to fly through the pipes.
- **Real-Time Stats**: Displays score, generation number, and how many birds are alive during gameplay.
- **Save & Load AI Models**: Save the best-performing AI bird model for future use.
- **Neural Network Visualization** (coming soon): See the neural network evolve in real-time.

## How It Works

1. **Initial Population**: A group of birds (each represented by a neural network) is randomly created.
2. **Fitness Evaluation**: Birds are evaluated based on how long they survive and how far they move without crashing.
3. **Natural Selection**: Birds that perform better are more likely to reproduce and pass their neural network "genes" to the next generation.
4. **Mutation**: Small mutations are introduced to create variety and increase the chances of improvement.
5. **Evolution**: Over generations, birds improve and become more skilled at avoiding pipes, eventually learning to play the game well.

## Project Structure

### 1. **Bird Class**
Manages the bird’s movement, jumping, and animations. It also handles the physics behind the bird’s falling motion.

```python
class Bird:
    def jump(self):
        # Makes the bird jump
    def move(self):
        # Updates the bird's movement
    def draw(self, win):
        # Draws the bird with its tilt and animation
```

### 2. **Pipe Class**
Manages the pipes, including their position, movement, and collision detection with the bird.

```python
class Pipe:
    def move(self):
        # Moves pipes to the left
    def draw(self, win):
        # Draws the pipes on the screen
    def collide(self, bird):
        # Checks for collisions with the bird
```

### 3. **Base Class**
Controls the moving ground, giving the illusion of movement as the bird flies.

```python
class Base:
    def move(self):
        # Moves the base along with the game’s motion
    def draw(self, win):
        # Draws the base at the bottom of the screen
```

### 4. **NEAT Algorithm**
The core of the AI. This function runs the NEAT algorithm for each generation, allowing birds to learn from their mistakes and improve over time.

```python
def eval_genomes(genomes, config):
    # Evaluates each bird and assigns fitness scores based on performance
```

### 5. **Main Run Function**
This is where the magic happens! It sets up the NEAT configuration, starts the evolution process, and begins the game loop.

```python
def run(config_file):
    # Configures and runs the NEAT algorithm for 50 generations
```

## How to Run This Project

### 1. Clone the Repository
First, clone this repository to your local machine:

```bash
git clone https://github.com/yourusername/flappy-bird-neat-ai.git
```

### 2. Install Dependencies
Make sure you have the required libraries installed. You can do this using pip:

```bash
pip install pygame neat-python
```

### 3. Run the Game
Start the game and AI training by running the following command:

```bash
python flappy_bird.py
```

### 4. NEAT Configuration
The AI's learning process is configured in the **config-feedforward.txt** file. You can tweak parameters such as population size, mutation rates, and fitness thresholds to see how they affect the AI's evolution.

## Saving & Loading Models
After training, the best bird model can be saved as a `pickle` file, so you can load it later and watch it play without retraining. To load a saved model:

```python
with open("best.pickle", "rb") as f:
    model = pickle.load(f)
```

## Future Improvements

- **Neural Network Visualization**: Display how the bird's neural network changes in real-time.
- **More Challenges**: Add new obstacles and random events to make the game more difficult for the AI.
- **Hyperparameter Tuning**: Adjust the NEAT settings to optimize the AI's learning process.

## Conclusion

This project demonstrates how evolutionary algorithms like NEAT can be applied to solve complex problems. Watching the AI improve and become more adept at playing Flappy Bird is both fascinating and a practical example of **machine learning** in action.

Feel free to clone the project, modify the code, and experiment with your own ideas! If you enjoyed working on this, please give it a ⭐ on GitHub!

---

Happy coding and have fun watching your AI learn to play Flappy Bird! 😊

