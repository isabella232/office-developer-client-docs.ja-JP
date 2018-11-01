---
title: Field.ValidationText プロパティ (DAO)
TOCTitle: ValidationText Property
ms:assetid: 6d9ec790-a9d2-84d7-ccba-57d738491e36
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195540(v=office.15)
ms:contentKeyID: 48545494
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c582795dc104171bd4c8435521e0da31718b1a38
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868890"
---
# <a name="fieldvalidationtext-property-dao"></a>Field.ValidationText プロパティ (DAO)


**適用されます**Access 2013、Office 2013。

**Field** オブジェクトの値が **ValidationRule** プロパティの設定に設定されている入力規則を満たさない場合に、アプリケーションに表示するメッセージのテキストを示す値を設定または取得します (Microsoft Access ワークスペースのみ)。値の取得および設定が可能です。文字列型 ( **String**) の値を使用します。

## <a name="syntax"></a>構文

*式*です。ValidationText

*式***Field**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

設定値または戻り値は、ユーザーがフィールドに無効な値を入力した場合に表示するテキストを指定する文字列型 ( **String**) の値です。コレクションに追加されていないオブジェクトでは、このプロパティは値の取得および設定が可能です。

**Field** オブジェクトの場合、 **ValidationText** プロパティの使用方法は、次の表に示すように、 [Field](fields-collection-dao.md) オブジェクトの追加先の ****Fields**** コレクションを含むオブジェクトによって異なります。

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
<td><p>値の取得および設定が可能です。</p></td>
</tr>
</tbody>
</table>

