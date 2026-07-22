# MDP REPRESENTATION
### NAME : LEKASRI G
### REGISTER NUMBER : 212223100025
## AIM:
To model the Weather Prediction problem using a Markov Decision Process (MDP).

## PROBLEM STATEMENT:

### Problem Description
A person observes the weather every day. The weather can be Sunny, Cloudy, or Rainy. Based on the current weather, the person decides whether to Carry an Umbrella or Don't Carry an Umbrella. The agent receives a reward based on whether the decision is appropriate for the weather conditions.

### State Space
States represent the current weather condition.

0 = Sunny
1 = Cloudy
2 = Rainy
### Sample State
1 → Cloudy

The current weather is Cloudy.

### Action Space
0 → Carry Umbrella
1 → Don't Carry Umbrella

### Sample Action
Carry Umbrella – The person carries an umbrella.
Don't Carry Umbrella – The person does not carry an umbrella.

### Reward Function
Carry Umbrella

Sunny → +5

Cloudy → +3

Rainy → +5

Don't Carry Umbrella

Sunny → −5

Cloudy → −3

Rainy → −10

The weather changes according to the transition probabilities shown in the MDP diagram, and rewards are assigned based on the action taken.

### Graphical Representation:
<img width="1578" height="996" alt="image" src="https://github.com/user-attachments/assets/f5581cba-cb97-4d08-a621-a4740599dbd6" />

## PYTHON REPRESENTATION:
```
<img width="862" height="148" alt="Screenshot 2026-07-22 095001" src="https://github.com/user-attachments/assets/b15fdfb0-948c-4129-9319-d8f85ce2fdd0" />
# Weather Prediction MDP
# Actions:
# 0 -> Carry Umbrella
# 1 -> Don't Carry Umbrella

P ={
    
0: {
    0: [(0.6, 0, 5, False),        #0-SUNNY
        (0.3, 1, 2, False)],
    1: [(0.6, 0, -5, False),
        (0.3, 1, -2, False)]
},

1: {
    0: [(0.1, 0, -5, False),      #1-CLOUDY
        (0.5, 1, 3, False),
        (0.3, 2, 1, False)],
    1: [(0.1, 0, 2, False),
        (0.5, 1, -3, False),
        (0.3, 2, -10, False)]
},

2: {
    0: [(0.2, 1, -3, False),      #2-RAINY
        (0.6, 2, 5, True)],
    1: [(0.2, 1, -5, False),
        (0.6, 2, -10, True)]
}
}
print(P)
```
## OUTPUT:
<img width="862" height="148" alt="Screenshot 2026-07-22 095001" src="https://github.com/user-attachments/assets/c0f3a197-166f-4317-b052-1d730cd924e3" />

## RESULT:
Thus, the Weather Prediction problem is successfully represented in Markov Decision Process (MDP) form.

