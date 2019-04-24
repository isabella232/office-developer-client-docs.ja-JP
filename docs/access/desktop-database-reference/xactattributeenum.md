---
title: XactAttributeEnum (Access デスクトップデータベースリファレンス)
TOCTitle: XactAttributeEnum
ms:assetid: 9206698b-7cfa-1229-2701-f2b6949e54fc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249643(v=office.15)
ms:contentKeyID: 48546366
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e79a6143c65637660b2d59b7c7efb6a21e8935bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302570"
---
# <a name="xactattributeenum"></a>XactAttributeEnum

**適用先:** Access 2013、Office 2013

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
<td><p>中断の保持を実行します。つまり、 <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a>を呼び出すと、新しいトランザクションが自動的に開始されます。 この設定をサポートしていないプロバイダーもあります。</p></td>
</tr>
<tr class="even">
<td><p><strong>adXactCommitRetaining</strong></p></td>
<td><p>131072</p></td>
<td><p>保持コミットを実行します。つまり、 <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a>を呼び出すと、新しいトランザクションが自動的に開始されます。 この設定をサポートしていないプロバイダーもあります。</p></td>
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
<td><p>XactAttribute 保持 AdoEnums</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums XactAttribute</p></td>
</tr>
</tbody>
</table>

