---
title: Workspace プロパティ (DAO)
TOCTitle: Type Property
ms:assetid: 89e59280-d2cd-b6a2-16c5-9f14f42fdd99
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197086(v=office.15)
ms:contentKeyID: 48546177
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e698963d60809e8d88c4ff87532fb7b74cff275c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311306"
---
# <a name="workspacetype-property-dao"></a>Workspace プロパティ (DAO)


**適用先:** Access 2013、Office 2013

オブジェクトの操作の種類またはデータ型を示す値を設定または取得します。値の取得のみ可能です。整数型 (**Integer**) の値を使用します。

## <a name="syntax"></a>構文

*式*。種類

*式***Workspace**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

**Workspace** オブジェクトの場合、設定できる値と戻り値は次のようになります。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
<th><p>ワークスペースの種類</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbusejet</strong></p></td>
<td><p><strong>Workspace</strong> は Microsoft Access データベース エンジンに接続されます。</p></td>
</tr>
<tr class="even">
<td><p><strong>dbUseODBC</strong></p></td>
<td><p><strong>Workspace</strong> は ODBC データ ソースに接続されます。</p></td>
</tr>
</tbody>
</table>

