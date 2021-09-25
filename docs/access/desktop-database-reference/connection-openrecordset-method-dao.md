---
title: Connection.OpenRecordset メソッド (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: 584a3e00-7589-90f1-aa6a-5d6116f0b5b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194324(v=office.15)
ms:contentKeyID: 48544993
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f8cdcd5313095992b9e3d0983dc1c6691ccb5e5f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615779"
---
# <a name="connectionopenrecordset-method-dao"></a>Connection.OpenRecordset メソッド (DAO)

**適用先:** Access 2013、Office 2013

新しい **[Recordset](recordset-object-dao.md)** オブジェクトを作成し、**Recordsets** コレクションに追加します。

## <a name="syntax"></a>構文

*式* .OpenRecordset(***Name** _, _*_Type_*_, _*_Options_*_, _*_LockEdit_**)

*式***Connection** オブジェクトを表す変数です。

## <a name="parameters"></a>パラメーター

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>必須かどうか</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>名前</em></p></td>
<td><p>必須</p></td>
<td><p><strong>String</strong></p></td>
<td><p>新しい <strong>Recordset</strong> のレコードの取得元です。テーブル名、クエリ名、またはレコードを返す SQL ステートメントを指定できます。Microsoft Office Access データベース エンジンのデータベースに含まれるテーブル タイプの <strong>Recordset</strong> オブジェクトの場合は、テーブル名でのみ指定できます。</p></td>
</tr>
<tr class="even">
<td><p><em>Type</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>開く <strong>Recordset</strong> の型を示す <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> 定数。</p><p><strong>注</strong>: タイプを指定せずに <strong>Recordset</strong> を Microsoft Access ワークスペースで開くと、可能な場合は <strong>OpenRecordset</strong> はテーブルタイプの <strong>Recordset</strong> を作成します。 If you specify a linked table or query, <strong>OpenRecordset</strong> creates a dynaset-type <strong>Recordset</strong>.</p>
</td>
</tr>
<tr class="odd">
<td><p><em>オプション</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>新しい <strong>Recordset</strong> の特性を指定する <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> 定数の組み合わせ。</p><p><strong>注</strong>: 定数 <strong>dbConsistent</strong> と <strong>dbInconsistent</strong> は互いに排他的なので、この 2 つを同時に使用するとエラーになります。 オプションで <strong>dbReadOnly</strong> 定数を使用する場合に lockedits 引数を指定すると、エラーも発生します。</p>
</td>
</tr>
<tr class="even">
<td><p><em>LockEdit</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Recordset</strong> のロックを決定する <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> 定数。</p><p><strong>注</strong>: <strong>dbReadOnly</strong> を Options 引数または Lockedits 引数のどちらか一方で使用することはできますが、両方で使用することはできません。 両方の引数で使用すると、実行時エラーが発生します。</p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>戻り値

Recordset

## <a name="remarks"></a>注釈

通常、ユーザーがレコードを更新中にこのエラーが発生した場合は、フィールドの内容を更新して、新たに変更された値を取得するコードを記述します。レコードを削除中にこのエラーが発生した場合は、新しいレコード データと、そのデータが最近変更されたことを示すメッセージをユーザーに表示するという方法もあります。この時点で、レコードを削除するかどうかの確認をユーザーに求めることができます。

IDENTITY 列を持つ Microsoft SQL Server 6.0 以降のテーブルに対して Microsoft Access データベース エンジンが接続された ODBC ワークスペースの **Recordset** を開く場合は、**dbSeeChanges** 定数も使用する必要があり、使用しないとエラーが生じます。

ODBC データ ソースで複数の **Recordset** を開こうとすると、**OpenRecordset** に対する前の呼び出しで接続がビジー状態となるため、失敗する場合があります。これを回避する方法の 1 つは、**Recordset** を開いた直後に、**MoveLast** メソッドを使用して **Recordset** の末尾までデータを読み込むことです。

**[Close](connection-close-method-dao.md)** メソッドを使用して **Recordset** を閉じると、そのレコードセットは自動的に **Recordsets** コレクションから削除されます。

> [!NOTE]
> *source* が文字列と非整数値を連結したもので構成される SQL ステートメントを参照し、かつシステム パラメーターでコンマなどのピリオド以外の小数点の記号が使用されている場合 (たとえば、strSQL = "PRICE &gt; " &amp; lngPrice で lngPrice = 125,50)、**Recordset** を開こうとするとエラーが発生します。 連結時に数値がシステムの既定の小数点の記号を使って文字列に変換されますが、SQL で小数点の記号として使用できるのはピリオドのみになるからです。


