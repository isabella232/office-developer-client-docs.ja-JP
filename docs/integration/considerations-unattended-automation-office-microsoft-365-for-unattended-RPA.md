---
title: 無人の RPA 環境での Microsoft 365 での Office の無人自動化に関する考慮事項
ms.date: 03/30/2020
ms.audience: Developer
localization_priority: Normal
description: 無人の RPA 環境での Microsoft 365 での Office の無人自動化に関する考慮事項。
ms.openlocfilehash: 576217fc85f2980a6d2451e3f930296ea4c11a56
ms.sourcegitcommit: 007aa2ceb4f569201c3f4372de5c83b6c61f8875
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "43103051"
---
# <a name="considerations-for-unattended-automation-of-office-in-the-microsoft-365-for-unattended-rpa-environment"></a>無人の RPA 環境での Microsoft 365 での Office の無人自動化に関する考慮事項

Microsoft 365 for 無人 RPA にはユーザーがいない状態で Office の自動化を有効にするライセンスが用意されていますが、現在のすべてのバージョンの Office は、ユーザーが存在し、アプリケーションのインターフェイスを操作するユーザーが存在するクライアントワークステーション上のエンドユーザー製品として実行されるように設計およびテストされています。 ユーザーが存在しないアプリケーションを使用した結果として生じる予期しない動作は、欠陥ではありません。 この構成で Office を実行するには、アプリケーションロジックでこれらの予期しない動作を考慮する準備が整っている必要があります。

この記事では、この方法を使用する場合に役立つ Office の無人自動化の考慮事項について概説します。 ただし、この構成での Office の使用は厳密に "その他" であり、これらの予期しない動作を考慮する必要があることに注意してください。 ここで提供されている情報は網羅的ではないため、すべてのクライアントのすべての問題を解決することは保証されません。 を展開する前に、ソリューションを徹底的にテストすることをお勧めします。

## <a name="common-problems-in-unattended-automation"></a>無人オートメーションでの一般的な問題

ユーザーが存在しない Office を使用する場合は、Office が想定どおりに動作しない以下の点に注意してください。 ソリューションを正常に実行するには、これらの問題に対処し、可能な限りその影響を最小限に抑える必要があります。 アプリケーションをビルドするときは、これらの問題を慎重に検討してください。

### <a name="interactive-ui-elements"></a>対話型 UI 要素

Office アプリケーションは、対話型で実行されることを前提としています。 予期しないエラーが発生した場合、または、関数の実行に必要なパラメーターが指定されていない場合、Office はユーザーに操作方法の確認を求めるダイアログボックスを表示するように設計されています。 無人オートメーションで、アプリケーションがこの入力を受け取るまで停止すると、アプリケーションが "ハング" したように表示されることがあります。 公開 Api を使用して Office を自動化している場合は、 [DisplayAlerts](https://docs.microsoft.com/office/vba/api/word.application.displayalerts)および[AutomationSecurity](https://docs.microsoft.com/office/vba/api/word.application.automationsecurity)などのプロパティを適切に構成することで、これらの通知の多くを抑制することができます。 コードは、いつでもブロックされる通知を識別して処理するように設計する必要があります。

### <a name="user-identity"></a>ユーザー id

Office アプリケーションは、オートメーション経由でアプリケーションが起動された場合でも、アプリケーションの実行時にユーザー id を必要とします。 このユーザー id は、次のいずれかまたはすべてを発生させることができます。

- 処理が必要な追加のサインイン UI があるかどうか。
- ユーザーごとのアクセス許可に基づいて開いたり、編集したりできないファイル。
- ファイルのメタデータに予期しない変更があります (たとえば、特定のファイルのプロパティは、自動アプリケーションインスタンスのユーザー id の id に基づいて更新されます)。

これらの問題を軽減するには、さまざまな方法が役立ちます。たとえば、[ドキュメント検査](https://docs.microsoft.com/office/vba/library-reference/concepts/using-the-document-inspector)を実行してメタデータを削除します。 これらの方法がシナリオに基づいて適切かどうかを検討します。

### <a name="server-side-security"></a>サーバー側のセキュリティ

Office を無人で実行して、任意のファイルコンテンツを処理する場合、そのような環境では、そのようなファイルに格納されているマクロの読み込みと実行が行われないようにするための、その環境での追加の保護は Office では、コードから故意にマクロを実行したり、マクロを実行する別のサーバーを起動したりすることはできません。 [AutomationSecurity](https://docs.microsoft.com/office/vba/api/word.application.automationsecurity)のようなプロパティを使用してこのリスクを軽減できますが、必ず信頼できるコンテンツのみを読み込むようにする必要があります。

さらに、Office では、クライアント認証情報をキャッシュして処理を高速化できる、多くのコンポーネント (簡易 MAPI、WinInet、MSDAIPP など) を使用しています。 Office が自動サーバー側で、複数のファイルを処理している場合、そのセッションに対して認証情報がキャッシュされていると、1つのクライアントは別のクライアントのキャッシュされた資格情報を使用できます。 そのため、クライアントは他のユーザーを偽装することによって、付与されていないアクセス許可を取得できます。

### <a name="ui-changes"></a>UI の変更

Office の UI 要素は基本的に安定していますが、UI 要素の特定の場所は保証されず、ユーザーフィードバックを組み込んでユーザーのニーズを満たすために製品設計が発展するにつれて変わる可能性があります。 自動化のロジックでは、このことを考慮する必要があります。 これらの変更により、ボタンまたはグループタブの名前変更、タブ間のコマンドの移動、新しいタブの追加、または機能が廃止された機能に合わせたコマンドの削除が行われることがあります。 これらの変更は、アプリケーションによって提供されるアクセシビリティ情報に加えて、その情報が変更されて、ユーザーからの継続的なフィードバックの利便性が向上し、さまざまなユーザーに対して異なる時間に展開される可能性があります。

製品の変更がなくても、システム環境 (画面のサイズ/解像度/DPI など) の違いによって、画面上のアイテムの位置が変更されることがあります。 画面座標に依存してユーザー入力をシミュレートする方法では、これらの変更を考慮し、それに応じて適応する必要があります。

### <a name="single-threading"></a>シングルスレッド

Office アプリケーションは、単一のクライアントに対して、リソースを多用するさまざまな機能を提供するように設計された、再入可能ではない STA ベースのアプリケーションです。 このアプリケーションでは、メモリマップトファイル、グローバルアドイン、テンプレート、共有されたオートメーションサーバーなどのグローバルリソースを使用します。 これにより、同時に実行できるインスタンスの数を制限したり、multiclient 環境でアプリケーションが構成されている場合に競合状態を発生させることができます。 Office アプリケーションの複数のインスタンスを実行することを計画している場合は、それらを仮想マシンレベルで分離して、結果として得られるソリューションの安定性を確保するように計画する必要があります。

### <a name="resiliency-and-stability"></a>復元性と安定性

前述の考慮事項を使用している場合でも、アプリケーションが自動化されている場合は、ユーザー入力をシミュレートする方法、または対話的な使用率を大幅に超えたセッションの長さが必要になる場合がありますが、対話的に実行した場合には発生しません。 このコンテキストで Office を使用するソリューションでは、必要に応じて、アプリケーションの状態を監視し、それらを (またはその両方を実行している仮想マシンを) 再起動するメカニズムを事前に構築する必要があります。

## <a name="suggested-alternatives"></a>推奨候補

Microsoft では、Office をインストールしてサーバー側を実行する必要がないいくつかの方法をお勧めします。これにより、この構成の自動化よりも、一般的なタスクをより効率的かつ迅速に実行できます。 Office をプロジェクトのサーバー側コンポーネントとして使用する前に、代替手段を検討してください。

### <a name="microsoft-graph"></a>Microsoft Graph

Microsoft Graph API は、Microsoft クラウドの一部として提供されるサービス、データ、およびインテリジェンスへのアクセスを提供します。これには、無人自動化のニーズをサポートする多くのサービス (ユーザーのメール/予定表/連絡先/ファイルへのアクセス、ドキュメント変換、Excel ブックの計算など) があります。 これらのサービスは、無人使用および大規模なアクセスのために設計されており、標準の RESTful API 構文を使用します。 Microsoft Graph の詳細と、これを使用してユーザーのデータを操作する方法については、次を参照してください。

- [Microsoft Graph の概要](https://docs.microsoft.com/graph/overview) 
- [Microsoft Graph の概要](https://developer.microsoft.com/graph/get-started)
- [別の形式でファイルをダウンロードする](https://docs.microsoft.com/graph/api/driveitem-get-content-format?view=graph-rest-1.0&tabs=http)(ファイルの変換)
- [Microsoft Graph での Excel](https://docs.microsoft.com/graph/api/resources/excel?view=graph-rest-1.0)の使用 (ブックの詳細)

### <a name="open-xml-file-formats"></a>Open XML ファイル形式

多くの自動化タスクには、ドキュメントの作成や編集が含まれます。 Office は Open XML ファイル形式をサポートしており、開発者は、ISO 29500 International 標準で定義されている標準 XML および ZIP テクノロジを使用して、ファイルコンテンツを作成、編集、読み取り、および変換できます。 これらのファイル形式は、Microsoft .NET 3 .x フレームワークの System.IO.Package.IO 名前空間を含む、任意の ZIP/XML ツールを使用して操作できます。 サービスから Office ファイルへの変更を処理するには、ファイル形式を直接編集することをお勧めし、サポートされている方法を使用することをお勧めします。

Microsoft では、.NET 3.x フレームワークから Open XML ファイル形式を操作するための SDK を提供しています。 SDK の詳細と、SDK を使用して Open XML ファイルを作成または編集する方法については、次を参照してください。

- [Open XML ファイル形式について](https://docs.microsoft.com/office/open-xml/understanding-the-open-xml-file-formats)
- [Open XML SDK 2.5 for Office へようこそ](https://docs.microsoft.com/office/open-xml/open-xml-sdk)
