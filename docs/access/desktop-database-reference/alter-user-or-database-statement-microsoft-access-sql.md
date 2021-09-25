---
title: ALTER USER または DATABASE ステートメント (Microsoft Access SQL)
TOCTitle: ALTER USER or DATABASE statement (Microsoft Access SQL)
ms:assetid: 86ccd296-5171-97e7-683f-cdaab4bde9ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197012(v=office.15)
ms:contentKeyID: 48546093
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 9e2ef710d9a7036cc9f15e2c69d37e84393f978d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559074"
---
# <a name="alter-user-or-database-statement-microsoft-access-sql"></a>ALTER USER または DATABASE ステートメント (Microsoft Access SQL)

**適用先:** Access 2013、Office 2013

既存のユーザーまたはデータベースのパスワードを変更します。

## <a name="syntax"></a>構文

ALTER DATABASE PASSWORD *newpassword oldpassword*

ALTER USER *user* PASSWORD *newpassword oldpassword*

ALTER USER ステートメントまたは DATABASE ステートメントには次の指定項目があります。

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
<td><p><em>newpassword</em></p></td>
<td><p>指定のユーザー名またはデータベース名に関連付けられる新規のパスワード。</p></td>
</tr>
<tr class="odd">
<td><p><em>oldpassword</em></p></td>
<td><p>指定のユーザー名またはグループ名に関連付けられる既存のパスワード。</p></td>
</tr>
</tbody>
</table>

