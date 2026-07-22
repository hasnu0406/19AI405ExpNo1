<h1>ExpNo 1 :Developing AI Agent with PEAS Description</h1>
<h3>Name: HASNA MUBARAK AZEEM</h3>
<h3>Register Number/Staff Id: 212223240052</h3>


<h3>AIM:</h3>
<br>
<p>To find the PEAS description for the given AI problem and develop an AI agent.</p>
<br>
<h3>Theory</h3>
<h3>Medicine prescribing agent:</h3>
<p>Such this agent prescribes medicine for fever (greater than 98.5 degrees) which we consider here as unhealthy, by the user temperature input, and another environment is rooms in the hospital (two rooms). This agent has to consider two factors one is room location and an unhealthy patient in a random room, the agent has to move from one room to another to check and treat the unhealthy person. The performance of the agent is calculated by incrementing performance and each time after treating in one room again it has to check another room so that the movement causes the agent to reduce its performance. Hence, agents prescribe medicine to unhealthy.</p>
<hr>
<h3>PEAS DESCRIPTION:</h3>
<table>
  <tr>
    <td><strong>Agent Type</strong></td>
    <td><strong>Performance</strong></td>
     <td><strong>Environment</strong></td>
    <td><strong>Actuators</strong></td>
    <td><strong>Sensors</strong></td>
  </tr>
    <tr>
    <td><strong>Medicine prescribing agent</strong></td>
    <td><strong>Treating unhealthy, agent movement</strong></td>
     <td><strong>Rooms, Patient</strong></td>
    <td><strong>Medicine, Treatment</strong></td>
    <td><strong>Location, Temperature of patient</strong></td>
  </tr>
</table>
<hr>
<H3>DESIGN STEPS</H3>
<h3>STEP 1:Identifying the input:</h3>
<p>Temperature from patients, Location.</p>
<h3>STEP 2:Identifying the output:</h3>
<p>Prescribe medicine if the patient in a random has a fever.</p>
<h3>STEP 3:Developing the PEAS description:</h3>
<p>PEAS description is developed by the performance, environment, actuators, and sensors in an agent.</p>
<h3>STEP 4:Implementing the AI agent:</h3>
<p>Treat unhealthy patients in each room. And check for the unhealthy patients in random room</p>
<h3>STEP 5:</h3>
<p>Measure the performance parameters: For each treatment performance incremented, for each movement performance decremented</p>

## PROGRAM:
```Python
import random
class MedicinePrescribingAgent:
    def __init__(self):
        self.location = "A"
        self.temperature = {
            "A": round(random.uniform(97.0, 102.0), 1),
            "B": round(random.uniform(97.0, 102.0), 1)
        }
        self.performance = 0
    def move_left(self):
        if self.location == "B":
            self.location = "A"
    def move_right(self):
        if self.location == "A":
            self.location = "B"
    def prescribe_medicine(self):
        if self.temperature[self.location] > 98.5:
            print(f"Patient in Room {self.location} has fever ({self.temperature[self.location]}°F).")
            print("Medicine Prescribed.")
            self.temperature[self.location] = 98.5
             self.move_left()
            self.performance -= 1
        elif action == "right":
            self.move_right()
            self.performance -= 1
        elif action == "prescribe":
            self.prescribe_medicine()
        elif action == "nothing":
            pass
        else:
            print("Invalid action")
    def print_status(self):
        print("----------------------------------------")
        print(f"Current Room      : {self.location}")
        print(f"Room Temperatures : {self.temperature}")
        print(f"Performance       : {self.performance}")
        print("----------------------------------------")
agent = MedicinePrescribingAgent()
agent.print_status()
agent.perform_action("prescribe")
agent.print_status()
agent.perform_action("right")
agent.print_status()
agent.perform_action("prescribe")
agent.print_status()
agent.perform_action("left")
agent.print_status()
agent.perform_action("nothing")
agent.print_status()           self.performance += 10
        else:
            print(f"Patient in Room {self.location} is healthy ({self.temperature[self.location]}°F).")
            print("No medicine required.")
    def perform_action(self, action):
        if action == "left":

```

## OUTPUT:

<img width="386" height="349" alt="image" src="https://github.com/user-attachments/assets/3a5ab0de-20b7-4431-924a-aa0ac4d0f476" />
