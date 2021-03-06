---
layout: post
title: "Chronicles of a beginner Machine Learner attempting GAN - Part 1"
date: 2017-12-16
---


Putting this out there for all other beginners so we can all learn together (that's what GANs' all about eh!). Legit machine learners out there, please feel free to correct me!!

---

This is 2017, the second week of December, and Christmas is in the air - literally, for it was the Christmas decor hanging in the air that made me go:

"HEY! Why don't I create a __CHRISTMAS CARD GENERATOR__? Then we'll have endless Christmas cards forever more!!!"

![Xmas_Card](https://user-images.githubusercontent.com/21985915/34067873-62a03d1e-e26c-11e7-997b-58148cc59224.png)
*Credits: http://howtochristmas.co.uk/wp-content/uploads/2014/10/cards-hanging-display_20883838.jpg*

Crazily enough (haha) there was support from the groun (read: prof and fellow classmates), and it is from them I first discovered the magical world of __GANs - Generative Adversarial Networks__.


And so it begins...


---


### Step 1 - What are GANs?!


Imagine two machines: machine one is trying to create fake money and bluff machine two into thinking it is real money. 


The catch? At the beginning, neither knows what is real and what is fake! Only I know the real answer (muahaha).


1) Machine one creates a fake 5 dollar note, and I take a real 5 dollar note out of my wallet.
2) We randomly give one of the 5 dollar notes to machine two.
3) Machine two evaluates the 5 dollar note given to him and decides whether it is real or fake.
4) I reveal the true answer!
5) Rinse and repeat.


Over time, machine one learns to make fake notes that look more real, and machine two learns what is not real.


![GAN](https://user-images.githubusercontent.com/21985915/34067884-a6ad54ec-e26c-11e7-960b-dac5415ff0ac.png)
*Credits: https://www.kdnuggets.com/2017/01/generative-adversarial-networks-hot-topic-machine-learning.html*


Let's take a minute here to applause Ian Goodfellow for introducing this incredible system to the world in 2014! *claps*


The above is a very simplistic explanation - many others have put out more detailed ones, take a read around! And yes, I did start with just this very basic understanding... *gulps*.


---


### Step 2 - Getting the images


Alright I'm pretty excited to jump right in - LET'S GET INTO THE IMAGES!!
Wait a minute - as I'm scrolling through potential images, I realise...


__Obstacle 1 : My images have WORDS.__

__Takeaway 1 : Keep it simple. Do pure images OR pure words. Mix = gonna take a looong time...__


A lot of Christmas cards have words. Like, I mean, who doesn't write 'Merry Christmas' on the front of a card?! It's a GREETING card for heaven's sake.


Me: It'll be fine, the machine will be smart enough to like, recognise 'Merry' as one whole object and like, the snowman as another whole object right?
Rest of the world: ...No? <sup>[1](#footnote1)</sup>


Ok I mean, technically it's possible (everything's possible with AI!!!) but it's going to be reallyyy painful.


Abandon plan.


PLAN B: I'm going to generate STOCK IMAGES! Like, who wouldn't want endless free stock images for their websites and everything?! Ok but to generate REAL images... that's tough. Like, REALLY tough. Maybe I should try this after I actually know what's going on with GANs.


Abandon plan.


NEW PLAN: I'm going to generate LOGOS! Like, brand logos. Stop paying millions of dollars for a logo guys!! Also, logos have no words. Right? ...Right?


I convince myself that even if they appear, distorted words in logos are like, cool. So it wouldn't matter. I pray hard that this will not come back to haunt me later.


*Disclaimer - what seemed like split second decisions above, I spent days and nights brainstorming and agonizing over!!!*


__Obstacle 2 : How many images do I actually need??__

__Takeaway 2 : Ballpark upwards of 50,000, minimum ~6,000 (take this with a BOWL of salt, I am no expert!!!)__


I heavily referenced this question in Quora (lifesaver):
[https://www.quora.com/How-many-images-required-for-Generative-Adversarial-Nets-GANs](https://www.quora.com/How-many-images-required-for-Generative-Adversarial-Nets-GANs)


Also saw some projects that managed to generate some good stuff with 10,000 images!


[https://github.com/AlexiaJM/Deep-learning-with-cats](https://github.com/AlexiaJM/Deep-learning-with-cats)

Ok this is ~143,000 images but gave us Anime!!! How incredible is this?

[https://github.com/jayleicn/animeGAN]
(https://github.com/jayleicn/animeGAN)


If you use only 900 images (see the below pokemon set), you get rough shapes but without details. With more training epoches (rounds), only the shapes and colors look better.

[https://lilianweng.github.io/lil-log/2017/08/20/from-GAN-to-WGAN.html]
(https://lilianweng.github.io/lil-log/2017/08/20/from-GAN-to-WGAN.html)

Note: The number I am referring to are UNIQUE images - you may subsequently come across methods that allow for image augmentation (flip, distort, tilt, etc) which can easily increase your number of images by five-fold or more.


---


To be continued...



__Footnotes:__
<a name="footnote1">1</a>: Apparently, machines recognise things by their edges - I'm guessing it can begin to recognise each letter separately, and in time to come, recognise 'Merry' usually appears as one whole chunk instead of bits and pieces... but that's going to take a loooong time.

