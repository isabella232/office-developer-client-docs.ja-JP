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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709783"
---
# <a name="datacontrol-object-rds"></a>DataControl オブジェクト (RDS)

**適用されます**Access 2013、Office 2013。

1 つまたは複数のコントロール (たとえば、テキスト ボックス、グリッド コントロール、またはコンボ ボックス) web ページの**レコード セット**データを表示するには、データ クエリ[のレコード セット](recordset-object-ado.md)をバインドします。

## <a name="syntax"></a>構文

```vb
    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DataControl"
       <PARAM NAME="Connect" VALUE="DSN=DSNName;UID=usr;PWD=pw;">
       <PARAM NAME="Server" VALUE="https://awebsrvr">
       <PARAM NAME="SQL" VALUE="QueryText">
    </OBJECT>
```

## <a name="remarks"></a>備考

**RDS.DataControl** オブジェクトのクラス ID は、BD96C556-65A3-11D0-983A-00C04FC29E33 です。

> [!NOTE]
> [!メモ] [RDS.DataSpace](dataspace-object-rds.md) オブジェクトまたは **RDS.DataControl** オブジェクトを読み込むことができないというエラーが発生した場合は、正しいクラス ID を使用していることを確認してください。これらのオブジェクトのクラス ID は、バージョン 1.0 とバージョン 1.1 から変更されています。

基本的なシナリオでは、既定のビジネス オブジェクトの **RDSServer.DataFactory** を自動的に呼び出す、 **RDS.DataControl** オブジェクトの **SQL** 、 **Connect** 、および [Server](datafactory-object-rdsserver.md) の各プロパティのみ設定する必要があります。

**RDS.DataControl** のすべてのプロパティは、カスタムのビジネス オブジェクトでその機能を置き換えられるため省略可能です。

> [!NOTE]
> [!メモ] 複数の結果を求めるクエリを実行すると、最初の [Recordset](recordset-object-ado.md) のみ取得されます。 複数の結果セットが必要な場合は、それぞれを独自の **DataControl** に割り当てます。 
> 
> 複数の結果のクエリの例は以下である可能性があります: `"Select * from Authors, Select * from Topics"`。

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

  - 2 つの追加**rds.DataControl**オブジェクトを web ページにします。

  - 2 つの **RDS.DataControl** オブジェクトの各 **SQL** プロパティに 1 つずつ、合計 2 つのクエリを記述します。1 つ目の **RDS.DataControl** オブジェクトには、顧客の情報を要求する SQL クエリを、2 つ目のオブジェクトには、顧客が購入した商品の一覧を要求するクエリを格納します。

  - 連結コントロールの各 OBJECT タグで、DATAFLD 値を指定して、各ビジュアル コントロールに表示するデータの値を設定します。

**Rds. 数のカウントの制限はありません。DataControl**オブジェクトを 1 つの web ページ上のオブジェクト タグを使用して埋め込むことができます。

Rds. の**を定義する場合DataControl** web ページ上のオブジェクト、1、0 以外の**幅**と**高さ**の値を使用して、避けるために余分なスペースを含めること)。

リモート データ サービスのクライアント コンポーネントは、Internet Explorer 4.0 の一部として既に組み込まれています。このため、 **RDS.DataControl** オブジェクトのタグに、CODEBASE パラメーターを含める必要はありません。

Internet Explorer 4.0 以降では、アパートメント モデル コントロールとしてマークされている場合にのみ、HTML コントロールおよび ActiveX コントロールを使用してデータにバインドできます。

**Microsoft Visual Basic のユーザー****Rds.DataControl** 、web ベースのアプリケーションでのみ使用します。 Visual Basic クライアント アプリケーションでは不要です。

