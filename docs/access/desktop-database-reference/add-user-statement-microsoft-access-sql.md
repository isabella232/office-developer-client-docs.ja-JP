---
title: ユーザーの追加のステートメント (Microsoft Access SQL)
TOCTitle: ADD USER statement (Microsoft Access SQL)
ms:assetid: 1feb631f-cb8c-14ae-6214-276f1faf1a55
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845862(v=office.15)
ms:contentKeyID: 48543652
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 7a27874a7264258fee51f90fabaeecd180d7aeae
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868610"
---
# <a name="add-user-statement-microsoft-access-sql"></a>ユーザーの追加のステートメント (Microsoft Access SQL)

**適用されます**Access 2013、Office 2013。

1 つまたは複数の既存の*ユーザー*の既存の*グループ*に追加します。

## <a name="syntax"></a>構文

ユーザーの追加*ユーザー*\[、*ユーザー*、.\] *グループ*に

ADD USER ステートメントには次の指定項目があります。

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
<td><p><em>group</em></p></td>
<td><p>ワークグループ情報ファイルに追加されるグループの名前。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

*ユーザー* *グループ*に追加された後、*ユーザー*は、*グループ*に与えられているすべてのアクセス許可を持っています。

