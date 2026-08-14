# Neuromorphic AI Systems

- AI that resemble biological brain systems.

## Plan
- Create a blind robot (or outsource it) with 360° LiDAR sensing, motor feedback, battery state monitoring, etc in CAD. Can also implement ultrasound scanning for the terrain.
- Now, build 2 or more models. Such as:

### Neocortex Neural Net
- 100M Parameters. Does Predictive Generation because it generates output slowly based on some previous sensor feeds (LiDAR, velocity, orientation, motor load, etc).
- Predictive Generation may be wrong and AI might stumble in between or face error.
- Only makes progress towards the destination. Gives Predictive Generation to Cerebellum.

### Cerebellum Neural Engine 
- This is pure Maths + Neural Network.
- Around 1M Parameters Neural Network, which only controls motors, and maintains balance.
- Provides free, mooth motion rather than rigid control.
- Maths Engine calculates delta values (error between prediction and reality), and also builds a point map using LiDAR for the Cerebellum to process and generate a path.
- It can also build a terrain map using the ultrasound sensor.

### Limbic Neural Net
- 100K Paramter Model. Only for emergency. Runs at high frequency (100Hz loops)
- Quick reaction. Doesn't care about the end destination. Only for immediate damage prevention and mitigation.
- Takes Real Time Input and acts.

### Hippocampus Engine
- Abstracts the long context (long number of frames and data) into a small set of data, which can be useful for creating a general idea or alertness in Neocortex or Limbic System.

## Principles
- Vision Processing using Cameras and large VLA-models is computation heavy and limits real-time action
- Small specialised models require less compute and perform better than Large Generalised Models.
- No need to learn complex maths algorithms (AI learns itself like a toddler).
- Can be easily trained for cheap using software like MuJoCo.

## Scope
- Find new structure or use case, becuase this is explored by many institutes.

## Use Cases
- Search and Rescue Operations
- Naval Ship Disaster Management
- Autonomous Cars
- Humanoid robots in future
- Extra-terrestrial exploration (rovers, etc)

## References
- [NeuroVLA (Alpha Brain)](https://github.com/guoweiyu/NeuroVLA)
- [MIT Cheetah 3: Design and Control of a Robust, Dynamic Quadruped Robot](https://doi.org/10.1109/IROS.2018.8593885)