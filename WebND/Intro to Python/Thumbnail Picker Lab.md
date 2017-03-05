Thumbnail Image Picker Lab

Imagine that you're building an online news aggregator, UdaciNews, similar to [Hacker News](https://news.ycombinator.com/), [Reddit](https://www.reddit.com/), or [Digg](http://digg.com/). Your users submit links to interesting articles, which are then posted to the UdaciNews homepage.


You've been tasked with writing a new feature for UdaciNews, article thumbnails. When users submit a link, an image from the page should be chosen as a thumbnail image for the article. Your task is to write a program that inspects a web page and chooses a suitable image to use as a thumbnail.

# Requirements:

Write a program called ThumbnailPicker.py that takes a command line argument, the url of an HTML document. The program should find the largest image on the page that is approximately square, and print its url.

Here's a demonstration of the program in operation:

$ python3 ThumbnailPicker.py http://www.udacity.com

https://d125fmws0bore1.cloudfront.net/assets/pages/homepage/thumb-content@1x-c9f1c26bcef02100eee3b5f336bf25a17c6dfdf039f12814fb0e7ca20d1e5c76.png

The selected image must be approximately square, this prevents us from selecting navigation banners or other UI elements to use as a thumbnail. An approximately square image is no more than 1.5 times taller than it is wide, and is no more than 1.5 times wider than it is tall.

Note: Your program should ignore svg images. [Vector graphics](https://en.wikipedia.org/wiki/Vector_graphics) don't have a defined size, which complicates our task.

# Libraries:

The third party libraries you need to complete this project are:

* [requests](http://docs.python-requests.org/), to get the specified page, and to get the images from that page.

* [BeautifulSoup4](https://www.crummy.com/software/BeautifulSoup/bs4/doc/), to parse the page and locate images.

* The Python Image Library, [Pillow](https://pillow.readthedocs.io/en/3.4.x/handbook/tutorial.html), to find the dimensions of images.

I've put these requirements into a [requirements.txt file](https://d17h27t6h515a5.cloudfront.net/topher/2016/December/584f1e87_requirements/requirements.txt). Place this requirements.txt file in a directory on your computer, and use pip to install the libraries:

$ pip3 install -r requirements.txt

You will also need to use packages from the standard library. Getting all of these libraries to work together will be a challenge. Use your favorite search engine to find solutions to the problems you encounter!

# Rubric:

* The submitted program accepts input and produces output as demonstrated in the Requirements section of this assignment

* The program finds the biggest image on page that is approximately square

* The program uses functions to break the task into smaller parts

