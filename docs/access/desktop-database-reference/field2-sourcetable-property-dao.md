---
title: Field2.SourceTable プロパティ (DAO)
TOCTitle: SourceTable Property
ms:assetid: 24d2fdda-d924-d95e-8458-063dd1d36d5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191839(v=office.15)
ms:contentKeyID: 48543768
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: af404f3b741445ef434c4f3266f89aa318e13ad2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477752"
---
# <a name="field2sourcetable-property-dao"></a>Field2.SourceTable プロパティ (DAO)


**適用されます**Access 2013 |。Office 2013

**Field2** オブジェクトのデータの元のソースであるテーブルの名前を示す値を返します。値の取得のみ可能です。文字列型 ( **String**) の値を使用します。

## <a name="syntax"></a>構文

*式*です。SourceTable

*式***Field2**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**Field2** オブジェクトでは、 **SourceField** プロパティと **SourceTable** プロパティを使用できるかどうかは、次の表に示すように、 **Field2** オブジェクトが追加される **Fields** コレクションを含むオブジェクトによって決まります。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>オブジェクトの追加先</p></th>
<th><p>使用例</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Index</strong></p></td>
<td><p>サポートされません。</p></td>
</tr>
<tr class="even">
<td><p><strong>QueryDef</strong></p></td>
<td><p>値の取得のみ可能です。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong></p></td>
<td><p>値の取得のみ可能です。</p></td>
</tr>
<tr class="even">
<td><p><strong>Relation</strong></p></td>
<td><p>サポートされません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong></p></td>
<td><p>値の取得のみ可能です。</p></td>
</tr>
</tbody>
</table>


これらのプロパティは、 **Field2** オブジェクトに関連付けられた元のフィールドおよびテーブル名を示します。たとえば、これらのプロパティを使用して、基になるテーブルのフィールド名に無関係な名前を持つクエリ フィールド内データの元のソースを調べることができます。


> [!NOTE]
> <P>[!メモ] <STRONG>SourceTable</STRONG> プロパティは、テーブル タイプの <STRONG>Recordset</STRONG> オブジェクトの <STRONG>Fields</STRONG> コレクションに含まれる <STRONG>Field2</STRONG> オブジェクトで使用した場合、有効なテーブル名を返しません。</P>


