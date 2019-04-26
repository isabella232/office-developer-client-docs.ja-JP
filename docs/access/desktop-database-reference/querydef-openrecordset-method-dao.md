---
title: QueryDef.OpenRecordset メソッド (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: b4908c36-c156-e269-e2ad-b1fa20ec4884
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822070(v=office.15)
ms:contentKeyID: 48547232
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: a046359f39611e38b9e517495f54041f876addfc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302850"
---
# <a name="querydefopenrecordset-method-dao"></a>QueryDef.OpenRecordset メソッド (DAO)

**適用先:** Access 2013、Office 2013

新しい **[Recordset](recordset-object-dao.md)** オブジェクトを作成し、**Recordsets** コレクションに追加します。

## <a name="syntax"></a>構文

*expression* .OpenRecordset(***Type***, ***Options***, ***LockEdit***)

*expression*: **QueryDef** オブジェクトを表す変数。

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
<th><p>必須/省略可能</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Type</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>開く <strong>Recordset</strong> の型を示す <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> 定数。</p><p><strong>注</strong>: Microsoft Access ワークスペースで <STRONG>Recordset</STRONG> を開き、型を指定しない場合、可能であれば<STRONG>OpenRecordset</STRONG>はテーブル タイプの <STRONG>Recordset</STRONG> を作成します。 If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</p>
</td>
</tr>
<tr class="even">
<td><p><em>オプション</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>新しい <strong>Recordset</strong> の特性を指定する <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> 定数の組み合わせ。</p></p><p><strong>注</strong>: 定数 <STRONG>dbConsistent</STRONG> と <STRONG>dbInconsistent</STRONG> は互いに排他的なので、この 2 つを同時に使用するとエラーになります。 Supplying a lockedits argument when options uses the <STRONG>dbReadOnly</STRONG> constant also causes an error.</p>
</td>
</tr>
<tr class="odd">
<td><p><em>LockEdit</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Recordset</strong> のロックを決定する <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> 定数。</p></p><p><strong>注</strong>: <STRONG>dbReadOnly</STRONG> を Options 引数または Lockedits 引数のどちらか一方で使用することはできますが、両方で使用することはできません。 両方の引数で使用すると、実行時エラーが発生します。</p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>戻り値

Recordset

## <a name="remarks"></a>注釈

IDENTITY 列を持つ Microsoft SQL Server 6.0 以降のテーブルに対して Microsoft Access データベース エンジンが接続された ODBC ワークスペースの **Recordset** を開く場合は、**[dbSeeChanges](recordsetoptionenum-enumeration-dao.md)** 定数も使用する必要があり、使用しないとエラーが生じます。

ODBC データ ソースで複数の **Recordset** を開こうとすると、 **OpenRecordset** に対する前の呼び出しで接続がビジー状態となるため、失敗する場合があります。これを回避する方法の 1 つは、 **Recordset** を開いた直後に、 **[MoveLast](recordset-movelast-method-dao.md)** メソッドを使用して **Recordset** の末尾までデータを読み込むことです。

**Close** メソッドを使用して **Recordset** を閉じると、そのレコードセットは自動的に **Recordsets** コレクションから削除されます。

> [!NOTE]
> *source* が文字列と非整数値を連結したもので構成される SQL ステートメントを示し、かつシステム パラメーターでコンマなどのピリオド以外の小数点の記号が使用されている場合 (たとえば、strSQL = "PRICE &gt; " &amp; lngPrice と lngPrice = 125,50)、**Recordset** を開こうとするとエラーが発生します。 連結時に数値がシステムの既定の小数点の記号を使って文字列に変換されますが、SQL で小数点の記号として使用できるのはピリオドのみになるからです。


