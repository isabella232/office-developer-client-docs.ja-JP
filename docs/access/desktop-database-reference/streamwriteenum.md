---
title: streamwriteenum (Access デスクトップデータベースリファレンス)
TOCTitle: StreamWriteEnum
ms:assetid: b4356999-d7a8-abfa-f6a8-6c2dd04b9257
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249861(v=office.15)
ms:contentKeyID: 48547216
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 87144e5409fb54cf0cb8f59ad4d593ab05d694a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308478"
---
# <a name="streamwriteenum"></a>StreamWriteEnum

**適用先:** Access 2013、Office 2013

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
<td><p>.0</p></td>
<td><p>既定値。<strong>Stream</strong> オブジェクトに、<em>Data</em> パラメーターで指定したテキスト文字列を書き込みます。</p></td>
</tr>
<tr class="even">
<td><p><strong>adwriteline</strong></p></td>
<td><p>1-d</p></td>
<td><p><strong>Stream</strong> オブジェクトに、テキスト文字列と行区切り記号を書き込みます。<a href="lineseparator-property-ado.md">LineSeparator</a> プロパティが定義されていない場合は、実行時エラーを返します。</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC と同等

これらの定数に ADO/WFC 等価はありません。

