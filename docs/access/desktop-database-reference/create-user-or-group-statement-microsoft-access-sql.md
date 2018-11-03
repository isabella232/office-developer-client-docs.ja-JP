---
title: 作成するユーザーまたはグループのステートメント (Microsoft Access SQL)
TOCTitle: CREATE USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 62148ce2-0f81-944e-a1ab-edef990fff9f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194914(v=office.15)
ms:contentKeyID: 48545229
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 52d376b05c195ed0ea4707e849c5ae395c2b5590
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936827"
---
# <a name="create-user-or-group-statement-microsoft-access-sql"></a>作成するユーザーまたはグループのステートメント (Microsoft Access SQL)

**適用されます**Access 2013、Office 2013。

ユーザーまたはグループを作成します。

## <a name="syntax"></a>構文

### <a name="create-a-user"></a>ユーザーを作成します。

ユーザーの作成*ユーザー* *パスワード pid* \[、*ユーザー* *パスワード pid*、.\]

### <a name="create-a-group"></a>グループを作成します。

グループの作成*グループ* *pid*\[、*グループ* *pid*をしています.\]

CREATE USER ステートメントまたは GROUP ステートメントには次の指定項目があります。

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
<td><p>ワークグループ情報ファイルに追加されるユーザーの名前。</p></td>
</tr>
<tr class="even">
<td><p><em>group</em></p></td>
<td><p>ワークグループ情報ファイルに追加されるグループの名前</p></td>
</tr>
<tr class="odd">
<td><p><em>password</em></p></td>
<td><p>指定した<em>ユーザー</em>名に関連付けられるパスワード。</p></td>
</tr>
<tr class="even">
<td><p><em>pid</em></p></td>
<td><p>パーソナル ID</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

*ユーザー*と*グループ*は、同じ名前を持つことはできません。

*パスワード*は、各*ユーザー*または*グループ*を作成する必要があります。

