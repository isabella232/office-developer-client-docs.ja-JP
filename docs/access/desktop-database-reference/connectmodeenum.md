---
title: ConnectModeEnum (デスクトップ データベース参照のアクセス)
TOCTitle: ConnectModeEnum
ms:assetid: a15aa733-f899-5fe9-e705-67a4301706d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249743(v=office.15)
ms:contentKeyID: 48546728
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 6a09ea4d781e5560e335c2e75fc2da9a5508bae8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874007"
---
# <a name="connectmodeenum"></a>ConnectModeEnum

**適用されます**Access 2013、Office 2013。

[Connection](connection-object-ado.md) 内のデータの編集、 [Record](record-object-ado.md) のオープン、または [Record](mode-property-ado.md) および **Stream** オブジェクトの [Mode](stream-object-ado.md) プロパティの値の指定に対する権限を表します。

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
<td><p><strong>adModeRead</strong></p></td>
<td><p>1</p></td>
<td><p>読み取り専用の権限を表します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adModeReadWrite</strong></p></td>
<td><p>3</p></td>
<td><p>読み取り/書き込み両方の権限を表します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adModeRecursive</strong></p></td>
<td><p>0x400000</p></td>
<td><p>(<strong>AdModeShareDenyNone</strong>、 <strong>adModeShareDenyWrite</strong>、または<strong>adModeShareDenyRead</strong>) サブのすべてのレコードをカレント<strong>レコード</strong>の共有の制限を適用するその他の<em>*ShareDeny*</em>値と組み合わせて使用します。 <strong>レコード</strong>に子がない場合は影響ありません。</p><p><strong>AdModeShareDenyNone</strong>のみで使用されている場合は、実行時エラーが生成されます。 ただし、 <strong>adModeShareDenyNone</strong>その他の値と組み合わせることで使用できます。 たとえば、使用することができます&quot; <strong>adModeRead</strong>または<strong>adModeShareDenyNone</strong>または<strong>adModeRecursive</strong>&quot;。</p></td>
</tr>
<tr class="even">
<td><p><strong>adModeShareDenyNone</strong></p></td>
<td><p>16</p></td>
<td><p>権限の種類に関係なく、他のユーザーが接続を開けるようにします。他のユーザーに対して、読み取りと書き込みの両方のアクセスを許可します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adModeShareDenyRead</strong></p></td>
<td><p>4</p></td>
<td><p>他のユーザーが読み取り権限で接続を開くのを禁止します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adModeShareDenyWrite</strong></p></td>
<td><p>8</p></td>
<td><p>他のユーザーが書き込み権限で接続を開くのを禁止します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adModeShareExclusive</strong></p></td>
<td><p>12</p></td>
<td><p>他のユーザーが接続を開くのを禁止します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adModeUnknown</strong></p></td>
<td><p>0</p></td>
<td><p>既定値。権限が設定されていないか、権限を判定できないことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adModeWrite</strong></p></td>
<td><p>2</p></td>
<td><p>書き込み専用の権限を示します。</p></td>
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
<td><p>AdoEnums.ConnectMode.READ</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ConnectMode.READWRITE</p></td>
</tr>
<tr class="odd">
<td><p>(AdoEnums.ConnectMode.RECURSIVE と等価なものはありません)</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ConnectMode.SHAREDENYNONE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ConnectMode.SHAREDENYREAD</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ConnectMode.SHAREDENYWRITE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ConnectMode.SHAREEXCLUSIVE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ConnectMode.UNKNOWN</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ConnectMode.WRITE</p></td>
</tr>
</tbody>
</table>

