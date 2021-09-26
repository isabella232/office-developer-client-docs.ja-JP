---
title: DROP USER または GROUP ステートメント (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4054256c8a158fdee13af683a4bd80ea93647985
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597437"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a>DROP USER または GROUP ステートメント (Microsoft Access SQL)

**適用先**: Access 2013、Office 2013

1 つ以上の既存 *のユーザーまたはグループ* を *削除* するか、既存のグループから1 つ以上の既存のユーザーを削除 *します*。

## <a name="syntax"></a>構文

### <a name="delete-one-or-more-users-or-remove-one-or-more-users-from-a-group"></a>1 人または複数のユーザーを削除するか、グループから 1 人または複数のユーザーを削除する

DROP USER *user* \[ , *user*, ... \] \[FROM *グループ*\]

### <a name="delete-one-or-more-groups"></a>1 つ以上のグループを削除する

DROP GROUP *group* \[ , *group*, ...\]

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
<td><p><em>ユーザー</em></p></td>
<td><p>ワークグループ情報ファイルから削除されるユーザー名。</p></td>
</tr>
<tr class="even">
<td><p><em>group</em></p></td>
<td><p>ワークグループ情報ファイルから削除されるグループ名。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

FROM キーワードが DROP USER ステートメントで使用されている場合、ステートメントにリストされている各ユーザーは、FROM キーワードの後に指定されたグループから削除されます。 ただし、 *ユーザー* 自身は削除されません。

DROP GROUP ステートメントは、指定のグループを削除します。 グループ *の* メンバーであるユーザーは影響を受け取りますが、削除されたグループの *メンバーではなくなりました*。

