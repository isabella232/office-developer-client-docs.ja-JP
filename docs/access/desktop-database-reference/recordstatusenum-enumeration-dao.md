---
title: RecordStatusEnum 列挙 (DAO)
TOCTitle: RecordStatusEnum Enumeration
ms:assetid: bf4492f2-8d8f-f10f-7a3c-d6296d2ce96b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822784(v=office.15)
ms:contentKeyID: 48547483
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 78f86e8c80a6bbc09499e9512e2daee87fc67998
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477241"
---
# <a name="recordstatusenum-enumeration-dao"></a>RecordStatusEnum 列挙 (DAO)


**適用されます**Access 2013 |。Office 2013

**RecordStatus** プロパティで、一括更新の場合の現在のレコードの更新状態を示すために使用します。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>値</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>dbRecordDBDeleted</p></td>
<td><p>4</p></td>
<td><p>レコードはローカルで削除され、データベース内でも削除されました。</p></td>
</tr>
<tr class="even">
<td><p>dbRecordDeleted</p></td>
<td><p>3</p></td>
<td><p>レコードは削除されましたが、データベース内ではまだ削除されていません。</p></td>
</tr>
<tr class="odd">
<td><p>dbRecordModified</p></td>
<td><p>1</p></td>
<td><p>レコードは変更されましたが、データベース内では更新されていません。</p></td>
</tr>
<tr class="even">
<td><p>dbRecordNew</p></td>
<td><p>2</p></td>
<td><p>レコードは <strong>AddNew</strong> メソッドによって挿入されましたが、データベースにはまだ挿入されていません。</p></td>
</tr>
<tr class="odd">
<td><p>dbRecordUnmodified</p></td>
<td><p>0</p></td>
<td><p>(既定値) レコードはまだ変更されていないか、正しく更新されました。</p></td>
</tr>
</tbody>
</table>

