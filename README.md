# Envirowear-CPS
A Cyber Physical System "Envirowear": Temperature control wear

Synopsis:
Greenhouse Climate Control system facilitates the growth of plants in a controlled environment. The system monitors internal conditions like soil humidity, light, temperature and humidity, and CO2 concentration in a greenhouse and alters these parameters to provide an optimal environment for plant growth.

Description:
Plant growth is dependent on many parameters like soil humidity, light, temperature and humidity, and CO2. Its growth can be optimized by providing an optimal environment. The Greenhouse Climate Control system monitors and collects data on each parameter using various sensors. The collected data is then analyzed in real-time and the greenhouse's environmental condition is altered accordingly using actuators.

The system is a CPS because
1.	Reactive: The system continuously interacts with the environments by taking inputs via sensors and altering the climate conditions in real time.
2.	Concurrent: The system collects the sensor's data for all parameters that are processed concurrently, and multiple components alter the greenhouse climatic conditions in parallel.
3.	Feedback control: The system interacts with the internal greenhouse environment via sensors and changes the climatic conditions via actuators. There is a continuous feedback loop of changing environmental conditions based on data received from sensors.
4.	Real Time computation: The collected data from sensors is analyzed in real-time and the environmental conditions of greenhouse is altered accordingly in real time.

Programming languages and software frameworks:
Python/Java.


Tests/Experiments:
We will be using a real time data available at IEEE website (ROSESGREENHDB).
We will use this data to simulate the input parameters for The Greenhouse Climate Control system. Each row in the data set provides soil humidity, light, temperature and humidity, and CO2 for each round of computation.

Risks:
1.	The team members must have basic domain knowledge about Greenhouse agriculture, effects of climate parameters on plant growth.
2.	The team members must be proficient in Python/Java.
