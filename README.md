# Trovebox Uploader

## What is this?
This is a script for uploading images/folder of images to a Trovebox (https://github.com/photo) server.

## Requirements
* Python 2.7
* Trovebox Python Library 

## Installation
Install the Trovebox Python Library

    pip install trovebox 

Clone the repo or just download the file trovebox-uploader.py

    git clone https://github.com/endast/trovebox_uploader.git

## Usage

First make sure you have specified the credentials 
file in ``~/.config/trovebox/default``

    # ~/.config/trovebox/default
    host = your.host.com
    consumerKey = your_consumer_key
    consumerSecret = your_consumer_secret
    token = your_access_token
    tokenSecret = your_access_token_secret

for more info see https://github.com/photo/openphoto-python/

Simplest use case, just upload the specified image or folder of images:

    python trovebox-uploader.py -i path_to_image_or_folder

Adding the tags 42 and Panic to the image/images:

    python trovebox-uploader.py -i path_to_image_or_folder -t 42 Panic

Adding the image/images to album Dead_Parrot:

    python trovebox-uploader.py -i path_to_image_or_folder -a Dead_Parrot

Check if the image is a duplicate before uploading the image to the server, makes an extra request to the server. But can save you a time if you have duplicates in your source. Default off:

    python trovebox-uploader.py -i path_to_image_or_folder -c


Making the uploaded images public:
    
    python trovebox-uploader.py -i path_to_image_or_folder -p
  
You can of course combine all of the arguments:

    python trovebox-uploader.py -i dark_knight.jpg -c -p -t pass none shall -a Grail


## Help


## Versions
0.2 - Added support for permissions and albums

0.1 - First version
