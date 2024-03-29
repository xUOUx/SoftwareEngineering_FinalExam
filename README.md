# 計算機畢業設計SSM員工宿舍管理系統
11024241陳俊佑 
11024232林政彥

## 環境配置：
`Jdk1.8 + Tomcat7.0 + Mysql + HBuilderX（Webstorm也行）+ Eclispe（IntelliJ IDEA,Eclispe,MyEclispe,Sts都支援）。`

## 項目技術：
`SSM + mybatis + Maven + Vue 等等組成，B/S模式 + Maven管理等等。`

## 環境需要
`1.運行環境：最好是java jdk 1.8，我們在這個平台上運行的。其他版本理論上也可以。 2.IDE環境：IDEA，Eclipse,Myeclipse都可以。推薦IDEA; 3.tomcat環境：Tomcat 7.x,8.x,9.x版本均可 4.硬件環境：windows 7/8/10 1G內存以上；或 Mac OS； 5.是否Maven項目: 否；查看源碼目錄中是否包含pom.xml；若包含，則為maven項目，否則為非maven項目 6.數據庫：MySql 5.7/8.0等版本均可；`

## 系統功能
`通過前面的功能分析可以將員工宿舍管理系統的功能分為管理者、員工和維修員三個部分，系統的主要功能包括首頁、個人中心、員工管理、維修員管理、宿舍信息管理、床位信息管理、宿舍衛生管理、員工入住管理、報修信息管理、分配任務管理、維修反饋管理、繳費中心管理、繳費記錄管理等內容。任何用戶只要進入網站不需登入也可瀏覽到的信息，後台管理是針對已登入的用戶看到滿意的員工宿舍信息而設計的。`

## 一般用戶的功能及權限
`所謂一般用戶就是指還沒有註冊的過客,他們可以瀏覽主頁上的信息。但如果要進入後台進行信息管理時，要登入註冊，只有註冊成功才有的權限。`

## 管理員的功能及權限
`用戶信息的添加和管理，員工宿舍詳細信息添加和管理和文檔信息添加和管理以及網站信息管理，這些都是管理員的功能。`

## 系統功能結構圖
`系統功能結構圖是系統設計階段，系統功能結構圖只是這個階段一個基礎，整個系統的架構決定了系統的整體模式，是系統的根據。員工宿舍管理系統的整個設計架構如圖1所示。`

![圖1](https://img-blog.csdnimg.cn/e6738054ec8a4cf9822e44afe1350d25.png)

## 可行性研究
`通過對系統研究目標及內容的分析審查後，提出可行性方案，並對其進行論述。主要從技術可行性出發，再進一步分析經濟可行性和操作可行性等方面。`

## 經濟可行性
`開發系統所涉及到的資料，一般是在圖書館查閱，或是在網上進行查找收集。所需要的一些應用軟件也都是在網上可以免費下載的，因此，開發成本幾乎為零。但是開發出來的系統，還是具有高效率，低成本，較高質量的。所以，從經濟可行性的角度，該系統符合標準。`

## 技術可行性
`技術可行性是考慮在現有的技術條件下，能否順利完成開發任務。以及判斷現有的軟硬件配置是否能滿足開發的需求。而本系統採用的是java技術開發，並非十分困難，所以在技術上是絕對可行的。此外，計算機硬件配置是完全符合發展的需求。`

## 運行可行性
`當前計算機信息化的知識已經十分普及了，現在的操作人員也都是對系統環境有很強的適應性，各類操作人員大都是有過培訓補充的，因此完全不影響組織結構，所以在運行上也是可行的。`

## 時間可行性
`從時間上看，在大四的最後一個學期，在實習工作與完成畢設兩件大事相交叉的時間裡，結合之前學習的相關知識，並開發系統，時間上是有點緊，但是也不是完全沒可能實現，通過這段時間的努力功能基本實現。`

## 系統業務過程分析
`員工宿舍管理系統是三種身份的用戶，主要涉及管理員、維修員和員工。每個身份都是操作起來都是清楚方便的。對於一些員工信息，這是任何人都可以查看的，但是如果用戶想進入後台進行操作，則必須是已經進行登錄的用戶，或者想修改員工宿舍信息的話，也是需要用戶登錄狀態。這些用戶的基本信息都由管理員對其統一管理。`

`根據員工宿舍實際過程的分析，網站有以下幾個部分，其中用戶註冊，發布個人信息，修改個人信息；用戶註冊登錄，發布員工宿舍信息；管理員管理用戶信息；一般用戶只可以瀏覽不可以發布信息。以上業務過程從用戶角度可以分為三類 使用本系統的用戶角色，包括管理員、員工和維修員。以下針對各類用戶說明相應的業務過程。`

## 系統用例圖
`系統用例圖如下圖2所示:`

![圖2](https://img-blog.csdnimg.cn/8e0eb55e295d4caead126457d21c2030.png)

## 系統設計
`數據庫設計
信息管理系統的效率和實現的效果完全取決於數據庫結構設計的好壞。為了保證數據完整性，提高數據庫存儲的效率，那麼統一合理地設計數據庫結構是必要的。數據庫設計一般包括如下幾個步驟:`

### 1.根據用戶需求，確定數據庫信息進行保存
`對用戶的需求分析是數據庫設計的第一階段，用戶的需求調研，熟悉小區運作流程，系統要求，這些都是以概念模型為基礎的。`

### 2.設計數據的概念模型
`概念模型與數據建模用戶的觀點一致，用於信息世界的建模工具。通過E-R圖可以清楚地描述系統涉及到的實體之間的相互關係。`
`員工註冊實體圖如圖3所示:`
`宿舍衛生管理實體圖如圖4所示:`

![圖3](https://img-blog.csdnimg.cn/abff1f553ddb4927aa1961c88714bdd5.png)
![圖4](https://img-blog.csdnimg.cn/a03da6d8aa49473b82fc0ab318c19037.png)

## 登錄註冊模塊
`員工宿舍管理系統，管理員、員工和維修員通過填寫用戶名、密碼等信息選擇角色進行登錄就可以使用了，如圖5所示。`

![圖5](https://img-blog.csdnimg.cn/af4d447be1db43e38c3d1c8a02919264.png)

`員工註冊，在員工註冊頁面通過填寫員工帳號、員工姓名、密碼、確認密碼、手機號碼、郵箱等信息完成員工註冊、如圖6所示。`
![圖6](https://img-blog.csdnimg.cn/38d78036b13d4fb3a33e9ab0945f9767.png)

`維修員註冊，通過填寫維修員帳號、維修員帳號、密碼、卻仁密碼、聯繫方式、郵箱等內容進行註冊等操作，如圖7所示。`
![圖7](https://img-blog.csdnimg.cn/173333822da743bc8319841ef78ef024.png)

## 管理員功能模塊
`管理員登錄系統後，可以對首頁、個人中心、員工管理、維修員管理、宿舍信息管理、床位信息管理、宿舍衛生管理、員工入住管理、報修信息管理、分配任務管理、維修反饋管理、繳費中心管理、繳費紀錄管理等內容進行詳細操作，如圖8所示。`
![圖8](https://img-blog.csdnimg.cn/e81edb8d415c47feb1016ba7f61ba175.png)

`員工管理，在員工管理頁面中可以對索引、員工帳號、員工姓名、手機號碼、頭像、性別、郵箱、審核回復、審查狀態、審核等內容進行詳情、修改或刪除等操作，如圖9所示。`
![圖9](https://img-blog.csdnimg.cn/df9d00eea906402ca73d097f18cd7ddc.png)

`維修員管理，在維修員管理頁面中可以對索引、維修員帳號、維修員姓名、聯繫號碼、頭像、性別、郵箱、審核回復、審查狀態、審核等內容進行詳情、修改或刪除等操作，如圖10所示。`
![圖10](https://img-blog.csdnimg.cn/8b6a95f70d654cfba06bf7de896d39f0.png)

`宿舍信息管理，在宿舍信息管理頁面可以對索引、宿舍名稱、位置、床位數、狀態等內容進行發布、宿舍衛生修改或刪除等操作，如圖11所示。`
![圖11](https://img-blog.csdnimg.cn/b086d312916e41a88e07cc21bad1c7a5.png)

`床位信息管理，在床位信息管理頁面可以對索引、宿舍名稱、位置、床位數等內容進行詳情、員工入住、修改或刪除等操作，如圖12所示。`
![圖12](https://img-blog.csdnimg.cn/de81d106855e4a67bbfebdc951da3c51.png)

`宿舍衛生管理，在宿舍衛生管理頁面可以對索引、宿舍名稱、位置、是否消毒、消毒時間、時間等內容進行詳情、修改或刪除等操作，如圖13所示。`
![圖13](https://img-blog.csdnimg.cn/456ea7cd2e5f4c3493b9e4213d1b2f9f.png)

`員工入住管理，在員工入住管理頁面可以對索引、宿舍名稱、位置、床位數、員工帳號、員工姓名等內容進行詳情、修改或刪除等操作，如圖14所示。`
![圖14](https://img-blog.csdnimg.cn/06f71d78b62746ff9ff36e162bf7e123.png)

`報修信息管理，在報修信息管理頁面可以對索引、宿舍名稱、位置、報修名稱、員工帳號、員工姓名，上報日期、審核回復、審核狀態，審核等內容進行詳情、分配任務、修改或刪除等操作，如圖15所示。`
![圖15](https://img-blog.csdnimg.cn/de891f347b59419fba8f0f377a7bb7b6.png)

`分配任務管理，在分配任務管理頁面可以對索引、宿舍名稱、位置、報修名稱、員工帳號、員工姓名，上報日期、維修員帳號、維修員姓名、分配時間等內容進行詳情、修改或刪除等操作，如圖16所示。`
![圖16](https://img-blog.csdnimg.cn/0061530335314f63974dc57c6d8539ea.png)


參考資料:
https://blog.csdn.net/bishe401/article/details/127224532#comments_30413275
