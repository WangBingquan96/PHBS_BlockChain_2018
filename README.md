# PHBS_BlockChain_2018
## The application of blockchain in music industry
### 1. Background information in music industry
The global music industry is a tremendous one. In 2017, the revenues in the music industry were around 16 billion USD. In particular, approximately 176 million users were paying the subscription services and the revenues were mainly coming from them (Angel D., 2018). However, nowdays, there are some serious problems in the music industry due to the centralized and mediated nature of production and distribution. <br>
(1)Piracy of digital records <br>
(2)Improper rights management <br>
(3)Cumbersome royalty management <br>
(4)Delay In rewards to artists. <br>
More specifically, A report suggests that for every $1,000 of music sold, the average income musician gets only is $23.40 (just over 2%)(Angel D., 2018). To meet the US monthly minimum wage, musicians would need over 188,000 total plays on Apple Music (and even more on the competing platforms). Most of the revenues goes to the intermediaries like music streaming services like Spotify and Apple Music. They centralize the music industry and make it harder for independent musicians to become known and earn from their work. <br>
There have been many attempts to solve this problem in the past few years. It includes building single large comprehensive databases, such as the Global Repertory Database (GRD), the World Intellectual Property Organization’s International Music Registry (IMR), and the International Music Joint Venture (IMJV)(DIGIMARC, 2017).None of these efforts have succeeded, due to issues of funding, control, and the  complexity of gathering and maintaining all that data in one place.When the blockchain entered the public view, people started to think use blockchain in music industry for its decentralized, immutable and transparent characteristics. 
### 2. How music industry is operating 
First I will introduce how music industry is operating at present and what is the problem which can be solved using blockchain. There are several main participants in music industry including: <br>
(1)DSP( Any music streaming website) <br>
(2)Label (A record label or record company, is a brand or trademark associated with the marketing of music recordings and music video marketing.) <br> 
(3)Artist <br>
(4)Mechanical rights organizations (MROs) (Who handle mechanical royalties. The rights to copy and distribute are combined by music industry convention into one set of rights called mechanical rights.) <br>
(5)Performing rights organizations (PROs) (Who handle performance royalties.Performance means on a recording as well as before a live audience) <br>
(6)Users. <br>
![](https://github.com/WangBingquan96/PHBS_BlockChain_2018/blob/master/picture2.png)
When a user downloads or plays the music, the music service pays a royalty to a record label. The label passes mechanical royalties to the publishers of the underlying composition and also pays to the recording artist. Becasue the streaming of music is regarded as the performance of music, royalty is also paid to PRO. The creator of music is rewarded/paid according to number of plays of the song from DSP website (Preetam R., 2018). <br>
The problem here is that music label needs to trust on whatever data is provided by DSPs (eg. Number of downloads of a music file) and music artist in turn needs to trust on the music label. 
### 3. How blockchain could be used to solve this problem
Because music file is too big to be saved in blockchain, it just needs to create links between transactions of music on blockchain and the music files that are the subjects of the transactions to prove the music files being traded. The links are called identifiers. The link is created by putting an identifier in each transaction record which matches that of music file. The identifiers must satisfy four key requirements:<br> 
(1)robustness(the identifier remains associated with the file even after the file has been transformed in various ways, such as   transcoding, excerpting, pitch-shifting, re-equalizing, and digital-analog-digital conversion.) <br>
(2)data flexibility(the same audio data can exist in multiple files with different identifiers.) <br>
(3)identifier reliability (the identifier can reliably identify the recording in the file for rights and royalty management purpose) <br> 
(4)security (the identifier is difficult to remove or change without altering or marring the content) <br>
The identifiers could be hash of music files but a paper says that they are not robust ,flexible and secure. They can be changed by changing as little as a single bit of the audio data, and different versions of the same content (e.g., in diferent formats, codecs, or bitrates)(Preetam R., 2018). <br> 
Watermarking is a good choice for identifiers. A digital audio watermark is a set of data that is embedded directly into the audio in a way that is difficult for the listener to perceive. A well-designed watermarking scheme is robust to transformations such as transcoding, excerpting, digital-analog-digital conversion, and many types of signal processing(DIGIMARC, 2017). <br>
When someone plays music on the DSP websits, the service could deposit a transaction on a blockchain so that all identifiers such as watermarking related to music files will be recorded on blockchain.<br>
![](https://github.com/WangBingquan96/PHBS_BlockChain_2018/blob/master/picture3.png)
(1) A label sends a music file which is X to a DSP <br>
(2)File X has the file' s ID include its name, composer, MRO and PRO. We call it ID X which is a watermark embedded directly in the audio. <br>
(3)Now, a user of DSP websit plays the music and the DSP deposits a transaction on the blockchain containing ID X. <br>
(4)The label also sends copies of the file with the embedded watermarks ID X  to two PROs and an MRO.<br>
(5)The label, PROs, and MRO can all query the blockchain, using the ID embedded in File X, to find transactions involving File X. <br>
DSPs can deposit the transactions in real time, while the royalty processing organizations and also music artist can query the blockchain at them anytime to check. These data are critical to the distribution of profits. Because the data is transparent to all parties involved, the issue of trust is solved, and musicians can also promptly monitor the volume of their work to maintain their rights.<br>
### 4. One popular company using block chain in music industry
![](https://github.com/WangBingquan96/PHBS_BlockChain_2018/blob/master/ujo%20picture.png)
There are sveral companies using block chain in music industry now including  Ujo, dotBlockchain, Musiccoin and so on. Ujo is the most popular and biggest one of them. The following contents mainly discuss the portal of Ujo and analyze its disadvantages and solutions.<br>
#### (1) Introduction
Ujo Music is a music streaming and download platform. It was launched by a small team in 2015 and is gradually evolving, with more and more artists and lebels joining it. Its aim is to make musicians make more money. Artists register and publish their work, allowing listeners to discover and download albums using Ethereum cryptocurrency. It allows fans to buy music directly from artists or to tip. It uses smart contracts instead of bitcoin because smart contracts make it easier to implement many functions. In contrast to Bitcoin, Ethereum is easy to understand (eg. coding in assembly vs encoding in Javascript) and can contain more than just transactions(Anne G., 2016).<br>
#### (2) System
There are four main layers in to support the Ujo platform including core layer, service Layer, application layer and Space Layer.<br>
The core layer contain functions developed as modular components. These components are open source including artist registry, licensing handlers, oracle and ERC-721 badges which are implemented by smart contracts. Artist registry is a publish/subscribe event logger. By this function, individuals or applications could use content-ID to link their ethereum address identity to metadata which is stored off-chain via decentralized storage systems. This feature enables event subscribers to find metadata of music files linked with the Ethereum identity. The Licensing handlers are used for dealing with licensing payments. The Oracle contract is used to obtain the ETH to USD exchange rate. The ERC-721 badge includes an utilization of the ERC-721 specification and a non-forgery token (NFT).The badge contract is similar to a souvenir. In the real world, the singer's souvenir can be a signed album or a T-shirt with a singer's photo, which is used to express the fans' love for the singer and is also a common symbol of the fans group. In the virtual world, Ujo uses tokens as souvenirs, including but not limited to proof of purchase of music acquired through the platform. <br>
The service layer leverages the functions of the core layer to design a series of APIs which could be the base of applications. The businesses and application developers can use and organize them easily because they are upgradeable, interoperable, and interchangeable.<br>
The application layer is mainly for the users. It contains many front-end applications. Users could utilize the services provided by the applications or websites in the user interfaces. They could be developed for various user's needs and experience by different developers using the underlying protocols.<br>
The space layer is a new layer that is directly linked to the musical nature of the community. Ujo wants to create a decentralized world that provides a virtual space for people in the music community to interact. It will provide artists and fans with a unique and unprecedented way to interact with each other. This could be implemented by the badges. The badges holder can gain access to the musician's private chat room or a discount ticket which are incentives for fans to support their favorite artists. (Alexander A., 2018)<br>
#### (3) Payment Channel
Because streaming pay events are frequent and single payment amount is small, processing every transaction of music files on Ethereum main net will result in huge amount of cost of gas fees. By using payment channels, transaction gas costs are only paid when a channel is closed and money is withdrawn (Ujo, 2019). Payment channels are based on the state channels which are a "Layer 2 " scaling technology for Ethereum. By payment channels, users could trade among themselves directly so there is no need for gas fees until a certain number of transactions completed.<br>
#### (4) Drawbacks
(1) In order to use Ujo, one needs to utilize new software such as MetaMask or cryptocurrency wallets which can be complex and confusing for fresh users. What's worse, cryptocurrencies as most know them are volatile. For musicians that want to make a living, this volatility can be serious (Simon R., 2018).<br>
(2) It means that mistakes in the code can easily end up losing the involved parties a lot of money when the smart contracts deal with funds. Having no way of altering the code means people have to think way ahead carefully (Anne G., 2016). <br>
#### (5) Solutions and future development 
In order to solve the problem of price fluctuations in the Ethereum, they can consider using Dai as the currency of the transaction. A core benefit of Dai is that it brings the stability and utility of money into the future by unlocking the power of a decentralized stablecoin. <br>
In addition, in order to facilitate the understanding and use of customers, the process of purchasing albums using digital currency should  be completely simplified to purchase in ordinary currency, and the transaction process of converting ordinary currency into digital currency will be automatically executed by the platform. In this case users don't need to be confused by the use of digital currency. For users, there is no difference between using this platform and using Apple music or Spotify. <br>
To avoid the mistakes in code, the code writing process of smart contracts should be automatically completed by the computer. The platform only needs to provide some packaged APIs to users such as program developers, which will minimize the possibility of contract content errors. Besides, these APIs themselves must also have risk control functions and alert users as soon as a large amount of abnormal funds are found. 

### Rederence list
Alexander A. (2018, Jul 3). The Ujo platform: a decentralized music ecosystem. Medium. Retrieved from https://blog.ujomusic.com/the-ujo-platform-a-decentralized-music-ecosystem-e530c31b62bc <br>

Angel D. (2018, Jul 20). Can blockchain technology disrupt the music industry? Medium. Retrieved from https://medium.com/blockstreethq/to-which-extent-can-blockchain-technology-disrupt-the-music-industry-e6182fb5741a  <br>

Anne G. (2016) Insights from Ujo: The Challenges of Building on Ethereum. OFFERZEN. Retrieved from https://www.offerzen.com/blog/insights-from-ujo-the-challenges-of-building-on-ethereum <br>


DIGIMARC. (2017). Watermarking technology and blockchains in the music industry. Beaverton, Oregon : Bill Rosenblatt <br>

Preetam R. (2018, Aug 16). How blockchain can be used in the music industry beyond the hype. Medium. Retrieved from https://medium.com/quillhash/how-blockchain-can-be-used-in-the-music-industry-beyond-the-hype-339e1dbf18a7 <br>

Simon R. (2018, Dec 13). Introducing Ujo portal: making musicians more money. Medium. Retrieved from https://blog.ujomusic.com/introducing-ujo-portal-making-musicians-more-money-9224d808a57a <br>


Ujo (2019, Mar 28). Introducing streaming payments for Ujo with connext payment channels and dai. Medium. Retrieved from https://media.consensys.net/introducing-streaming-payments-for-ujo-with-connext-payment-channels-and-dai-16725929fe38 <br>


