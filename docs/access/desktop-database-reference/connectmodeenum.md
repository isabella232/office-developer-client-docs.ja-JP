---
title: connectmodeenum (Access デスクトップデータベースリファレンス)
TOCTitle: ConnectModeEnum
ms:assetid: a15aa733-f899-5fe9-e705-67a4301706d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249743(v=office.15)
ms:contentKeyID: 48546728
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 453d84e687a31f7df5082e17b80fe2a1bda756be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295696"
---
# <a name="connectmodeenum"></a>ConnectModeEnum

**適用先:** Access 2013、Office 2013

[Connection](connection-object-ado.md) 内のデータの編集、[Record](record-object-ado.md) のオープン、または **Record** および [Stream](stream-object-ado.md) オブジェクトの [Mode](mode-property-ado.md) プロパティの値の指定に対する権限を表します。

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
<td><p><strong>admoderead です</strong></p></td>
<td><p>1-d</p></td>
<td><p>読み取り専用の権限を表します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adModeReadWrite</strong></p></td>
<td><p>1/3</p></td>
<td><p>読み取り/書き込み両方の権限を表します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adModeRecursive</strong></p></td>
<td><p>0x400000</p></td>
<td><p>他の共有<em>*拒否*</em>値 (<strong>adModeShareDenyNone</strong>、 <strong>adModeShareDenyWrite</strong>、または<strong>adModeShareDenyRead</strong>) と共に使用して、現在の<strong>レコード</strong>のすべてのサブレコードに共有制限を伝達します。 <strong>Record</strong> に子がない場合は機能しません。</p><p><strong>adModeShareDenyNone</strong> のみと組み合わせて使用すると、実行時エラーが発生します。 ただし、その他の値と組み合わせた場合は <strong>adModeShareDenyNone</strong> と組み合わせて使用できます。 たとえば、 &quot; <strong>admoderead です</strong>または<strong>adModeShareDenyNone</strong>または<strong>adModeRecursive</strong>&quot;を使用できます。</p></td>
</tr>
<tr class="even">
<td><p><strong>adModeShareDenyNone</strong></p></td>
<td><p>16</p></td>
<td><p>権限の種類に関係なく、他のユーザーが接続を開けるようにします。他のユーザーに対して、読み取りと書き込みの両方のアクセスを許可します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adModeShareDenyRead</strong></p></td>
<td><p>2/4</p></td>
<td><p>他のユーザーが読み取り権限で接続を開くのを禁止します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adModeShareDenyWrite</strong></p></td>
<td><p>~</p></td>
<td><p>他のユーザーが書き込み権限で接続を開くのを禁止します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adModeShareExclusive</strong></p></td>
<td><p>個</p></td>
<td><p>他のユーザーが接続を開くのを禁止します。</p></td>
</tr>
<tr class="even">
<td><p><strong>admodeunknown です</strong></p></td>
<td><p>.0</p></td>
<td><p>既定値。権限が設定されていないか、権限を判定できないことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>admodewrite</strong></p></td>
<td><p>pbm-2</p></td>
<td><p>書き込み専用の権限を示します。</p></td>
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
<td><p>AdoEnums モード。読み取り</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums の読み取りモード</p></td>
</tr>
<tr class="odd">
<td><p>(AdoEnums.ConnectMode.RECURSIVE と等価なものはありません)</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums を1つにします。</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums (読み取り専用)</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums の読み取り/書き込み</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums 排他的</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums モードが不明です。</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums の書き込み</p></td>
</tr>
</tbody>
</table>

