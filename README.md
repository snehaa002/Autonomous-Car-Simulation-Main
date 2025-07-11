Neural Network Self-Driving Car
A browser-based simulation of a self-driving car using neural networks and genetic algorithms. The car learns to navigate through traffic using sensors and a neural network brain.

🚗 Live Demo
Try the simulation here!

🌟 Features
Neural Network Brain: The car uses a multi-layer neural network to make driving decisions
Sensor System: 5 sensors detect obstacles and road boundaries
Traffic Simulation: Navigate through randomly placed traffic cars
Genetic Algorithm: Save and mutate successful neural network configurations
Real-time Visualization: See the neural network in action with visual feedback
Interactive Controls: Save the best performing brain or discard current progress
🧠 How It Works
Neural Network Architecture
Input Layer: 5 sensors providing distance readings
Hidden Layer: 6 neurons for processing
Output Layer: 4 neurons controlling car movement (forward, left, right, reverse)
Learning Process
Cars are spawned with random neural network weights
Sensors provide input about the environment
Neural network processes sensor data and controls the car
The car that travels the furthest without crashing is considered the "best"
The best brain can be saved and used as a starting point for mutation
Genetic Algorithm
Save successful neural network configurations
Mutate saved brains to create variations
Gradually improve performance through evolution
🎮 Controls
💾 Save Button: Save the current best-performing neural network
🗑️ Discard Button: Clear saved neural network data
Arrow Keys: Manual control (when using KEYS mode)
🛠️ Technical Implementation
Core Components
Car Class (car.js)

Physics simulation (acceleration, friction, collision)
Sensor integration
Neural network brain integration
Neural Network (network.js)

Multi-layer perceptron implementation
Forward propagation
Mutation algorithms for genetic learning
Sensor System (sensor.js)

Ray casting for obstacle detection
5 sensors with 150-pixel range
90-degree spread pattern
Road & Traffic (road.js)

Road boundary generation
Traffic car spawning and movement
Lane management system
Visualization (visualizer.js)

Real-time neural network visualization
Color-coded neuron activity
Connection weight visualization
🚀 Getting Started
Prerequisites
Modern web browser with JavaScript support
Local web server (for development)
Installation & Setup
Clone or download the repository
Navigate to the project directory
Serve the files using a local web server:
# Using Python 3
python -m http.server 8000

# Using Node.js (http-server)
npx http-server

# Using Live Server extension in VS Code
Right-click on index.html → "Open with Live Server"
Open your browser and navigate to http://localhost:8000
File Structure
neural-network-self-driving-car/
├── index.html          # Main HTML file
├── main.js            # Main application logic
├── car.js             # Car physics and behavior
├── network.js         # Neural network implementation
├── sensor.js          # Sensor system
├── controls.js        # Input handling
├── road.js            # Road and traffic management
├── visualizer.js      # Neural network visualization
├── utils.js           # Utility functions
├── style.css          # Styling
├── car_topview.svg    # Car sprite
└── README.md          # This file
🔧 Customization
Adjust Neural Network Parameters
// In car.js - modify network architecture
this.brain = new NeuralNetwork([
    this.sensor.rayCount, // Input neurons (5)
    6,                    // Hidden layer neurons
    4                     // Output neurons
]);
Modify Car Physics
// In car.js - adjust car behavior
this.acceleration = 0.2;    // Acceleration rate
this.maxSpeed = 3;          // Maximum speed
this.friction = 0.05;       // Friction coefficient
Change Sensor Configuration
// In sensor.js - modify sensor setup
this.rayCount = 5;              // Number of sensors
this.rayLength = 150;           // Sensor range
this.raySpread = Math.PI/2;     // Sensor spread angle
📊 Performance Tips
Training: Let the simulation run for several iterations to find good neural network weights
Mutation Rate: Adjust the mutation rate (0.03 default) for fine-tuning
Population Size: Increase N value in main.js for more cars per generation
Traffic Density: Modify traffic array for different difficulty levels
🤝 Contributing
Contributions are welcome! Here are some ideas for improvements:

Add more sophisticated traffic patterns
Implement different neural network architectures
Add speed/performance metrics
Create different road layouts
Add weather/environmental effects
Implement reinforcement learning algorithms
🎯 Future Enhancements
 Multiple car types with different behaviors
 Highway on/off ramps
 Weather conditions affecting driving
 Multiplayer racing mode
 Performance analytics dashboard
 Mobile touch controls
 Different AI algorithms comparison
Enjoy watching the AI learn to drive! 🚗🤖
