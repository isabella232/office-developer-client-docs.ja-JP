---
title: DROP USER ステートメントまたは GROUP ステートメント (Microsoft access SQL)
TOCTitle: DROP USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 995f935ceea5af3b740215c5a4137e02e7ebb1b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293645"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a>DROP USER ステートメントまたは GROUP ステートメント (Microsoft access SQL)

**適用先:** Access 2013、Office 2013

1つ以上の既存の*ユーザー*または*グループ*を削除するか、既存の*グループ*から1つ以上の既存の*ユーザー*を削除します。

## <a name="syntax"></a>構文

### <a name="delete-one-or-more-users-or-remove-one-or-more-users-from-a-group"></a>1人または複数のユーザーを削除するか、グループから1人以上のユーザーを削除する

DROP user *user*\[、 *user*、...\] \[ **\]

### <a name="delete-one-or-more-groups"></a>1つまたは複数のグループを削除する

ドロップグループ*グループ*\[、*グループ*、...\]

DROP USER ステートメントまたは GROUP ステートメントには、次の指定項目があります

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>パーツ</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>user</em></p></td>
<td><p>ワークグループ情報ファイルから削除されるユーザー名。</p></td>
</tr>
<tr class="even">
<td><p><em>グループ</em></p></td>
<td><p>ワークグループ情報ファイルから削除されるグループ名。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

DROP USER ステートメントで FROM キーワードが使用されている場合、ステートメントに記述されている各*ユーザー*は、from キーワードの後に指定した*グループ*から削除されます。 ただし、*ユーザー*自体は削除されません。

DROP GROUP ステートメントは、指定のグループを削除します。 *グループ*のメンバーである*ユーザー*は影響を受けませんが、削除された*グループ*のメンバーになることはなくなります。

