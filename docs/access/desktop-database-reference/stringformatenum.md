---
title: StringFormatEnum (デスクトップ データベース参照のアクセス)
TOCTitle: StringFormatEnum
ms:assetid: ab069d67-d983-f390-5d45-876a9f9d9691
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249794(v=office.15)
ms:contentKeyID: 48546964
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 0e673c7ae5a7e0c6e2ffa2120ed52a4b726a834d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881147"
---
# <a name="stringformatenum"></a>StringFormatEnum

**適用されます**Access 2013、Office 2013。

文字列として [Recordset](recordset-object-ado.md) を取得するときの形式を表します。

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
<td><p><strong>adClipString</strong></p></td>
<td><p>2</p></td>
<td><p>行が <em>RowDelimiter</em> によって、列が <em>ColumnDelimiter</em> によって、null 値が <em>NullExpr</em> によって区切られます。<a href="getstring-method-ado.md">GetString</a> メソッドのこれらの 3 つのパラメーターは、<strong>adClipString</strong> の <em>StringFormat</em> とのみ併用できます。</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC に相当

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
<td><p>AdoEnums.StringFormat.CLIPSTRING</p></td>
</tr>
</tbody>
</table>

