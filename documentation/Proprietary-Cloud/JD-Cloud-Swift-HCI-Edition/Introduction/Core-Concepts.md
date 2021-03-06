# 核心概念

了解京东云敏捷专有云产品，通常需要涉及如下概念：

| **概念**   | **介绍**                                                     |
| ---------- | ------------------------------------------------------------ |
| 集群       | 集群是一组物理服务器，它们作为一个整体向用户提供资源。集群具有可扩展性、高可用性、负载均衡、错误恢复等特性，在同一个集群中的物理服务器必须安装相同的操作系统（虚拟机管理程序，Hypervisor），拥有相同的二层网络连接。 |
| 基础节点   | 一类物理服务器，负责运行集群中基础组件服务，为整个集群提供运行环境支持。 |
| 控制节点   | 一类物理服务器，负责对其余节点的控制，包含云主机建立、迁移、网络分配、存储分配等。 |
| 计算节点   | 一类物理服务器，负责云主机运行，为云主机实例提供计算、网络、存储等资源。 |
| 存储节点   | 一类物理服务器，负责对云主机的额外存储进行管理等，是用于存储云主机磁盘文件的存储服务器。 |
| 网络节点   | 一类物理服务器，负责对外网络（公有网段）与云内网络（私有网段）之间的通信，以及管理云主机网络之间的通信/拓扑。 |
| 云主机     | 京东云敏捷专有云平台上的计算资源，是运行在物理机上的虚拟机实例，具有独立的IP地址，可以访问公共网络，运行应用服务。 |
| 可用区     | 云主机和其他资源的部署物理位置。                             |
| 云主机规格 | 云主机规格标识不同的云主机配置，包括vCPU（核）、内存（GB）、系统盘容量（GB）及系统盘类型等。 |
| 镜像       | 云主机运行环境预置模版，包含服务器的预配置环境（目前版本仅包含操作系统）。 |
| 云硬盘     | 分布式持久块存储设备，可以作为云主机实例的数据盘使用，给云主机提供额外的存储空间。 |
| 云硬盘快照 | 某一个时间点上某一个磁盘的数据备份                           |
| 云硬盘规格 | 创建云硬盘容量大小的定义。                                   |
| 对象存储   | 基于对象的存储。每个对象都存储于一个具有扁平地址空间的存储池中，该空间中的全部对象属于同一层级，去除了文件系统中的多层级树形目录结构。 |
| 存储空间   | 存储空间（Bucket）是对象存储中数据的基本组织单位，所有的数据都必须在某一个存储空间中，存储空间的名称全局唯一。每个存储空间均具有自己的访问权限等属性，配合其他高级属性满足不同场景的存储需求。 |
| 对象       | 对象（Object）是对象存储中的基本单位，一个对象包含对象名称、文件的数据及其相关元数据。用户上传至京东云敏捷专有云平台对象存储的数据都以对象的形式保存在存储空间中。 |
| AK/SK      | AccessKeyId（AK）与SecretAccessKey（SK）是用户访问京东云敏捷专有云平台对象存储的身份标识。 |
| VLAN       | 在计算机网络中，一个二层网络可以被划分为多个不同的广播域，称为虚拟局域网VLAN（Virtual Local   Area Network），一个广播域对应一个特定的用户组，默认情况下这些不同的广播域相互隔离。不同广播域之间想要通信，需要通过一个或多个路由器。 |
| 公有网络   | 由因特网信息中心分配的公有IP地址段或者可以连接到外部互联网的IP地址段。 |
| 私有网络   | 自定义的虚拟网络空间，实现资源间的逻辑隔离。                 |
| 内网地址   | 为来源IP为私网的客户端提供服务的连接地址                     |
| 浮动IP     | 可与云主机动态绑定/解绑的公网IP，即公有网络接入到私有网络的IP地址。 |
| 安全组     | 生效于云主机级别的安全访问控制，可指定进出云主机的IP、网络包流向、协议及端口规则。 |
| 云管平台   | 基于Web的用户资源管理界面。                                  |
| 子网       | 子网是所属私有网络内的IP地址块。目前私有网络中的云资源部署在子网内，如云主机、负载均衡。在创建网络后，可以在网络下添加子网，或在创建网络的同时创建子网。相同网络下子网的IP地址块不可以重叠，不同网络下子网的IP地址块可以重叠。 |
| 虚拟路由   | 在软、硬件层实现物理路由器的功能仿真，属于一种逻辑设备。虚拟路由单独地运行各自的路由协议实例，具有专用的I/O端口、地址空间、路由表等。 |
| 路由表     | 路由表是一系列路由规则的集合，用于控制私有网络中子网的流量流入流出方向。 |
| NAT        | NAT为Network Address Translator的缩写。虚拟路由可以通过NAT为用户提供企业级公网接入服务。 |
| 负载均衡   | 负载均衡可以对多台云主机进行流量分发，提升应用系统的对外服务能力，消除单点故障。 |
| 组织       | 组织为一组用户的集合。京东云敏捷专有云平台中除根组织外共有4级组织，利用组织分级的方式，系统管理员可以更方便地进行资源划分与权限分配。 |
| 系统管理员 | 京东云敏捷专有云平台初始化时默认的用户角色，系统的最高权限持有者，对系统有完全的控制权，管理整个平台的组织、用户、配额与运维监控。 |
| 租户管理员 | 租户所在组织的领导，管理自己的组织人员，并分配配额，能够使用云资源。 |
| 租户       | 被赋予基础云权限的用户，云资源的使用者。通过系统管理员或者上级租户管理员创建。 |
| 运维管理员 | 运维人员的领导，能够管理运维人员，并同时具有运维权限。       |
| 运维人员   | 云平台的运维保障人员，主要处理云平台上产生的问题和故障。通过系统管理员或者上级运维管理员创建。 |