# ECE 440: Introduction to Online and Reinforcement Learning

## Project 2: Inverse Reinforcemnt Learning for Eigenspectrum Optimiziation

#### By Nicolas Kozachuk



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
