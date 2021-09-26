---
title: ADD USER ステートメント (Microsoft Access SQL)
TOCTitle: ADD USER statement (Microsoft Access SQL)
ms:assetid: 1feb631f-cb8c-14ae-6214-276f1faf1a55
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845862(v=office.15)
ms:contentKeyID: 48543652
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 9eed2a6f66a2e23294aa3354178a051fe4a699b7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590171"
---
# <a name="add-user-statement-microsoft-access-sql"></a>ADD USER ステートメント (Microsoft Access SQL)

**適用先**: Access 2013、Office 2013

既存のユーザーを既存のグループに追加します。

## <a name="syntax"></a>構文

ADD USER *user* \[ , *user*, ... \]TO *グループ*

ADD USER ステートメントには次の指定項目があります。

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
<td><p><em>ユーザー</em></p></td>
<td><p>ワークグループ情報ファイルに追加されるユーザーの名前。</p></td>
</tr>
<tr class="even">
<td><p><em>group</em></p></td>
<td><p>ワークグループ情報ファイルに追加されるグループの名前。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

ユーザーが *グループ* に追加された後、そのユーザーには、グループに付与されているすべてのアクセス許可が付与 *されます*。

