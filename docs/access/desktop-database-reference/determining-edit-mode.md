---
title: 編集モードの決定
TOCTitle: Determining Edit mode
ms:assetid: 45e21fa7-94e8-3449-e062-09cbcf15cba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249215(v=office.15)
ms:contentKeyID: 48544563
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5e455fd93d009a7fd0a3b4326b8f683b58a390c0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59632057"
---
# <a name="determining-edit-mode"></a>編集モードの決定


**適用先**: Access 2013、Office 2013

ADO では、現在のレコードに関連付けられた編集バッファーが保持されます。 **EditMode** プロパティは、このバッファーに変更が加えられたかどうかや、新しいレコードが作成されたかどうかを示します。 **EditMode** を使用すると、現在のレコードの編集ステータスを判断できます。編集処理が中断された場合に、保留中の変更を確認し、 **Update** メソッドまたは **CancelUpdate** メソッドを使用する必要があるかどうかを判断できます。

**EditMode** は、次の表に示す **EditModeEnum** 定数のうちいずれか 1 つを返します。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adEditNone</strong></p></td>
<td><p>進行中の編集操作がないことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adEditInProgress</strong></p></td>
<td><p>現在のレコードのデータが変更されたが、保存されていないことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adEditAdd</strong></p></td>
<td><p><strong>AddNew</strong> メソッドが呼び出されたことを示します。このため、コピー バッファー内の現在のレコードは、データベースに保存されていない新しいレコードです。</p></td>
</tr>
<tr class="even">
<td><p><strong>adEditDelete</strong></p></td>
<td><p>現在のレコードが削除されたことを示します。</p></td>
</tr>
</tbody>
</table>


**EditMode** が有効な値を返すことができるのは、現在のレコードが存在する場合のみです。 **EditMode** は、 **BOF** または **EOF** が **True** であるか、現在のレコードが削除されている場合には、エラーを返します。

