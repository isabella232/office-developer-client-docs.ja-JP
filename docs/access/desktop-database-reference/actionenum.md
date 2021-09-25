---
title: ActionEnum (Access デスクトップ データベースリファレンス)
TOCTitle: ActionEnum
ms:assetid: 225024c1-9088-b532-2a23-04c1aaaaa892
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248998(v=office.15)
ms:contentKeyID: 48543704
ms.date: 10/17/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c6d19ba5a19b8c49bb3c95fcc52040be62c364d8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569616"
---
# <a name="actionenum"></a>ActionEnum

**適用先:** Access 2013、Office 2013

[SetPermissions](setpermissions-method-adox.md) メソッドの呼び出し時に実行されるアクションの種類を示します。

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
<td><p><strong>adAccessDeny</strong></p></td>
<td><p>3</p></td>
<td><p>グループまたはユーザーは、指定した権限を拒否されます。</p></td>
</tr>
<tr class="even">
<td><p><strong>adAccessGrant</strong></p></td>
<td><p>1</p></td>
<td><p>グループまたはユーザーは、少なくとも要求した権限を持ちます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adAccessRevoke</strong></p></td>
<td><p>4 </p></td>
<td><p>グループまたはユーザーが持つすべての明示的なアクセス権は取り消されます。</p></td>
</tr>
<tr class="even">
<td><p><strong>adAccessSet</strong></p></td>
<td><p>2</p></td>
<td><p>グループまたはユーザーは、要求した権限を持ちます。</p></td>
</tr>
</tbody>
</table>

