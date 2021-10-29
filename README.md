## What is Tor ?
===============

        Tor is a connection-oriented anonymizing communication service. 
        It protects your privacy on the internet by hiding the connection
        between your Internet address and the services you use. We believe Tor
        is reasonably secure, but please ensure you read the instructions and
        configure it properly.

## To build Tor from source:
===========================

        ./configure && make && make install

## To build Tor from a just-cloned git repository:
=================================================

        sh autogen.sh && ./configure && make && make install

## Home page:
============

        https://www.torproject.org/


## Here is a list of the main goals Tor should accomplish:
=========================================================

        * Safe. Remember we are serving people under heavy censorship.

        * Easy to use. The fewer user interactions, the better.

        * Clean code. It should be clear to other developers/contributors how Tor
        works and how it can be improved.

        * Automated. We should try to automate things as much as possible.

        * Language and provider friendly. It should be easy to support new languages
        and to add new providers for storing packages and generate links.

## Installing Tor on powerpc64le
=================================

### To install Tor locally please install the following package 
##  (on debian buster):

        {
        wget https://github.com/flatcloud0b3/tor/releases/download/v0.4.6.8/tor-0.4.6.8-linux-gnu-ppc64le-buster.deb && \
        wget https://github.com/flatcloud0b3/tor/releases/download/v0.4.6.8/tor-0.4.6.8-linux-gnu-ppc64le-buster.deb.sig && \
        gpg --keyserver hkp://keyserver.ubuntu.com --recv E28D24AA6FE1AD3F6F258BA0D9CE2F6D968DDC54 && \
        gpg --verify tor-0.4.6.8-linux-gnu-ppc64le-buster.deb.sig && dpkg -i tor-0.4.6.8-linux-gnu-ppc64le-buster.deb 
        }
 
### To install Tor locally please install the following package 
##  (on debian bullseye):

        {
        wget https://github.com/flatcloud0b3/tor/releases/download/v0.4.6.8/tor-0.4.6.8-linux-gnu-ppc64le-bullseye.deb && \
        wget https://github.com/flatcloud0b3/tor/releases/download/v0.4.6.8/tor-0.4.6.8-linux-gnu-ppc64le-bullseye.deb.sig && \
        gpg --keyserver hkp://keyserver.ubuntu.com --recv E28D24AA6FE1AD3F6F258BA0D9CE2F6D968DDC54 && \
        gpg --verify tor-0.4.6.8-linux-gnu-ppc64le-bullseye.deb.sig && dpkg -i tor-0.4.6.8-linux-gnu-ppc64le-bullseye.deb \
        apt --fix-broken install -y
        }

## Download new versions:
========================

        https://www.torproject.org/download/download.html

## Documentation, including links to installation and setup instructions:
========================================================================

        https://www.torproject.org/docs/documentation.html

## Making applications work with Tor:
====================================

        https://gitlab.torproject.org/legacy/trac/-/wikis/doc/TorifyHOWTO

## Frequently Asked Questions:
=============================

        https://www.torproject.org/docs/faq.html

## Release timeline:
===================

        https://gitlab.torproject.org/tpo/core/team/-/wikis/NetworkTeam/CoreTorReleases

## To get started working on Tor development:
============================================

        See the doc/HACKING directory.

## Running tests
================

Tor includes PyTest unit tests. To run the tests, first install the dependencies above and then run:


        ```
        $ python3 scripts/create_db -n -c -o -f tests/tor.db
        $ python3 scripts/add_links_to_db -f tests/tor.db
        $ pytest-3 -s -v tests/
        ```
