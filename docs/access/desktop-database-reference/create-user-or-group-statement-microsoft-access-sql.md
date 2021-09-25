---
title: CREATE USER または GROUP ステートメント (Microsoft Access SQL)
TOCTitle: CREATE USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 62148ce2-0f81-944e-a1ab-edef990fff9f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194914(v=office.15)
ms:contentKeyID: 48545229
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5da68a0574bb0e81a403f456e48f6dd1b965b9e6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569210"
---
# <a name="create-user-or-group-statement-microsoft-access-sql"></a>CREATE USER または GROUP ステートメント (Microsoft Access SQL)

**適用先:** Access 2013、Office 2013

ユーザーまたはグループを作成します。

## <a name="syntax"></a>構文

### <a name="create-a-user"></a>ユーザーの作成

CREATE USER *user* *password pid* \[ , *user* *password pid*, ...\]

### <a name="create-a-group"></a>グループを作成する

CREATE GROUP *group* *pid* \[ , *group* *pid*, ...\]

CREATE USER ステートメントまたは GROUP ステートメントには次の指定項目があります。

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
<td><p>ワークグループ情報ファイルに追加されるユーザーの名前。</p></td>
</tr>
<tr class="even">
<td><p><em>group</em></p></td>
<td><p>ワークグループ情報ファイルに追加されるグループの名前</p></td>
</tr>
<tr class="odd">
<td><p><em>password</em></p></td>
<td><p>指定のユーザー名に関連付けられるパスワード</p></td>
</tr>
<tr class="even">
<td><p><em>pid</em></p></td>
<td><p>パーソナル ID</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

ユーザーとグループは、違う名前にする必要があります。

作成されたユーザーまたはグループごとにパスワードが必要です。

