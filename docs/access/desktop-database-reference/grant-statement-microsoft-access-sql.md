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
ms.localizationpriority: medium
ms.openlocfilehash: 977fe06ce2d42616f9212fc8095ba5807aecaf86
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568937"
---
# <a name="grant-statement-microsoft-access-sql"></a>GRANT ステートメント (Microsoft Access SQL)

**適用先:** Access 2013、Office 2013

既存のユーザーまたはグループに与える権限を指定します。

## <a name="syntax"></a>構文

GRANT {*privilege* \[ , *privilege*, ... \] }ON{TABLE *テーブル*|OBJECT *オブジェクト*|

CONTAINER *コンテナー* } TO {*authorizationname* \[ , *authorizationname*, ... \] }

GRANT ステートメントには、次の指定項目があります。

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
<td><p><em>特権</em></p></td>
<td><p>権限を与えます。 特権は、SELECT、DELETE、INSERT、UPDATE、DROP、SELECTSECURITY、UPDATESECURITY、DBPASSWORD、UPDATEIDENTITY、CREATE、SELECTSCHEMA、SCHEMA、および UPDATEOWNER を使用して指定されます。</p></td>
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
<td><p><em>コンテナー</em></p></td>
<td><p>有効なコンテナーの名前。</p></td>
</tr>
<tr class="odd">
<td><p><em>authorizationname</em></p></td>
<td><p>ユーザー名またはグループ名。</p></td>
</tr>
</tbody>
</table>

