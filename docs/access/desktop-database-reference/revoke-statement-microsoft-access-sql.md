---
title: ステートメント (Microsoft Access SQL) を失効させる
TOCTitle: REVOKE statement (Microsoft Access SQL)
ms:assetid: 69399fd6-c4e8-f2e2-e5f4-48ae779323f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195272(v=office.15)
ms:contentKeyID: 48545409
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277479
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c3a7a64eee4617c07c1a655e34223f0531e16b18
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2018
ms.locfileid: "25890898"
---
# <a name="revoke-statement-microsoft-access-sql"></a>ステートメント (Microsoft Access SQL) を失効させる

**適用されます**Access 2013、Office 2013。

既存のユーザーまたはグループから、指定の権限を無効にします。

## <a name="syntax"></a>構文

取り消し {*特権*\[、*特権*、.\]} に {テーブル*テーブル*|オブジェクトの*オブジェクト*|

コンテナー*コンテナー*} から {*authorizationname*\[、 *authorizationname*、.\]}

REVOKE ステートメントには、次の指定項目があります。

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
<td><p><em>privilege</em></p></td>
<td><p>権限または特権を無効にします。 次のキーワードを使用する権限を指定します。] を選択、削除、挿入、更新、ドロップ、SELECTSECURITY、UPDATESECURITY、DBPASSWORD、UPDATEIDENTITY、作成、SELECTSCHEMA、スキーマ、および UPDATEOWNER。</p></td>
</tr>
<tr class="even">
<td><p><em>table</em></p></td>
<td><p>任意の有効なテーブル名。</p></td>
</tr>
<tr class="odd">
<td><p><em>object</em></p></td>
<td><p>テーブル以外のどのオブジェクトも指定できます。たとえば、ストアド クエリ (ビューまたはプロシージャ) を指定できます。</p></td>
</tr>
<tr class="even">
<td><p><em>container</em></p></td>
<td><p>有効なコンテナーの名前。</p></td>
</tr>
<tr class="odd">
<td><p><em>authorizationname</em></p></td>
<td><p>ユーザー名またはグループ名。</p></td>
</tr>
</tbody>
</table>

