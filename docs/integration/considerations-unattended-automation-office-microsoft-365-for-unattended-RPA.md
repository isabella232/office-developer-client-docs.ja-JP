---
title: 無人 RPA 環境での自動OfficeのMicrosoft 365に関する考慮事項
ms.date: 03/30/2020
ms.audience: Developer
localization_priority: Normal
description: 無人 RPA 環境OfficeのMicrosoft 365自動化に関する考慮事項。
ms.openlocfilehash: 576217fc85f2980a6d2451e3f930296ea4c11a56
ms.sourcegitcommit: 007aa2ceb4f569201c3f4372de5c83b6c61f8875
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "43103051"
---
# <a name="considerations-for-unattended-automation-of-office-in-the-microsoft-365-for-unattended-rpa-environment"></a>無人 RPA 環境での自動OfficeのMicrosoft 365に関する考慮事項

無人 RPA の Microsoft 365 には、ユーザーが存在しない Office の自動化を可能にするライセンスが提供されています。Office のすべての現在のバージョンは、アプリケーションのインターフェイスを操作するために存在するユーザーが存在するクライアント ワークステーション上でエンド ユーザー製品として実行するように設計され、テストされました。 ユーザーが存在しないアプリケーションの使用に起因する予期しない動作は、欠陥ではありません。 この構成でOfficeする場合は、アプリケーション ロジックでこれらの予期しない動作を考慮する準備が必要です。

この記事では、この方法を使用する場合に役立つ、Office自動化に関する考慮事項の一部について説明します。 ただし、この構成でのOfficeは厳密に "AS IS" であり、これらの予期しない動作を考慮する必要があります。 ここで提供される情報は網羅的な情報ではなく、すべてのクライアントのすべての問題を解決する保証はありません。 展開する前に、ソリューションを徹底的にテストしてください。

## <a name="common-problems-in-unattended-automation"></a>無人オートメーションの一般的な問題

ユーザーが存在しない場合Officeを使用する場合は、ユーザーが想定とは異なる動作をOffice領域に注意してください。 ソリューションを正常に実行するには、これらの問題に対処し、可能な限り効果を最小限に抑える必要があります。 アプリケーションをビルドする際には、これらの問題を慎重に検討してください。

### <a name="interactive-ui-elements"></a>対話型 UI 要素

Officeアプリケーションは、対話的に実行されている必要があります。 予期しないエラーが発生した場合、または関数を完了するために指定されていないパラメーターが必要な場合は、Office は、続行方法をユーザーに求めるダイアログ ボックスをユーザーに表示するように設計されています。 無人オートメーションでは、この入力を受け取るまでアプリケーションが停止すると、アプリケーションが "ハング" する可能性があります。 パブリック API を使用して Officeを自動化する場合は[、Application.DisplayAlerts](https://docs.microsoft.com/office/vba/api/word.application.displayalerts)や[Application.AutomationSecurity](https://docs.microsoft.com/office/vba/api/word.application.automationsecurity)のようなプロパティを適切に構成することで、これらのアラートの多くを抑制できます。 コードは、ブロック通知をいつでも識別して処理するように設計する必要があります。

### <a name="user-identity"></a>ユーザー ID

Officeオートメーションを使用してアプリケーションを開始する場合でも、アプリケーションの実行時にユーザー ID が必要です。 このユーザー ID によって、以下の一部またはすべてが発生する可能性があります。

- 処理する必要がある追加のサインイン UI の存在。
- ユーザーごとのアクセス許可に基づいて開く、または編集できないファイル。
- ファイルのメタデータに対する予期しない変更 (たとえば、自動アプリケーション インスタンスのユーザー ID に基づいて特定のファイル プロパティが更新されます)。

さまざまなアプローチは、これらの問題を軽減するのに役立ちます。たとえば、ドキュメント インスペクターを [実行してメタデータ](https://docs.microsoft.com/office/vba/library-reference/concepts/using-the-document-inspector) を削除します。 これらのアプローチがシナリオに基づいて適切かどうかを検討します。

### <a name="server-side-security"></a>サーバー側のセキュリティ

無人でOfficeファイル コンテンツを処理する場合、それらのファイルに格納されているマクロが読み込みおよび実行されるのを防ぐために、その環境に固有の追加の保護は使用できません。 Office、コードから意図せずにマクロを実行したり、マクロを実行する可能性がある別のサーバーを起動したりから保護したりしません。 [Application.AutomationSecurity](https://docs.microsoft.com/office/vba/api/word.application.automationsecurity)のようなプロパティを使用してこのリスクを軽減できますが、信頼できるコンテンツのみを読み込む必要があります。

さらに、Officeは、クライアントの認証情報をキャッシュして処理を高速化できる多くのコンポーネント (Simple MAPI、WinInet、MSDAIPP など) を使用します。 サーバー Office自動化され、複数のファイルを処理する場合、そのセッションに対して認証情報がキャッシュされている場合、あるクライアントは別のクライアントのキャッシュされた資格情報を使用できます。 そのため、クライアントは他のユーザーを偽装して、許可されていないアクセス許可を取得できます。

### <a name="ui-changes"></a>UI の変更

Office の UI 要素は大きく安定していますが、UI 要素の特定の場所は保証されません。ユーザー フィードバックを組み込み、顧客のニーズを満たすために製品設計が進化するにつれて変化する可能性があります。 自動化のロジックは、これを考慮する必要があります。 これらの変更により、ボタンまたはグループ タブの名前付けの変更、タブ間のコマンドの移動、新しいタブの追加、または機能廃止ポリシーに合わせてコマンドが削除される可能性があります。 これらの変更は、UI およびアプリケーションによって提供されるアクセシビリティ情報内で行う場合があります。この情報は、ユーザービリティを向上させるために変更され、継続的な顧客からのフィードバックを考慮し、異なるユーザーに対して異なる時間に展開される可能性があります。

製品の変更がない場合でも、システム環境 (画面サイズ、解像度、DPI など) の違いにより、画面のアイテムの場所が変更される可能性があります。 ユーザー入力をシミュレートするために画面座標に依存する方法は、これらの変更を考慮し、対応する必要があります。

### <a name="single-threading"></a>シングル スレッド

Officeアプリケーションは、単一のクライアントに多様でリソースを消費する機能を提供するように設計された、再入可能でない STA ベースのアプリケーションです。 アプリケーションは、メモリ マップされたファイル、グローバル アドインまたはテンプレート、共有オートメーション サーバーなどのグローバル リソースを使用します。 これにより、同時に実行できるインスタンスの数が制限され、アプリケーションがマルチクライアント環境で構成されている場合、競争状態が発生する可能性があります。 任意の Office アプリケーションの複数のインスタンスを実行する予定の場合は、仮想マシン レベルで分離して、結果のソリューションの安定性を確保する必要があります。

### <a name="resiliency-and-stability"></a>復元性と安定性

上記の考慮事項を考慮しても、ユーザー入力をシミュレートする方法でアプリケーションが自動化されている場合や、対話型の使用を大幅に超えるセッション長の場合は、対話的に実行するときに存在しない問題が発生する可能性があります。 このコンテキストで Office を使用するソリューションは、アプリケーションの状態を監視し、必要に応じて再起動するメカニズム (および/または実行している仮想マシン) を事前に構築する必要があります。

## <a name="suggested-alternatives"></a>推奨される代替案

microsoft では、Office をインストールしてサーバー側で実行する必要がなく、この構成の自動化よりも効率的かつ迅速に一般的なタスクを実行できるいくつかの代替手段を強く推奨しています。 プロジェクトでサーバー Officeコンポーネントとして使用する前に、代替案を検討してください。

### <a name="microsoft-graph"></a>Microsoft Graph

Microsoft Graph API は、ユーザーのメール/カレンダー/連絡先/ファイルへのアクセス、ドキュメント変換、Excel ブックの計算など、無人オートメーションのニーズをサポートする多くのサービスを含む、Microsoft クラウドの一部としてユーザーおよびソリューションが利用できるサービス、データ、およびインテリジェンスへのアクセスを提供します。 これらのサービスは、無人使用と大規模アクセス用に設計され、標準の RESTful API 構文を使用します。 Microsoft Graphおよびユーザーのデータを使用する方法の詳細については、以下を参照してください。

- [Microsoft Graph の概要](https://docs.microsoft.com/graph/overview) 
- [Microsoft Graph の概要](https://developer.microsoft.com/graph/get-started)
- [別の形式でファイルをダウンロード](https://docs.microsoft.com/graph/api/driveitem-get-content-format?view=graph-rest-1.0&tabs=http) する (ファイル変換)
- [Microsoft ExcelでのGraph操作](https://docs.microsoft.com/graph/api/resources/excel?view=graph-rest-1.0)(ブックの詳細)

### <a name="open-xml-file-formats"></a>XML ファイル形式を開く

多くのオートメーション タスクには、ドキュメントの作成または編集が含まれます。 Officeは、ISO 29500 国際標準で定義されている標準の XML および ZIP テクノロジを使用して、開発者がファイル コンテンツを作成、編集、読み取り、変換できる Open XML ファイル形式をサポートしています。 これらのファイル形式は、Microsoft .NET 3.x Framework の System.IO.Package.IO 名前空間を含む、任意の ZIP/XML ツールを介して操作できます。 ファイル形式の直接編集は、サービスからのファイルの変更を処理するために推奨され、サポートOffice方法です。

Microsoft は、.NET 3.x Framework から Open XML ファイル形式を操作するための SDK を提供しています。 SDK の詳細と SDK を使用して Open XML ファイルを作成または編集する方法については、次のトピックを参照してください。

- [Open XML ファイル形式について](https://docs.microsoft.com/office/open-xml/understanding-the-open-xml-file-formats)
- [Open XML SDK 2.5 for Office](https://docs.microsoft.com/office/open-xml/open-xml-sdk)
