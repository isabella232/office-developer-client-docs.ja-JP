---
title: SeekEnum (デスクトップ データベース参照のアクセス)
TOCTitle: SeekEnum
ms:assetid: a0574809-db2d-8759-18cc-fb1cf776e8fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249737(v=office.15)
ms:contentKeyID: 48546706
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a151f7a4549a234c20f76bc1ac93d5eff6cf250
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476209"
---
# <a name="seekenum"></a>SeekEnum


**適用されます**Access 2013 |。Office 2013

実行する [Seek](seek-method-ado.md) の種類を表します。

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
<td><p>adSeekFirstEQ</p></td>
<td><p>1</p></td>
<td><p><em>KeyValues</em> と一致する最初のキーを検索します。</p></td>
</tr>
<tr class="even">
<td><p>adSeekLastEQ</p></td>
<td><p>2</p></td>
<td><p><em>KeyValues</em> と一致する最後のキーを検索します。</p></td>
</tr>
<tr class="odd">
<td><p>adSeekAfterEQ</p></td>
<td><p>4</p></td>
<td><p><em>KeyValues</em> と一致するキー、またはその直後のキーのいずれかを検索します。</p></td>
</tr>
<tr class="even">
<td><p>adSeekAfter</p></td>
<td><p>8</p></td>
<td><p><em>KeyValues</em> と一致するキーの直後のキーを検索します。</p></td>
</tr>
<tr class="odd">
<td><p>adSeekBeforeEQ</p></td>
<td><p>16</p></td>
<td><p><em>KeyValues</em> と一致するキー、またはその直前のキーのいずれかを検索します。</p></td>
</tr>
<tr class="even">
<td><p>adSeekBefore</p></td>
<td><p>32</p></td>
<td><p><em>KeyValues</em> と一致するキーの直前のキーを検索します。</p></td>
</tr>
</tbody>
</table>


**ADO/WFC 等価**

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
<td><p>AdoEnums.Seek.FIRSTEQ</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Seek.LASTEQ</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Seek.AFTEREQ</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Seek.AFTER</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Seek.BEFOREEQ</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Seek.BEFORE</p></td>
</tr>
</tbody>
</table>

