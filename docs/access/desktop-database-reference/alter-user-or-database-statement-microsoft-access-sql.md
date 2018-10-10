---
title: ALTER USER ステートメントまたは DATABASE ステートメント (Microsoft Access SQL)
TOCTitle: ALTER USER or DATABASE Statement (Microsoft Access SQL)
ms:assetid: 86ccd296-5171-97e7-683f-cdaab4bde9ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197012(v=office.15)
ms:contentKeyID: 48546093
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2d6e471adb7ef2c5826d24f569174b40247d0fd8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477414"
---
# <a name="alter-user-or-database-statement-microsoft-access-sql"></a>ALTER USER ステートメントまたは DATABASE ステートメント (Microsoft Access SQL)


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

