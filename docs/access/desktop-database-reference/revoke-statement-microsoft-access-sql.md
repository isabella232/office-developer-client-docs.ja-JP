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
localization_priority: Normal
ms.openlocfilehash: 20122fee617597987940766a076d5f968a87c2d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306532"
---
# <a name="revoke-statement-microsoft-access-sql"></a>REVOKE ステートメント (Microsoft Access SQL)

**適用先:** Access 2013、Office 2013

既存のユーザーまたはグループから、指定の権限を無効にします。

## <a name="syntax"></a>構文

REVOKE {*privilege*\[,*特権*,...\]} {table *table* |object*オブジェクト*|

{*authorizationname*\[, *authorizationname*,... **\]}

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
<td><p><em>オペレーター</em></p></td>
<td><p>権限を無効にします。 権限は、SELECT、DELETE、INSERT、UPDATE、DROP、selectsecurity、UPDATESECURITY、dbpassword、UPDATEIDENTITY、CREATE、selectsecurity、schema、および updateowner の各キーワードを使用して指定します。</p></td>
</tr>
<tr class="even">
<td><p><em>テーブル</em></p></td>
<td><p>任意の有効なテーブル名。</p></td>
</tr>
<tr class="odd">
<td><p><em>object</em></p></td>
<td><p>テーブル以外のどのオブジェクトも指定できます。 たとえば、ストアド クエリ (ビューまたはプロシージャ) を指定できます。</p></td>
</tr>
<tr class="even">
<td><p><em>格納</em></p></td>
<td><p>有効なコンテナーの名前。</p></td>
</tr>
<tr class="odd">
<td><p><em>authorizationname</em></p></td>
<td><p>ユーザー名またはグループ名。</p></td>
</tr>
</tbody>
</table>

