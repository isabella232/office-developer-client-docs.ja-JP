---
title: RDS プログラミング モデルの詳細
TOCTitle: RDS programming model in detail
ms:assetid: 133fc059-9b51-52e2-2e61-339716d8d965
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248906(v=office.15)
ms:contentKeyID: 48543364
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a3144f3f981d42868dfe2841ba9fd93dbb73c564
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597038"
---
# <a name="rds-programming-model-in-detail"></a>RDS プログラミング モデルの詳細

**適用先**: Access 2013、Office 2013

RDS プログラミング モデルの主な要素は以下のとおりです。

- RDS。DataSpace
- RDSServer.DataFactory
- RDS。DataControl
- イベント

## <a name="rdsdataspace"></a>RDS。DataSpace

クライアント アプリケーションでは、サーバーおよび呼び出すサーバー プログラムを指定する必要があります。それに対し、クライアント アプリケーションはサーバー プログラムへの参照を受け取り、その参照をサーバー プログラムそのものと同じように扱うことができます。

RDS オブジェクト モデルでは、この機能は [RDS.DataSpace](dataspace-object-rds.md) オブジェクトに組み込まれています。

サーバー プログラムは、プログラム識別子 (*ProgID*) で指定します。サーバーは、*ProgID* とサーバー コンピューターのレジストリを使用して、実際に起動するプログラムに関する情報を検索します。

RDS は、サーバー プログラムを、インターネットまたはイントラネット上のリモート サーバー、ローカル エリア ネットワーク上のサーバー、またはサーバーではなくローカルのダイナミック リンク ライブラリ (DLL) のどこに存在するかによって、内部的に区別します。この区別に基づいて、クライアントとサーバーとの間で情報を交換する方法を決定し、クライアント アプリケーションに返される参照の種類を明確に区別します。ただし、ユーザーにとっては、この区別は特別な意味を持ちません。ユーザーにとって重要なのは、使用可能なプログラム参照を受け取るということだけです。

## <a name="rdsserverdatafactory"></a>RDSServer.DataFactory

RDS が提供する既定のサーバー プログラムは、データ ソースに対して SQL クエリを実行して [Recordset](recordset-object-ado.md) オブジェクトを返すか、または **Recordset** オブジェクトを受け取ってデータ ソースを更新することができます。

RDS オブジェクト モデルでは、この機能は [RDSServer.DataFactory](datafactory-object-rdsserver.md) オブジェクトに組み込まれています。

さらに、このオブジェクトには、プログラムで入力できる空の **Recordset** オブジェクトを作成するメソッド [(CreateRecordset)](createrecordset-method-rds.md)と **、Recordset** オブジェクトをテキスト文字列に変換して Web ページ [(ConvertToString)](converttostring-method-rds.md)を作成するための別のメソッドがあります。

ADO では、 **DataFactory** ハンドラーの **RDSServer.DataFactory** の既定の接続およびコマンドの動作の一部、および接続、コマンド、セキュリティなどのパラメーターが格納されたカスタマイズ ファイルを無効にすることができます。

サーバー プログラムは、ビジネス オブジェクトと呼 *ばれる場合があります*。 You can write your own custom business object that can perform complicated data access, validity checks, and so on. Even when writing a custom business object, you can create an instance of an **RDSServer.DataFactory** object and use some of its methods to accomplish your own tasks.

## <a name="rdsdatacontrol"></a>RDS。DataControl

RDS では、 **RDS.DataSpace** と **RDSServer.DataFactory** の機能を組み合わせるための手段、およびクエリの結果としてデータ ソースから返される **Recordset** オブジェクトを、ビジュアル コントロールで容易に使用できるようにするための手段が提供されています。通常、RDS は、可能な限り自動的に、サーバー上の情報にアクセスしてビジュアル コントロールにその情報を表示しようとします。

RDS オブジェクト モデルでは、この機能は [RDS.DataControl](datacontrol-object-rds.md) オブジェクトに組み込まれています。

**RDS.DataControl** には 2 つの側面があります。1 つはデータ ソースに関する側面です。 **RDS.DataControl** の **Connect** プロパティおよび **SQL** プロパティを使用して、コマンドおよび接続の情報を設定すると、自動的に **RDS.DataSpace** が使用されて、既定の **RDSServer.DataFactory** オブジェクトへの参照が作成されます。その後、 **RDSServer.DataFactory** は、 **Connect** プロパティの値を使用してデータ ソースに接続し、 **SQL** プロパティの値を使用してデータ ソースから **Recordset** を取得して、 **Recordset** オブジェクトを **RDS.DataControl** に返します。

もう 1 つの側面は、返された **Recordset** 情報のビジュアル コントロールでの表示に関するものです。 ビジュアル コントロールを **RDS に関連付けできます。DataControl** (バインドと呼ばれるプロセス) と関連付けられた **Recordset** オブジェクト内の情報にアクセスし、Microsoft Internet Explorer の Web ページにクエリ結果を表示します。 各 **RDS.DataControl** オブジェクトは、単一のクエリの結果を表す 1 つの **Recordset** オブジェクトを、1 つまたは複数のビジュアル コントロール (テキスト ボックス、コンボ ボックス、グリッド コントロールなど) にバインドします。 各ページに複数の **RDS.DataControl** オブジェクトが存在する場合があります。 それぞれの **RDS.DataControl** オブジェクトを異なるデータ ソースに接続し、別のクエリの結果を取得することができます。

また、 **RDS.DataControl** オブジェクトには、関連する **Recordset** オブジェクトの行に対して移動、並べ替え、およびフィルター選択を行うためのメソッドがあります。これらのメソッドは、ADO の **Recordset** オブジェクトのメソッドと似ていますが、同じではありません。

## <a name="events"></a>イベント

RDS は、2 種類の独自のイベントをサポートしています。 [onReadyStateChange](onreadystatechange-event-rds.md)イベントは **、RDS のたびに呼び出されます。DataControl** [ReadyState](readystate-property-rds.md)プロパティが変更され、非同期操作が正常に完了、終了、またはエラーが発生した場合に通知されます。 [onError](onerror-event-rds.md) イベントはエラーが発生するたびに (エラーが非同期操作の途中で発生した場合でも) 呼び出されます。

> [!NOTE]
> [!メモ] Microsoft Internet Explorer は、 **onDataSetChanged** ( **Recordset** は有効だが、まだ行を取得している) および **onDataSetComplete** ( **Recordset** は行の取得を終了した) という 2 つの追加イベントを提供します。


