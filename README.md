# Open AI Lunar Lander - Reinforcement Learning Algorithm vs Supervised Machine Learning Algorithm

## Introduction
In the OpenAI Gym game Lunar Lander
(https://gym.openai.com/envs/LunarLander-v2/) the player's job is to control a
small spaceship to land if safely on a landing pad. There are three thrusters which
can be used for control. These work in three directions: up, left, and right. The
player can also choose to do nothing. A dataset has been collected from an expert
player of LunarLander that contains screenshots of the state of the game and the
player's associated action (none, up, left, and right). A dataset describing the
same scenario using high-level derived features representing the state of the
Lunar Lander world has also been collected through the same process.


Following tasks were preformed:
<ul>
  <li><b>Part 1.</b> A supervised machine learning model was trained to control the Lunar Lander
craft based on the extracted high-level state representations.<br>
    <ul>
  <li>This dataset is contained in the file LunarLanderStateVectors.csv</li>
  <li>The features in this dataset are as follows:</li>
      <ul>
        <li>step: The step in the game that the player was on</li>
        <li>pos_x: The x position of the centre of the spaceship - the
middle of the landing pad is always at (0, 0)</li>
        <li>pos_y: The y position of the centre of the spaceship - the
middle of the landing pad is always at (0, 0)</li>
        <li>vel_x: The velocity of the spaceship in the x direction</li>
        <li>vel_y: The velocity of the spaceship in the y direction</li>
        <li>ship_lander_angle: The angle between the centre of the
spaceship and the centre of the landing pad</li>
        <li>ship_lander_angular_vel: The spaceship's angular velocity
with respect to the landing pad</li>
        <li>leg_1_ground_contact: A binary flag indicating if the left
leg of the spaceship is in contact with the ground</li>
        <li>leg_2_ground_contact: A binary flag indicating if the left
leg of the spaceship is in contact with the ground</li>
        <li>action: The action that the expert player took in this
scenario</li>
      </ul>  
  <li>A few classifier types were used while selecting sensible hyper-parameters</li>
  <li>Evaluation experiment was preformed in order to determine how effective the model trained is</li>
</ul>  
 </li>
  <li><b>Part 2.</b>Supervised machine learning model was trained in order to control the Lunar Lander
craft based on the image dataset.
  <ul>
  <li>Each image shows the state of the world and the image filename
indicates the action that the expert player took in that scenario</li>
  <li>Images were converted to greyscale and shrinked</li>
  <li>A couple of model architectures were tested while selecting sensible hyper-
parameters</li>
  <li>Evaluation experiment was perfomed to determine how effective the model trained is</li>
</ul>
  </li>
  <li><b>Part 3.</b> DeepQLearning reinforcement learning algorithm was used to train an
agent to play the Lunar Lander. Sensible hyper-parameters were used. Evaluation experiment was perfomed to determine how effective the model trained is.
</ul>  



4. Deploy each of the three models trained to the Lunar Lander Game play
200 episodes and analyse the reward achieved by the models trained
using each approach
• The lunar_lander_ml_images_player.py,
lunar_lander_ml_state_player.py and
lunar_lander_rl_player.py python scripts contain the code to load
a saved model and run iterations of the game using that model.
• Write a short document (no more that 350 words) in a Jupyter
notebook to describe the results of the experiments
• Reflect on the performance of each model
• Reflect on the amount of computation required to train each model
