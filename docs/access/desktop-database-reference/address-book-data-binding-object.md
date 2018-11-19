---
title: アドレス帳のデータバインディング オブジェクト
TOCTitle: Address Book Data-Binding object
ms:assetid: cf43f645-1ee1-8655-eb70-86d601e9f3f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250030(v=office.15)
ms:contentKeyID: 48547807
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bc8fe1fa2addab5338d7c330d90e8616f0af9b5c
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025715"
---
# <a name="address-book-data-binding-object"></a>アドレス帳のデータバインディング オブジェクト


**適用されます**Access 2013、Office 2013。

Address Book アプリケーションでは、[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを使って、SQL Server データベースのデータをクライアントの HTML ページに表示されるオブジェクト (この場合は DHTML テーブル) にバインドします。イベントドリブン型の VBScript プログラム ロジックでは、 [RDS.DataControl](datacontrol-object-rds.md) を使って次の処理を行います。

  - データベースのクエリ、データベースへの更新の送信、およびデータ グリッドの更新を行います。

  - ユーザーがデータ グリッド内の最初のレコード、最後のレコード、または現在のレコードの前後のレコードに移動できるようにします。

次のコードで、 **RDS.DataControl** コンポーネントを定義します。

```vb 
 
<OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
   ID=DC1 Width=1 Height=1> 
   <PARAM NAME="SERVER" VALUE="https://<%=Request.ServerVariables("SERVER_NAME")%>"> 
   <PARAM NAME="CONNECT" VALUE="Provider=sqloledb; 
Initial Catalog=AddrBookDb;Integrated Security=SSPI;"> 
</OBJECT> 
```

OBJECT タグで、 **RDS.DataControl** コンポーネントをプログラム内に定義します。このタグには、次の 2 種類のパラメーターがあります。

  - 一般的な OBJECT タグに関連するパラメーター

  - **RDS.DataControl** オブジェクトに固有のパラメーター

## <a name="generic-object-tag-parameters"></a>一般的な OBJECT タグ パラメーター

次の表に、OBJECT タグに関連するパラメーターを示します。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>パラメーター</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><em>CLASSID</em></strong></p></td>
<td><p>一意の 128 ビットの数字で、システムの埋め込みオブジェクトの種類を識別します。この識別子は、ローカル コンピューターのシステム レジストリに保持されます (<strong>RDS.DataControl</strong> オブジェクトのクラス ID については、「<a href="datacontrol-object-rds.md">DataControl オブジェクト (RDS)</a>」を参照してください)。</p></td>
</tr>
<tr class="even">
<td><p><strong><em>ID</em></strong></p></td>
<td><p>埋め込みオブジェクトの、ドキュメント全体での識別子であり、コード内でオブジェクトを識別するために使用されます。</p></td>
</tr>
</tbody>
</table>


## <a name="rdsdatacontrol-tag-parameters"></a>RDS.DataControl タグ パラメーター

次の表に、 **RDS.DataControl** オブジェクトに固有のパラメーターを示します。 **RDS.DataControl** オブジェクトのすべてのパラメーター一覧、およびその実装時期については、「 [DataControl オブジェクト (RDS)](datacontrol-object-rds.md)」を参照してください。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>パラメーター</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="server-property-rds.md">サーバー</a></p></td>
<td><p>HTTP を使用する場合値は、https://サーバー コンピューターの名前です。</p></td>
</tr>
<tr class="even">
<td><p><a href="connect-property-rds.md">接続</a></p></td>
<td><p>SQL Server に接続するために <strong>RDS.DataControl</strong> に必要な接続情報を指定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado">SQL</a></p></td>
<td><p><a href="recordset-object-ado.md">Recordset</a> を取得するために使用されるクエリ文字列を設定または取得します。</p></td>
</tr>
</tbody>
</table>

