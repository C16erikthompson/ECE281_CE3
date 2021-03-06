ECE281_CE3
==========

# Moore Waveform and Explanation
![](https://github.com/C16erikthompson/ECE281_CE3/blob/master/MooreWaveform.png?raw=true)

- The floor is initially set to one by the reset
- The floor only goes up when up_down is high, stop is low, and there is a rising edge (the exception being floor4, which stays the same)
- The floor only goes down when both up_down and stop are low and there is a rising edge (the exception being floor1, which stays the same)
- Stop remains high for two clock cycles, becomes low, then becomes high again
- After stop is high when the state is floor4, both up_down and stop are made low and the system returns to floor1, decreasing by one floor with each rising edge


# Mealy Waveform and Explanation
![](https://github.com/C16erikthompson/ECE281_CE3/blob/master/MealyWaveform.png?raw=true)
(zoom in on the picture to see it better)
- The floor is initially set to zero by the reset
- The floor only goes up when up_down is high, stop is low, and there is a rising edge (the exception being floor4, which stays the same)
- The floor only goes down when both up_down and stop are low and there is a rising edge (the exception being floor1, which stays the same)
- Stop remains high for two clock cycles, becomes low, then becomes high again
- After stop is high when the state is floor4, both up_down and stop are made low and the system returns to floor1, decreasing by one floor with each rising edge
- The value for next floor is consistent with the floor that occurs next and changes values in tandem with the change in floor output (mimics the arrows on the state machine design)
- Output floor remains the same as Moore output floor

# Questions and Answers
1. What is the clock frequency? What value would we set to simulate a 50Mhz clock?
  - 100 Mhz / 20ns
2. Is reset synchronous or asynchronous?
  - synchronous
3. Will it be different from your Moore Machine?
  - No, how the output is obtained will change though

