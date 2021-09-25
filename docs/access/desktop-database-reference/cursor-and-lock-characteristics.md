---
title: カーソルとロックの特性
TOCTitle: Cursor and lock characteristics
ms:assetid: 5f8b6700-14f6-d342-42f6-cc8e89c71a1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249347(v=office.15)
ms:contentKeyID: 48545164
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: e7793aa5beca79b8027abde8f3434a1b4d321417
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585999"
---
# <a name="cursor-and-lock-characteristics"></a>カーソルとロックの特性

**適用先**: Access 2013、Office 2013

カーソルの特性はプロバイダーの機能によって異なりますが、一般には、カーソルとロックの種類別に、次のような長所と短所があります。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>カーソルまたはロックの種類</p></th>
<th><p>メリット</p></th>
<th><p>デメリット</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adOpenForwardOnly</strong></p></td>
<td><p></p>
<ul>
<li><p>必要なリソースが少ない</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>後方にスクロールできない</p></li>
<li><p>データの同時操作ができない</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenStatic</strong></p></td>
<td><p></p>
<ul>
<li><p>スクロール可能</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>データの同時操作ができない</p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenKeyset</strong></p></td>
<td><p></p>
<ul>
<li><p>データの同時操作が部分的にできる</p></li>
<li><p>スクロール可能</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>必要なリソースが比較的多い</p></li>
<li><p>ネットワークに接続されていない場合は使用できない</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenDynamic</strong></p></td>
<td><p></p>
<ul>
<li><p>データの高度な同時操作ができる</p></li>
<li><p>スクロール可能</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>必要なリソースが最も多い</p></li>
<li><p>ネットワークに接続されていない場合は使用できない</p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><strong>adLockReadOnly</strong></p></td>
<td><p></p>
<ul>
<li><p>必要なリソースが少ない</p></li>
<li><p>拡張性が高い</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>カーソルを通じてデータを更新できない</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adLockBatchOptimistic</strong></p></td>
<td><p></p>
<ul>
<li><p>バッチ更新ができる</p></li>
<li><p>ネットワークに接続されていない場合も使用できる</p></li>
<li><p>他のユーザーがデータにアクセスできる</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>データが複数のユーザーによって同時に変更される可能性がある</p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><strong>adLockPessimistic</strong></p></td>
<td><p></p>
<ul>
<li><p>ロックされているときは他のユーザーがデータを変更できない</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>ロックされているときは他のユーザーがデータにアクセスできない</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adLockOptimistic</strong></p></td>
<td><p></p>
<ul>
<li><p>他のユーザーがデータにアクセスできる</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>データが複数のユーザーによって同時に変更される可能性がある</p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

