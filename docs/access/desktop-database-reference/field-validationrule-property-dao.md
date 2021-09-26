---
title: Field.ValidationRule プロパティ (DAO)
TOCTitle: ValidationRule Property
ms:assetid: b07e644d-54d3-7199-6f99-178774e54398
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821784(v=office.15)
ms:contentKeyID: 48547123
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 0a5ec1c25e8364253143ea3379f4888ee65bddea
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612170"
---
# <a name="fieldvalidationrule-property-dao"></a>Field.ValidationRule プロパティ (DAO)


**適用先**: Access 2013、Office 2013

テーブルのフィールドを変更するかテーブルにフィールドを追加するときに、フィールド内のデータを検証する値を設定または取得します (Microsoft Access ワークスペースのみ)。値の取得および設定が可能です。文字列型 ( **String**) の値を使用します。

## <a name="syntax"></a>構文

*式* .ValidationRule

*式* Field オブジェクトを返 **す式** 。

## <a name="remarks"></a>注釈

設定値または戻り値は、WHERE 予約語のない SQL WHERE 句の形式による比較方法が記述された文字列型 (String) の値です。 **[Fields](fields-collection-dao.md)** コレクションに追加されていないオブジェクトでは、このプロパティは値の取得および設定が可能です。

**ValidationRule** プロパティは、フィールドに有効なデータが含まれているかどうかを指定します。データが有効でない場合、トラップ可能な実行時エラーが発生します。エラー メッセージには、 **[ValidationText](field-validationtext-property-dao.md)** プロパティが指定されている場合はそのテキストが表示され、それ以外は、 **ValidationRule** に指定されている式のテキストが表示されます。

**[Field](field-object-dao.md)** オブジェクトの場合、 **ValidationRule** プロパティの使用方法は、 **Field** オブジェクトの追加先の **Fields** コレクションを含むオブジェクトによって変わります。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>オブジェクトの追加先</p></th>
<th><p>使用法</p></th>
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
<td><p>読み取り/書き込み</p></td>
</tr>
</tbody>
</table>


検証は、Microsoft Access データベース エンジンを使用しているデータベースに対してのみサポートされます。

**Field** オブジェクトの **ValidationRule** プロパティで指定される文字列式は、該当する **Field** のみ参照できます。ユーザー定義関数、SQL 集計関数、またはクエリを参照することはできません。 **Field** オブジェクトの **ValidateOnSet** プロパティが **True** に設定されているときに、このオブジェクトの **ValidationRule** プロパティを設定するには、この式の解析が正常に終了し (フィールド名を暗黙のオペランドとして)、 **True** と評価される必要があります。 **ValidateOnSet** プロパティが **False** に設定されている場合、 **ValidationRule** プロパティの設定は無視されます。


> [!NOTE]
> 整数以外の値で連結された文字列にプロパティを設定し、システム パラメーターで米国以外の値を指定する場合。コンマなどの 10 進文字 (strRule = "PRICE &gt; " &amp; lngPrice、lngPrice = 125,50 など) は、コードがデータを検証しようとするときにエラーが発生します。 連結時に数値がシステムの既定の小数点の記号を使って文字列に変換されますが、Microsoft Acces データベース エンジンの SQL で小数点の記号として使用できるのはピリオドのみであるためです。


