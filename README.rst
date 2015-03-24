=========================
An introduction to Docker
=========================

Date:
 * Tuesday, March 24, 2015 6:30 PM

Venue:
 * MixRadio, Prudential Buildings, 11-19 Wine St., Bristol, BS1 2PH, Bristol, Bristol
 * http://maps.google.com/maps?f=q&hl=en&q=Prudential+Buildings%2C+11-19+Wine+St.%2C+Bristol%2C+BS1+2PH%2C+Bristol%2C+Bristol%2C+gb

Meetup:
 * http://www.meetup.com/CodeHub-Bristol/events/219720033/

(There are a limited number of places at the venue, so if any of you have RSVPd to the Meetup but are not able to attend, please go to the Meetup page and change your status so that others can take your place and so that we can estimate how much food and drink to order.)

Slides:
 * http://htmlpreview.github.io/?https://github.com/wallrj/docker-tutorial/blob/master/docker-tutorial.html#/

Presenter:
 * Richard Wall


Preparations
============

It would be really helpful if you could install some or all of the following software on your laptop before the Docker workshop.
Don't worry if you can't, we'll be able to help you get set up when you arrive.
But the more you can get installed before hand, the further we'll be able to get in the limited time tomorrow evening.

* **Bring your laptop!**

And if possible, pre-install:

* **VirtualBox**: https://www.virtualbox.org
* **Vagrant**: https://docs.vagrantup.com/v2/installation
* **Git**: http://git-scm.com/downloads

For bonus points, pre-install Docker:

* Docker: https://docs.docker.com/installation/#installation

(but we'll cover that during the workshop and provide an Ubuntu Linux virtual machine with Docker pre-installed)

I've also uploaded a tutorial box to Vagrantcloud.
So if you want to be super prepared and if you've managed to install Git and Vagrant on your laptop (see messages below),
please clone this repository:

```
git clone https://github.com/wallrj/docker-tutorial.git
```

Then change to the `docker-tutorial` directory
and install the tutorial environment, by running the following command:

```
vagrant up
```

Vagrant will download the virtual machine and start it up for you.

If all goes well you should now be able to run docker commands on the virtual machine:

```
vagrant ssh -- docker run hello-world
```

And see output like this:

```
Hello from Docker.
This message shows that your installation appears to be working correctly.
...
```
