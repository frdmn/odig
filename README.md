# odig

[![Current tag](http://img.shields.io/github/tag/frdmn/odig.svg)](https://github.com/frdmn/odig/tags) [![Repository issues](http://issuestats.com/github/frdmn/odig/badge/issue)](http://issuestats.com/github/frdmn/odig) [![Flattr this repository](http://api.flattr.com/button/flattr-badge-large.png)](https://flattr.com/submit/auto?user_id=frdmn&url=https://github.com/frdmn/odig)

A simple Bash script to lookup a hostname and the PTR record of the given IP address at a stroke.

## Installation

    brew tap frdmn/homebrew-formulas
    brew install odig

## Usage

#### Lookup A/CNAMES and reverse lookup them

    $ odig frd.mn
    frd.mn returned the following DNS records:
    1. returned IP: 82.196.7.61
       corresponding PTR: c-3po.frd.mn.

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

---

#### Lookup MX records and reverse lookup them

    $ odig -m google.de
    google.com returned the following MX records:
    1. returned hostname (CNAME): alt2.aspmx.l.google.com.
       -> resolved IP: 173.194.79.26
       -> resolved PTR: pb-in-f26.1e100.net.
    2. returned hostname (CNAME): alt3.aspmx.l.google.com.
       -> resolved IP: 173.194.64.27
       -> resolved PTR: oa-in-f27.1e100.net.
    3. returned hostname (CNAME): alt4.aspmx.l.google.com.
       -> resolved IP: 74.125.142.27
       -> resolved PTR: ie-in-f27.1e100.net.
    4. returned hostname (CNAME): aspmx.l.google.com.
       -> resolved IP: 173.194.70.26
       -> resolved PTR: fa-in-f26.1e100.net.
    5. returned hostname (CNAME): alt1.aspmx.l.google.com.
       -> resolved IP: 173.194.71.26
       -> resolved PTR: lb-in-f26.1e100.net.

## Contributing

1. Fork it
2. Create your feature branch: `git checkout -b feature/my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin feature/my-new-feature`
5. Submit a pull request

## Version

1.0.0

## License

[MIT](LICENSE)
