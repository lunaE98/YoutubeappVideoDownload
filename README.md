# YoutubeappVideoDownload
Tutorial, creat a Youtube Download  app with Python

we will create a simple YouTube video downloader using Python and the pytube library. Pytube is a lightweight library that allows you to download YouTube videos quickly and easily.

Here are the steps we will follow:

Install pytube library
Get the YouTube video URL
Download the YouTube video
Let's get started!

Step 1: Install Pytube library

First, we need to install the pytube library. Open your command prompt or terminal and type the following command:
pip install pytube

Step 2: Get the YouTube video URL

Now, we need to get the URL of the YouTube video that we want to download. There are different ways to do this, but we will use the pyperclip library to get the URL from the clipboard.

If you don't have pyperclip installed, run the following command:
pip install pyperclip

Here's the code:

import pyperclip

url = pyperclip.paste()

This code will get the URL from the clipboard and store it in the variable url.

Step 3: Download the YouTube video

Finally, we can use the pytube library to download the YouTube video. Here's the code:
from pytube import YouTube

# Create a YouTube object
yt = YouTube(url)

# Get the first stream
stream = yt.streams.first()

# Download the video
stream.download()

This code will create a YouTube object from the URL, get the first stream, and download the video. The video will be saved in the current working directory.

Here's the complete code:

import pyperclip
from pytube import YouTube

# Get the URL from the clipboard
url = pyperclip.paste()

# Create a YouTube object
yt = YouTube(url)

# Get the first stream
stream = yt.streams.first()

# Download the video
stream.download()

