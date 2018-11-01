---
title: XactAttributeEnum (デスクトップ データベース参照のアクセス)
TOCTitle: XactAttributeEnum
ms:assetid: 9206698b-7cfa-1229-2701-f2b6949e54fc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249643(v=office.15)
ms:contentKeyID: 48546366
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 28b81c45921120b8a3cd8768d22559355d8ff623
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870493"
---
# <a name="xactattributeenum"></a>XactAttributeEnum

**適用されます**Access 2013、Office 2013。

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
<td><p>保持中止は; を実行します。つまり、 <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a>を自動的に呼び出すことは、新しいトランザクションを開始します。 すべてのプロバイダーは、これをサポートします。</p></td>
</tr>
<tr class="even">
<td><p><strong>adXactCommitRetaining</strong></p></td>
<td><p>131072</p></td>
<td><p>保持コミット; を実行します。つまり、 <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a>を自動的に呼び出すことは、新しいトランザクションを開始します。 すべてのプロバイダーは、これをサポートします。</p></td>
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
<td><p>AdoEnums.XactAttribute.ABORTRETAINING</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.XactAttribute.COMMITRETAINING</p></td>
</tr>
</tbody>
</table>

