Saltstack Configuration Management Layout Proposal
==================================================

Here is a best practice[tm] layout for an infrastructure
managed by salt. 

In configuration management there isn't a single standard way
to do things. It depends on the needs of your infrastrucutre and 
challenges you face.

This guide is lagely based on experience of running infrastructure
with salt and having insight in a large ammonut of  
  

Principals of Config Management
---------------------------------

* KISS: Keep it Simple Stupid
  Refrain from complex constructs. If you cannot look at something 
  in cfgmgmt and undestand it straight away, chances are high that
  you are overengineering. 

* LHF: Low Hanging Fruits first.   
  100% Automation is a dream we are working towards, but some things take 
  exorbitant time to automate.


  What to automate in order:
    * Core system settings
      -  (DNS /etc/resolv.conf, NTP, Proxy Settings, Base-Packages) 
    * Repetitive Tasks



Saltstack vs. Ansible
---------------------
Key advantages of Salt:

Mutliple Operation modes: 
 - Salt can run via ssh, standalone , as well as in the master/slave constructs. 

 - Salt at its core has an event / reactor system that can automatically react to events

 - Salt has a f.a.r. more flexible targeting mechanism than ansible with its PCRE targeting

 - Salt can provide variables dynamically to the client dependening on many factors such as hostname, subnet, grains.. 

 - Salt can use pretty much anything as inventory (mysql, excel sheets, consul, ..)
 
 - Salt scales to 10 thousands of nodes easly, thanks to its zeromq bus. 
 
 - Salt makes clear distingshen between a module that (execution modules) vs one that (state module) tests

 - Salt can render states dynamically (jinja or other templating engine...) 
 
 - Salt has an extendible REST API

 - Salt's output can be had in text,csv,json,xml.. and easly programatically reused 

 - Salt's facts are simply extended and additional grains are availlebe
 
 - Salt Mine can share specific data from one host to other hosts

 - Salt actually has an orchestration layer that is aware of dependencies

 - Salt has fantastic/fanatic documentation

 - Salt can provision machines directly even before boot
