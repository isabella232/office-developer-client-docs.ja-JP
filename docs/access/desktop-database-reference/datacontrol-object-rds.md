---
title: DataControl オブジェクト (RDS)
TOCTitle: DataControl object (RDS)
ms:assetid: ac430669-7628-696c-c036-b5d35405d788
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249801(v=office.15)
ms:contentKeyID: 48547001
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2ffe674f3aa02e5cc8b1f89375ca66b4efa623f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294520"
---
# <a name="datacontrol-object-rds"></a>DataControl オブジェクト (RDS)

**適用先:** Access 2013、Office 2013

データクエリ[recordset](recordset-object-ado.md)を1つまたは複数のコントロール (テキストボックス、グリッドコントロール、コンボボックスなど) にバインドして、web ページに**Recordset**データを表示します。

## <a name="syntax"></a>構文

```vb
    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DataControl"
       <PARAM NAME="Connect" VALUE="DSN=DSNName;UID=usr;PWD=pw;">
       <PARAM NAME="Server" VALUE="https://awebsrvr">
       <PARAM NAME="SQL" VALUE="QueryText">
    </OBJECT>
```

## <a name="remarks"></a>注釈

**RDS.DataControl** オブジェクトのクラス ID は、BD96C556-65A3-11D0-983A-00C04FC29E33 です。

> [!NOTE]
> [!メモ] [RDS.DataSpace](dataspace-object-rds.md) オブジェクトまたは **RDS.DataControl** オブジェクトを読み込むことができないというエラーが発生した場合は、正しいクラス ID を使用していることを確認してください。これらのオブジェクトのクラス ID は、バージョン 1.0 とバージョン 1.1 から変更されています。

基本的なシナリオでは、既定のビジネス オブジェクトの **RDSServer.DataFactory** を自動的に呼び出す、 **RDS.DataControl** オブジェクトの **SQL** 、 **Connect** 、および [Server](datafactory-object-rdsserver.md) の各プロパティのみ設定する必要があります。

**RDS.DataControl** のすべてのプロパティは、カスタムのビジネス オブジェクトでその機能を置き換えられるため省略可能です。

> [!NOTE]
> [!メモ] 複数の結果を求めるクエリを実行すると、最初の [Recordset](recordset-object-ado.md) のみ取得されます。 複数の結果セットが必要な場合は、それぞれを独自の **DataControl** に割り当てます。 
> 
> 複数の結果に対するクエリの例は、次のよう`"Select * from Authors, Select * from Topics"`になります。

**RDS.DataControl** オブジェクトを使用する場合、接続文字列に "DFMode=20;" を追加すると、データ更新時のサーバーのパフォーマンスを向上させることができます。この設定によって、サーバー上の **RDSServer.DataFactory** オブジェクトはリソース消費量の少ないモードを使用します。ただし、この設定では次の機能は使用できません。

  - パラメーター クエリを使用する。

  - **Execute** メソッドを呼び出す前に、パラメーターまたは列の情報を取得する。

  - **Transact Updates** を **True** に設定する。

  - 行のステータスを取得する。

  - [Resync](resync-method-ado.md) メソッドを呼び出す。

  - [Update Resync](update-resync-property-dynamic-ado.md) プロパティによって明示的または自動的に更新する。

  - **Command** プロパティまたは [Recordset](recordset-sourcerecordset-properties-rds.md) プロパティを設定する。

  - **adCmdTableDirect** を使用する。

**RDS.DataControl** オブジェクトは、既定では非同期モードで実行されます。アプリケーションを同期モードで実行する必要がある場合は、次の例で示すように、 [ExecuteOptions](executeoptions-property-rds.md) パラメーターを **adcExecSync** と同じ値に、 [FetchOptions](fetchoptions-property-rds.md) パラメーターを **adcFetchUpFront** と同じ値に設定します。

```vb
    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
        ID="DataControl"
       <PARAM NAME="Connect" VALUE="DSN=DSNName;UID=usr;PWD=pw;">
       <PARAM NAME="Server" VALUE="https://awebsrvr">
       <PARAM NAME="SQL" VALUE="QueryText">
       <PARAM NAME="ExecuteOptions" VALUE="1">
       <PARAM NAME="FetchOptions" VALUE="1">
    </OBJECT>
```

単一のクエリの結果を 1 つまたは複数のビジュアル コントロールにリンクするには、1 つの **RDS.DataControl** オブジェクトを使用します。たとえば、名前、住居、出生地、年齢、優先得意先ステータスなどの顧客データを要求するクエリのコードを作成するとします。この場合、1 つの **RDS.DataControl** オブジェクトを使用して、顧客の名前、年齢、地域を 3 つの異なるテキスト ボックスに、優先顧客ステータスを 1 つのチェック ボックスに、すべてのデータをグリッド コントロールに表示できます。

複数のクエリの結果を異なるビジュアル コントロールにリンクするには、異なる **RDS.DataControl** オブジェクトを使用します。たとえば、1 つ目のクエリを使用して得意先に関する情報を取得し、2 つ目のクエリを使用して得意先が購入した商品に関する情報を取得するとします。最初のクエリの結果を 3 つのテキスト ボックスと 1 つのチェック ボックスに、2 つ目のクエリの結果をグリッド コントロールに表示します。既定のビジネス オブジェクト (**RDSServer.DataFactory**) を使用する場合、次のような操作を実行する必要があります。

  - 2つ**の RDS を追加します。DataControl**オブジェクトを web ページにします。

  - 2 つの **RDS.DataControl** オブジェクトの各 **SQL** プロパティに 1 つずつ、合計 2 つのクエリを記述します。1 つ目の **RDS.DataControl** オブジェクトには、顧客の情報を要求する SQL クエリを、2 つ目のオブジェクトには、顧客が購入した商品の一覧を要求するクエリを格納します。

  - 連結コントロールの各 OBJECT タグで、DATAFLD 値を指定して、各ビジュアル コントロールに表示するデータの値を設定します。

RDS の数にはカウント制限はありません **。DataControl**オブジェクトタグを使用して1つの web ページに埋め込むことができます。

RDS を定義する場合 **。DataControl**オブジェクト。 web ページでは、1 (余分なスペースを含めない) のように、0以外の**高さ**と**幅**の値を使用します。

リモート データ サービスのクライアント コンポーネントは、Internet Explorer 4.0 の一部として既に組み込まれています。このため、 **RDS.DataControl** オブジェクトのタグに、CODEBASE パラメーターを含める必要はありません。

Internet Explorer 4.0 以降では、アパートメントモデルコントロールとしてマークされている場合にのみ、HTML コントロールと ActiveX コントロールを使用してデータにバインドできます。

**Microsoft Visual Basic ユーザー****RDS。DataControl**は、web ベースのアプリケーションでのみ使用されます。 Visual Basic クライアント アプリケーションでは不要です。

