## Overview of project and further improvements
Action recognition takes gesture recognition to the next level. The applications are vast such as medical, fitness, yoga and wellbeing, sports,etc. Action recognition can help us monitor and provide analysis of the actions we perform.

Here i leverage the mediapipe's holistic model to draw landmarks in real time on my entire body. Then i record myself performing 4 basic moves of boxing namely: left jab, right jab, left hook and right hook.
This is not restricted to only boxing, we can extrapolate this and create AI coaches which can check the form of our movements. Obviously this means that the recorded actions used for training must be performed by an expert.
I then save these nump files which has my movements frame by frame in a sequential manner. Lastly i pass this through a layer of Stacked LSTM and Dense network to learn the sequential and time dependencies.

Then through some logic and opencv i predict the models outcome using probabilities. Due to this being a real time project i display the probability of the outcome (in short i display something like a confidence score for each class).

We can improve this further by recording more movements and making the real time more robust by compressing the models into edge devices. We can also create an AI boxing coach which will give us the combination from the sample space and check our form while performing these actions.
