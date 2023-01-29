# guacamoleのターミナルへのURL
https://gist.github.com/atomlab/376901845c3d474d1e60e6b7a3affaae

# guacamoleの認証
* guacamole/TunnelRequestService.java => createConnectedTunnel()
 ここからConnectable.connect()で接続・認証しているが実体(interfaceの未定義)がない.guacamole-ext内の定義が優先される。実態は下記。

* guacamole-ext/SimpleConnection => connect
 guacamole/のConnectableを実装している
* guacamole-ext/ConfiguredGuacamoleSocket.jsava => ConfiguredGuacamoleSocket (この中で認証プロパティの設定をしているっぽい）
