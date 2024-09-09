# AI Racing Simulator

Welcome to the AI Racing Simulator! This project is a car racing simulator built with Python, Pygame, and NEAT (NeuroEvolution of Augmenting Topologies). The simulator uses neural networks to train virtual cars to navigate a racing track autonomously.

## Features

- **Neural Network Training**: Uses NEAT to evolve neural networks that control the cars.
- **Pygame-based Simulation**: Utilizes Pygame for rendering the cars, track, and collision detection.
- **Customizable Environment**: Modify the track, car size, speed, and other parameters to suit your needs.

## Getting Started

### Prerequisites

Make sure you have the following installed:

- Python 3.x
- Pygame: `pip install pygame`
- NEAT-Python: `pip install neat-python`

### Running the Simulator

1. **Clone the repository** or download the code to your local machine.
2. **Prepare the environment** by installing the required libraries:

   ```bash
   pip install -r requirements.txt
   ```

3. **Place your track and car image** files in the same directory as the script. The simulator uses `car.png` for the car image and `silverstone.png` for the track.
4. **Run the simulator**:

   ```bash
   python ai_racing_simulator.py
   ```

## Configuration

The simulator is configured using the `config.txt` file, which specifies the parameters for the NEAT algorithm, such as population size, mutation rates, etc. You can adjust these settings to experiment with different configurations and see how they affect the performance of the neural networks.

## Controls

- The neural network controls the car automatically. 
- No manual input is required during the simulation.

## How It Works

- Each generation, a population of neural networks is created and evaluated.
- Each neural network controls a car, using sensors (radars) to detect distances to the track borders.
- Cars receive rewards based on the distance traveled without crashing. The networks with the highest rewards are selected and mutated to create the next generation.

## Customization

You can customize various aspects of the simulator, including:

- **Track and Car Images**: Replace `car.png` and `silverstone.png` with your own images.
- **Car Behavior**: Adjust parameters in the `Car` class, such as speed, radar range, collision detection, and rewards.
- **Neat Configuration**: Modify `config.txt` to change neural network settings like the number of nodes, activation functions, or the maximum number of generations.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [NEAT-Python](https://github.com/CodeReclaimers/neat-python) for the NEAT algorithm.
- [Pygame](https://www.pygame.org/) for the game engine.
