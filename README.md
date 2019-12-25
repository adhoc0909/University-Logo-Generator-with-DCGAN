# Generating University Logos with DCGAN

## Why did I do this project?
 
 Abstract things such as Universities, companies, cities require logos to represent their identity. Creating such logos requires a lot of design effort. I started out thinking that it would be good for designers to refer to the logos that were created from this project.
 
## Existing Research
 
https://www.researchgate.net/publication/328494719_LoGAN_Generating_Logos_with_a_Generative_Adversarial_Neural_Network_Conditioned_on_color
 
 In this paper, the model uses ACGAN(Auxiliary Classifier GAN) to generate a logo according to 12 color labels. But logos created by this model lack identity, considering where the logo will be used. Thus, in my project, I made identity, specifying the title of "University logo."
 
## Data Preparation

https://en.wikipedia.org/w/index.php?title=Category:University_and_college_logos&fileuntil=Catholic+university+college+of+Ghana+logo.png#mw-category-media

I collected 1376 logo data from wikipedia with crawling. The Source Code is uploaded.

## Model

I used DCGAN network which is stable to be learned.

## augumentation

First result was very disappointed because unrecognizable images had been created. There were no significant differences when I changed Batch size and Learning rate. So I thought a lack of data was a problem. I augmented the data by turning the images upside down and turning left and right. Then I found the following result was improved.

## Problems To Improve

Mode collapsing would have occurred because the dataset contained a circular logo and a non-circular logo.

Discriminator's loss value was very low whereas Generator's loss value is relatively high.

Generated results are not a good image for designers to refer to(This Is Big Problem).

# Project Significance

This was my first time to learn a model. So It was very good chance to learn Pytorch Library and by implementing the network that I have learned only from theory, I could understand even more deeply.
