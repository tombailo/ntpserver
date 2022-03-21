ntpserver
=========

A Python based ntp server.

Tested on Linux and Windows7.

Based on ntplib(https://pypi.python.org/pypi/ntplib/), thanks for their work.

If you have any question, please contact me at limifly@gmail.com.

Timewarp testing
================

To set an arbitrary time on an STB via NTP:

On PC:

        ntpserver.py --time "2022-03-27 00:45" # 15 minutes before BST starts

On STB:
        
        lsr-config platform.time.sources SNTP
        lsr-config isp.time.ntpserver.1 <Your PC IP>
        lsr-config isp.time.ntpserver.2 <Your PC IP>
        lsr-config isp.time.ntpserver.3 <Your PC IP>
        lsr-config isp.time.ntpserver.4 <Your PC IP>
        reboot
