# SCHEDULE-for-z/VM
The SCHEDULE program utilizes your z/VM virtual machine's clock comparator to receive interrupts at the date and time determined by you. 

Purpose:    To provide facility for scheduling and executing various
            CP and CMS commands,  as well as for writing messages to
            the console at the time(s) predetermined by the user.

Implementation: This program executes as a nucleus extension and is driven by the Clock Comparator external interrupt X'1004'.

Attributes:  Self-relocating nucleus extension. Designed to work under 370, XA or ESA architecture, below or above the 16Mb line.


Generation: 

            VMFHASM SCHEDULE ctlfname
            LOAD    SCHEDULE (CLEAR AMODE 31 RMODE ANY RLDSAVE
            GENMOD  SCHEDULE (SYSTEM

    where - 'ctlfname' is the filename of the control file for updat-
            ing the base source code
            
            Tested under both z/VM 7.1 and 7.2 
            
 Just get the VMARC file from here, uplod it to your CMS session in fixed(80),binary format, and unarc it. You will gedt all of the files necessary to build SCHEDULE, plus a pre-built module ready to go.

