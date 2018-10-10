---
title: DROP USER ステートメントまたは GROUP ステートメント (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP Statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3a5cf75de06c13e2452e5f33b8355b7fb480d8a3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476726"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a>DROP USER ステートメントまたは GROUP ステートメント (Microsoft Access SQL)


**適用されます**Access 2013 |。Office 2013

削除の 1 つまたは複数既存*ユーザー*や*グループ*、または既存の*グループ*から 1 つまたは複数の既存の*ユーザー*を削除します。

## <a name="syntax"></a>構文

1 つまたは複数の*ユーザー*を削除するか、*グループ*から 1 つまたは複数の*ユーザー*%s を削除します。

DROP USER*ユーザー*\[、*ユーザー*、.\] \[*グループ*から\]

1 つまたは複数の*グループ*%s を削除します。

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

DROP USER ステートメントで FROM キーワードを使用する場合、各ステートメントに記載されている*ユーザー*から削除されます*グループ*指定した FROM キーワードの後します。 ただし、*ユーザー*自体は削除されません。

ドロップ グループ ステートメントは、指定した*グループ*(%s) を削除します。 (S)、*グループ*のメンバーである*ユーザー*の影響を受けませんが、削除された*グループ*(%s) のメンバーとなる、不要になった。

