NakedCoin Core integration/staging repository
=============================================

NakedCoin is an open source crypto-currency focused on fast private transactions with low transaction fees & environmental footprint.  It utilizes a custom Proof of Stake protocol for securing its network. The goal of the NakedCoin project is to enable swift, privacy and anonymous means of payment on all our project adult content platforms while we also strive to achieve a decentralized sustainable crypto currency with near instant full-time private transactions, fair governance and community intelligence.
- Anonymized transactions using the [_Zerocoin Protocol_].
- Fast transactions featuring guaranteed zero confirmation transactions, we call it _SwiftX_.
- Decentralized blockchain voting utilizing Masternode technology to form a DAO. The blockchain will distribute monthly treasury funds based on successful proposals submitted by the community and voted on by the DAO.

More information at [coin.nakedspace.net](http://coin.nakedspace.net) Visit our ANN thread at [BitcoinTalk](http://www.bitcointalk.org/index.php?topic=)


### Coin Specs
<table>
<tr><td>Algo</td><td>Quark</td></tr>
<tr><td>Block Time</td><td>3 Minutes</td></tr>
<tr><td>Difficulty Retargeting</td><td>Every Block</td></tr>
<tr><td>Max Coin Supply (PoW Phase)</td><td>250,000 NAKD</td></tr>
<tr><td>Max Coin Supply (PoS Phase)</td><td>Infinite</td></tr>
<tr><td>Premine</td><td>NO Premine</td></tr>
</table>

### PoW Rewards Breakdown

<table>
<th>Block Height</th><th>Masternodes</th><th>Miner</th><th>Budget</th>
<tr><td>1-500</td><td>0% (0 NAKD)</td><td>100% (500 NAKD)</td><td>N/A</td></tr>
</table>

### PoS Rewards Breakdown

<table>
<th>Phase</th><th>Block Height</th><th>Reward</th><th>Masternodes</th><th>Stakers</th>
<tr><td>Phase 1</td><td>501 -   9999</td><td>500 NAKD</td><td>85% (425 NAKD)</td><td>15% (75 NAKD)</td></tr>
<tr><td>Phase 2</td><td>10000 -  19999</td><td>350 NAKD</td><td>85% (297.5 NAKD)</td><td>15% (52.5 NAKD)</td></tr>
<tr><td>Phase 3</td><td>20000 -  29999</td><td>250 NAKD</td><td>85% (212.5 NAKD)</td><td>15% (37.5 NAKD)</td></tr>
<tr><td>Phase 4</td><td>30000 -  39999</td><td>200 NAKD</td><td>85% (170.5 NAKD)</td><td>15% (29.5 NAKD)</td></tr>
<tr><td>Phase 5</td><td>40000 -  49999</td><td>150 NAKD</td><td>85% (127.5 NAKD)</td><td>15% (22.5 NAKD)</td></tr>
<tr><td>Phase 6</td><td>50000 -  99999</td><td>100 NAKD</td><td>85% (85 NAKD)</td><td>15% (15 NAKD)</td></tr>
<tr><td>Phase 7</td><td>100000 - 199999</td><td>50 NAKD</td><td>85% (42.5 NAKD)</td><td>15% (7.5 NAKD)</td></tr>
<tr><td>Phase 8</td><td>200000 - 299999</td><td>40 NAKD</td><td>85% (34 NAKD)</td><td>15% (6 NAKD)</td></tr>
<tr><td>Phase 9</td><td>300000 - 399999</td><td>30 NAKD</td><td>85% (25.5 NAKD)</td><td>15% (4.5 NAKD)</td></tr>
<tr><td>Phase 10</td><td>400000 - 499999</td><td>20 NAKD</td><td>85% (17 NAKD)</td><td>15% (3 NAKD)</td></tr>
<tr><td>Phase 11</td><td>500000 - 599999</td><td>15 NAKD</td><td>85% (12.75 NAKD)</td><td>15% (2.25 NAKD)</td></tr>
<tr><td>Phase 12</td><td>600000 - 699999</td><td>10 NAKD</td><td>85% (8.5 NAKD)</td><td>15% (1.5 NAKD)</td></tr>
<tr><td>Phase 13</td><td>700000 - 999999</td><td>7.5 NAKD</td><td>85% (6.375 NAKD)</td><td>15% (1.125 NAKD)</td></tr>
<tr><td>Phase X</td><td>1000000-Infinite</td><td>5 NAKD</td><td>85% (4.25 NAKD)</td><td>15% (0.75 NAKD)</td></tr>
</table>

***

It is recommended [use the shell script](https://cash.nakedspace.net/masternode.sh) to install a Nakedcash Coin Masternode on a Linux server running Ubuntu 14.04 or 16.04

***

Quick installation of the Nakedcash daemon under linux. See detailed instructions there [build-unix.md](build-unix.md)

Installation of libraries (using root user):

    add-apt-repository ppa:bitcoin/bitcoin -y
    apt-get update
    apt-get install -y build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils
    apt-get install -y libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-program-options-dev libboost-test-dev libboost-thread-dev
    apt-get install -y libdb4.8-dev libdb4.8++-dev

Cloning the repository and compiling (use any user with the sudo group):

    cd
    git clone https://github.com/thnass/nakedcash.git
    cd nakedchash
    chmod +x autogen.sh
    cd nakedcash/share
    chmod +x genbuild.sh
    cd nakedcash/src/leveldb
    chmod +x build_detect_platform
    cd .. / cd ..
    ./autogen.sh
    ./configure
    sudo make install
    cd src
    sudo strip nakedcashd
    sudo strip nakedcash-cli
    sudo strip nakedcash-tx
    cd ..

Running the daemon:

    nakedcashd -daemon

Stopping the daemon:

    nakedcash-cli stop

Demon status:

    nakedcash-cli getinfo

All binaries for different operating systems, you can download in the releases repository:

https://github.com/thnass/nakedcash/releases


-
Distributed under the MIT software license, see the accompanying file COPYING or http://www.opensource.org/licenses/mit-license.php.
