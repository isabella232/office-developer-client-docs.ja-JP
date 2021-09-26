---
title: フィールドに関連するエラー情報
TOCTitle: Field-related error information
ms:assetid: 81a2c5a4-ab09-53d8-b270-e889b00a0c1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249559(v=office.15)
ms:contentKeyID: 48545958
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d0849868becbe21b502c46fa2445dac42b2a1ad4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589533"
---
# <a name="field-related-error-information"></a>フィールドに関連するエラー情報


**適用先**: Access 2013、Office 2013

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
<td><p>6 </p></td>
<td><p>プロバイダーから返されたデータがフィールドのデータ型をオーバーフローしたことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldDefault</strong></p></td>
<td><p>13</p></td>
<td><p>データの設定時にフィールドの既定値が使われたことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldIgnore</strong></p></td>
<td><p>15 </p></td>
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

