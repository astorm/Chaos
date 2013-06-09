Chaos
=====

A Magento module that randomly changes configuration values — useful for developers who want to write bullet proof extensions. 

###Background

Inspired by the Netflix Chaos monkey, Chaos is the start to an extension which provides a framework for swapping configuration node values randomly.  Ships with code that will swap Magento in and out of flat category/product mode at random, helping your team ensure their extensions/customizations work as expected. 

Original Blog Post: http://alanstorm.com/magento_flat_collection_chaos

###Build Instructions

The `build_chaos.bash` file is a bash script that will create a simple tar archive of the extension files. 

    $ ./build_chaos.bash
    
This script assumes the existence of a `var` folder.    

The `magento-tar-to-connect.chaos.php` file is a configuration file for the <a href="https://github.com/astorm/MagentoTarToConnect/">MagentoTarToConnect</a> command-line script.  This will allow you to build a Magento Connect 2.0 extension with the following.

    $ magento-tar-to-connect.phar magento-tar-to-connect.chaos.php
    
See the <a href="https://github.com/astorm/MagentoTarToConnect/#readme">MagentoTarToConnect README.md</a> for more information on how this tool works.     