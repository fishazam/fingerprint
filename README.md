FISHazam FISH FINGERPRINT ALGORITHM
==========


The fish fingerprint algorithm is based on the Dejavu audio fingerprinting and recognition algorithm implemented in Python by Will Devro.

See his [blog post here](http://willdrevo.com/fingerprinting-and-audio-recognition-with-python.html) for a good explanation of how it works.

The main difference is that the spectrogram in our case is not derived from **audio waves** but from **infrared waves**.

Instead of a microphone, the data is from a spectrometer.  In our case, we use the [python usb module](https://walac.github.io/pyusb/) and assume an infrared spectrometer is connected via usb.  We pass the spectrogram data directly to be fingerprinted.  Check out our [api repo](https://github.com/fishazam/api) for more details on how that works.    

For a video screencast providing an overview of the algorithm, check out our [YouTube channel](https://www.youtube.com/channel/UC4iefN94hdmy2HIM8PxcBPA).

Please keep in mind that we created the project in a single weekend for [Fishackathon](http://www.fishackathon.co/) 2016 in London.  Our devpost describing the experience can be [found here](http://devpost.com/software/fishazam-ensrpw/).  We were only two in our team.  And we did not have a professional spectrometer to do tests.  So there is bound to be bugs.  But we will, hopefully with some funding, continue working on the project.  Feel free to fork the project and improve it.

Visit [our website](http://fishazam.com/) for an overview of the problem we are trying to address along with some helpful links.  A video of the presentation we made can be [found here](https://www.youtube.com/watch?v=zIM8cgRy17Y).


##Installation and Dependencies:

Read [INSTALLATION.md](INSTALLATION.md)

## Database Setup

First, install the above dependencies.

Second, you'll need to create a MySQL database where Dejavu can store fingerprints. For example, on your local setup:

	$ mysql -u root -p
	Enter password: **********
	mysql> CREATE DATABASE IF NOT EXISTS dejavu;

## How does it work?

These papers describe in depth how the fingerprint algorithm works,

* [Shazam](http://www.ee.columbia.edu/~dpwe/papers/Wang03-shazam.pdf)
* [MusicRetrieval](http://www.cs.cmu.edu/~yke/musicretrieval/)
* [Chromaprint](https://oxygene.sk/2011/01/how-does-chromaprint-work/)
