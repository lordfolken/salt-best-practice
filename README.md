Saltstack Configuration Management Layout Proposal
==================================================

Here is a best practice[tm] layout for an infrastructure
managed by salt. 

In configuration management there isn't a single standard way
to do things. It depends on the needs of your infrastrucutre and 
challenges you face.  

Principals of Config Management
---------------------------------

* KISS: Keep it Simple Stupid
  Refrain from complex constructs. If you cannot look at something 
  in cfgmgmt and undestand it straight away, chances are high that
  you are overengineering. 

* LHF: Low Hanging Fruits first.   
  100% Automation is a dream we are working towards, but some things take 
  exorbitant time to automate.

  What to automate first:
    * System Settings (DNS /etc/resolv.conf, NTP, Proxy Settings, Base-Packages) 
    * 
