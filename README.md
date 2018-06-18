# AI-pong
AI pong game in JS
Pong made in JS and HTML.
Adapted to run AI training and prediction with Tensorflow
Tensorflow Sequential model.
 
Elements as input features = Player paddle x, computer paddle x, ball x, ball y, previous ball x, previous ball y, previous player paddle x, previous computer paddle x

You can decide whether to empty the training data and reset and start clean.

//hm games til train?
    if(this.turn > 3){ 
    // 
^ this is where you can change how many games to take data from before the training starts. I'd say 15+, if you want to see some real learning. 
