# Envirowear-CPS
A Cyber-Physical System "Envirowear": Temperature control wear

Synopsis 

Exposure to very cold and hot temperatures could be dangerous to health. Inconveniences such as heat stroke, heat rash, frostbite, hypothermia could occur. Some of these conditions, if left unchecked, may lead to unfortunate deaths. What if all the above problems can be avoided by regulating the temperature of your wear?
We propose one such system “Envirowear” which allows the user to control and monitor the body temperature depending on the environmental conditions. There are 6 
temperature sensors (2 legs, 2 shoulders,1 chest, and 1 back) which provide continuous measures of temperature in various parts of the body. Each temperature input 
is compared with the desired temperature set by the user. If they vary, the controller will set the actuators to heat or cool the body, until the desired 
temperature of the user is not obtained. Ultimately, our goal to achieve a bodysuit that is easy to wear, comfortable, and provides simple and adequate controls 
that allow for any user to utilize it to their needs. The wear’s functionalities can be used to prevent the unfortunate condition that is caused by heatstroke, 
hypothermia, and other thermally-induced maladies.

CPS Description

The system satisfies four characteristics of CPS:
Reactive Computation: The system performs reactive computation by constantly responding to its environment and adjusting itself based on the readings it receives.
The adjustments are based on the desired temperature inputs from the user. Several sequences of inputs and outputs can be described with this system.   
Concurrency: Computations are executed concurrently as each controller is monitoring and adjusting itself independently from other controllers.  Different desired 
temperature inputs can be set for each body section. As such, each controller will be focusing on its respective body section. 
Feedback Control of the Physical World: The culmination of the features above facilitates an accurate simulation of a feedback loop with the physical world. Sensor 
readings are analyzed at a constant rate within each controller. Each controller is independently reacting to the readings according to their temperature settings. 

Real-Time Computation: The use of sensors allows this system to function in real-time. They detect the shifts in temperature and tell the controllers to adjust the 
climate back to the desired settings. If any dangerous temperatures are detected, the real-time capability of the system provides the means to ensure the user is 
kept safe by immediately reverting to the system defaults.  

Technical Details

Standard set-up for this project would include an IDE compatible with Java 8+ (Eclipse). Tests would be developed and executed using popular testing frameworks 
compatible with Java such as JUnit. Astah will be used for UML and state diagrams. Draw.io will be used to draw SRC diagrams.

Tests/Experiments:
A set of tests that could be designed for this system are split into two categories:
1.	User-provided Inputs a.
  a)	Positive Tests:
      i.	Valid temperatures (i.e. integer values) accepted 
      ii.	The system allows all components to receive an input from the user  
  b)	Negative Tests:
      i.	Invalid inputs for temperatures (e.g. non-numerical values) are rejected 
      ii.	Unsafe temperatures (e.g. will not allow users to go too low or high)
      iii.	Not providing any inputs for desired temperatures will tell the system to use a default setting

2.	Individual Component Inputs 
  a)	Positive Tests 
      i.	Stores input from users and sensors to perform computations ii.	Correct calculations being performed to determine differential between sensor readings and 
          desired temperatures iii.	Correct outputs being generated in response to the differential 
          1.	 Computations indicate positive differential: cool down the wearer 
          2.	Computations indicate negative differential: heat the wearer iv.	Correct states are observed in response to input 
  b)	Negative Tests 
      i.	Components will not crash or fault in the chance a sensor fails (i.e. sensor sends “faulty” input in the form of null temperatures or non-numerical data) 
      ii.	Emergency scenarios (i.e. temperature readings outside of normal bounds) will trigger the appropriate recovery method.

Risk Evaluation

•	Hardware Risks
•	Physical sensors being unable to account for differences between external temperatures and temperatures inside of the clothing.
•	Physical sensor quality being ineffective for the needs of the project (i.e. not proving input quick enough or accurately enough) 
•	Controllers sending their adjustment inputs to other controllers (i.e. causing incorrect adjustments to temperature) 

•	Safety Risks 
•	Circuitry frying, causing the system to fail and no longer make adjustments 
•	Wearer being injured if electronics in the clothing experience a catastrophic failure 
