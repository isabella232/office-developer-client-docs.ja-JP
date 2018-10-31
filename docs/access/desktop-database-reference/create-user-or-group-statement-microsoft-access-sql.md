---
title: 作成するユーザーまたはグループのステートメント (Microsoft Access SQL)
TOCTitle: CREATE USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 62148ce2-0f81-944e-a1ab-edef990fff9f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194914(v=office.15)
ms:contentKeyID: 48545229
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 391c31240acf33a458895b00335d1600b975e834
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862647"
---
# <a name="create-user-or-group-statement-microsoft-access-sql"></a>作成するユーザーまたはグループのステートメント (Microsoft Access SQL)

**適用されます**Access 2013 |。Office 2013

ユーザーまたはグループを作成します。

## <a name="syntax"></a>構文

**ユーザーを作成**します。

ユーザーの作成*ユーザー* *パスワード pid* \[、*ユーザー* *パスワード pid*、.\]

**グループを作成**します。

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

