---
title: UpdateCriteriaEnum 列挙 (DAO)
TOCTitle: UpdateCriteriaEnum Enumeration
ms:assetid: 1f83a0c6-bdc8-9c3e-380b-524f611f6476
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845853(v=office.15)
ms:contentKeyID: 48543644
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e27eb1bdfb9b393df76af8bdf54bc7f05fd82c2e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306371"
---
# <a name="updatecriteriaenum-enumeration-dao"></a>UpdateCriteriaEnum 列挙 (DAO)


**適用先:** Access 2013、Office 2013

**UpdateOptions** メソッドで、一括更新の構築方法を指定するために使用します。

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
<td><p>dbの基準 aallcols</p></td>
<td><p>2/4</p></td>
<td><p>キー列 (1 つまたは複数) とすべての列を where 句で使用します。</p></td>
</tr>
<tr class="even">
<td><p>dbの基準 adeleteinsert</p></td>
<td><p>16</p></td>
<td><p>変更された行ごとに、DELETE ステートメントと INSERT ステートメントのペアを使用します。</p></td>
</tr>
<tr class="odd">
<td><p>dbCriteriaKey</p></td>
<td><p>1-d</p></td>
<td><p>キー列 (1 つまたは複数) のみを where 句で使用します。</p></td>
</tr>
<tr class="even">
<td><p>dbCriteriaModValues</p></td>
<td><p>pbm-2</p></td>
<td><p>キー列 (1 つまたは複数) と更新されたすべての列を where 句で使用します。</p></td>
</tr>
<tr class="odd">
<td><p>dbmeたスタンプ</p></td>
<td><p>~</p></td>
<td><p>タイムスタンプ列が使用可能な場合、タイムスタンプ列のみを使用します (結果セットにタイムスタンプ列が含まれない場合は、実行時エラーを生成します)。</p></td>
</tr>
<tr class="even">
<td><p>dbCriteriaUpdate</p></td>
<td><p>32</p></td>
<td><p>変更された行ごとに UPDATE ステートメントを使用します。</p></td>
</tr>
</tbody>
</table>

