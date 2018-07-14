# AI-pong
AI pong game in JS
Pong made in JS and HTML.
Adapted to run AI training and prediction with Tensorflow

- Using TensorFlow js library - Sequential model
Taking in the following inputs as features:
Player paddle x
Computer paddle x
Ball x
Ball y
previous ball x
previous ball y
previous player paddle x
previous computer paddle x

Rendering of pong. - comments included for where the custom code is. 

Then defining the parameters for the "computer" to update the paddle position.

After that i made a function to control the AI's paddle - eventually the model outputs 3 things whether to move left, stay or move right which translates to [1,0,0], [0,1,0], [0,0,1] then finding the argmax and passing that as a -1, 0 or a 1 so the function moves at a multiple of 4 of that many pixels. 

"function AI()" - in order to train the AI i needed to be able to collect that data so i stored it to variables then saved them to an array, every frame.

So as the "computer" just follows the ball i had to decide when to switch to AI since it's the one i want to train.

"if(this.turn > 1)" - Here is where i set how many games you want to play to get data from, i'd suggest more than 20 to see some improvement- the more the better.

Finally i made a function for training and predictions based on the data it collects.

To improve on this i realise that users would not want to actually play a few hundred, or thousand, pong games before they get to play with an AI. Instead, what i'm thinking of doing is collecting a bunch of data in javascript and outputting it to JSON for a base AI model.

From there, i could load in this data to python, train it in TensorFlow with Python, and then export that model back out to the format TensorFlow.js wants, then load it into the javascript Pong game. Quite a few steps.


![GitHub Logo](https://github.com/Amrit-PennySoft/AI-pong/blob/master/AIpong.jpg)
