## AI-for-Dating

![alt_text](https://eyeondesign.aiga.org/wp-content/uploads/2017/03/Tinder-its-a-match-typography-aiga.png)


In 2017, when a journalist asked the co-founder of Tinder how he imagined his dating app in five years’ time, Sean Rad pulled out his smartphone and pretended to have a conversation with the device.

“The Tinder voice might pop up and say, ‘There’s someone down the street that we think you’re going to be attracted to, and she’s also attracted to you, and guess what, she’s free tomorrow night! And we know you both like this indie band, and it’s playing, so would you like us to buy your tickets?’”

And now in 2019 — a little more than 2 years later, the prospect of algorithms finding your perfect match by compiling enormous amounts of data — from age, gender, location, and sexual preferences, to online purchasing history and even Spotify playlists — has become very real.

And Artificial intelligence (AI) is progressively redefining love and making it brutally effective in ways more than one. To build a relationship between human beings using technology, was never as easy as it has become. So, lets take advantage of AI methodologies that is at our disposal. But first, we need to come up with a pipeline based on which these methodologies can be deployed one after the other.

## The PipeLine

![alt_text](https://github.com/soumyadip1995/AI-for-Dating/blob/master/figs/Screenshot%20(162).png?raw=true)

## Description


- For any kind of data analysis , first we need to collect data. Data from dating apps will be particularly helpful. We need to be Looking for image information on which we can perform image processing, swipe information, Bio information . Fortunately, we have resources.

- Finding an optimal match is crucial to find a suitable partner. If it is not right, it is not right..!!. Dating apps that are currently using AI, use information such as bio description, pictures etc very precisely to provide the user with the best possible result/match.

- The next step to building a relationship is communication. We need to have meaningful conversations in order to develop an emotional connection with the selected person. AI can help us here as well. Humans need less time swiping and more time interacting.

- And finally, the one ingredient without which a proper relationship will be unsustainable is intimacy. Without intimacy, all the above points will fall flat and we will be needing to start from square one.

- Now, granted that all the above points in the pipeline vary immensely from user to user, it is also important to realise the fact that this is the exact situation where AI can be helpful.

## Installations

To install everything, follow these instructions:

You must have the correct packages installed. To install the packages run the following command on the commandline:

 pip install -r requirements.txt

Once you have the requirements installed, you'll need to get your FB authentication token & ID and store it in the auth.json file. I have a script in here to extract the token called helpers.py so run that script.

If you're running into issues. Read this to get your ID. Read this to get your Token. If you really have trouble, you can message me.

If you want to use the model trained on the female preferences, you can now just run bot.py.

If you want to train your own model, there are additional steps you'll need to follow:

- Use img_scrape.py to access Tinder through your terminal. When running the program, press 1 to dislike or 2 to like. Do this for thousands of images.

- Once you have your dataset, run prepare_data.ipynb to extract the faces from the images. Save as a numpy file. Aim for 3000 use-able images for decent performance.

- I wouldn't recommend training the CNN on your PC. You'll need to start a deep learning server using AWS or Google Cloud. On AWS, I used the Deep Learning AMI t2.medium.

- Once you're done training, you need to export your model as an h5 file. Transport this h5 file into the bot. Within bot.py, find the load_model() function and plug the name of your file into that functino.

- Voila, you should be good to go!
