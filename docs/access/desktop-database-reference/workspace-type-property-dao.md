---
title: Workspace.Type プロパティ (DAO)
TOCTitle: Type Property
ms:assetid: 89e59280-d2cd-b6a2-16c5-9f14f42fdd99
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197086(v=office.15)
ms:contentKeyID: 48546177
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d062adbde4e9d7053e61342b7433939d4fbffcb8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476861"
---
# <a name="workspacetype-property-dao"></a>Workspace.Type プロパティ (DAO)


**適用されます**Access 2013 |。Office 2013

オブジェクトの操作の種類またはデータ型を示す値を設定または取得します。値の取得のみ可能です。整数型 ( **Integer** ) の値を使用します。

## <a name="syntax"></a>構文

*式*です。タイプ

*式***ワークスペース**オブジェクトを表す変数です。

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
<td><p><strong>dbUseJet</strong></p></td>
<td><p><strong>Workspace</strong> は Microsoft Access データベース エンジンに接続されます。</p></td>
</tr>
<tr class="even">
<td><p><strong>dbUseODBC</strong></p></td>
<td><p><strong>Workspace</strong> は ODBC データ ソースに接続されます。</p></td>
</tr>
</tbody>
</table>

