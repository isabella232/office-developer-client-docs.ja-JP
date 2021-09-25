---
title: Field2.ValidationRule プロパティ (DAO)
TOCTitle: ValidationRule Property
ms:assetid: 5464d2de-f3d7-5d6b-4fc5-66df6a5540cb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194105(v=office.15)
ms:contentKeyID: 48544896
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 3e2c8ba72f55f5c362e01726d0a528b12d9a9960
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552942"
---
# <a name="field2validationrule-property-dao"></a>Field2.ValidationRule プロパティ (DAO)


**適用先:** Access 2013、Office 2013

テーブルのフィールドを変更するかテーブルにフィールドを追加するときに、フィールド内のデータを検証する値を設定または取得します (Microsoft Access ワークスペースのみ)。値の取得および設定が可能です。文字列型 ( **String**) の値を使用します。

## <a name="syntax"></a>構文

*式* .ValidationRule

*式* Field2 オブジェクトを **返す** 式。

## <a name="remarks"></a>注釈

設定値または戻り値は、WHERE 予約語のない SQL WHERE 句の形式による比較方法が記述された文字列型 (String) の値です。 **[Fields](fields-collection-dao.md)** コレクションに追加されていないオブジェクトでは、このプロパティは値の取得および設定が可能です。

**ValidationRule** プロパティは、フィールドに有効なデータが含まれているかどうかを示します。データが無効の場合は、トラップ可能な実行時エラーが発生します。エラー メッセージには、 **ValidationText** プロパティが設定されている場合はそのテキストが表示され、それ以外は **ValidationRule** に指定されている式のテキストが表示されます。

**Field2** オブジェクトでは、 **ValidationRule** プロパティの使用方法は、 **Field2** オブジェクトを追加する **Fields** コレクションが含まれているオブジェクトに応じて異なります。

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

**Field2** オブジェクトの **ValidationRule** プロパティに指定されている文字列式は、その **Field2** オブジェクトのみを参照できます。この式は、ユーザー定義関数、SQL 集計関数、およびクエリは参照できません。 **Field2** オブジェクトの **ValidateOnSet** プロパティが **True** に設定されている場合に、その **ValidationRule** プロパティを設定するには、文字列式が正常に解析され (明示されないオペランドとしてフィールド名を指定)、 **True** に評価されている必要があります。 **ValidateOnSet** プロパティが **False** に設定されている場合、 **ValidationRule** プロパティの設定は無視されます。


> [!NOTE]
> 整数以外の値で連結された文字列にプロパティを設定し、システム パラメーターで米国以外の値を指定する場合。コンマなどの 10 進文字 (strRule = "PRICE &gt; " &amp; lngPrice、lngPrice = 125,50 など) は、コードがデータを検証しようとするときにエラーが発生します。 連結時に数値がシステムの既定の小数点の記号を使って文字列に変換されますが、Microsoft Acces データベース エンジンの SQL で小数点の記号として使用できるのはピリオドのみであるためです。


