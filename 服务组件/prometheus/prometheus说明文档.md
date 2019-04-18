# Prometheus说明文档
#临时 #自动化流程

## 目录结构及说明
> README.md：说明文档  
> 组件位置图：高亮显示组件在系统内的位置  
> Dockerfile：用于在构建服务器生成镜像  
> Yaml*：K8S部署代码  

## 组件说明
1. 概述：监控服务器，通过exporter代理获取日志后将时序数据写入influx DB，通过聚合查询功能为grafana提监控供仪表盘信息
2. 部署类型：Deployment
3. ServiceName：Prometheus
4. PortType：Ambassador
5. ServicePort：9090
6. URL：test.prom.com
7. 高可用：单实例部署，通过K8S副本机制实现高可用

## APIList
略

## 组件部署验证
执行`sh ../ops/prom/check.sh`，结果为`health`即可

## 组件运维
详见`../ops/prom/prometheus运维指南.md`
