# README #

This README would normally document whatever steps are necessary to get your application up and running.

################
# featureAdder #
################

OVERVIEW

Just click anywhere to start drawing features. Keep in mind that the order that the features are drawn
for each respective image will be maintained for the output phase; e.g., the sixth feature drawn on the
source image (SI) will correlate to the sixth feature drawn on the destination image (DI), even if they 
were not meant to be correlated. That being said, the user can draw any number of times on either image 
without restriction. Five features can be drawn on the SI, followed by three on the DI, followed by two 
on the SI, followed by four on the DI. It is up to the user to keep track of the correct correlation of 
the features.

USAGE

Note the command line usage:
	./featureAdder <source PNG image> <destination PNG image>
				   [--es <source 	   image input file name>] 
				   [--ed <destination  image input file name>]
				   [--os <source 	   image output file name>] 
				   [--od <destination  image output file name>]
				   [--s  <screenshot   image output file name>]

The es/ed flags are for opening and editing feature files.
The os/od flags are for base-naming the output feature files.
The s flag is for base-naming the screenshot files.

Note the program usage:
At any point you may quit the program by pressing the 'q' key.
At any point you may undo your last action by pressing the 'u' key. 
At any point you may produce a screenshot of your current window by pressing the 's' key. ***
At any point you may produce two .feat output files for your features by pressing the 'o' key. ***
At any point you may force-produce two .feat output files for your features by pressing the 'f' key. *** ^

*** Note that you may do this multiple times in one session. Multiple versions will be created.
^   Required when number of features specified on the SI and DI not match.

SUGGESTED NOTES

Because we will probably be adjusting the features of multiple images several times, here are some guidelines
to follow, both in terms of order and number of features. All directions specified are from the perspective of
the viewer, not the image individual.

----------------
|||| Legend ||||
----------------

L       =>   left
R       =>   right
any #   =>   number of features

(1) Eyebrows, 6
	--> L eyebrow, L-R, 3
	--> R eyebrow, R-L, 3
(2) Eyes, 12 features
	--> L eye top, 


##############
# imageMorph #
##############

OVERVIEW

This program generates the intermediate frames between the two images.

The number of frames generated is up to the user.

The steepness of the time progression is also up to the user, there are two modes available for now:
1) a truncated sine curve, which means the changes in the beginning and at the end are gradual, however the change in the center is steep.
2) a linear line, i.e. constant rate of change

NOTE

Right now it only supports PNG files - we will assume this for simplicity, since pre-processing is easy.

USAGE

Note the command line usage:
	./imageMorph <source.feat> <target.feat> <source.png> <target.png> 
				 <intermediaryImagesBaseName> <numFrames> <easingFunction>

The easing function is either linear or sine, indicated by '-l' and '-s' respectively.

### What is this repository for? ###

* Quick summary
* Version
* [Learn Markdown](https://bitbucket.org/tutorials/markdowndemo)

### How do I get set up? ###

* Summary of set up
* Configuration
* Dependencies
* Database configuration
* How to run tests
* Deployment instructions

### Contribution guidelines ###

* Writing tests
* Code review
* Other guidelines

### Who do I talk to? ###

* Repo owner or admin
* Other community or team contact