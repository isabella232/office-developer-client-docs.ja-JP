---
title: Recordset.OpenRecordset メソッド (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: 7d5ca4d5-5a0b-c0c8-d8e8-2c4e6c5f361f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196402(v=office.15)
ms:contentKeyID: 48545853
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c6eebd129a5f721a69e140133bf08cb7bee4f4fd
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868918"
---
# <a name="recordsetopenrecordset-method-dao"></a>Recordset.OpenRecordset メソッド (DAO)


**適用されます**Access 2013、Office 2013。

新しい **[Recordset](recordset-object-dao.md)** オブジェクトを作成して **Recordsets** コレクションに追加します。

## <a name="syntax"></a>構文

*式*です。何らかの (***型***、***オプション***)

*式***レコード セット**オブジェクトを表す変数です。

### <a name="parameters"></a>パラメーター

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
<td><p>名前</p></td>
<td><p>必須</p></td>
<td><p><strong>文字列型 (String)</strong></p></td>
<td><p>新しい <strong>Recordset</strong> のレコードの取得元です。テーブル名、クエリ名、またはレコードを返す SQL ステートメントを指定できます。Microsoft Access データベース エンジンのデータベースに含まれるテーブル タイプの <strong>Recordset</strong> オブジェクトの場合は、テーブル名でのみ指定できます。  </p></td>
</tr>
<tr class="even">
<td><p>型</p></td>
<td><p>省略可能</p></td>
<td><p><strong>バリアント型 (Variant)</strong></p></td>
<td><p>開く <a href="recordsettypeenum-enumeration-dao.md">Recordset</a> の型を示す <strong><strong>RecordsetTypeEnum</strong></strong> 定数。</p>

> [!NOTE]
> <P>Microsoft Access ワークスペースで <STRONG>Recordset</STRONG> を開くときに、型を指定しない場合、<STRONG>OpenRecordset</STRONG> は、テーブル タイプの <STRONG>Recordset</STRONG> を作成します (可能な場合)。リンクされたテーブルまたはクエリを指定した場合、<STRONG>OpenRecordset</STRONG> は、ダイナセット タイプの <STRONG>Recordset</STRONG> を作成します。</P>


</td>
</tr>
<tr class="odd">
<td><p>選択肢</p></td>
<td><p>省略可能</p></td>
<td><p><strong>バリアント型 (Variant)</strong></p></td>
<td><p>新しい <a href="recordsetoptionenum-enumeration-dao.md">Recordset</a> の特性を指定する <strong><strong>RecordsetOptionEnum</strong></strong> 定数の組み合わせ。</p>

> [!NOTE]
> <P>定数 <STRONG>dbConsistent</STRONG> と <STRONG>dbInconsistent</STRONG> は互いに排他的なので、この 2 つを同時に使用するとエラーになります。Options で <STRONG>dbReadOnly</STRONG> 定数を使用する場合に Lockedits 引数を指定してもエラーになります。</P>


</td>
</tr>
<tr class="even">
<td><p>LockEdit</p></td>
<td><p>省略可能</p></td>
<td><p><strong>バリアント型 (Variant)</strong></p></td>
<td><p><a href="locktypeenum-enumeration-dao.md">Recordset</a> のロックを決定する <strong><strong>LockTypeEnum</strong></strong> 定数。</p>

> [!NOTE]
> <P><STRONG>dbReadOnly</STRONG> を Options 引数または Lockedits 引数のどちらか一方で使用することはできますが、両方で使用することはできません。両方の引数で使用した場合、実行時エラーが発生します。</P>


</td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>戻り値

Recordset

## <a name="remarks"></a>注釈

通常、ユーザーがレコードを更新中にこのエラーが発生した場合は、フィールドの内容を更新して、新しく変更された値を取得するコードを記述します。レコードの削除中にこのエラーが発生した場合は、新しいレコード データと、そのデータが最近変更されたことを示すメッセージをユーザーに表示するという方法もあります。このとき、レコードを削除してもよいかどうかユーザーに確認できます。

IDENTITY 列を持つ Microsoft SQL Server 6.0 以降のテーブルに対して Microsoft Access データベース エンジンが接続された ODBC ワークスペースの **Recordset** を開く場合は、 **dbSeeChanges** 定数も使用する必要があり、使用しないとエラーが生じます。

ODBC データ ソースで複数の **Recordset** を開こうとすると、 **OpenRecordset** に対する前の呼び出しで接続がビジー状態となるため、失敗する場合があります。これを回避する方法の 1 つは、 **Recordset** を開いた直後に、 **MoveLast** メソッドを使用して **Recordset** の末尾までデータを読み込むことです。

[**Close**](connection-close-method-dao.md) メソッドを使用して **Recordset** を閉じると、そのレコードセットは自動的に **Recordsets** コレクションから削除されます。


> [!NOTE]
> <P><EM>ソース</EM>を指す場合、整数以外の値に連結された文字列、SQL ステートメントで構成され、システム ・ パラメーターは、米国以外の小数点の記号、カンマなどを指定 (たとえば、strSQL ="価格&gt;" &amp; lngPrice でと lngPrice =125,50)、<STRONG>レコード セット</STRONG>を開こうとするとエラーが発生します。 連結時に数値がシステムの既定の小数点の記号を使って文字列に変換されますが、SQL で小数点の記号として使用できるのはピリオドのみになるからです。</P>


