---
title: GRANT ステートメント (Microsoft Access SQL)
TOCTitle: GRANT statement (Microsoft Access SQL)
ms:assetid: 50ae97ae-d5be-57e5-d9da-f3fc42f01d83
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193820(v=office.15)
ms:contentKeyID: 48544800
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277478
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7c109d1993d4f092439ae10828ce3143625b4ad6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871956"
---
# <a name="grant-statement-microsoft-access-sql"></a>GRANT ステートメント (Microsoft Access SQL)

**適用されます**Access 2013、Office 2013。

既存のユーザーまたはグループに与える権限を指定します。

## <a name="syntax"></a>構文

付与 {*特権*\[、*特権*、.\]} に {テーブル*テーブル*|オブジェクトの*オブジェクト*|

コンテナー*コンテナー* } に {*authorizationname*\[、 *authorizationname*、.\]}

GRANT ステートメントには、次の指定項目があります。

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
<td><p>特権または権限が与えられます。 次のキーワードを使用する権限を指定します。] を選択、削除、挿入、更新、ドロップ、SELECTSECURITY、UPDATESECURITY、DBPASSWORD、UPDATEIDENTITY、作成、SELECTSCHEMA、スキーマ、および UPDATEOWNER。</p></td>
</tr>
<tr class="even">
<td><p><em>tablename</em></p></td>
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

