---
title: ユーザーの変更、またはデータベースのステートメント (Microsoft Access SQL)
TOCTitle: ALTER USER or DATABASE statement (Microsoft Access SQL)
ms:assetid: 86ccd296-5171-97e7-683f-cdaab4bde9ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197012(v=office.15)
ms:contentKeyID: 48546093
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: ad03607b6452da016bad09fd33561bd811a2a16d
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862612"
---
# <a name="alter-user-or-database-statement-microsoft-access-sql"></a>ユーザーの変更、またはデータベースのステートメント (Microsoft Access SQL)

**適用されます**Access 2013 |。Office 2013

既存のユーザーまたはデータベースのパスワードを変更します。

## <a name="syntax"></a>構文

*Newpassword oldpassword*のデータベース パスワードの変更

ユーザーの変更*ユーザー*のパスワード*newpassword oldpassword*

ALTER USER ステートメントまたは DATABASE ステートメントには次の指定項目があります。

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
<td><p><em>newpassword</em></p></td>
<td><p>指定した<em>ユーザー</em>名または<em>データベース</em>名に関連付けられる新しいパスワードです。</p></td>
</tr>
<tr class="odd">
<td><p><em>oldpassword</em></p></td>
<td><p>指定した<em>ユーザー</em>または<em>グループ</em>名に関連付けられる既存のパスワード。</p></td>
</tr>
</tbody>
</table>

