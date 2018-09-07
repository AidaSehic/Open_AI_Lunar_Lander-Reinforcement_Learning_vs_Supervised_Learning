# Open AI Lunar Lander - Reinforcement Learning Algorithm vs Supervised Machine Learning Algorithm
### Aida Sehic & Mashal Ahmad 

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


Each of the three models were deployed and the reward achieved by the models trained
using each approach was analysed.
Following Python scriptis contain the code to load a saved model and run iterations of the game using that model.:
<ul>
  <li>lunar_lander_ml_images_player.py,</li>
  <li>lunar_lander_ml_state_player.py and</li>
  <li>lunar_lander_rl_player.py</li>
</ul>  


## Description and the results of the experiments              

[Project Folder](https://drive.google.com/open?id=1u3N_UYeUP63MqTQngrooQRNxoR7Bgl41) has follwoing files
* part1.ipynb    implementation of part 1
* part1.html     html file for part1
* part2A.ipynb    implementation of part 2 (uses: Model1 described below)
* part2A.html     html file for part 2
* part2B.ipynb    implementation of part 2 (uses: Model1_distr described below)
* part2B.html     html file for part 2
* part2C.ipynb    implementation of part 2 (uses: Model1Distr10Folds described below)
* part2C.html     html file for part 2
* part3.py       implementation of part 3
* part3.html     html of part 3
* Models_rewards   Folder for rewards and Models    
[Link ](https://drive.google.com/open?id=1g5DRsV6jO06ixJgHqs0J5pyL4UN4IXdH)
* part2notebooks-7architectures   Folder with implementation of 7 different model architectures for part 2 described below (for the assessment we are submitting only three notebooks: part2A and part2B and/or part2C)
[Link ](https://drive.google.com/open?id=1XjUtehiXCmhi9nnD__vel6K3pxSGJP1Q)
