---
title: FieldEnum (Access デスクトップ データベース リファレンス)
TOCTitle: FieldEnum
ms:assetid: fbd415c0-d6b4-278f-318b-98432c013634
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250289(v=office.15)
ms:contentKeyID: 48548876
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d684c6f50a07efd07b28b64fd36b5106a940e55f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626639"
---
# <a name="fieldenum"></a>FieldEnum

**適用先**: Access 2013、Office 2013

[Record](record-object-ado.md) オブジェクトの [Fields](fields-collection-ado.md) コレクションで参照される特定のフィールドを表します。

## <a name="remarks"></a>注釈

これらの定数は、**Record** に関連付けられた特定のフィールドにアクセスするための "ショートカット" として利用できます。**Fields** コレクションから [Field](field-object-ado.md) オブジェクトを取得し、**Field** オブジェクトの [Value](value-property-ado.md) プロパティを使用してその内容を取り出します。

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
<th><p>値</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adDefaultStream</strong></p></td>
<td><p>-1</p></td>
<td><p><strong>Record</strong> に関連付けられた既定の <a href="stream-object-ado.md">Stream</a> オブジェクトを含むフィールドを参照します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecordURL</strong></p></td>
<td><p>-2</p></td>
<td><p>現在の <strong>Record</strong> の絶対 URL 文字列を含むフィールドを参照します。</p></td>
</tr>
</tbody>
</table>

