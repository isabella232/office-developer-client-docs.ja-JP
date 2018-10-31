---
title: StreamWriteEnum (デスクトップ データベース参照のアクセス)
TOCTitle: StreamWriteEnum
ms:assetid: b4356999-d7a8-abfa-f6a8-6c2dd04b9257
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249861(v=office.15)
ms:contentKeyID: 48547216
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 76286fcd09e5b92f19d8dbf0e8d0419ad4c600df
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861891"
---
# <a name="streamwriteenum"></a>StreamWriteEnum

**適用されます**Access 2013 |。Office 2013

[Stream](stream-object-ado.md) オブジェクトに書き込む文字列に、行区切り記号を追加するかどうかを表します。

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
<td><p><strong>adWriteChar</strong></p></td>
<td><p>0</p></td>
<td><p>既定値。<strong>Stream</strong> オブジェクトに、<em>Data</em> パラメーターで指定したテキスト文字列を書き込みます。</p></td>
</tr>
<tr class="even">
<td><p><strong>adWriteLine</strong></p></td>
<td><p>1</p></td>
<td><p><strong>Stream</strong> オブジェクトに、テキスト文字列と行区切り記号を書き込みます。<a href="lineseparator-property-ado.md">LineSeparator</a> プロパティが定義されていない場合は、実行時エラーを返します。</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC に相当

これらの定数に ADO/WFC 等価はありません。

