# 零知識證明-走進PLONK世界
# Day01
https://ithelp.ithome.com.tw/articles/10351538

在進入PLONK世界之前，先向大家簡單講解一下什麼是零知識證明。

零知識證明 (Zero-knowledge proof, 簡稱為ZKP) 是一種密碼學技術，它可以在不透露資料本身或任何額外資料(例如敏感的數據內容)的情況下驗證某數字資料的真實性。在Web3的領域中，零知識證明在結構區塊鏈技術之下，能夠進一步提升保護個人私隱的能力及解決當下存在的數字安全問題。 

大家為了獲得互聯網帶來的便利，在日常生活中都會利用互聯網來進行各種動作、交易、社交等等，在過程中難免需要透露個人的私隱數據。例如在平台購物時要輸入信用卡號碼以進行交易，進行身份認證時就可能需要提交身份證明文件等。然而，在工作中都有機會需要處理各種公司或客戶的私隱數據，需要嘍其他同事分享某些私隱數據的資訊。但究竟是不是必須要用上一些私隱數據呢? 其實有很多情況是不需要用上私隱數據，例如參加一個線上語言培訓班，是不需要你的個人住址、也不需要知道你的性別等，因為都不會影響到整個教學，相關個人資訊也是用不上的。

零知識證明 (ZKP) 是在 1985 年由 Shafi Goldwasser、Silvio Micali、Chales Rackoff 合著的論文《The knowledge complexity of interactive proof systems》首次提出的數學協議，除了某一要證明的事實之外，不會透露任何其他信息。驗證者無法獲得生成證明的秘密信息。

零知識證明的原理
在零知識證明架構中，會存在兩個角色包括證明方及驗證方，證明方可以在無須透露任何額外資訊下，向驗證方證明一個陳述是真的。在這情況下，證明方可以不用提供一些敏感的資訊而向驗證方提供證明，因為驗證方可以在不獲得證明方的敏感資訊之下完成一個驗證。

證明方只需要提供一個只有他能夠生成的證明，然後發送給驗證方，驗證方則用收到的證明來驗證指定的陳述真偽。在整個過程中，驗證方不能透過收到的證明來獲得證明中的內容，換言之，是沒有人能夠對證明進行解密。

給大家一個例子說明，假設有一條路，起點是在路牌A 而終點是路牌B。在路中間有一道唯一的密碼門，需要輸入正確的密碼才能通過，要怎樣在一個不透露密碼的情況之下向其他人證明你是有密碼門的密碼? 最簡單就是在終點的路牌B拍一張照片。當然是還有其他方式去證明，所以要是我們能夠用一個可以保障到自己私隱或利益的情況之下進行某些證明，的確是能夠進一步減低安全風險。

參考資料:
1. The knowledge complexity of interactive proof systems
* https://people.csail.mit.edu/silvio/Selected%20Scientific%20Papers/Proof%20Systems/The_Knowledge_Complexity_Of_Interactive_Proof_Systems.pdf

2. Zero Knowledge Canon, part 1 & 2
* https://a16zcrypto.com/posts/article/zero-knowledge-canon/

# Day02
https://ithelp.ithome.com.tw/articles/10351713

在Day1講解了零知識證明的基礎，今天會講解
- 零知識證明的特性及
- 為什麼要使用零知識證明
- 零知識證明的應用

1. 當中提及到的例子也展示了它應該要具備的三個特性:
完整性(complete)、可靠性(sound)、零知識性(zero-knowledge)

- 完整性(complete):
如果陳述是真的，驗證方只需要正確地遵守協議完成驗證就可以。最後會得出證明該是否真。
在例子中如果證明方提供的證明是正確的，在證明方完成所有測試(多輪測試)後。
只要提供的證明只要是正確，驗證方獲得結果會是真。

- 可靠性(sound): 
如果陳述是假的，就不會有任何證明方能夠讓驗證方通過這個陳述。
在例子中如果證明方提供的證明不是正確的，是無法通過驗證方的驗證。
為了提高可靠性，在過程中就可能需要證明方進行多次測試，目的是為了確保證明方是真的知道陳述。

- 零知識(zero-knowledge):
在整過驗證過程中，除了陳述之外，驗證方是不會得知道其他資訊。
因為驗證方只能道驗證結果的真偽，而不會知道其他資訊(例如例子中證明方所擁有的密碼或相關個人資料等等 )。
其實可以理解為驗證方的存在目的，只有一個，就是進行驗證。只要對證明進行驗證及得出結果就可以，
完全不用去檢視其他資料。

2. 為什麼要使用零知識證明？ 
零知識證明在web3領域中越來越受到關注及應用，主要是隨時代發展，數字化的應用越來越廣泛。基本上大家每天都會用到手機或電腦等，都需要用上互聯網，需要用到各種應用程式。大家都開始意識到數字資料的安全性及對保護敏感資訊的意識開始提高，就開始尋找一些解決方案，希望可以進一步地保護敏感資訊。
由於零知識證明的出現已經引起了很多關注和研究，最近幾年在零知識證明也出現各種的新型算法和應用方案。

3. 零知識證明的應用
零知識領域可分為基礎設施、網路和應用程式三層
- 基礎設施: 
包括用於開發協議或應用程式的軟件或硬件裝置，例如編程框架、零知識證明處理器、零知識證明網路和硬體加速等。這些基礎設施為開發者提供了開發零知識證明應用的工具。
- 網路:
利用零知識證明技術的L1/L2協議，包括ZK-EVM和ZK-Rollup等。
- 應用程式:
利用零知識證明技術的產品，包括私密支付、各種身份驗證、交易等。
![alt text](https://miro.medium.com/v2/resize:fit:1100/format:webp/0*71IZTzpQm3HPNzX-?raw=true)

4. 零知識證明的應用案例
* Zcash
Zcash是最早採用到零知識證明技術的區塊鏈項目，他們使用zk-SNARK(Zero-Knowledge Succinct Non-Interactive argument of Knowledge)來驗證交易是合法正確的，同一時間又可以不用向驗證者透露交易雙方的背景、交易內容或其他敏感的資訊，只要能夠驗證到證明是否正確就可以。因此整個交易流程可以做到匿名交易的效果。
Zcash 的目的是想加強經濟自由的加密貨幣。它的設計與比特幣差不多，但它使用私隱技術來加密交易相關的資訊令到用戶可以進一步地保護自己的個人私隱和資產。 
2016年Zcash 的出現讓到大家可以體驗到真正在整個交易中能夠隱藏匯款人、收款人及進行交易的金額的加密貨幣種類，這種應用是運用 zk-SNARKs技術將可以被其他人查詢的資訊隱藏，實現進一步保障用戶的個人私隱，零知識證明就能讓區塊鏈上的加密貨幣及交易雙方的資訊也能具有私隱權，可以進行隱藏，保障私穩。 

參考資料:
1. Zero-knowledge proofs | ethereum.org
* https://ethereum.org/en/zero-knowledge-proofs/ 
2. Understanding the Zero-Knowledge Landscape
* https://www.coinbase.com/blog/understanding-the-zero-knowledge-landscape
3. Zcash 官網
* https://z.cash/learn/what-is-zcash/


# Day03
https://ithelp.ithome.com.tw/articles/10351893

## 零知識證明 (ZKP) 是如何工作?
零知識證明結構分為交互式和非交互式兩大類別:
1. 交互式零知識證明(Interactive Zero Knowledge Proof (iZKP))
交互式零知識證明需要證明者和驗證者之間進行至少一次交互，以確保零知識證明正確進行。
在交互式零知識證明中，證明者和驗證者會進行一次或多次交互，過程中需要交換訊息來證明證明者擁有相關知識。
當中最常用的是Fiat-Shamir heuristic，驗證者會產生一個隨機值然後用於對證明者的挑戰。
證明者在接收到驗證者的挑戰後，必須使用他所擁有或知道的秘密知識來產生一個對挑戰的回應(需要進行一項計算，然後返回結果)，然後驗證者在收到證明者的回應之後，可以驗證那個回應是否正確。如果回應正確，驗證者會接受證明(確認回應是真的)及確認這次交互完成。

交互式零知識證明的其一個主要優勢是它們的高度靈活，可用於證明許多不同類型的資訊知識。
例如，它可用於證明某人知道秘密值(例如:大門密碼/軟件密碼)，
或證明他們對數字資產(例如: 加密貨幣/知識產權/數據)具有一定程度的權限或擁有權。

交互式零知識證明的另一個優點是它十分安全。
因為隨機挑戰中的使用及證明者和驗證者之間交互的方式可以使到造假風險大大降低。

不過交互式零知識證明也有存在一些缺點。
主要缺點是它需要證明者和驗證者之間高度信任。
如果任何一方受到損害或入侵，證明的安全性就會受到影響。
另外，執行交互式零知識證明的過程可以會非常花費時間，因為需要證明者和驗證者之間進行交互，
而且更需要大量的運算資源(算力)，從而對應用普及上造成一些局限。

這個交互過程需要重復多次進行，目的是確保證明者在不知道秘密信息的情況下而又猜出正確答案的概率變得足夠低。

2. 非交互式零知識證明(Non-Interactive Zero Knowledge Proof (niZKP))
非交互式零知識證明是不需要證明者和驗證者之間互動的ZKP。
相反，證明者創建一個可以由驗證者驗證而無需任何交互的證明就可以，之後就給驗證者去做驗證。

最常見的非交互式零知識證明之一是 SNARK (Succinct Non-Interactive Argument of Knowledge)。
SNARK使用高階的數學演算法來創建可由驗證者無需任何交互即可驗證的證明。
證明通常是產生要證明是資訊簡短的、高度壓縮的，驗證者會驗證該證明是否有效。

非交互式零知識證明的主要優點是它們比交互式零知識證明更有效率且可擴展。
由於證明者和驗證者之間沒有交互，因此可以更快地驗證，而且可以使用更少的計算資源。

不過，非交互式零知識證明也存在缺點，其中一個主要缺點是它們不如交互式零知識證明靈活，
並且只能用於證明某些類型資訊的知識。

交互式和非交互式的確各有其優缺點。交互式零知識證明高度靈活且安全，但可能非常耗時，並且需要相關各方之間高度信任。
非交互式的更有效率及可擴展，但靈活性可能較差。

## 非交互式零知識證明
在當下生態中﹐比較多人關注/使用的零知識證明系統有以下3類，
分別有 ZK-SNARK、ZK-STARK、Recursive SNARK(遞歸SNARK)。

什麼是 ZK-SNARK？
ZK-SNARK (全稱 Zero-Knowledge Succinct Non-Interactive Argument of Knowledge)，是一種用於產生零知識證明的協議，
在不暴露底層資料的情況下驗證資訊的真實性。  
ZK-SNARK 協議主要有兩個角色：證明者和驗證者。

證明者（Alice）是提出主張的一方，而驗證者（Bob）則是負責驗證主張的一方。 
而主張會被稱為witness(證人)或者secret(秘密)。
證明者（Alice）使用 ZK-SNARK 機制產生證明，然後會向驗證者（Bob）表示該聲明是真的，但又不用透露引用的資訊。
以下會以一個例子說明:
1. 驗證使用者身分:
個人可以在不透露個人資訊(例如護照/身份證號碼)的情況下證明自己是某個地方的合法居民。 

ZK-SNARK具有以下特質:
1. 零知識：驗證者只需驗證一個陳述的真實性，可以不用理會其他資訊，因為對驗證沒有幫助。 
2. 簡潔：只要證明的大小足夠小，驗證者就不用花費大量時間去進行驗證。 
3. 非交互式：證明者和驗證者不需要進行交換當下證明以外的資訊，從而改善到效率問題。
4. 論證：SNARK 是一種"計算可靠"的陳述，只要滿足嚴格的要求，是很難會出現作弊的情況。 
5. 知識：無法透過存取底層資訊或witness(證人)來創建同樣的SNARK證明。

ZK-SNARK有什麼優點?
高吞吐量、小有效性證明大小和安全性。

1. 高吞吐量
例子:
* ZK-SNARK 透過縮小以太坊基礎層的運算量來擴展吞吐量。利用ZK-SNARK，"roolups"可以將 TPS 率提高到數千個單位。 
* ZK-SNARK 通常比它驗證的交易資料小很多倍。這樣可以減少區塊鏈的擁堵，及實現更便宜的gas fee和更快速的交易時間。 

2. 數據小的證明
SNARK證明的數據小就可以易於在主鏈上進行驗證。
例子:
在以太坊上，驗證鏈下交易的gas fee較低，用戶的總和成本也因此降低。 

3. 安全性 
ZK-SNARK 中使用了尖端的加密安全機制。 
另外，ZK-SNARK 證明具"計算可靠"的特性，所以可以進一步讓惡意行為更難實現。
ZK-SNARK 的非互動性也意味著任何人都可以不可信地驗證證明。

ZK-SNARK 的有什麼缺點？
使用 ZK-SNARK 有三個主要缺點：它需要可信任設定、容易受到量子運算攻擊以及依賴特殊硬體。

1. 可信任的環境設置
設定 ZK-SNARK 協議時，需要建立通用公共參考字串 (Common Reference String: CRS)。 
CRS 也被稱為公共參數，可實現證明者和驗證者之間的安全溝通。 
如果惡意行為者獲得到公共參數，他們有機會產生虛假的有效性證明。
有些項目試圖利用多方計算(MPC)來產生公共參數以解決這個問題。 
不過這種方法要求使用者必須信任相關人員的誠信。這就會形成一個矛盾的問題，因為區塊鏈的出現是想做到去中心化，減低信任的依賴。 

2. 容易受到量子計算攻擊
ZK-SNARK利用橢圓曲線密碼技術(ECC)來加密會用於產生有效性證明的資訊。
ECC目前是安全可靠的，不過隨量子計算的發展，將會有可能破壞到ECC的安全機制。 

3. 對指定硬體的依賴 
利用ZK-SNARK產生有效性證明是一個密集型的計算過程，因此證明者必須使用到有足夠算力的硬體以支持計算過程。
當然要使用到怎樣的硬件是取決於項目對ZK-SNARK產生有效性證明的要求是怎樣及其他相關要求標準。

什麼是 ZK-STARK？
ZK-STARK (Zero-Knowledge Scalable Transparent Argument of Knowledge)。
是一種零知識證明系統，由 Eli Ben-Sasson、Iddo Bentov、Yinon Horesh 和 Michael Riabzev 
在 2018 年的論文中作為 SNARK 的替代方案引入。
如論文中所述，STARK 可以為當下的社會帶來好處：
「"人類的尊嚴(Human dignity)"要求向公眾隱藏用戶的個人訊息，例如醫療和法醫方面的數據。
但在保護私隱的事件上也可能被負責處理資料的機構濫用來掩蓋謊言和欺騙，不公正地傷害大眾及削弱對政府機構的信任。
零知識證明技術是一種巧妙的密碼學解決方案，可以解決個人私隱與機構誠信之間的緊張關係，
以不損害前者的形式強制地讓後者實施相關方案。」

像 ZK-SNARK 一樣，可以展示一個有效的陳述而不透露陳述本身的任何內容。 
STARK 與 SNARK 是具有相同的屬性。所以STARK-based的有效性證明是能夠使用一條對驗證者隱藏的資訊產生，
同樣可以在不洩漏輸入的情況之下，驗證交易的正確性。

ZK-STARK有什麼優點?
1. 具透明的(transparency):
因為它可以在沒有公共參考字符串(Common Reference String: CRS)的可信設置的情況下執行。

2. 是可擴展的(scalability):
STARK具有更大的證明大小，會更適合在更大型的計算。使用ZK-SNARK的話，證明和驗證的複雜性規模與底層計算會是線性關係。

3. 不用可信任的環境設定
ZK-STARK 不需要可信任的環境設定就可以立馬運行，而是依賴公共的隨機性。
因此這樣減少了用戶的信任假設，及提高了基於STARK的協議的安全性。

4. 更高的安全保護
ZK-STARK 使用抗碰撞雜湊進行加密，而不是 ZK-SNARK 中使用的橢圓曲線方案。
這被認為可以抵抗量子計算的攻擊，因此比 SNARK 中使用的橢圓曲線更安全。

在驗證一個需要計算量更大的情況下，ZK-SNARK協議需要比ZK-STARK需要更多的時間來生成證明和驗證證明。
因此STARK會更適合處理大量交易的應用場景。

ZK-STARK 的缺點是什麼？
使用ZK-STARK的兩個主要缺點是它使用更大的證明大小，及在區塊鏈空間中採用情況較少。

1. 更大的證明大小
雖然STARK提供了更快速的證明計算，不過其缺點是這些證明與基於SNARK的證明大小相比會更大。
這讓STARK證明在以太坊(區塊鏈上的數據大小會影響到成本)上的驗證成本更高，
因為計算更大的證明是需要更高的gas fee。

2. 採用率較低
SNARK是零知識技術在區塊鏈中的第一個實際應用，這就是為什麼它們比STARK擁有更多的市場佔有率。
在現在的生態，大多數ZK rollups都使用ZK-SNARK。

儘管ZK-STARK也有一些知名/大型組織的支持者，包括以太坊基金會，但他們的採用率較低。
因此，行業中的開發人員會發現使用STARK開發零知識證明項目的支持和工具也相關較少。
從而可想而知，要是想開發STARK項目，就會投放更多時間和資源。

什麼是遞歸ZK-SNARK？
遞歸SNARK(Recursive SNARK)可以為每一層計算或遞歸產生一個證明，然後將這些證明遞歸地組合成一個以產生整個計算的證明。這表示一個SNARK可以驗證其他SNARK。
這更可以有效地去驗證涉及大量遞歸的計算，例如涉及 Merkle 樹、graph computations和區塊鏈的計算。

遞歸ZK-SNARK是如何運作?
證明的遞歸組合會有以下三個步驟:
1. 證明每一層或層級(level)的計算的正確性。
2. 以遞歸地組合SNARK來產生整個計算的證明。
3. 利用驗證演算法去驗證證明。例如：Groth16、BCTV14、Pinocchio、PLONK、Aurora）
SNARK 的遞歸組合可以以不同方式完成，例如通過使用遞歸證明（例如 Marlin、Sonic、Fractal、Hyrax）。

遞歸ZK-SNARK有什麼優點？
1. 遞歸ZK-SNARK通過將多個L2(區塊鏈)證明整合在一起，然後向L1鏈(區塊鏈)提交單個證明，
這樣可以極大地增加了可以用零知識證明完成的交易數量。

總結，可以留意到ZK-SNARK、ZK-STARK、Recursive SNARK(遞歸SNARK)各有分別，然而在每個類型之下也有不同產品，可以因應不同的需求及場景選用合適的方案。

參考資料:
1. Scalable, transparent, and post-quantum secure computational integrity
https://eprint.iacr.org/2018/046
2. From Extractable Collision Resistance to Succinct Non-Interactive Arguments of Knowledge, and Back Again
https://eprint.iacr.org/2011/443.pdf
3. SNARKs vs. STARKS vs. Recursive SNARKs
https://www.alchemy.com/overviews/snarks-vs-starks
4. Nova: Recursive Zero-Knowledge Arguments from Folding Schemes
https://eprint.iacr.org/2021/370.pdf
5. Recursion and Cycles
https://cs.brown.edu/courses/cs173/2012/book/recursion.html
6. On Valiant’s Conjecture: Impossibility of Incrementally Verifiable Computation from Random Oracles
https://eprint.iacr.org/2022/542.pdf
7. Zilch: A Framework for Deploying Transparent Zero-Knowledge Proofs
https://ieeexplore.ieee.org/document/9410618
8. The Knowledge Complexity of Interactive Proof-Systems
https://people.csail.mit.edu/silvio/Selected%20Scientific%20Papers/Proof%20Systems/The_Knowledge_Complexity_Of_Interactive_Proof_Systems.pdf
9. Decentralized Speed: Advances in Zero Knowledge Proofs
https://a16zcrypto.com/posts/article/decentralized-speed-advances-in-zero-knowledge-proofs/
