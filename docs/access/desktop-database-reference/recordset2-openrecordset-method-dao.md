---
title: OpenRecordset メソッド (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: da6ce86e-957e-21f8-07ac-8acd57326a12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835325(v=office.15)
ms:contentKeyID: 48548082
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 08120f4ebb6b2d9989051171a0c71b6d9fcf6e5c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307253"
---
# <a name="recordset2openrecordset-method-dao"></a>OpenRecordset メソッド (DAO)

**適用先:** Access 2013、Office 2013

新しい **[Recordset](recordset-object-dao.md)** オブジェクトを作成して **Recordsets** コレクションに追加します。

## <a name="syntax"></a>構文

*式*。OpenRecordset ([***種類***]、[***オプション]***)

*式***Recordset2**オブジェクトを表す変数を取得します。

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
<th><p>必須/オプション</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>名前</em></p></td>
<td><p>必須</p></td>
<td><p><strong>String</strong></p></td>
<td><p>新しい <strong>Recordset</strong> のレコードの取得元です。テーブル名、クエリ名、またはレコードを返す SQL ステートメントを指定できます。Microsoft Access データベース エンジンのデータベースに含まれるテーブル タイプの <strong>Recordset</strong> オブジェクトの場合は、テーブル名でのみ指定できます。  </p></td>
</tr>
<tr class="even">
<td><p><em>Type</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>開く<strong>Recordset</strong>の種類を示す<strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong>定数を指定します。</p><p><strong>注</strong>: Microsoft access ワークスペースで<STRONG>レコードセット</STRONG>を開き、種類を指定しない場合、 <STRONG>OpenRecordset</STRONG>はテーブルタイプの<STRONG>recordset</STRONG>を作成します (可能な場合)。 If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</p>
</td>
</tr>
<tr class="odd">
<td><p><em>Options</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>新しい<strong>Recordset</strong>の特性を指定する<strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong>定数の組み合わせ。</p><p><strong>注</strong>: <STRONG>dbconsistent</STRONG>および<STRONG>dbInconsistent</STRONG>定数は相互に排他的です。両方を使用するとエラーが発生します。 Supplying a lockedits argument when options uses the <STRONG>dbReadOnly</STRONG> constant also causes an error.</p>
</td>
</tr>
<tr class="even">
<td><p><em>LockEdit</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Recordset</strong>のロックを決定する<strong><a href="locktypeenum-enumeration-dao.md">locktypeenum</a></strong>定数。</p><p><strong>注</strong>: <STRONG>dbreadonly</STRONG>は、options 引数または lockedits 引数のいずれかで使用できますが、両方を使用することはできません。 If you use it for both arguments, a run-time error occurs.</p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>戻り値

Recordset

## <a name="remarks"></a>注釈

通常、ユーザーがレコードを更新中にこのエラーが発生した場合は、フィールドの内容を更新して、新たに変更された値を取得するコードを記述します。レコードを削除中にこのエラーが発生した場合は、新しいレコード データと、そのデータが最近変更されたことを示すメッセージをユーザーに表示するという方法もあります。この時点で、レコードを削除するかどうかの確認をユーザーに求めることができます。

IDENTITY 列を持つ Microsoft SQL Server 6.0 以降のテーブルに対して Microsoft Access データベース エンジンが接続された ODBC ワークスペースの **Recordset** を開く場合は、定数 **dbSeeChanges** も使用する必要があり、使用しないとエラーが生じます。

ODBC データ ソースで複数の **Recordset** を開こうとすると、 **OpenRecordset** に対する前の呼び出しで接続がビジー状態となるため、失敗する場合があります。これを回避する方法の 1 つは、 **Recordset** を開いた直後に、 **MoveLast** メソッドを使用して **Recordset** の末尾までデータを読み込むことです。

[**Close**](connection-close-method-dao.md) メソッドを使用して **Recordset** を閉じると、そのレコードセットは自動的に **Recordsets** コレクションから削除されます。

> [!NOTE]
> *source*が整数以外の値で連結された文字列で構成されている SQL ステートメントを参照しており、システムパラメーターでコンマ以外の小数点 (たとえば、strsql = "PRICE &gt; " &amp; lngPrice、lngPrice = など) を指定している場合。125, 50) **Recordset**を開こうとすると、エラーが発生します。 連結時に数値がシステムの既定の小数点の記号を使って文字列に変換されますが、SQL で小数点の記号として使用できるのはピリオドのみになるからです。


