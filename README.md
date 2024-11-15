# OPEN IPv6 ダイナミック DNS API Python Client

「OPEN IPv6 ダイナミック DNS for フレッツ・光ネクスト」サービスの `new` および `renew` 操作を行うことができる 非公式Python クライアントです。

## インストール方法
### PyPIからインストールする場合
```bash
pip install openipv6ddns
```
### リポジトリをクローンしてインストールする場合
```bash
git clone https://github.com/ne53/openipv6ddns.git
cd openipv6ddns
pip install . 
```

## サンプルコード
### DDNS ホスト新規登録 (`New`)
```python
from openipv6ddns import new

hostname = "test12345"
ipv6 = "2001:db8::1234:5678"  # 省略可能
mail = "test@example.com"  # 省略可能
print(new(hostname=hostname, ipv6=ipv6, mail=mail))
```
### DDNS ホスト IPv6 アドレス更新 (`Renew`)
```python
from openipv6ddns import renew

key = "A12BC34567DE890FG"
ipv6 = "2001:db8::8756:4321"  # 省略可能
print(renew(key=key, ipv6=ipv6))
```

## API及び返却されるデータの詳細
返却されるデータのカラムの内容やその他詳細については、[OPEN IPv6 ダイナミック DNS for フレッツ・光ネクスト API マニュアル](https://i.open.ad.jp/api/)を参照してください。