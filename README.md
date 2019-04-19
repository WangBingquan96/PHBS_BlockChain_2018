# PHBS_BlockChain_2018
## The application of blockchain in music industry
![](https://github.com/WangBingquan96/PHBS_BlockChain_2018/blob/master/preface%20picture.gif)
### 1. Background information in music industry
The global music industry is a tremendous one. In 2017, the revenues from the industry were around 16 billion USD. In particular, approximately 176 million users of paid subscription services shaped this revenue stream. However, nowdays, the music industry, due to the centralized and mediated nature of production and distribution, suffers mainly through these following issues.<br>
(1)Piracy of digital records <br>
(2)Improper rights management <br>
(3)Cumbersome royalty management <br>
(4)Delay In rewards to artists. <br>
![](https://github.com/WangBingquan96/PHBS_BlockChain_2018/blob/master/pricture1.gif)  <br>
More specifically, A report suggests that for every $1,000 of music sold, the average musician gets a paltry $23.40 (just over 2%). To meet the US monthly minimum wage, musicians would need over 188,000 total plays on Apple Music (and even more on the competing platforms). Most of the revenues goes to the intermediaries like music streaming services inlcuding Spotify and Apple Music. They centralize the music industry and make it harder for independent musicians to become known and earn from their work. <br>
When the blockchain entered the public view, people started to think use blockchain in music industry for its decentralized, immutable and transparent characteristics. 
### 2. How music industry is operating 
First I will introduce how music industry is operating at present and what is the problem which can be solved using blockchain. There are several main participants in music industry including: <br>
(1)DSP( Any music streaming website) <br>
(2)Label (A record label or record company, is a brand or trademark associated with the marketing of music recordings and music videos.) <br> 
(3)Artist <br>
(4)Mechanical rights organizations (MROs) (Who handle mechanical royalties. The rights to copy and distribute are combined by music industry convention into one set of rights called mechanical rights.) <br>
(5)Performing rights organizations (PROs) (Who handle performance royalties.Performance means on a recording as well as before a live audience) <br>
(6)Users. <br>
![](https://github.com/WangBingquan96/PHBS_BlockChain_2018/blob/master/picture2.png)
The music service pays a royalty to a record label for each track that a user downloads or plays. The label passes mechanical royalties to the publishers of the underlying composition and pays to the recording artist. Royalty is also paid to PRO as streaming of music is count as performance of music composition under the case of streaming music. The creator of music is rewarded/paid according to number of plays of the song from content DSP website. <br>
The problem here is music label needs to trust on whatever data is provided by DSPs (For ex: Number of downloads of a music file) and music artist in turn needs to trust on the music label. 
### 3. How blockchain could be used to solve this problem
Because music file is too big to be saved in blockchain, people just create links between transactions of music on blockchain and the music files that are the subjects of the transactions. The links are called identifiers. By putting an identifier in each transaction record that matches an identifier in each music file the link could be created. The identifiers must satisfy four key requirements:<br> (1)robustness(the identifier remains associated with the file even after the file has been transformed in various ways, such as   transcoding, excerpting, pitch-shifting, re-equalizing, and digital-analog-digital conversion.) <br>
(2)data flexibility(the same audio data can exist in multiple files with different identifiers.) <br>
(3)identifier reliability (the identifier can reliably identify the recording in the file for rights and royalty management purpose) <br> 
(4)security (the identifier is difficult to remove or change without altering or marring the content) <br>
The identifiers could be hash of music files but a paper says that they are not robust ,flexible and secure. They can be changed by changing as little as a single bit of the audio data, and different versions of the same content (e.g., in diferent formats, codecs, or bitrates) <br> 
Watermarking is a good choice for identifiers. A digital audio watermark is a set of data embedded directly into audio in such a way as to be imperceptible to listeners. A well-designed watermarking scheme is robust to transformations such as transcoding, excerpting, digital-analog-digital conversion, and many types of signal processing. <br>
So the process will be whenever someone plays music through an interactive streaming service, the service could deposit a transaction on a blockchain so that all identifiers such as watermarking related to music files will be recorded on blockchain.<br>
![](https://github.com/WangBingquan96/PHBS_BlockChain_2018/blob/master/picture3.png)
(1) A label sends a music file, File X, to a DSP <br>
(2)File X has the file' s ID. ID X, embedded as a watermark. <br>
(3)One of the DSP' s users plays the track, and the DSP deposits a transaction on the blockchain containing ID X. <br>
The label also sends copies of the file with the embedded watermarks ID X  to two PROs (4 and 5) and an MRO (6).<br>
The label, PROs, and MRO can all query the blockchain, using the ID embedded in File X, to find transactions involving File X.
There are two such transactions in the figure: one is from the DSP in the figure (3), while the other (7) could have come from another DSP or another users.<br>
DSPs can deposit the transactions in real time, while the royalty processing organizations and also music artist can query the blockchain at them anytime to check. <br>
### 4. Several companies used block chain in music industry
![](https://github.com/WangBingquan96/PHBS_BlockChain_2018/blob/master/ujo%20picture.png)
(1)Ujo Music is a blockchain-powered beta music streaming and download platform. Artists sign up and publish their work, allowing listeners to discover and download albums using Ethereum. It allows for direct fan-to-artist purchase of music (and tipping). Full streaming of tracks is currently free, but the platform plans to introduce paid streaming in future. Listeners purchase albums and tip artists.<br>
![](https://github.com/WangBingquan96/PHBS_BlockChain_2018/blob/master/dot%20picture.png)
(2) The dotBlockchain Music Project (dotblockchainmusic.com) is a public benefit corporation which is creating open-source technology to support a new file format for music called .bc (dotBlockchain), which will contain digital audio along with metadata that points to entries in blockchains denoting music rights transactions. <br>
### 5.What's the drawbacks ?
(1) In order to use Ujo, one needs to utilize new software such as MetaMask or cryptocurrency wallets. Like any pioneering frontier, this can be scary and confusing.  What's worse, cryptocurrencies as most know them are volatile. For musicians that want to make a living, this volatility can be serious.<br>
(2) It means that mistakes in the code can easily end up losing the involved parties a lot of money when the smart contracts deal with funds. Having no way of altering the code means people have to think way ahead carefully. <br>
(3) These individual technologies are great, but they still create the issue of a fragmented music industry where artists and fans are forced to participate in a large collection of platforms in order to access the different music they want to hear. <br>
