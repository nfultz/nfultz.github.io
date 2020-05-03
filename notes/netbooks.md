Netbooks are low-cost, lower-power computers. Typically, they have screens under 12" and cost less than $400.

 

I purchased a 1015pe in January 2011 and used it for three and a half years of grad school.

I purchased my X200ca in Fall 2014 using saved up loose change, credit card rewards and gift certificates.

# in /etc/X11/xorg.conf

#Enable Sandy Bridge acceleration



Section "Device"

        Identifier "Intel Graphics"

        Driver "intel"

        Option "AccelMethod" "sna"

EndSection



Not only does <code>sna</code> have superior performance but it also fixes several GTK3 graphical glitches.

