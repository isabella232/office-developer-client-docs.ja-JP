---
title: REVOKE ステートメント (Microsoft Access SQL)
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
ms.localizationpriority: medium
ms.openlocfilehash: 41ae1f88b89a7fb0293b4f0cd3df500687edd799
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580889"
---
# <a name="revoke-statement-microsoft-access-sql"></a>REVOKE ステートメント (Microsoft Access SQL)

**適用先:** Access 2013、Office 2013

既存のユーザーまたはグループから、指定の権限を無効にします。

## <a name="syntax"></a>構文

REVOKE {*privilege* \[ , *privilege*, ... \] }ON {TABLE *table |* OBJECT *オブジェクト*|

CONTAINTER *コンテナー*} FROM {*authorizationname* \[ , *authorizationname*, ... \] }

REVOKE ステートメントには、次の指定項目があります。

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
<td><p>権限を無効にします。 特権は、SELECT、DELETE、INSERT、UPDATE、DROP、SELECTSECURITY、UPDATESECURITY、DBPASSWORD、UPDATEIDENTITY、CREATE、SELECTSCHEMA、SCHEMA、および UPDATEOWNER を使用して指定されます。</p></td>
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
<td><p><em>コンテナー</em></p></td>
<td><p>有効なコンテナーの名前。</p></td>
</tr>
<tr class="odd">
<td><p><em>authorizationname</em></p></td>
<td><p>ユーザー名またはグループ名。</p></td>
</tr>
</tbody>
</table>

