# プライバシーポリシー / Privacy Policy

**最終更新: 2026年6月24日**

---

# 電波見太郎 for L13 プライバシーポリシー

本プライバシーポリシーは、Android アプリ「電波見太郎 for L13」（パッケージ名 `com.ztr02.monitor`、以下「本アプリ」）に適用されます。

本アプリは、ユーザーが設定したローカルルーターの管理画面からネットワーク・電波情報を取得し、端末上で表示するためのアプリです。**開発者のサーバーへ、利用者を特定する情報や診断ログを自動送信することはありません。** ただし、端末内には設定や動作記録を保存します（後述）。

## 1. 収集・表示する情報

本アプリは、**ルーターから取得した技術情報**を画面に表示します。例:

- 基地局関連情報（PCI、セル ID、周波数帯など）
- 電波強度（RSRP / SINR / RSRQ / SNR / RSSI 等）
- ネットワーク種別、キャリア表示、接続状態
- ルーターのファームウェア版など（取得できる場合）

これらは**ユーザーが指定したローカルルーター**（例: `http://192.168.0.1`）への通信で取得します。

## 2. 端末内に保存する情報

本アプリは、次の情報を**端末内のみ**に保存します。開発者へ自動送信しません。

| 種類 | 内容 | 保存場所の例 |
|------|------|----------------|
| ルーター接続設定 | URL、ログインパスワード | アプリのプライベート領域 |
| 表示の復元用データ | 直近のモニター表示データ | 同上 |
| ユーザー設定 | 簡易/詳細の選択、プライバシー表示（サンプル表示）の ON/OFF 等 | 同上 |
| NSA Hunter 記録 | 基地局（PCI 等）ごとの NSA 可否のメモ | 同上 / WebView 内ストレージ |
| スピードテスト履歴 | 計測結果（最大 20 件） | WebView 内ストレージ |
| 計測ログ | 電波の時系列データ（データログタブ） | アプリ内メモリ / エクスポート時のみ端末へ |
| 診断ログ | 動作記録（ログイン成否、データ取得成否、ルーター操作の概要など） | 端末内ファイル（最大約 512KB） |
| Pro 版の購入状態 | 購入済みかどうか | 同上（Google Play 課金と連携） |
| WiFi 再接続補助 | ルーター接続時に記憶した WiFi SSID | 同上 |

**パスワードはルーターへのログインにのみ使用し、診断ログには意図的に記録しません。**

## 3. 開発者へ送る情報（ユーザーの操作がある場合のみ）

不具合報告などのため、ユーザーが **設定 → ログ → 「ログをメールで送る」** を選んだ場合に限り、メールアプリ経由で開発者（`a.trading.firm@gmail.com`）へ次を送れます。

- 診断ログファイル（添付）
- メール本文に含まれる端末型番・OS バージョン・アプリ版（アプリが自動挿入）
- ユーザーが自由に記入した説明文

**送信はユーザーがメールアプリで「送信」を押すまで完了しません。** 開発者はメール受信以外の方法でログを自動取得しません。

「ログを共有」から、ユーザーが選んだアプリ（Gmail 以外の共有先を含む）で送ることもできます。

## 4. 意図的に取得しない情報

本アプリは、次を**取得・利用しません**。

- GPS による位置情報
- 連絡先・写真・一般ファイルへの Access（診断ログ共有時のメール添付を除く）
- IMEI 等の端末固有 ID の収集（広告 SDK 側の処理は後述）

## 5. ネットワーク通信

| 通信先 | 目的 | タイミング |
|--------|------|------------|
| ユーザー設定のルーター（ローカル IP） | ログイン、電波・設定の取得、ルーター操作（Pro 版） | アプリ利用中 |
| Google AdMob | 広告表示（Pro 版購入済みの場合は非表示） | アプリ利用中 |
| Cloudflare Speed Test | スピードテスト（速度・遅延の計測） | ユーザーがスピードテストを実行したとき |
| Google Play 課金 | Pro 版の購入・復元確認 | ユーザーが購入操作をしたとき |

上記のほか、**開発者のサーバーへ定期的にデータを送る通信はありません。**

### 位置情報に関する権限について

Android の仕様上、一部端末・OS バージョンでは WiFi 状態の取得に位置情報権限が関係する場合があります。本アプリは** GPS による位置追跡を行いません。**

## 6. 第三者サービス

### Google AdMob

広告表示のため [Google AdMob](https://admob.google.com/) を利用しています。Google により、広告 ID・IP アドレス・おおよその位置情報（端末設定による）・利用状況などが処理される場合があります。詳細は [Google のプライバシーポリシー](https://policies.google.com/privacy) をご確認ください。

### Cloudflare Speed Test

スピードテスト実行時、Cloudflare の計測エンドポイント（`speed.cloudflare.com`）と通信します。速度・遅延の計測のみを目的とします。

### Google Play 課金

Pro 版の購入処理は Google Play の課金システムを利用します。支払い情報は Google が処理し、開発者はクレジットカード番号等を受け取りません。

## 7. 解析・広告計測

本アプリは **Firebase Analytics 等の利用者行動解析 SDK を使用していません。**

## 8. データの削除

- **診断ログ**: 設定 → ログ → 「ログを消去」
- **NSA 基地局記録**: 設定 → ログ → 「NSA基地局記録を消す」
- **アプリの全データ**: Android の「アプリ情報」からストレージを消去、またはアプリをアンインストール

## 9. お問い合わせ

不具合報告・ご質問は、次のメールアドレスまでご連絡ください。

**a.trading.firm@gmail.com**

（Google Play ストアの「アプリのサポート」にも同じ連絡先を表示しています。）

診断ログを添えていただく場合は、アプリ内の **「ログをメールで送る」** をご利用ください。

---

# Privacy Policy for 電波見太郎 for L13

**Last updated: June 24, 2026**

This Privacy Policy applies to the Android app **電波見太郎 for L13** (package `com.ztr02.monitor`, the “App”).

The App reads network and signal information from a **user-configured local router** and displays it on the device. **We do not automatically transmit personally identifying information or diagnostic logs to the developer’s servers.** Some data is stored locally on the device as described below.

## 1. Information displayed

The App displays technical data obtained from the router, such as cell / signal metrics (RSRP, SINR, RSRQ, etc.), network type, and connection status.

## 2. Information stored on the device

Examples include router URL and login password, UI preferences, NSA Hunter notes, speed test history, in-app measurement logs, diagnostic logs (up to ~512KB), Pro purchase state, and cached Wi‑Fi SSID for router reconnect assist. **Passwords are not intentionally written to diagnostic logs.**

## 3. Information sent to the developer (user-initiated only)

Only when the user chooses **Settings → Log → “Send log by email”** and completes sending in their mail app, the user may send a diagnostic log attachment and optional description to **a.trading.firm@gmail.com**. No automatic upload occurs.

## 4. Information we do not collect

We do not collect GPS location, contacts, photos, or IMEI (third-party ad SDK processing is described separately).

## 5. Network communication

- User’s local router (monitoring and optional router control with Pro)
- Google AdMob (ads; hidden when Pro is active)
- Cloudflare Speed Test (when the user runs a speed test)
- Google Play Billing (when the user purchases Pro)

## 6. Third-party services

See the Japanese section above for AdMob, Cloudflare, and Google Play Billing.

## 7. Analytics

The App does **not** use Firebase Analytics or similar behavioral analytics SDKs.

## 8. Deleting data

Diagnostic logs and NSA registry can be cleared from the in-app Log menu. Uninstalling the App removes local app data.

## 9. Contact

**a.trading.firm@gmail.com**

For bug reports, please use **“Send log by email”** in the app when possible.
