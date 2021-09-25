---
title: AllowNullsEnum (Access desktop database reference)
TOCTitle: AllowNullsEnum
ms:assetid: 7bb42b38-6b3b-5930-b1d7-16323a3bdf37
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249515(v=office.15)
ms:contentKeyID: 48545819
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ca33c16c4588127998527b7f4a9cdcedd50d35e0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559109"
---
# <a name="allownullsenum"></a>AllowNullsEnum

**適用先:** Access 2013、Office 2013

Null 値を含むレコードにインデックスを付けるかどうかを示します。

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
<td><p><strong>adIndexNullsAllow</strong></p></td>
<td><p>0</p></td>
<td><p>インデックスは、キー列が Null 値のエントリを許可します。Null 値がキー列に入力された場合、そのエントリはインデックスに挿入されます。</p></td>
</tr>
<tr class="even">
<td><p><strong>adIndexNullsDisallow</strong></p></td>
<td><p>1</p></td>
<td><p>既定値です。インデックスは、キー列が Null 値のエントリを許可しません。Null 値がキー列に入力された場合、エラーが発生します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adIndexNullsIgnore</strong></p></td>
<td><p>2</p></td>
<td><p>インデックスは、Null 値のキーを含むエントリを挿入しません。Null 値がキー列に入力された場合、そのエントリは無視され、エラーは発生しません。</p></td>
</tr>
<tr class="even">
<td><p><strong>adIndexNullsIgnoreAny</strong></p></td>
<td><p>4 </p></td>
<td><p>インデックスは、キー列に Null 値を含むエントリを挿入しません。複数列キーを持つインデックスでは、Null 値が入力された列がある場合、そのエントリは無視され、エラーは発生しません。</p></td>
</tr>
</tbody>
</table>

