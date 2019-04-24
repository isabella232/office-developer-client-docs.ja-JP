---
title: editmodeenum (Access デスクトップデータベースリファレンス)
TOCTitle: EditModeEnum
ms:assetid: 4da0e504-aca2-b769-04a2-0df687fa4422
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249248(v=office.15)
ms:contentKeyID: 48544737
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 246d9e29f084efb975783fd15c15993eba5a6e74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293582"
---
# <a name="editmodeenum"></a>EditModeEnum

**適用先:** Access 2013、Office 2013

レコードの編集状況を示します。

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
<td><p><strong>adEditNone</strong></p></td>
<td><p>.0</p></td>
<td><p>進行中の編集操作がないことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adEditInProgress</strong></p></td>
<td><p>1-d</p></td>
<td><p>現在のレコードのデータが変更されたが、保存されていないことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adEditAdd</strong></p></td>
<td><p>pbm-2</p></td>
<td><p><a href="addnew-method-ado.md">AddNew</a> メソッドが呼び出され、コピー バッファー内の現在のレコードが、データベースに保存されていない新しいレコードであることを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adEditDelete</strong></p></td>
<td><p>2/4</p></td>
<td><p>現在のレコードが削除されたことを示します。</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC と同等

パッケージ: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums</p></td>
</tr>
</tbody>
</table>

