---
title: InheritTypeEnum (Access デスクトップ データベースリファレンス)
TOCTitle: InheritTypeEnum
ms:assetid: aa505c66-5871-10a8-35a7-cb30bb5dc21a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249787(v=office.15)
ms:contentKeyID: 48546944
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7b4a66853fcb51c617d8afdd9b806a6faa567a2f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626373"
---
# <a name="inherittypeenum"></a>InheritTypeEnum

**適用先**: Access 2013、Office 2013

[SetPermissions](setpermissions-method-adox.md) メソッドで設定された権限をオブジェクトが継承する方法を示します。

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
<td><p><strong>adInheritBoth</strong></p></td>
<td><p>3</p></td>
<td><p>主オブジェクトに含まれるオブジェクトおよびその他のコンテナーの両方が、エントリを継承します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adInheritContainers</strong></p></td>
<td><p>2</p></td>
<td><p>主オブジェクトに含まれるその他のコンテナーが、エントリを継承します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adInheritNone</strong></p></td>
<td><p>0</p></td>
<td><p>既定値です。継承は行われません。</p></td>
</tr>
<tr class="even">
<td><p><strong>adInheritNoPropagate</strong></p></td>
<td><p>4 </p></td>
<td><p><strong>adInheritObjects</strong> フラグおよび <strong>adInheritContainers</strong> フラグは、継承されたエントリに伝えられません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adInheritObjects</strong></p></td>
<td><p>1</p></td>
<td><p>コンテナー内のコンテナー以外のオブジェクトが、権限を継承します。</p></td>
</tr>
</tbody>
</table>

