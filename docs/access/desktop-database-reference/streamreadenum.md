---
title: StreamReadEnum (デスクトップ データベース参照のアクセス)
TOCTitle: StreamReadEnum
ms:assetid: 12432c0d-dc2e-10ea-13db-0c07b6ba29bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248895(v=office.15)
ms:contentKeyID: 48543336
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e4d9c96a7bb34fe0ab3512a316a92e1f7a01ef4b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713661"
---
# <a name="streamreadenum"></a>StreamReadEnum

**適用されます**Access 2013、Office 2013。

[Stream](stream-object-ado.md) オブジェクトから、ストリーム全体を読み取るか、または次の行を読み取るかを表します。

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
<td><p><strong>adReadAll</strong></p></td>
<td><p>-1</p></td>
<td><p>既定値。現在の位置から <a href="eos-property-ado.md">EOS</a> マーカー方向に、すべてのバイトをストリームから読み取ります。これは、バイナリ ストリーム (<a href="type-property-ado-stream.md">Type</a> は <strong>adTypeBinary</strong>) に唯一有効な <strong>StreamReadEnum</strong> 値です。</p></td>
</tr>
<tr class="even">
<td><p><strong>adReadLine</strong></p></td>
<td><p>-2</p></td>
<td><p>ストリームから次の行を読み取ります  (<a href="lineseparator-property-ado.md">LineSeparator</a> プロパティで指定)。</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC に相当

これらの定数に ADO/WFC 等価はありません。

