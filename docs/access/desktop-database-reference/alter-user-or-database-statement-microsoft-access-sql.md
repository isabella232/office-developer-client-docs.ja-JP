---
title: ALTER USER ステートメントまたは database ステートメント (Microsoft access SQL)
TOCTitle: ALTER USER or DATABASE statement (Microsoft Access SQL)
ms:assetid: 86ccd296-5171-97e7-683f-cdaab4bde9ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197012(v=office.15)
ms:contentKeyID: 48546093
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2514ca6403ce70acae9e344d610fbd7b9ba7d73b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297180"
---
# <a name="alter-user-or-database-statement-microsoft-access-sql"></a>ALTER USER ステートメントまたは database ステートメント (Microsoft access SQL)

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
<td><p><em>user</em></p></td>
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

