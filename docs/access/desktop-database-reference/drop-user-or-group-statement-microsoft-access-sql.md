---
title: ドロップのユーザーまたはグループのステートメント (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: f9662c4f0cb691136a556faa32cb0d5a1c775268
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936834"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a>ドロップのユーザーまたはグループのステートメント (Microsoft Access SQL)

**適用されます**Access 2013、Office 2013。

1 つ以上の既存の*ユーザー*または*グループ*を削除、または既存の*グループ*から 1 つまたは複数の既存の*ユーザー*を削除します。

## <a name="syntax"></a>構文

### <a name="delete-one-or-more-users-or-remove-one-or-more-users-from-a-group"></a>1 つまたは複数のユーザーを削除するか、1 つまたは複数のユーザーをグループから削除

DROP USER*ユーザー*\[、*ユーザー*、.\] \[*グループ*から\]

### <a name="delete-one-or-more-groups"></a>1 つまたは複数のグループを削除します。

ドロップ グループ*グループ*\[、*グループ*、.\]

DROP USER ステートメントまたは GROUP ステートメントには、次の指定項目があります

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>指定項目</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>user</em></p></td>
<td><p>ワークグループ情報ファイルから削除されるユーザー名。</p></td>
</tr>
<tr class="even">
<td><p><em>group</em></p></td>
<td><p>ワークグループ情報ファイルから削除されるグループ名。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

DROP USER ステートメントで FROM キーワードを使用する場合、明細書に記載されている*ユーザー*の*グループ*指定した FROM キーワードの後から削除されます。 ただし、*ユーザー*自体は削除されません。

ドロップ グループ ステートメントは、指定した*グループ*(%s) を削除します。 (S)、*グループ*のメンバーである*ユーザー*には影響しませんが、削除された*グループ*(%s) のメンバーとなる、不要になった。

