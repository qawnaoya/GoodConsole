---

theme: "Black"
transition: "Default"

---

# 快適なコンソール環境の実現

---

# コンソール環境の変遷

1. conhost  
  所謂、レガシーなコンソール環境
2. Terminal  
  DirectWriteなどを利用したモダンなコンソール
3. Cmder  
  
--

# conhost

Windowsのレガシーなコンソール環境、Windows NT 3.1以降ほぼ手を付けられていない。
Terminalに置き換えられつつある。


--

# Terminal

conhostに代わる新しいコンソール環境。Windows Terminalとも言うが最近の更新で
単にTerminalと改名された。

--

# Cmder

Terminal以前からOSSとして開発されているコンソール環境。

---

# 快適なコンソールを実現するためのパッケージマネージャ

--

# お勧めできるパッケージマネージャ

* WinGet
* Scoop
* Chocolatey

--

# WinGet

Microsoftから提供されているパッケージマネージャ。Microsoft Storeからアプリインストーラという名前で提供されている。

--

# Scoop

OSSとして開発されているパッケージマネージャ。コマンドラインの特に開発者向けのアプリケーションに注力している。

--

# Chocolatey

Chocolatey Softwareから提供されているパッケージマネージャ。WinGetより先行して頭角を現した。

--

# パッケージマネージャを選定するポイント

* アンインストールの確実性
* 運用の容易性
* レポジトリの強固さ

--

# アンインストールの確実性

アンインストールの確実性においてはScoopが頭一つ抜けている。
Scoopはホームディレクトリ内に

```
scoop - apps - 
      - buckets
      - cache
      - persist
      - shims
      - workspace
```
という形で展開するだけ。

--

# 運用の容易性

運用の容易性はScoopが優秀。Scoopは管理者権限なしに運用できる。

--

# レポジトリの強固さ

* Scoopは配布物のハッシュ値をレポジトリの情報と比較する
* WinGetは登録時にシステム側で既知の悪意あるコードと比較する

--

# 参考: 水飲み場攻撃

* 攻撃対象とする特定分野の企業や組織のユーザーが普段利用するWebサイトを改ざんし、マルウェアに感染させる攻撃手法

--

# 既知の水飲み場攻撃

* pypiへの著名なパッケージに偽装した悪意あるパッケージ
* npmへの著名なパッケージに偽装した悪意あるパッケージ

