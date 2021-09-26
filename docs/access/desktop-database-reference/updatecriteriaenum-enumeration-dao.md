---
title: UpdateCriteriaEnum 列挙 (DAO)
TOCTitle: UpdateCriteriaEnum Enumeration
ms:assetid: 1f83a0c6-bdc8-9c3e-380b-524f611f6476
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845853(v=office.15)
ms:contentKeyID: 48543644
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ca550cf77b70d27cd1fbc8b7b21af98fe10d7e54
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621627"
---
# <a name="updatecriteriaenum-enumeration-dao"></a>UpdateCriteriaEnum 列挙 (DAO)


**適用先**: Access 2013、Office 2013

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
<td><p>dbCriteriaAllCols</p></td>
<td><p>4 </p></td>
<td><p>キー列 (1 つまたは複数) とすべての列を where 句で使用します。</p></td>
</tr>
<tr class="even">
<td><p>dbCriteriaDeleteInsert</p></td>
<td><p>16 </p></td>
<td><p>変更された行ごとに、DELETE ステートメントと INSERT ステートメントのペアを使用します。</p></td>
</tr>
<tr class="odd">
<td><p>dbCriteriaKey</p></td>
<td><p>1</p></td>
<td><p>キー列 (1 つまたは複数) のみを where 句で使用します。</p></td>
</tr>
<tr class="even">
<td><p>dbCriteriaModValues</p></td>
<td><p>2</p></td>
<td><p>キー列 (1 つまたは複数) と更新されたすべての列を where 句で使用します。</p></td>
</tr>
<tr class="odd">
<td><p>dbCriteriaTimestamp</p></td>
<td><p>8 </p></td>
<td><p>タイムスタンプ列が使用可能な場合、タイムスタンプ列のみを使用します (結果セットにタイムスタンプ列が含まれない場合は、実行時エラーを生成します)。</p></td>
</tr>
<tr class="even">
<td><p>dbCriteriaUpdate</p></td>
<td><p>32</p></td>
<td><p>変更された行ごとに UPDATE ステートメントを使用します。</p></td>
</tr>
</tbody>
</table>

