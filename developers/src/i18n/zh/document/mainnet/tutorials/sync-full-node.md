# 同步全节点数据

如果需要做数据节点或者挖矿节点需要先同步 MixinNetwork 全节点数据

1. 从 GitHub 下载 Mixin 最新的版本 https://github.com/MixinNetwork/mixin/releases, 里面包含配置文件和执行程序
2. 创建一个目录来存储 Mixin 节点数据 `mkdir ~/.mixin`
3. 把主网的配置 genesis.json, nodes.json, config.example.toml 放入 ～/.mixin 目录
4. 修改 config.example.toml 重命名为 config.toml, 需要修改其中的几个配置
   - signer-key 设置为签名的 spend key 私钥
   - listener 修改为本机的 IP 和端口 7239, 并允许 7239 穿透防火墙
   - consensus-only 如果只是同步数据节点(archive mode)设置为 false, 如果挖矿节点设置为 true
5. 启动 `./mixin kernel -d ~/.mixin`
