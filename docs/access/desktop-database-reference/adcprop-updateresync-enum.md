---
title: ADCPROP_UPDATERESYNC_ENUM
TOCTitle: ADCPROP_UPDATERESYNC_ENUM
ms:assetid: 890210c4-2290-ddb2-8814-022093c318de
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249600(v=office.15)
ms:contentKeyID: 48546145
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 056e68456b3f5bcf30768b0a5a616467c8271a5a
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861408"
---
# <a name="adcpropupdateresyncenum"></a>ADCPROP\_UPDATERESYNC\_列挙型

**適用されます**Access 2013 |。Office 2013

[UpdateBatch](updatebatch-method-ado.md) メソッドに暗黙の [Resync](resync-method-ado.md) メソッド操作が続くかどうかを示し、続く場合はその操作の適用範囲を指定します。

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
<th><p>値</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adResyncAll</strong></p></td>
<td><p>15</p></td>
<td><p>他のすべての ADCPROP_UPDATERESYNC_ENUM メンバーの結合された値を使用して、<strong>Resync</strong> を呼び出します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adResyncAutoIncrement</strong></p></td>
<td><p>1</p></td>
<td><p>既定値です。Microsoft Jet AutoNumber フィールドや Microsoft SQL Server の Identity 列など、データ ソースによって自動的に増分または生成される列の新しい ID 値を取得します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adResyncConflicts</strong></p></td>
<td><p>2</p></td>
<td><p>同時実行の競合により更新操作または削除操作が失敗したすべての行について、<strong>Resync</strong> を呼び出します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adResyncInserts</strong></p></td>
<td><p>8</p></td>
<td><p>正常に挿入されたすべての行について、 <strong>Resync</strong>を呼び出します。 ただし、オートインクリメント ・ カラムの値は再同期できません。 代わりに、新しく挿入された行の内容は、既存の主キーの値に基づいて再同期化されます。 主キーがオートインクリメント値の場合は、<strong>再同期</strong>と、目的の行の内容を取得できません。 オートインクリメント ・ プライマリ ・ キー値を自動的にインクリメントするには、合計値の<strong>adResyncAutoIncrement</strong> + <strong>adResyncInserts</strong>に<strong>UpdateBatch</strong>を呼び出します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adResyncNone</strong></p></td>
<td><p>0</p></td>
<td><p><strong>Resync</strong> を呼び出しません。</p></td>
</tr>
<tr class="even">
<td><p><strong>adResyncUpdates</strong></p></td>
<td><p>4</p></td>
<td><p>正常に更新されたすべての行について、<strong>Resync</strong> を呼び出します。</p></td>
</tr>
</tbody>
</table>

