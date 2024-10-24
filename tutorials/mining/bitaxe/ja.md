---
name: BitAxeの設定
Description: BitAxeの設定方法は？
---

### はじめに

BitAxeは、Skotによって作成されたオープンソースプロジェクトで、[GitHubで入手可能](https://github.com/skot/bitaxe)です。これにより、コスト効率の良いマイニングの実験が可能になります。

このプロジェクトは、ASIC（ビットコインマイニング用の特殊なマシン）の市場リーダーであるBitmainの有名なAntminer S19の仕組みを逆エンジニアリングしました。これにより、これらの強力なチップを新しいオープンソースプロジェクトで使用できるようになりました。Nerdminerとは異なり、BitAxeはマイニングプールに接続するのに十分な計算能力を持っており、定期的にいくつかのサトシを稼ぐことができます。一方、Nerdminerはいわゆるソロプールにのみ接続でき、これは宝くじのチケットのようなものです：全ブロック報酬を獲得するチャンスはわずかです。

BitAxeには、異なるチップと性能を持ついくつかのバージョンがあります：

| Bitaxe モデル シリーズ      | ASIC チップ | 使用されるもの                     | 期待されるハッシュレート          | 理想的な用途                                                                                                  |
| ------------------------ | --------- | --------------------------- | --------------------------- | ---------------------------------------------------------------------------------------------------------- |
| Bitaxe Max (シリーズ 100)  | 1 x BM1397| Antminer シリーズ 17          | 400 GH/s (最大 450 GH/s)   | ビットコインマイニング初心者向け。適度な電力消費で安定したハッシュレートを提供します。                      |
| Bitaxe Ultra (シリーズ 200)| 1 x BM1366| Antminer S19 XP と S19k Pro| 500 GH/s (最大 550 GH/s)   | 効率と高いハッシュレートのバランスを目指す本格的なマイナー向け。                                          |
| Bitaxe Hex (シリーズ 300)  | 6 x BM1366| Antminer S19k Pro と S19 XP| 3.0 TH/s (最大 3.3 TH/s)   | 効率を犠牲にすることなく、スケーラビリティと高性能を求めるマイナー向け。                             |
| Bitaxe Supra (シリーズ 400)| 1 x BM1368| Antminer S21                | 600 GH/s (最大 700 GH/s)   | 最高のハッシュレートと効率を求める真剣な愛好家向け。                                         |

このチュートリアルでは、Antminer S19XP用のBM1366チップを搭載したBitAxe Ultra 204を使用します。これはすでに小売業者によって組み立てられ、フラッシュされています。

### [小売業者のリストはこのページで確認できます](https://bitaxe.org/legit.html)

![signup](assets/2.webp)

一般的に、電源はそれに付属しています。そうでない場合は、5Vジャックケーブルと少なくとも4Aを持つ電源を購入する必要があります。

![signup](assets/1.webp)

### 設定
BitAxeを最初に接続すると、デフォルトでWi-Fiネットワークに接続しようとします。5回の試みの後、自身のWi-Fiネットワークの名前を表示し、それに接続して設定できるようになります。
これを行うには、任意のコンピューターやスマートフォンを使用できます。Wi-Fi設定に移動し、新しいネットワークを検索します。そこで、`Bitaxe_XXXX`という名前のWi-Fiを見つけることができます。ここでは、`Bitaxe_A859`です。このWi-Fiネットワークに接続し、自動的にウィンドウが開きます。

![signup](assets/3.webp)

このウィンドウで、左上の三つの小さな水平バーをクリックし、次に`Settings`をクリックします。

![signup](assets/4.webp)

自動検出システムがないため、Wi-Fiネットワーク情報を手動で入力する必要があります。
![signup](assets/5.webp)
したがって、Wi-FiのSSID、つまりネットワークの名前、パスワード、選択したマイニングプールの情報を指定してください。注意してください、ここではプールのURLが同じ方法で提示されていません。例えば、Braiinsの場合、提供されるプールURLは：`stratum+tcp://eu.stratum.braiins.com:3333`です。

![signup](assets/6.webp)

画面で見ることができるように、`stratum+tcp://`と`:3333`の部分を削除し、`eu.stratum.braiins.com`のみを残してください。その後、`Port`フィールドに、プールから与えられたURLの最後の4桁を`:`なしで入力します。ここでは、それは`3333`です。

このチュートリアルでは、Braiinsマイニングプールを使用していますが、他のものを選択する自由があります。マイニングプールに関する私たちのチュートリアルは[PlanB Networkのウェブサイト](https://planb.network/en/tutorials/mining)で見つけることができます。

次に、`User`にあなたの識別子を入力し、その後に`Password`を入力します。通常、それは`"x"`または`"Anything123"`です。

`Core Voltage`設定はデフォルトで`1200`のままにしておき、`Frequency`についても初期値をそのままにしておきます。この設定は後で調整して、より多くの計算能力を得ることが可能です。しかし、BitAxeは過熱時に性能を下げるシステムを持っていないため、チップの温度が65-70°Cを超えないようにすることが重要です。温度が65°Cを大幅に超えると、BitAxeが損傷する可能性があります。

![signup](assets/7.webp)

すべての設定を正しく入力したら、下部の`Save`ボタンをクリックし、BitAxeを単にアンプラグして再度プラグインすることで再起動してください。
情報を正しく入力していれば、デバイスはすぐにWi-Fiに接続し、マイニングプールに接続し、小さな画面にいくつかの情報を表示し始めるはずです。マイニングプールのダッシュボードに表示されるまでには数分かかるかもしれません。
### ダッシュボードと画面

3つの異なる表示がスクロールします。3ページ目では、ダッシュボードに接続するためのIPアドレスである`IP`情報を見ることができます。ここでは、アドレスは`192.168.1.19`です。

![signup](assets/8.webp) ![signup](assets/9.webp) ![signup](assets/10.webp)

ダッシュボードにアクセスするには、このアドレスをインターネットブラウザに入力するだけです。

ダッシュボードでは、小さな画面に表示されるすべての情報を詳しく見ていきます。

![signup](assets/11.webp)

| BitAxe画面 | ダッシュボード                                   | 説明                                                                                                                                                                                                               |
| ------------- | ------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Gh            | ハッシュレート                                    | 現在の計算能力をGigaHash/sで表したもの                                                                                                                                                                      |
| W/THs         | 効率                                  | BitAxeの効率をW/THsで表したものです。これは、消費される電力と生成される計算能力の比率です。                                                                          |
| A/R           | シェア                                      | プールに送信されたBitAxeからの`シェア`の量で、提供された作業量を表します。                                                                                                                          |
| UT            | アップタイム                                      | BitAxeが中断なく稼働している時間（`ログ`の下のメニューで利用可能）。                                                                                                                |
| BD            | 最高難易度                                   | 最後の再起動以来に達した最大難易度。比較のために、現在のネットワーク難易度は約85Tです。                                                                                                                                                 |
| FAN           | `Heat`ボックス内のFAN                       | 分速で表されるファンの回転速度。                                                                                                                                                                                       |
| Temp          | `Heat`ボックス内のASIC温度                  | チップ温度は65°Cを超えてはならない。                                                                                                                                                                                   |
| Pwr           | 電力                                         | 消費されるワット数の電力。ただし、この情報は画面、ファン、または電源を考慮に入れていません。例えば、11.7Wと表示されている場合、実際の総消費電力は15.8Wです。                                                                                   |
| mV mA         | 入力電圧 入力電流                           | 機械によって消費される電圧と電流。ワット数の電力は、電圧に電流を掛けたものと等しい。                                                                                                                                 |
| FH            | 空きヒープメモリ（左メニュー -> `Logs`）    | 利用可能なメモリ。                                                                                                                                                                                                       |
| vCore         | ASIC電圧（パフォーマンスボックス内）        | ASICチップ上で測定される電圧。                                                                                                                                                                                          |
| IP            | NA                                          | IPアドレス。                                                                                                                                                                                                             |
| V2.1.0        | バージョン（左メニュー -> `Logs`）          | ファームウェアのバージョン。                                                                                                                                                                                             |
Wi-Fiやプールの設定は、いつでも問題なく変更できます。
換気と部屋の温度によっては、パフォーマンスを上げる必要があるかもしれませんし、温度が65°Cを超えないようにパフォーマンスを下げる必要があるかもしれません。パフォーマンスを上げると、より多くのサトシを稼ぐことができますが、BitAxeはより多くの電気を消費することになります！