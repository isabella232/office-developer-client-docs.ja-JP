---
title: ユーザーの変更、またはデータベースのステートメント (Microsoft Access SQL)
TOCTitle: ALTER USER or DATABASE statement (Microsoft Access SQL)
ms:assetid: 86ccd296-5171-97e7-683f-cdaab4bde9ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197012(v=office.15)
ms:contentKeyID: 48546093
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2514ca6403ce70acae9e344d610fbd7b9ba7d73b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702286"
---
# <a name="alter-user-or-database-statement-microsoft-access-sql"></a>ユーザーの変更、またはデータベースのステートメント (Microsoft Access SQL)

**適用されます**Access 2013、Office 2013。

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

