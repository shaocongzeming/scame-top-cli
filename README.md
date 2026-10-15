# SCAME-CLI

SCAME 工业连接器的产品参数查询、面价查询、库存查询和简易报价工具。

## 运行

需要 Python 3 和 `cryptography`：

```bash
python3 -m pip install cryptography
python3 scame_cli.py search 63A 3P+N+E IP67
python3 scame_cli.py info 213.1630 --json
```

技术参数可直接查询；面价、库存和报价需要使用者已配置有效授权码。配置方法见 [技能说明](scame-cli-skill/SKILL.md)。

```bash
python3 scame_cli.py price 213.1630 --json
python3 scame_cli.py stock 423.6367 --json
python3 scame_cli.py quote 213.1630x10 --json
```

## 数据说明

数据来自选型工具服务。面价和库存通过授权码在本地解密；授权码应仅保存在使用者自己的环境中。

面价是目录价格，不等于实际成交价。库存为快照，订单交期和可用量请与商务或仓库确认。

## License

见 [LICENSE](LICENSE)。

---

**班底 Zecrew** · 北京韶聪泽明智能科技有限责任公司

[官网](https://zecrew.shaocongzeming.com)
