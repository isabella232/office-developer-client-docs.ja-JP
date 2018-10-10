---
title: FieldEnum (デスクトップ データベース参照のアクセス)
TOCTitle: FieldEnum
ms:assetid: fbd415c0-d6b4-278f-318b-98432c013634
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250289(v=office.15)
ms:contentKeyID: 48548876
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5efcdbd9da4214d7f2b78ffbcfb81fb13265087e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476383"
---
# <a name="fieldenum"></a>FieldEnum


**適用されます**Access 2013 |。Office 2013

[Record](record-object-ado.md) オブジェクトの [Fields](fields-collection-ado.md) コレクションで参照される特定のフィールドを表します。

**解説**

これらの定数は、 **Record** に関連付けられた特定のフィールドにアクセスするための "ショートカット" として利用できます。 [Fields](field-object-ado.md) コレクションから **Field** オブジェクトを取得し、 **Field** オブジェクトの [Value](value-property-ado.md) プロパティを使用してその内容を取り出します。

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

