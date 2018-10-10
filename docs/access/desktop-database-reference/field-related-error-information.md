---
title: フィールド関連のエラー情報
TOCTitle: Field-Related Error Information
ms:assetid: 81a2c5a4-ab09-53d8-b270-e889b00a0c1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249559(v=office.15)
ms:contentKeyID: 48545958
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dfa35220e463cada69c94fe56a72732591683686
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476800"
---
# <a name="field-related-error-information"></a>フィールド関連のエラー情報


**適用されます**Access 2013 |。Office 2013

エラーがフィールドに直接関係するものである場合 (データが存在しない場合やデータがフィールドの型と一致しない場合など) は、 **Field** オブジェクトの **Status** プロパティを調べることで、問題の原因に関するより詳細な情報を得ることができます。このプロパティは、問題に関する具体的な情報を示すよう拡張されています。このため、たとえば **UpdateBatch** の呼び出しが失敗したときに、影響を受けた各レコードに含まれる **Field** の **Status** プロパティを調べることにより、問題の原因を確認できます。このプロパティには、 **FieldStatusEnum** 定数の値のうち 1 つが含まれます。エラー発生時に特に関係のある値を次の表に示します。

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
<td><p><strong>adFieldCantConvertValue</strong></p></td>
<td><p>2</p></td>
<td><p>フィールドの取得または保存を行うときにデータが失われてしまうことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldDataOverflow</strong></p></td>
<td><p>6</p></td>
<td><p>プロバイダーから返されたデータがフィールドのデータ型をオーバーフローしたことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldDefault</strong></p></td>
<td><p>13</p></td>
<td><p>データの設定時にフィールドの既定値が使われたことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldIgnore</strong></p></td>
<td><p>15</p></td>
<td><p>ソースのデータ値が設定されたときにこのフィールドがスキップされたことを示します。プロバイダーによって値が設定されていません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldIntegrityViolation</strong></p></td>
<td><p>10</p></td>
<td><p>計算エンティティまたは派生エンティティであるため、フィールドを編集できないことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldIsNull</strong></p></td>
<td><p>3</p></td>
<td><p>プロバイダーが Null 値を返したことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldOutOfSpace</strong></p></td>
<td><p>22</p></td>
<td><p>移動またはコピー操作を実行するために必要な記憶域をプロバイダーが確保できないことを示します。</p></td>
</tr>
</tbody>
</table>

