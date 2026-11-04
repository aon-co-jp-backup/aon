# aon (旧称: open-aruaru-runo-iLumi)

🏢 GitHub organization: **[aon-co-jp](https://github.com/aon-co-jp)**

このリポジトリは、`aon-co-jp` organization配下に分散する複数プロジェクト
(`F:\open-runo`をローカルの作業ドライブとするエコシステム)全体の
**「プロジェクトシリーズ索引」を担うメタリポジトリ**です。このリポジトリ
自体は個別の実装コードを持たず、各プロジェクトへの入口(README・
CLAUDE.md・PORTING.md・役割の要約)をまとめて一覧できることだけを目的と
しています。

対応する実装は [`aruaru-tokyo`](https://github.com/aon-co-jp/aruaru-tokyo)
(Rust + [Poem](https://github.com/poem-web/poem)製)側にもあり、
`/open-aruaru-runo-iLumi`(および互換パス`/open-aruaru-runo`)で
このメタ索引と同じ内容をWebページとして13ヶ国語・GitHub API連携付きで
閲覧できます。

## プロジェクトシリーズ一覧

`F:\open-runo`配下で実際にgitリポジトリとして存在し、GitHub
(`aon-co-jp`)上にリモートが確認できるプロジェクトを掲載しています。
各プロジェクトの役割説明は、それぞれのリポジトリの実際の
`README.md`/`CLAUDE.md`の記載に基づく要約です(推測での記載はしていません)。

| プロジェクト | GitHub | README | PORTING | 設計思想＆開発方針＆開発環境ルール | 役割 |
|---|---|---|---|---|---|
| RCosmo | [aon-co-jp/RCosmo](https://github.com/aon-co-jp/RCosmo) | [README](https://github.com/aon-co-jp/RCosmo/blob/main/README.md) | [PORTING](https://github.com/aon-co-jp/RCosmo/blob/main/PORTING.md) | [CLAUDE.md](https://github.com/aon-co-jp/RCosmo/blob/main/CLAUDE.md) | Rust製GraphQL Federationプラットフォーム(Poem/Tauri/Cosmoは非依存・互換自前実装)。WunderGraph Cosmoの有料版機能をOSS・Pure Rustで実現し、独自の自己学習AIを搭載(外部LLM契約不要)。姉妹リポジトリ`poem-cosmo-tauri`と並行開発。 |
| RFrontEnd | [aon-co-jp/RFrontEnd](https://github.com/aon-co-jp/RFrontEnd) | [README](https://github.com/aon-co-jp/RFrontEnd/blob/main/README.md) | [PORTING](https://github.com/aon-co-jp/RFrontEnd/blob/main/PORTING.md) | [CLAUDE.md](https://github.com/aon-co-jp/RFrontEnd/blob/main/CLAUDE.md) | HTML5/CSS3/TypeScript/React相当を、既存実装のコードを一切流用せず一から開発する複数プロジェクト(RHTML/RCSS/RTypeScript等)を束ねる親リポジトリ。 |
| RPoem | [aon-co-jp/RPoem](https://github.com/aon-co-jp/RPoem) | [README](https://github.com/aon-co-jp/RPoem/blob/main/README.md) | [PORTING](https://github.com/aon-co-jp/RPoem/blob/main/PORTING.md) | [CLAUDE.md](https://github.com/aon-co-jp/RPoem/blob/main/CLAUDE.md) | RCosmoと同種のRust製GraphQL Federationプラットフォーム(Poem/Tauri/Cosmo非依存の互換自前実装)。`open-runo`を正本として分岐した`poem-runo`をさらにリネーム・統合した後継リポジトリ。 |
| aruaru-db | [aon-co-jp/aruaru-db](https://github.com/aon-co-jp/aruaru-db) | [README](https://github.com/aon-co-jp/aruaru-db/blob/main/README.md) | [PORTING](https://github.com/aon-co-jp/aruaru-db/blob/main/PORTING.md) | [CLAUDE.md](https://github.com/aon-co-jp/aruaru-db/blob/main/CLAUDE.md) | CockroachDBの分散強整合×Snowflakeのストレージ/コンピュート分離×Git-on-SQLバージョン管理を、すべてPure Rustで実装するハイブリッド分散データベース。 |
| aruaru-llm | [aon-co-jp/aruaru-llm](https://github.com/aon-co-jp/aruaru-llm) | [README](https://github.com/aon-co-jp/aruaru-llm/blob/main/README.md) | [PORTING](https://github.com/aon-co-jp/aruaru-llm/blob/main/PORTING.md) | [CLAUDE.md](https://github.com/aon-co-jp/aruaru-llm/blob/main/CLAUDE.md) | `aruaru`エコシステム(aruaru-tokyo・aruaru-db・e-gov.info・karu.tokyo等)共通の「AIチャットコマース」応答サービス。リポジトリ名は「LLM」を冠するが、実際のLLM推論への差し替えは今後という正直な開示がREADMEに明記されている。 |
| aruaru-tokyo | [aon-co-jp/aruaru-tokyo](https://github.com/aon-co-jp/aruaru-tokyo) | [README](https://github.com/aon-co-jp/aruaru-tokyo/blob/main/README.md) | [PORTING](https://github.com/aon-co-jp/aruaru-tokyo/blob/main/PORTING.md) | [CLAUDE.md](https://github.com/aon-co-jp/aruaru-tokyo/blob/main/CLAUDE.md) | [aruaru.tokyo](https://aruaru.tokyo/)のTOPページ。Rust + Poem製、DB非依存・1バイナリ完結。`audiocafe.tokyo`(PHP)とは別ドメイン・別スタックの姉妹サイト。 |
| audiocafe-tokyo-rust | [aon-co-jp/audiocafe-tokyo-rust](https://github.com/aon-co-jp/audiocafe-tokyo-rust) | [README](https://github.com/aon-co-jp/audiocafe-tokyo-rust/blob/main/README.md) | [PORTING](https://github.com/aon-co-jp/audiocafe-tokyo-rust/blob/main/PORTING.md) | [CLAUDE.md](https://github.com/aon-co-jp/audiocafe-tokyo-rust/blob/main/CLAUDE.md) | `audiocafe.tokyo`の既存PHPモノリスをRust + Poemへ段階的に移行するプロジェクト(第一段)。既存PHP実装は`audiocafe-tokyo`リポジトリのまま並行運用。 |
| audiocafe.tokyo | [aon-co-jp/audiocafe-tokyo](https://github.com/aon-co-jp/audiocafe-tokyo) | [README](https://github.com/aon-co-jp/audiocafe-tokyo/blob/main/README.md) | [PORTING](https://github.com/aon-co-jp/audiocafe-tokyo/blob/main/PORTING.md) | [CLAUDE.md](https://github.com/aon-co-jp/audiocafe-tokyo/blob/main/CLAUDE.md) | PHP製のマルチコンテンツサイト。IT/建築系求人情報(`aruaru`)・女性向け求人/夜間エンターテインメント情報(`aruaru-lady`)・楽天モバイル関連情報・会社案内などを扱う。 |
| e-gov.info | [aon-co-jp/e-gov](https://github.com/aon-co-jp/e-gov) | [README](https://github.com/aon-co-jp/e-gov/blob/main/README.md) | [PORTING](https://github.com/aon-co-jp/e-gov/blob/main/PORTING.md) | [CLAUDE.md](https://github.com/aon-co-jp/e-gov/blob/main/CLAUDE.md) | 行政のデジタル化と、個人〜貿易商社まで対応するオンライン貿易・不動産プラットフォームを、LINEアプリ・WEBサイト・コンビニ端末という複数の入口から利用できる形で統合するプロジェクト。**まだサンプル・デモンストレーション段階**(READMEに明記)。 |
| karu.tokyo | [aon-co-jp/karu-tokyo](https://github.com/aon-co-jp/karu-tokyo) | [README](https://github.com/aon-co-jp/karu-tokyo/blob/main/README.md) | [PORTING](https://github.com/aon-co-jp/karu-tokyo/blob/main/PORTING.md) | [CLAUDE.md](https://github.com/aon-co-jp/karu-tokyo/blob/main/CLAUDE.md) | `karu.tokyo`のTOPページ。Rust + Poem製、DB非依存の1バイナリ完結サーバー。軽井沢・あきる野市・東京の観光とリモートワーク、IT・AI・AUDIO・貿易産業を紹介。 |
| open-cuda | [aon-co-jp/open-cuda](https://github.com/aon-co-jp/open-cuda) | — (README.mdは無く`README-Japan.md`等が代わりに存在) | — (PORTING.mdは未整備) | — (CLAUDE.mdは未整備) | OmniGPU設計文書(`OmniGPU-Design.md`)等を含むGPUランタイム関連プロジェクト(現時点で標準構成のREADME.md/CLAUDE.md/PORTING.mdは未整備)。 |
| open-easy-web | [aon-co-jp/open-easy-web](https://github.com/aon-co-jp/open-easy-web) | [README](https://github.com/aon-co-jp/open-easy-web/blob/main/README.md) | [PORTING](https://github.com/aon-co-jp/open-easy-web/blob/main/PORTING.md) | [CLAUDE.md](https://github.com/aon-co-jp/open-easy-web/blob/main/CLAUDE.md) | 「第二のKUSANAGI」——アプリのアップロード後にIPアドレスで起動し、ドメイン登録・HTTPS化を簡単に自動適用できる運用ツール(Rust → WebAssembly、フレームワーク不使用)。 |
| open-raid-z | [aon-co-jp/open-raid-z](https://github.com/aon-co-jp/open-raid-z) | [README](https://github.com/aon-co-jp/open-raid-z/blob/main/README.md) | [PORTING](https://github.com/aon-co-jp/open-raid-z/blob/main/PORTING.md) | [CLAUDE.md](https://github.com/aon-co-jp/open-raid-z/blob/main/CLAUDE.md) | Rust製の実マウント可能なRAID-Z/Z2/Z3ストレージプール実装(ZFS「風」のCoW/チェックサム/スナップショット。ZFS自体・OpenZFSへの依存やオンディスク互換性はなし)。**エコシステム開発ルールの正本**リポジトリ。 |
| open-web-server | [aon-co-jp/open-web-server](https://github.com/aon-co-jp/open-web-server) | [README](https://github.com/aon-co-jp/open-web-server/blob/main/README.md) | [PORTING](https://github.com/aon-co-jp/open-web-server/blob/main/PORTING.md) | [CLAUDE.md](https://github.com/aon-co-jp/open-web-server/blob/main/CLAUDE.md) | Rust + tokio/hyper自前実装のWebサーバー — 課金アイテム・金融データを「消失させない」ために設計。`open-runo`・`aruaru-db`と4層防御通信で連携するミッションクリティカル向け。 |
| rs-to-readme | [aon-co-jp/rs-to-readme](https://github.com/aon-co-jp/rs-to-readme) | [README](https://github.com/aon-co-jp/rs-to-readme/blob/main/README.md) | [PORTING](https://github.com/aon-co-jp/rs-to-readme/blob/main/PORTING.md) | [CLAUDE.md](https://github.com/aon-co-jp/rs-to-readme/blob/main/CLAUDE.md) | Rustクレートの`Cargo.toml`メタデータからREADME.mdを自動生成するCLIツール([crates.io](https://crates.io/crates/rs-to-readme)公開)。 |
| **aon**(このリポジトリ、旧称: open-aruaru-runo-iLumi) | [aon-co-jp/open-aruaru-runo-iLumi](https://github.com/aon-co-jp/aon) | [README](https://github.com/aon-co-jp/aon/blob/main/README.md) | [PORTING](https://github.com/aon-co-jp/aon/blob/main/PORTING.md) | [CLAUDE.md](https://github.com/aon-co-jp/aon/blob/main/CLAUDE.md) | このエコシステム全体の「プロジェクトシリーズ索引」を担うメタリポジトリ。個別のコード実装は持たない。 |

> 📝 **正直な開示**: 上表はローカル作業ドライブ`F:\open-runo`配下に
> 実在し、`.git/config`のリモートURLで`aon-co-jp`上の存在を確認できた
> プロジェクトのみを掲載しています。`poem-cosmo-tauri`のように
> ドキュメント上は言及されるものの本ドライブ上にローカルclone・実体が
> 確認できなかったプロジェクトは、確認が取れ次第この表へ追加します。

## Overview (English)

This repository is a **meta index for the entire `aon-co-jp` project
ecosystem** rooted at the local working drive `F:\open-runo`. It holds no
implementation code of its own — its sole purpose is to provide a single
place listing, for every sibling project actually present as a Git
repository under `aon-co-jp`, its README, PORTING.md (if any), development
policy document (`CLAUDE.md`), and a short, source-based summary of its
role. See the table above (labels in Japanese, links work regardless of
language).

The same content is also served as a live, 13-language web page with
live GitHub API lookups from
[`aruaru-tokyo`](https://github.com/aon-co-jp/aruaru-tokyo) at
`/open-aruaru-runo-iLumi` (alias: `/open-aruaru-runo`).

## GitHub organization

🏢 https://github.com/aon-co-jp

## API 方針: REST 全廃・gRPC / Connect へ (2026-11-04)

### 日本語
- **REST は全廃する。新しい API は REST で作らない。** ブラウザや `curl` から呼ぶ API は **Connect の単純呼び出し**(`POST /<パッケージ>.<Service>/<Method>`、`content-type: application/json`、本文は JSON)、サービス間は **gRPC / gRPC-web**(RPoem の管理API `open_runo.admin.v1.Admin` と同じ流儀)。ストリーミングは、必要になってから。
- **既存の REST は、触るときに順に移す。** 移したら旧 REST の経路は消す。移行が終わるまで残るが、**新規には追加しない**。
- **JSON は RS-JSON に統一**する(読み込みは `from_str_secure` / `parse_secure` でサイズ・深さ・重複キーの上限つき、書き出しは `rust_json::fast`)。ブラウザの WASM に `prost` は入れない(サイズが増えるため)。
- **例外(自分たちの API ではなく、相手の規格が決めているもの)**: ACME、OAuth/OIDC のコールバック、第三者(GitHub など)からの Webhook、ヘルスチェック、静的ファイル配信、OTLP など。これらは規格どおりの HTTP を受ける。
- 参考実装: `RPoem`(`open_runo.admin.v1.Admin`)、`open-easy-web`(`server/src/connect.rs`、`proto/open_easy_web/admin/v1/admin.proto`)。
- ※ このリポジトリのコードが既に方針どおりかどうかは、各リポジトリの現状による。この節は方針の記録であり、コードの変更を意味しない。

### English
- **REST is being abolished. New APIs are not built as REST.** APIs called from browsers or `curl` use **Connect unary calls** (`POST /<package>.<Service>/<Method>`, `content-type: application/json`, JSON body); service-to-service calls use **gRPC / gRPC-web** (the same style as RPoem's admin API `open_runo.admin.v1.Admin`). Streaming only when it is actually needed.
- **Existing REST endpoints are migrated one by one, when they are touched.** The old REST route is removed once migrated. Until migration is finished they remain, but **no new ones are added**.
- **JSON is unified on RS-JSON**: reading with `from_str_secure` / `parse_secure` (size, depth and duplicate-key limits), writing with `rust_json::fast`. `prost` is not put into browser WASM (it would grow the binary).
- **Exceptions (shapes dictated by someone else's standard, not our own API)**: ACME, OAuth/OIDC callbacks, webhooks from third parties (e.g. GitHub), health checks, static file serving, OTLP, and so on. These accept plain HTTP as the standard requires.
- Reference implementations: `RPoem` (`open_runo.admin.v1.Admin`) and `open-easy-web` (`server/src/connect.rs`, `proto/open_easy_web/admin/v1/admin.proto`).
- Note: whether the code in a given repository already follows this policy depends on that repository. This section records the policy; it does not mean the code has been changed.

### Deutsch (KI-Übersetzung, redaktionell überarbeitet; noch nicht von Muttersprachlern geprüft)
- **REST wird vollständig abgeschafft; neue APIs entstehen nicht mehr als REST.** APIs, die aus dem Browser oder per `curl` aufgerufen werden, verwenden **unäre Connect-Aufrufe** (`POST /<Paket>.<Service>/<Methode>`, `content-type: application/json`, JSON-Body). Zwischen Diensten kommen **gRPC bzw. gRPC-web** zum Einsatz, im selben Stil wie die Admin-API von RPoem (`open_runo.admin.v1.Admin`). Streaming wird erst ergänzt, wenn es tatsächlich gebraucht wird.
- **Bestehende REST-Endpunkte werden schrittweise umgestellt, und zwar immer dann, wenn man ohnehin an ihnen arbeitet.** Sobald ein Endpunkt umgestellt ist, wird die alte REST-Route entfernt. Bis zum Abschluss der Migration bleiben die übrigen bestehen, es werden aber **keine neuen mehr hinzugefügt**.
- **JSON wird einheitlich über RS-JSON verarbeitet**: Gelesen wird mit `from_str_secure` bzw. `parse_secure` (mit Obergrenzen für Größe, Verschachtelungstiefe und doppelte Schlüssel), geschrieben mit `rust_json::fast`. `prost` wird nicht in das Browser-WASM aufgenommen, da es die Datei vergrößern würde.
- **Ausnahmen (Schnittstellen, deren Form ein fremder Standard vorgibt und die nicht zu unserer eigenen API gehören)**: ACME, OAuth/OIDC-Callbacks, Webhooks von Drittanbietern (z. B. GitHub), Health-Checks, die Auslieferung statischer Dateien, OTLP und Ähnliches. Diese nehmen, wie vom jeweiligen Standard verlangt, gewöhnliches HTTP entgegen.
- Referenzimplementierungen: `RPoem` (`open_runo.admin.v1.Admin`) und `open-easy-web` (`server/src/connect.rs`, `proto/open_easy_web/admin/v1/admin.proto`).
- Hinweis: Ob der Code eines einzelnen Repositorys diese Richtlinie bereits erfüllt, hängt vom jeweiligen Repository ab. Dieser Abschnitt dokumentiert lediglich die Richtlinie; er besagt nicht, dass der Code schon angepasst wurde.

### Русский (перевод выполнен с помощью ИИ и отредактирован; носителями языка пока не проверен)
- **От REST мы полностью отказываемся; новые API больше не создаются в стиле REST.** API, к которым обращаются из браузера или через `curl`, используют **унарные вызовы Connect** (`POST /<пакет>.<Service>/<Method>`, `content-type: application/json`, тело запроса — JSON). Для взаимодействия между сервисами применяются **gRPC и gRPC-web** — в том же стиле, что и административный API RPoem (`open_runo.admin.v1.Admin`). Потоковая передача данных добавляется лишь тогда, когда в ней действительно возникает необходимость.
- **Существующие REST-эндпоинты переводятся поэтапно — по мере того, как с ними приходится работать.** После перевода старый REST-маршрут удаляется. Пока миграция не завершена, оставшиеся эндпоинты сохраняются, но **новые не добавляются**.
- **Работа с JSON унифицирована на основе RS-JSON**: чтение — через `from_str_secure` или `parse_secure` (с ограничениями на размер, глубину вложенности и повторяющиеся ключи), запись — через `rust_json::fast`. `prost` в браузерный WASM не включается, поскольку это увеличило бы размер файла.
- **Исключения (интерфейсы, форму которых определяет чужой стандарт, а не наш собственный API)**: ACME, обратные вызовы OAuth/OIDC, вебхуки сторонних сервисов (например, GitHub), проверки работоспособности, раздача статических файлов, OTLP и тому подобное. Такие интерфейсы принимают обычный HTTP, как того требует соответствующий стандарт.
- Эталонные реализации: `RPoem` (`open_runo.admin.v1.Admin`) и `open-easy-web` (`server/src/connect.rs`, `proto/open_easy_web/admin/v1/admin.proto`).
- Примечание: соответствует ли код конкретного репозитория этой политике, зависит от самого репозитория. Данный раздел лишь фиксирует политику и не означает, что код уже изменён.

## API 方針の補足: 用語の整理と使い分け (2026-11-04)

### 日本語
**1つに統一するものではなく、別の層の話です。** 「REST の代わり」になるのは Connect・gRPC・GraphQL だけで、WASM は画面を作る技術です。

| 用語 | 何か | REST の代わりか |
|---|---|---|
| REST | URL と HTTP メソッドで操作を表す API の作り方 | 全廃する側 |
| **Connect** | `POST /サービス名/メソッド名` に JSON を送る形式。`curl` でもブラウザの `fetch` でも呼べる | はい(**採用**) |
| **gRPC** | 同じ「サービス/メソッド」の考え方を、バイナリ(protobuf)と HTTP/2 で行う形式。速く、ストリーミングも得意 | はい(**サービス同士に採用**) |
| gRPC-web | gRPC のブラウザ向けの変形版 | はい(必要なら) |
| GraphQL | 欲しい項目を問い合わせる形式 | 一部だけ(**問い合わせ(読み取り)専用**) |
| WASM | Rust をブラウザの中で動かす仕組み | いいえ(画面を作る技術) |

- **ブラウザの画面や `curl` から呼ぶ API は Connect**(POST、JSON を RS-JSON で読み書き)。ブラウザの WASM は素の gRPC を話せず、Connect なら `fetch` のままで、`prost` を足さずに済む(画面のサイズも増えない)。
- **サービス同士の通信(サーバー間、重い処理、ストリーミング)は gRPC。** 多くは Connect で足りるので、ストリーミングが必要になった所だけ gRPC に上げる。
- **GraphQL は、まとめて問い合わせたいときの読み取り専用。** 書き込み(操作)には使わない。
- **WASM は画面を作る技術として、そのまま使う。** 画面から呼ぶ API が Connect になっただけ。
- 外部の規格が形を決めるもの(ACME、OAuth のコールバック、第三者の Webhook、ヘルスチェック、静的ファイル、OTLP)は、規格どおりの HTTP のまま。
- **迷ったら Connect。**

### English
**These are not alternatives to unify; they sit at different layers.** Only Connect, gRPC and GraphQL can replace REST; WASM is a way to build the UI.

| Term | What it is | Replaces REST? |
|---|---|---|
| REST | API style that expresses operations through URLs and HTTP methods | The thing being abolished |
| **Connect** | `POST /Service/Method` with a JSON body; callable from `curl` and from a browser `fetch` | Yes (**adopted**) |
| **gRPC** | The same service/method idea over binary (protobuf) and HTTP/2; fast, good at streaming | Yes (**for service-to-service**) |
| gRPC-web | A browser-friendly variant of gRPC | Yes (if needed) |
| GraphQL | A query language: ask for exactly the fields you want | Partly (**read-only queries**) |
| WASM | Runs Rust inside the browser | No (a UI technology) |

- **APIs called from browser screens or `curl` use Connect** (POST, JSON read and written with RS-JSON). Browser WASM cannot speak plain gRPC; with Connect it stays a `fetch`, and `prost` is not needed (the binary does not grow).
- **Service-to-service calls (server to server, heavy work, streaming) use gRPC.** Connect is enough in most places; move a call to gRPC only where streaming is actually needed.
- **GraphQL is read-only**, for queries that gather several pieces of data. It is not used for writes (operations).
- **WASM stays as the way to build the UI.** The API it calls simply became Connect.
- Interfaces whose shape an outside standard dictates (ACME, OAuth callbacks, third-party webhooks, health checks, static files, OTLP) stay plain HTTP.
- **When in doubt, use Connect.**

### Deutsch (KI-Übersetzung, sprachlich überarbeitet; noch nicht von Muttersprachlern geprüft)
**Es geht nicht darum, eine einzige Technik auszuwählen – die Begriffe liegen auf unterschiedlichen Ebenen.** Als Ersatz für REST kommen nur Connect, gRPC und GraphQL in Frage; WASM dagegen ist eine Technik, mit der die Benutzeroberfläche gebaut wird.

| Begriff | Was ist das? | Ersatz für REST? |
|---|---|---|
| REST | Ein API-Stil, bei dem Operationen über URLs und HTTP-Methoden ausgedrückt werden | wird abgeschafft |
| **Connect** | `POST /Dienst/Methode` mit JSON im Body; aufrufbar mit `curl` ebenso wie mit `fetch` im Browser | ja (**gewählt**) |
| **gRPC** | Dasselbe Prinzip aus Dienst und Methode, aber über binäres protobuf und HTTP/2; schnell und gut für Streaming geeignet | ja (**zwischen Diensten**) |
| gRPC-web | Eine für den Browser angepasste Variante von gRPC | ja (bei Bedarf) |
| GraphQL | Abfragesprache, mit der man genau die benötigten Felder anfordert | teilweise (**nur für lesende Abfragen**) |
| WASM | Führt Rust-Code direkt im Browser aus | nein (Technik für die Oberfläche) |

- **APIs, die von Browseroberflächen oder per `curl` aufgerufen werden, verwenden Connect** (POST; JSON wird mit RS-JSON gelesen und geschrieben). WASM im Browser kann kein reines gRPC sprechen. Mit Connect bleibt es bei einem gewöhnlichen `fetch`, und `prost` ist nicht nötig – die WASM-Datei wird dadurch nicht größer.
- **Für die Kommunikation zwischen Diensten (Server zu Server, rechenintensive Aufgaben, Streaming) wird gRPC eingesetzt.** In den meisten Fällen reicht Connect aus; auf gRPC wird nur dort umgestellt, wo Streaming tatsächlich gebraucht wird.
- **GraphQL dient ausschließlich lesenden Abfragen**, wenn mehrere Informationen gebündelt abgefragt werden sollen. Für Schreibzugriffe (Operationen) wird es nicht verwendet.
- **WASM bleibt die Technik für die Oberfläche.** Geändert hat sich lediglich, dass die aufgerufene API nun auf Connect beruht.
- Schnittstellen, deren Form durch einen externen Standard festgelegt ist (ACME, OAuth-Callbacks, Webhooks von Drittanbietern, Health-Checks, statische Dateien, OTLP), bleiben gewöhnliches HTTP.
- **Im Zweifel: Connect.**

### Русский (перевод выполнен с помощью ИИ и литературно отредактирован; носителями языка пока не проверен)
**Это не варианты, из которых нужно выбрать один, а технологии разных уровней.** Заменить REST могут только Connect, gRPC и GraphQL; WASM же — это способ создания пользовательского интерфейса.

| Термин | Что это | Заменяет REST? |
|---|---|---|
| REST | Стиль построения API, при котором операции выражаются через URL и HTTP-методы | отменяется |
| **Connect** | `POST /Сервис/Метод` с телом в формате JSON; вызывается как из `curl`, так и из браузерного `fetch` | да (**выбран**) |
| **gRPC** | Тот же принцип «сервис — метод», но поверх двоичного формата protobuf и HTTP/2; работает быстро и хорошо подходит для потоковой передачи | да (**для связи между сервисами**) |
| gRPC-web | Адаптированный для браузера вариант gRPC | да (при необходимости) |
| GraphQL | Язык запросов: клиент запрашивает ровно те поля, которые ему нужны | частично (**только запросы на чтение**) |
| WASM | Позволяет выполнять код на Rust прямо в браузере | нет (технология для интерфейса) |

- **API, которые вызываются из браузерных интерфейсов или через `curl`, строятся на Connect** (POST; JSON читается и записывается через RS-JSON). Браузерный WASM не умеет работать с «чистым» gRPC. С Connect достаточно обычного `fetch`, а `prost` не требуется — размер WASM-файла не увеличивается.
- **Для обмена между сервисами (сервер — сервер, ресурсоёмкие задачи, потоковая передача) применяется gRPC.** В большинстве случаев достаточно Connect; на gRPC переходят только там, где потоковая передача действительно необходима.
- **GraphQL используется только для чтения**, когда нужно получить сразу несколько связанных данных. Для записи (операций) он не применяется.
- **WASM по-прежнему остаётся технологией для интерфейса.** Изменилось лишь то, что вызываемый им API теперь построен на Connect.
- Интерфейсы, форма которых задана внешним стандартом (ACME, обратные вызовы OAuth, вебхуки сторонних сервисов, проверки работоспособности, статические файлы, OTLP), остаются обычным HTTP.
- **Если есть сомнения — выбирайте Connect.**
