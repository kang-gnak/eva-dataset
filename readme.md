Explainable Visual Aesthetics(EVA) Dataset

This Explainable Visual Aesthetics(EVA) Dataset contains 5 csv files and the resized images from AVA dataset that were shown in our experiment.


**If you want to use EVA dataset, please cite our paper "EVA: An Explainable Visual Aesthetics Dataset" by Chen Kang, Giuseppe Valenzise, Frédéric Dufaux in [Joint Workshop on Aesthetic and Technical Quality Assessment of Multimedia and Media Analytics for Societal Trends (ATQAM/MAST'20)](https://atqam-workshop.net/).**

The method, filter method and basic summary can be found in the paper. All of the processings we did are in python 3.6 and MATLAB.

#images folder#

This folder contains all the resized images we selected from AVA dataset.

You can use our classification of image category in image_content_category.csv or use your own classification. Notice the images are 600-700MB.

#data folder#

##image_content_category.csv##

The first column is the image id, which is their names in AVA dataset.

The second column is the content 6 categories. Each image only belongs to one category. The classification method is described in the paper.

##users.csv##

The delimiter is "=".

id: user's id

age: user's birth year

region: user's region. The region list is in "region_index.csv"

photographic_level_id: '1':'Beginner','2':'Amateur','0':'none','3':'Professional'

gender_id: '1':'male','2':'female'

eyecheck: '1':'glasses','2':'colour blind','0':'none','1,2':'both'

Among them, 'E1773','C76','C77','E148','E1389','E1248','E2261', 'E2340', 'E150', 'E1853', 'E1798','E2334'and 'E2316'are the users that we can rely on their honesty in voting.

##votes.csv##

The delimiter is "=".

image_id: image names without '.jpg'

user_id: user id. It is related with the "id" in "users.csv".

score: general score, the integer ranges in [0,10].

difficulty: very difficult=1, difficult=2, easy=3, very easy=4

visual, composition, quality, semantic: the attributes, very bad=1, bad=2, good=3, very good=4

factor: light and colour=1, composition and depth=2, quality=3, semantic=4

device: the browser information

vote_time: the voting time from last vote's submittion to this vote's submittion in seconds.

##votes_filtered.csv##

These are filtered votes we used.

The delimiter is "=".

image_id: image names without '.jpg'

user_id: user id. It is related with the "id" in "users.csv".

score: general score, integer ranges in [0,10]

difficulty: very difficult=1, difficult=2, easy=3, very easy=4

visual, composition, quality, semantic: the attributes, very bad=1, bad=2, good=3, very good=4

vote_time: the voting time from last vote's submittion to this vote's submittion.

1,2,3,4: 1=light and colour, 2=composition and depth, 3=quality, 4=semantic; value 1 means this checkbox is clicked, value 0 means it is not.

##region_index.csv##

This is the region list and their codes used in users.csv.

The delimiter is "=".The first column is the codes, and the second column is the regions.

#More info#

Analysis between AVA and EVA will be updated.
