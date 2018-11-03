---
title: RDS のプログラミング モデルの詳細
TOCTitle: RDS programming model in detail
ms:assetid: 133fc059-9b51-52e2-2e61-339716d8d965
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248906(v=office.15)
ms:contentKeyID: 48543364
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b152715c104c9c3a4d503254d0dc36622e29006c
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943830"
---
# <a name="rds-programming-model-in-detail"></a>RDS のプログラミング モデルの詳細

**適用されます**Access 2013、Office 2013。

RDS プログラミング モデルの主な要素は以下のとおりです。

- RDS.インスタンス
- RDSServer.DataFactory
- RDS.DataControl
- イベント

## <a name="rdsdataspace"></a>RDS.インスタンス

クライアント アプリケーションでは、サーバーおよび呼び出すサーバー プログラムを指定する必要があります。それに対し、クライアント アプリケーションはサーバー プログラムへの参照を受け取り、その参照をサーバー プログラムそのものと同じように扱うことができます。

RDS オブジェクト モデルでは、この機能は [RDS.DataSpace](dataspace-object-rds.md) オブジェクトに組み込まれています。

サーバー プログラムは、プログラム識別子 (*ProgID*) で指定します。サーバーは、*ProgID* とサーバー コンピューターのレジストリを使用して、実際に起動するプログラムに関する情報を検索します。

RDS は、サーバー プログラムを、インターネットまたはイントラネット上のリモート サーバー、ローカル エリア ネットワーク上のサーバー、またはサーバーではなくローカルのダイナミック リンク ライブラリ (DLL) のどこに存在するかによって、内部的に区別します。この区別に基づいて、クライアントとサーバーとの間で情報を交換する方法を決定し、クライアント アプリケーションに返される参照の種類を明確に区別します。ただし、ユーザーにとっては、この区別は特別な意味を持ちません。ユーザーにとって重要なのは、使用可能なプログラム参照を受け取るということだけです。

## <a name="rdsserverdatafactory"></a>RDSServer.DataFactory

RDS が提供する既定のサーバー プログラムは、データ ソースに対して SQL クエリを実行して [Recordset](recordset-object-ado.md) オブジェクトを返すか、または **Recordset** オブジェクトを受け取ってデータ ソースを更新することができます。

RDS オブジェクト モデルでは、この機能は [RDSServer.DataFactory](datafactory-object-rdsserver.md) オブジェクトに組み込まれています。

さらにこのオブジェクトは、プログラムを使用して入力できる空の**レコード セット**オブジェクトを作成するためのメソッド ([CreateRecordset](createrecordset-method-rds.md)) と ([の web ページを作成するテキスト文字列、**レコード セット**オブジェクトに変換するための別の方法ConvertToString](converttostring-method-rds.md))。

ADO では、 **DataFactory** ハンドラーの **RDSServer.DataFactory** の既定の接続およびコマンドの動作の一部、および接続、コマンド、セキュリティなどのパラメーターが格納されたカスタマイズ ファイルを無効にすることができます。

サーバー プログラムは、*ビジネス オブジェクト*とも呼ばれます。 複雑なデータ アクセスや妥当性検査を実行できる、独自のカスタム ビジネス オブジェクトを作成することができます。 カスタム ビジネス オブジェクトを作成する場合は、 **RDSServer.DataFactory**オブジェクトのインスタンスを作成およびそのメソッドの一部を使用して、独自のタスクを実行します。

## <a name="rdsdatacontrol"></a>RDS.DataControl

RDS では、 **RDS.DataSpace** と **RDSServer.DataFactory** の機能を組み合わせるための手段、およびクエリの結果としてデータ ソースから返される **Recordset** オブジェクトを、ビジュアル コントロールで容易に使用できるようにするための手段が提供されています。通常、RDS は、可能な限り自動的に、サーバー上の情報にアクセスしてビジュアル コントロールにその情報を表示しようとします。

RDS オブジェクト モデルでは、この機能は [RDS.DataControl](datacontrol-object-rds.md) オブジェクトに組み込まれています。

**RDS.DataControl** には 2 つの側面があります。1 つはデータ ソースに関する側面です。 **RDS.DataControl** の **Connect** プロパティおよび **SQL** プロパティを使用して、コマンドおよび接続の情報を設定すると、自動的に **RDS.DataSpace** が使用されて、既定の **RDSServer.DataFactory** オブジェクトへの参照が作成されます。その後、 **RDSServer.DataFactory** は、 **Connect** プロパティの値を使用してデータ ソースに接続し、 **SQL** プロパティの値を使用してデータ ソースから **Recordset** を取得して、 **Recordset** オブジェクトを **RDS.DataControl** に返します。

もう 1 つの側面は、返された **Recordset** 情報のビジュアル コントロールでの表示に関するものです。 **Rds. のビジュアル コントロールを関連付けることができます。DataControl** (バインドと呼ばれるプロセス) で、Microsoft Internet Explorer で web ページのクエリ結果を表示する、関連付けられた**レコード セット**オブジェクト内の情報にアクセスします。 各 **RDS.DataControl** オブジェクトは、単一のクエリの結果を表す 1 つの **Recordset** オブジェクトを、1 つまたは複数のビジュアル コントロール (テキスト ボックス、コンボ ボックス、グリッド コントロールなど) にバインドします。 各ページに複数の **RDS.DataControl** オブジェクトが存在する場合があります。 それぞれの **RDS.DataControl** オブジェクトを異なるデータ ソースに接続し、別のクエリの結果を取得することができます。

また、 **RDS.DataControl** オブジェクトには、関連する **Recordset** オブジェクトの行に対して移動、並べ替え、およびフィルター選択を行うためのメソッドがあります。これらのメソッドは、ADO の **Recordset** オブジェクトのメソッドと似ていますが、同じではありません。

## <a name="events"></a>イベント

RDS は、2 種類の独自のイベントをサポートしています。 [OnReadyStateChange](onreadystatechange-event-rds.md)イベントが呼び出されたときに**の rds.DataControl** [ReadyState](readystate-property-rds.md)プロパティの変更、非同期操作が正常に完了を通知する、終了、またはエラーが発生しました。 [onError](onerror-event-rds.md) イベントはエラーが発生するたびに (エラーが非同期操作の途中で発生した場合でも) 呼び出されます。


> [!NOTE]
> <P>[!メモ] Microsoft Internet Explorer は、 <STRONG>onDataSetChanged</STRONG> ( <STRONG>Recordset</STRONG> は有効だが、まだ行を取得している) および <STRONG>onDataSetComplete</STRONG> ( <STRONG>Recordset</STRONG> は行の取得を終了した) という 2 つの追加イベントを提供します。</P>


