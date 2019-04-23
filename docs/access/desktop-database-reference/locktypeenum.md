---
title: locktypeenum (Access デスクトップデータベースリファレンス)
TOCTitle: LockTypeEnum
ms:assetid: 966b4952-5591-4a99-82d5-99cb9ae3fc72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249667(v=office.15)
ms:contentKeyID: 48546448
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d4b9dc49e647bdcd3123ade065da0c74538c9a88
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289865"
---
# <a name="locktypeenum"></a>LockTypeEnum

**適用先:** Access 2013、Office 2013

編集時にレコードに適用されるロックの種類を表します。

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
<td><p><strong>adLockBatchOptimistic</strong></p></td>
<td><p>2/4</p></td>
<td><p>共有的バッチ更新を示します。バッチ更新モードの場合に必要です。</p></td>
</tr>
<tr class="even">
<td><p><strong>adLockOptimistic</strong></p></td>
<td><p>1/3</p></td>
<td><p>レコード単位の共有的ロックを示します。<a href="update-method-ado.md">Update</a> メソッドを呼び出した場合にのみ、プロバイダーは共有的ロックを使ってレコードをロックします。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adLockPessimistic</strong></p></td>
<td><p>pbm-2</p></td>
<td><p>レコード単位の排他的ロックを示します。プロバイダーは、レコードを確実に編集するための措置を行います。通常は、編集直後にデータ ソースでレコードをロックします。</p></td>
</tr>
<tr class="even">
<td><p><strong>adlockreadonly です</strong></p></td>
<td><p>1-d</p></td>
<td><p>読み取り専用のレコードを示します。データの変更はできません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adlockunspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>ロックの種類を指定しません。複製の場合、複製元と同じロックの種類が適用されます。</p></td>
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
<td><p>AdoEnums 楽観的</p></td>
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
<tr class="odd">
<td><p>AdoEnums</p></td>
</tr>
</tbody>
</table>

