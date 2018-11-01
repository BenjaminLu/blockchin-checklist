# Blockchain checklist

## 公私鑰演算法

SECP256K1或其他橢圓曲線或公私鑰系統

## glossary

鏈上的角色名詞

Validators, Block producers, Super Representatives?

## install environment

### pre-requisite

Java 8, Golang, Boost C++?

記憶體至少要8G?
硬碟要SSD? 200G?

### node installation

安裝指令為何?

apt install? wget再解壓縮?

## config privatenet, testnet or mainnet

設定創世區塊與區塊鏈指令

## genesis block

創世區塊設定細節
私有鏈設定預設有錢地址方式

## service ports

RPCs功能的port?
admin RPCs port?
節點同步的port?
websocket port?

## startup scripts

啟動腳本有特殊指令?

需要trap SIGTERM才能安全結束節點程式?

## syncing blocks

同步主鏈需要多久? 區塊鏈資料位置如何指定?

## shutdown nodes

如何安全的關閉節點?

## 節點資料備援 (backup blockchain data)

備援方式?
VM snapshot?
2次rsync完全同步作法?
單一節點異常zero downtime的切換作法?

# 開發社群相關軟體及文件

官方文件，社群文件連結

## blockchain explorer

主鏈與測試鏈的explorer

## testnet faucet

測試鏈水龍頭網址與使用方式

## peer management

手動加入新的鄰居節點方式

## address encoding

出金時交易所常會讓用戶自己填轉出地址
此時後台會有相關的地址驗證程式檢驗user輸入的資訊
故一個鏈的新舊版地址格式的認知也非常重要，會影響到用戶出金

## transaction types

出入金關心的交易種類有哪些?

## custom assets detection

若需要關心該鏈上的代幣資產該如何偵測?

## fee 出入金手續費拿捏

如何在交易速度與成本間拿捏?
是否有額外成本，Omni layer的reference amount, 0.00000546 BTC

## 個人帳戶連續送交易的問題，nonce的抓取(含mempool)與設定

如要啟用備用節點，如何處理個nonce與重發問題
(account based區塊鏈常見)

## Key Generation - 中心化交易所替用戶創地址

創建地址等待用戶申請，需要如何加密存放

## 偵測入金

需要考慮該鏈恰當的confirmation數

## get last block of your node

最新高度為何? 用來比較自家節點是否有跟上外部節點

## get block by a specific height

考慮confirmation數後應該取得的區塊資料

## get transaction

有最終性的區塊中交易資訊送方、收方資產種類與餘額變化

## 查詢餘額 get balance

確認交易所水位

## 用戶提幣出金 - 離線簽名

離線簽章的SDK或是演算法資訊

## token to coin migraiton 主網切換問題

ERC20轉換到主鏈的流程與作法

## 維運疑難雜症

節點不定時程式異常的錯誤與經驗學習

## references

上述所有資料的索引
