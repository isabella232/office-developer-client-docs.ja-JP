---
title: XactAttributeEnum (Access デスクトップ データベース リファレンス)
TOCTitle: XactAttributeEnum
ms:assetid: 9206698b-7cfa-1229-2701-f2b6949e54fc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249643(v=office.15)
ms:contentKeyID: 48546366
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: fd37696d5bf83d96259548cfda7d804183d5fd60
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593195"
---
# <a name="xactattributeenum"></a>XactAttributeEnum

**適用先**: Access 2013、Office 2013

[Connection](connection-object-ado.md) オブジェクトのトランザクション属性を表します。

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
<td><p><strong>adXactAbortRetaining</strong></p></td>
<td><p>262144</p></td>
<td><p>中止の保持を実行します。つまり <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">、RollbackTrans を呼び出すことによって、新しい</a> トランザクションが自動的に開始されます。 この設定をサポートしていないプロバイダーもあります。</p></td>
</tr>
<tr class="even">
<td><p><strong>adXactCommitRetaining</strong></p></td>
<td><p>131072</p></td>
<td><p>コミットの保持を実行します。つまり <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">、CommitTrans を呼び出すことによって、新しい</a> トランザクションが自動的に開始されます。 この設定をサポートしていないプロバイダーもあります。</p></td>
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
<td><p>AdoEnums.XactAttribute.ABORTRETAINING</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.XactAttribute.COMMITRETAINING</p></td>
</tr>
</tbody>
</table>

