Circular dig (odig)
===================

A simple Bash script to lookup a hostname and the PTR record of the given IP address at a stroke.

# Installation

    cd /tmp
    git clone https://github.com/frdmn/circular-dig.git
    sudo mv circular-dig/bin/odig /usr/bin/odig
    sudo chmod +x /usr/bin/odig

# Usage

    $ odig frd.mn
    frd.mn returned the following DNS records:
    1. returned IP: 82.196.7.61
       corresponding PTR: c-3po.frd.mn.

---

    $ odig www.google.de
    www.google.de returned the following DNS records:
    1. returned IP: 173.194.113.191
       corresponding PTR: ham02s12-in-f31.1e100.net.
    2. returned IP: 173.194.113.183
       corresponding PTR: ham02s12-in-f23.1e100.net.
    3. returned IP: 173.194.113.184
       corresponding PTR: ham02s12-in-f24.1e100.net.

---


    $ odig bukkit.org
    bukkit.org returned the following DNS records:
    1. returned IP: 190.93.240.99
       Error: No PTR set for 190.93.240.99
    2. returned IP: 190.93.241.99
       Error: No PTR set for 190.93.241.99
    3. returned IP: 141.101.112.99
       Error: No PTR set for 141.101.112.99
    4. returned IP: 141.101.113.99
       Error: No PTR set for 141.101.113.99
    5. returned IP: 141.101.123.99
       Error: No PTR set for 141.101.123.99
