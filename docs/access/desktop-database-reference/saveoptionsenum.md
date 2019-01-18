---
title: SaveOptionsEnum (デスクトップ データベース参照のアクセス)
TOCTitle: SaveOptionsEnum
ms:assetid: 2a4e4c7a-6331-7270-0514-cc549c721ffd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249053(v=office.15)
ms:contentKeyID: 48543906
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77a617dc54d8acd145648d926e10cf7c9a3cf252
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705996"
---
# <a name="saveoptionsenum"></a>SaveOptionsEnum

**適用されます**Access 2013、Office 2013。

[Stream](stream-object-ado.md) オブジェクトからファイルに保存するときに、ファイルを作成するか、上書きするかを表します。これらの値は AND 演算子で結合できます。

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
<td><p><strong>adSaveCreateNotExist</strong></p></td>
<td><p>1</p></td>
<td><p>既定値。<em>FileName</em> パラメーターで指定したファイルがない場合は新しいファイルが作成されます。</p></td>
</tr>
<tr class="even">
<td><p><strong>adSaveCreateOverWrite</strong></p></td>
<td><p>2</p></td>
<td><p><em>Filename</em> パラメーターで指定したファイルがある場合は、現在開かれている <strong>Stream</strong> オブジェクトのデータでファイルが上書きされます。</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC に相当

これらの定数に ADO/WFC 等価はありません。

