# Imitation Learning for Distributed Eigenspectrum Optimization

This project explores the use of **Imitation Learning** to optimize the eigenspectrum of graph networks for mitigating resonance risk caused by adversarial attacks. The approach employs preference comparison algorithms to simulate eigenspectrum optimization in a decentralized setting, using Proximal Policy Optimization (PPO) to learn a policy for edge weight manipulation.

## Project Description

Graph eigenspectrum optimization is critical in dynamic networks for reducing resonance risks that external agents may exploit. This project addresses the challenges of implementing optimization in decentralized systems where full network information is unavailable. The method involves:
- Using imitation learning with preference-based queries to approximate centralized eigenspectrum optimization.
- Implementing a custom environment and defining Markov Decision Processes for learning.
- Utilizing **Proximal Policy Optimization (PPO)** for robust policy learning.

The trained model achieves significant optimization while reducing computational costs compared to traditional gradient descent methods.

## Code Details

The implementation, provided in a Jupyter Notebook, includes:
1. **Environment Setup**:
   - Defines the observation and action spaces based on graph properties.
   - Enforces constraints such as constant edge weight sums.
2. **Algorithm Implementation**:
   - Utilizes PPO with custom reward and preference comparison mechanisms.
   - Parameters include trajectory sampling and hyperparameter tuning.
3. **Training and Evaluation**:
   - Optimizes the eigenspectrum and evaluates the model’s performance against benchmarks.

## Results

- **Initial Objective Value**: **213.23**
- **Optimized Objective Value (Imitation Learning)**: **76.01**
- **Optimized Objective Value (Centralized Gradient Descent)**: **71.04**
- **Percent Difference**: The imitation learning approach achieves an optimized value within **6.99%** of the centralized gradient descent method, while significantly reducing computational time from 2 hours to just 5 minutes.

## Key Features

- **Customizable Environment**: Defines the constraints and properties of graph-based systems.
- **Preference-Based Learning**: Uses imitation learning to reduce resonance risk in decentralized settings.
- **Efficiency**: The method significantly decreases computational time compared to traditional approaches.

## Future Work

- Extend the model to accommodate multi-agent systems for fully decentralized solutions.
- Build custom wrappers to evaluate performance across various graph configurations.
- Explore alternative libraries for enhanced flexibility in imitation learning.

## References

Key references include seminal works on imitation learning, preference-based optimization, and PPO algorithms. A complete reference list is provided in the accompanying report.

---

For a detailed explanation, refer to the full report and codebase.


### How to run code
1. Open the Python notebook in desired enviroment - Google Colab is Recommended
    * Note that code was written in Google Colab, so reading/writing files may have to be modified in other enviroments
2. Upload the Graphs_and_Env.zip zip file containing custom OpenAI Gym enviroment and initial graph
    * If using Google Collab(what I used to code), simpy upload zip file to Google Collab file directory
    * If running locally, add zip file to local directory where code is located
3. Run first code section to unzip file and make such the file was properly extracted
4. Run the second section to install the necessary packages, then the third section containing the imports used, and then the fourth section containing functions to be used
5. Run the fifth section of code to ensure that the custom environment is successful registered with gym
6. Run the sixth code section to build and train preference comparison algorithm
    * While the code runs, the training parameters and results will be displayed
7. Run the seventh code section to plot the training results(Takes about 5 minutes)
8. Run the eighth code section to build the same enviroment, but that outputs rewards and laplacian matrix
    *  This is different than the other enviroment so that results arent outputted when training
9. Lastly, run the  ninth code section to plot graphs and the eigenvalue spectrums for the initial graph and the preference comparison optimized graph, as well as output objective values 
10. If one alters the custom enviroment or wants to save the results, one can run the last code section to zip the initally unzipped folder in order to download it
