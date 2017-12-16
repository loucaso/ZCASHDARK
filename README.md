Zcashdark integration/staging tree
================================

https://www.coin.zcashdark.xyz/

Copyright (c) 2009-2014 Bitcoin Developers
Copyright (c) 2017-2018 Zcashdark Developers

O que é Zcashdark?
------------------
Zcashdark é uma versão lite do Bitcoin usando o scrypt como um algoritmo de prova de trabalho.

- Alvos do bloco de 2,5 minutos
- Metades de subsídio em blocos de 840k (~ 4 anos)
- ~ 84 milhões de moedas totais
- O resto é o mesmo que Bitcoin.

- 50 moedas por bloco
- 2016 blocos para retarget dificuldade
- Para obter mais informações, bem como uma versão binária do software Zcashdark, imediatamente utilizável, veja 
- the Zcashdark client sofware, see https://www.coin.zcashdark.xyz/

License
-------

Zcashdark is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the Zcashdark
development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch
submitter will be asked to start a discussion with the devs and community.

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/loucaso/zcashdark/tags) are created
regularly to indicate new official, stable release versions of Zcashdark.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test. Please be patient and help out, and
remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code.

Unit tests for the core code are in `src/test/`. To compile and run them:

    cd src; make -f makefile.unix test

Unit tests for the GUI code are in `src/qt/test/`. To compile and run them:

    qmake BITCOIN_QT_TEST=1 -o Makefile.test bitcoin-qt.pro
    make -f Makefile.test
    ./zcashdark-qt_test



Install the dependencies
------
sudo apt-get install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev <br>
sudo apt-get install bsdmainutils libboost-system-dev libboost-filesystem-dev libboost-chrono-dev<br>
sudo apt-get install libboost-program-options-dev libboost-test-dev libboost-thread-dev<br>
sudo apt-get install libqt5gui5 libqt5core5a libqt5dbus5 qttools5-dev qttools5-dev-tools libprotobuf-dev <br>
sudo apt-get install libqrencode-dev protobuf-compiler miniupnpc<br>

To install the deprecated version of Berkeley DB 4.8 
------
sudo add-apt-repository ppa:bitcoin/bitcoin<br>
sudo apt-get update<br>
sudo apt-get install libdb4.8-dev libdb4.8++-dev<br>

 Compile
 ------
./autogen.sh<br>
./configure<br>
make<br>
