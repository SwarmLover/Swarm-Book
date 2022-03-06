<!-- [_The Book of Swarm_](/reference/The-Book-of-Swarm.pdf) 中文翻译项目，中文名《Swarm之书》。 -->


# 目录导航

## 前言 PROLEGOMENA
- [前言](/part-0/prolegomena.md)

## 致谢 ACKNOWLEDGMENTS
- [致谢](/part-0/acknowledgements.md)

## 第一部分-序言 PRELUDE

- 1-演进历史 THE EVOLUTION
  - 1.1-历史进程 historical context
    - 1.1.1-Web1.0
    - 1.1.2-Web2.0
    - 1.1.3-点对点网络 Peer-to-peer networks
    - 1.1.4-BitTorrent经济以及它的局限 The economics of BitTorrent and its limits
    - 1.1.5-奔赴Web 3.0 Towards Web 3.0
  - 1.2-公平数据经济 fair data economy
    - 1.2.1-当下的数据经济 The current state of the data economy
    - 1.2.2-当前的状况和数据主权问题 The current state and issues of data sovereignty
    - 1.2.3-奔赴主权数据 Towards self-sovereign data
    - 1.2.4-人工智能于主权数据Artificial intelligence and self-sovereign data
    - 1.2.5-集体信息 Collective information
  - 1.3-视角 the vision
    - 1.3.1-价值 Values
    - 1.3.2-设计原则 Design principles
    - 1.3.3-目标 Objectives
    - 1.3.4-影响区域 Impact areas
    - 1.3.5-未来 The future

## 第二部分-设计与架构 DESIGN AND ARCHITECTURE

- [2-网络 NETWORK](/part-2-design-and-architecture/design-and-architecture.md)
  - 2.1-拓扑与路由 topology and routing
    - 2.1.1-underlay网络的依赖 Requirements for underlay network
    - 2.1.2-Overlay地址 Overlay addressing
    - 2.1.3-Kademlia路由 Kademlia routing
    - 2.1.4-启动和维护Kademlia拓扑 Bootstrapping and maintaining Kademlia topology
  - 2.2-swarm存储 swarm storage
    - 2.2.1-分布式不可重入的块存储 Distributed immutable store for chunks
    - 2.2.2-内容寻址块 Content addressed chunks
    - 2.2.3-单拥有者块 Single-owner chunks
    - 2.2.4-块加密Chunk encryption
    - 2.2.5-副本冗余 Redundancy by replication
  - 2.3-推与拉：块检索和同步 push and pull: chunk retrieval and syncing
    - 2.3.1-检索 Retrieval
    - 2.3.2-推同步 Push syncing
    - 2.3.3-拉同步 Pull syncing
    - 2.3.4-轻量节点 Light nodes
- 3-激励 INCENTIVES
  - 3.1-共享带宽 sharing bandwidth
    - 3.1.1-供应雨中继的激励 Incentives for serving and relaying
    - 3.1.2-数据块检索的价格协议 Pricing protocol for chunk retrieval
    - 3.1.3-激励推同步 Incentivising push-syncing
  - 3.2-交换：账单与支付 swap: accounting and settlement
    - 3.2.1-点对点账单 Peer to peer accounting
    - 3.2.2-链下用于承诺支付的支票 Cheques as off-chain commitments to pay
    - 3.2.3-豁免 Waivers
    - 3.2.4-结算的尽全力策略 Best effort settlement strategy
    - 3.2.5-Zero cash entry
    - 3.2.6-Cashing out and risk of insolvency
    - 3.2.7-Sanctions and blacklisting
  - 3.3-存储激励 storage incentives
    - 3.3.1-用邮票做防作假保护Spam protection with postage stamps
    - 3.3.2-邮票彩票：对存储的正面激励 Postage lottery: positive incentives for storage
    - 3.3.3-Price signalling capacity pressure
    - 3.3.4-保险：反面激励 Insurance: negative incentives
  - 3.4-总结summary
- 4-高级功能 HIGH-LEVEL FUNCTIONALITY
  - 4.1-数据结构 data structures
    - 4.1.1-文件与swarm哈希 Files and the Swarm hash
    - 4.1.2-采集与清单 Collections and manifests
    - 4.1.3-基于URL的寻址和名字决议 URL-based addressing and name resolution
    - 4.1.4-maps和健值存储 Maps and key–value stores
  - 4.2-访问控制 access control
    - 4.2.1-加密 Encryption
    - 4.2.2-访问管理 Managing access
    - 4.2.3-多路径直达内容 Selective access to multiple parties
    - 4.2.4-访问等级制 Access hierarchy
  - 4.3-Swarm订阅和可重入的资源更新 swarm feeds and mutable resource updates
    - 4.3.1-订阅块 Feed chunks
    - 4.3.2-检索模式 Indexing schemes
    - 4.3.3-诚实 Integrity
    - 4.3.4-基于阶段的检索 Epoch-based indexing
    - 4.3.5-实时数据交换 Real-time data exchange
  - 4.4-PSS：用邮件盒子做信息直接推送 pss: direct push messaging with mailboxing
    - 4.4.1- 特洛伊块 Trojan chunks
    - 4.4.2-key交换的初次联系 Initial contact for key exchange
    - 4.4.3-信封殉职 Addressed envelopes
    - 4.4.4-请求通知 Notification requests
- 5-PERSISTENCE 可持续性
  - 5.1-冗余，延迟，修复 redundancy, latency and repair
    - 5.1.1-错误修正码 Error correcting codes
    - 5.1.2-通过擦除码实现冗余 Redundancy by erasure codes
    - 5.1.3-在swarm块树中各级别的擦除码 Per-level erasure coding in the Swarm chunk tree
  - 5.2-固定，重新上传，块丢失通知，pinning, reupload and missing chunk notifications
    - 5.2.1-本地固定 Local pinning
    - 5.2.2-全局固定 Global pinning
    - 5.2.3-恢复 Recovery
  - 5.3-保险 insurance
    - 5.3.1-保险池 Insurance pool
    - 5.3.2-为一个块购买保险 Buying insurance on a chunk
    - 5.3.3-用保险上传 Uploading with insurance
    - 5.3.4-访问收据 Accessing receipts
- 6-User experience 用户经验
  - 6.1-配置和追踪上传 configuring and tracking uploads
    - 6.1.1-上传选项 Upload options
    - 6.1.2-上传标签和进度条 Upload tags and progress bar
    - 6.1.3-邮票 Postage
    - 6.1.4-额外的上传特性 Additional upload features
  - 6.2-存储
    - 6.2.1-上传文件 Uploading files
    - 6.2.2-收集和清单 Collections and manifests
    - 6.2.3-访问控制 Access control
    - 6.2.4-下载 Download
  - 6.3-通信 communication
    - 6.3.1-订阅 Feeds
    - 6.3.2-PSS
  - 6.4-Swarm用作web3的后端
    - 6.4.1-Primitives
    - 6.4.2-Scripting
    - 6.4.3-Built-in composite APIs
    - 6.4.4-Standard library

## 第三部分-规范 SPECIFICATIONS

## 第四部分-附录 APPENDIX

## 第五部分-索引 INDEXES