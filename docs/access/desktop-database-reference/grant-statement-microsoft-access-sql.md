---
title: GRANT ステートメント (Microsoft Access SQL)
TOCTitle: GRANT Statement (Microsoft Access SQL)
ms:assetid: 50ae97ae-d5be-57e5-d9da-f3fc42f01d83
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193820(v=office.15)
ms:contentKeyID: 48544800
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277478
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d4fffc9ac40586be899de0dd4054ba39dd3a6489
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476229"
---
# <a name="grant-statement-microsoft-access-sql"></a>GRANT ステートメント (Microsoft Access SQL)


**適用されます**Access 2013 |。Office 2013

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
<td><p>特権または権限が与えられます。 次のキーワードを使用する権限を指定: 選択、削除、挿入、更新、削除、SELECTSECURITY、UPDATESECURITY、DBPASSWORD、UPDATEIDENTITY、作成、SELECTSCHEMA、スキーマおよび UPDATEOWNER。</p></td>
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

