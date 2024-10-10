## 资产选择

我们将创建实现房地产细分权益化的代币。所选资产将会是一项现实世界的房产，而相关数据则是通过使用 Chainlink Functions 调用 API 来获取的。<br/>

我们的通证化资产将代表一个链下资产。至于创建具有抵押品支撑的通证，则超出了本次训练营的内容范围。

## 通证规范

创建的是 ERC-1155 标准的通证，这使得我们能够融合 ERC-20 通证同质化的优点来进行资产细分，同时又可通过统一资源标识符 URI 为代币集合赋予独特的属性，类似于 ERC-721 标准所提供的能力。
![通证规范](/static/TokenStandard.avif "通证规范")

## 区块链的选择

代币化资产将使用 CCIP 以实现在任意链上的可用性。我们将把 issuer 合约部署在 Avalanche Fuji 区块链上。这意味着初始发行将在 Avalanche Fuji 上进行，但随后该通证可通过 Chainlink CCIP 转移到与 Avalanche Fuji 相连的任何其他区块链上。

## 链下数据获取

为了创建一个与现实世界资产关联并反映其价值的链上资产，我们需要将区块链与现实世界进行连接。为实现这一目标，我们将使用 Chainlink Functions 和 Automation 服务。 Functions 将使我们能够从 Zillow API 上读取数据，而 Automation 将自动化这一调用过程实现数据每日更新。
![链下数据获取](/static/DataFetch.webp "链下数据获取")

## 运用工厂模式发行 ERC-1155 通证

![架构图](/static/Architecture.avif "架构图")
