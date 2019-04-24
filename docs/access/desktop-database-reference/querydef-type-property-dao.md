---
title: Type プロパティ (DAO)
TOCTitle: Type Property
ms:assetid: 03db891d-b958-7cf9-56c1-524d9ff2b9b5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844814(v=office.15)
ms:contentKeyID: 48542993
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cb8856194d0b2ed14577bdc275adeb50ebdde212
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300946"
---
# <a name="querydeftype-property-dao"></a>Type プロパティ (DAO)


**適用先:** Access 2013、Office 2013

オブジェクトの操作の種類またはデータ型を示す値を設定あるいは取得します。値の取得のみ可能です。整数型 (**Integer**) の値を使用します。

## <a name="syntax"></a>構文

*式*。種類

*式***QueryDef**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

次の表は、**QueryDef** オブジェクトで使用可能な設定値および戻り値を示しています。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
<th><p>クエリの種類</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbqaction</strong></p></td>
<td><p>アクション</p></td>
</tr>
<tr class="even">
<td><p><strong>dbqappend</strong></p></td>
<td><p>追加</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbqcompound</strong></p></td>
<td><p>複雑化</p></td>
</tr>
<tr class="even">
<td><p><strong>dbqcrosstab 集計</strong></p></td>
<td><p>行列</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbqddl</strong></p></td>
<td><p>データ定義</p></td>
</tr>
<tr class="even">
<td><p><strong>dbqdelete</strong></p></td>
<td><p>削除</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbqmaketable</strong></p></td>
<td><p>テーブル作成</p></td>
</tr>
<tr class="even">
<td><p><strong>dbqprocedure</strong></p></td>
<td><p>プロシージャ (ODBCDirect ワークスペースのみ)</p><p><strong>注</strong>: ODBCDirect ワークスペースは、Microsoft access 2013 ではサポートされていません。 Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbqselect</strong></p></td>
<td><p>Select</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQSetOperation</strong></p></td>
<td><p>Union</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbqsptbulk</strong></p></td>
<td><p><strong>dbQSQLPassThrough</strong> と共に使用して、レコードを取得しないクエリを指定 (Microsoft Access ワークスペースのみ)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbqsqlpassthrough</strong></p></td>
<td><p>パススルー (Microsoft Access ワークスペースのみ)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQUpdate</strong></p></td>
<td><p>Update</p></td>
</tr>
</tbody>
</table>


新しい **[Field](field-object-dao.md)** オブジェクト、 **[Parameter](parameter-object-dao.md)** オブジェクト、または **[Property](property-object-dao.md)** オブジェクトを、 **[Index](index-object-dao.md)** オブジェクト、 **QueryDef** オブジェクト、 **[Recordset](recordset-object-dao.md)** オブジェクト、または **[TableDef](tabledef-object-dao.md)** オブジェクトのコレクションに追加するときに、基になるデータベースが新しいオブジェクトに指定されているデータ型をサポートしていない場合、エラーが発生します。

