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
    1. returned IP:  104.31.67.66
       resolved PTR: (none)
    2. returned IP:  104.31.66.66
       resolved PTR: (none)

---

    $ odig www.nsa.gov
    www.nsa.gov returned the following DNS records:
    1. returned hostname (CNAME): www.nsa.gov.edgekey.net.
    2. returned hostname (CNAME): e6655.dscna.akamaiedge.net.
    3. returned IP:  23.36.84.226
       resolved PTR: a23-36-84-226.deploy.static.akamaitechnologies.com.

---

#### Lookup MX records and reverse lookup them

    $ odig -m google.de
    google.de returned the following MX records:
    1. returned hostname (CNAME): alt2.aspmx.l.google.com.
       resolved IP:  74.125.68.27
       resolved PTR: sc-in-f27.1e100.net.
    2. returned hostname (CNAME): alt1.aspmx.l.google.com.
       resolved IP:  64.233.164.27
       resolved PTR: lf-in-f27.1e100.net.
    3. returned hostname (CNAME): aspmx.l.google.com.
       resolved IP:  64.233.166.27
       resolved PTR: wm-in-f27.1e100.net.
    4. returned hostname (CNAME): alt3.aspmx.l.google.com.
       resolved IP:  64.233.189.27
       resolved PTR: tl-in-f27.1e100.net.
    5. returned hostname (CNAME): alt4.aspmx.l.google.com.
       resolved IP:  173.194.72.27
       resolved PTR: tf-in-f27.1e100.net.

## Contributing

1. Fork it
2. Create your feature branch: `git checkout -b feature/my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin feature/my-new-feature`
5. Submit a pull request

## Version

1.0.1

## License

[MIT](LICENSE)
