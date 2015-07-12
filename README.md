Introduction 
===================

`#OpenAPS` is a development tool that provides an interface for users to build custom apps. A basic structure in to which a user can drop modules and content is provided. This tool fosters creativity as we collaborate and evaluate our work, by programming a custom solution to fit our needs, with the creation of an open source artificial pancreas, as patients with diabetes. A command-line interface is used and a graphical user interface (GUI) is unnecessary and not recommended. 

----------


Working with OpenAPS
---------------------------------
For getting started, please follow this [guide](https://github.com/openaps/openaps).

In order to have a fully operating OpenAPS, you will need to execute OpenAPS with your preprogrammed scripts, either in Python or JavaScript, as a bash shell script, using cron, to schedule the OpenAPS to make dosing changes at a specified time. See this tutorial on [cron](https://en.wikipedia.org/wiki/Cron). A tutorial on bash shell scripts is [here](http://tldp.org/HOWTO/Bash-Prog-Intro-HOWTO.html)

You can create and support plugins for OpenAPS, specifically, as a "process" type of plugin. So by typing for example 

>`openaps device add calciob process --require input node iob.js` 

tells OpenAPS that `iob.js` is a "node script". This also means that it takes a single input, which we will call `input` and to internally name that as a device called `calciob`. So now the plugin shows up under `openaps use calciob -h` and if your run the use case there, as stated in the getting started guide, it actually runs the node script with the required arguments.


