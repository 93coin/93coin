NinetyThreeCoin
=====================================

https://93coin.us

What is DISK?
----------------

`DISK` is a decentralised digital currency with near-instant transaction speeds and negligible transaction fees built upon Proof of Stake 3.0 (PoSV3, BPoS) as
introduced by the BlackCoin development team.

For more information about NinetyThreeCoin itself, see https://93coin.us.

What is NinetyThreeCoin?
----------------

NinetyThreeCoin is the name of open source software which enables the use of this currency. It takes NinetyThreeCoin to the next level by building upon
Bitcoin Core 0.13.2 with some patches from newer Bitcoin Core versions to offer performance enhancements, wider compatibility with third party services and a more advanced base.

For more information, as well as an immediately useable, binary version of the NinetyThreeCoin software, see https://93coin.us.

Genesis Block
-------------
```
$ python genesis.py -a scrypt -z "Do what thou wilt shall be the whole of the Law. Love is the law, love under will."
04ffff001d01044c52446f20776861742074686f752077696c74207368616c6c206265207468652077686f6c65206f6620746865204c61772e204c6f766520697320746865206c61772c206c6f766520756e6465722077696c6c2e
algorithm: scrypt
merkle hash: 48f5ce34fb431e335e0d7acabe7602ea0408c43bcb72df963a551733074a2f1e
pszTimestamp: Do what thou wilt shall be the whole of the Law. Love is the law, love under will.
pubkey: 04678afdb0fe5548271967f1a67130b7105cd6a828e03909a67962e0ea1f61deb649f6bc3f4cef38c4f35504e51ec112de5c384df7ba0b8d578a4c702b6bf11d5f
time: 1703921716
bits: 0x1e0ffff0
Searching for genesis hash..
genesis hash found!
nonce: 857842
genesis hash: c59313e50ab54a3b9f0934ce7740600d2d0fd5bae180a474ea939514561c679f
```

License
-------

NinetyThreeCoin is released under the terms of the MIT license. See [COPYING](COPYING) for more
information or see https://opensource.org/licenses/MIT.

Development Process
-------------------

The `main` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/93coin/93coin/tags) are created
regularly to indicate new official, stable release versions of NinetyThreeCoin.

Change log can be found in [CHANGELOG.md](CHANGELOG.md).

The contribution workflow is described in [CONTRIBUTING.md](CONTRIBUTING.md).


Testing
-------

Testing and code review might be the bottleneck for development. Please help out by testing
other people's pull requests, and remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write [unit tests](/doc/unit-tests.md) for new code, and to
submit new unit tests for old code. Unit tests can be compiled and run
(assuming they weren't disabled in configure) with: `make check`

There are also [regression and integration tests](/qa) of the RPC interface, written
in Python, that are run automatically on the build server.
These tests can be run (if the [test dependencies](/qa) are installed) with: `qa/pull-tester/rpc-tests.py`

The Travis CI system makes sure that every pull request is built for Windows, Linux, and OS X, and that unit/sanity tests are run automatically.

### Manual Quality Assurance (QA) Testing

Changes should be tested by somebody other than the developer who wrote the
code. This is especially important for large or high-risk changes. It is useful
to add a test plan to the pull request description if testing the changes is
not straightforward.
