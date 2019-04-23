---
title: actionenum (Access デスクトップデータベースリファレンス)
TOCTitle: ActionEnum
ms:assetid: 225024c1-9088-b532-2a23-04c1aaaaa892
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248998(v=office.15)
ms:contentKeyID: 48543704
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f098adb42df39d1509a6d22decd8d2cead684f11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280657"
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
<td><p><strong>adaccessdeny</strong></p></td>
<td><p>1/3</p></td>
<td><p>グループまたはユーザーは、指定した権限を拒否されます。</p></td>
</tr>
<tr class="even">
<td><p><strong>adaccessgrant</strong></p></td>
<td><p>1-d</p></td>
<td><p>グループまたはユーザーは、少なくとも要求した権限を持ちます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adAccessRevoke</strong></p></td>
<td><p>2/4</p></td>
<td><p>グループまたはユーザーが持つすべての明示的なアクセス権は取り消されます。</p></td>
</tr>
<tr class="even">
<td><p><strong>adaccessset</strong></p></td>
<td><p>pbm-2</p></td>
<td><p>グループまたはユーザーは、要求した権限を持ちます。</p></td>
</tr>
</tbody>
</table>

