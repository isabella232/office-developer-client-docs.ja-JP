---
title: RightsEnum (Access デスクトップ データベース リファレンス)
TOCTitle: RightsEnum
ms:assetid: 7647b9d5-5271-fdcf-489d-5a8beb931ca5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249485(v=office.15)
ms:contentKeyID: 48545693
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 90a86d25825662c7b29fee5fef091c094631e236
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621900"
---
# <a name="rightsenum"></a>RightsEnum

**適用先**: Access 2013、Office 2013

オブジェクトに対するグループまたはユーザーの権限を指定します。

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
<td><p><strong>adRightCreate</strong></p></td>
<td><p>16384<br />
( &amp; H4000)</p></td>
<td><p>ユーザーまたはグループは、この種類の新規オブジェクトを作成する権限を持っています。</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightDelete</strong></p></td>
<td><p>65536<br />
( &amp; H10000)</p></td>
<td><p>ユーザーまたはグループは、オブジェクトからデータを削除する権限を持っています。<strong>Tables</strong> などのオブジェクトでは、ユーザーはレコードからデータ値を削除する権限を持っています。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightDrop</strong></p></td>
<td><p>256<br />
( &amp; H100)</p></td>
<td><p>ユーザーまたはグループは、カタログからオブジェクトを削除する権限を持っています。たとえば、<strong>Tables</strong> を DROP TABLE SQL コマンドによって削除できます。</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightExclusive</strong></p></td>
<td><p>512<br />
( &amp; H200)</p></td>
<td><p>ユーザーまたはグループは、排他的にオブジェクトにアクセスする権限を持っています。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightExecute</strong></p></td>
<td><p>536870912<br />
( &amp; H200000000)</p></td>
<td><p>ユーザーまたはグループは、オブジェクトを実行する権限を持っています。</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightFull</strong></p></td>
<td><p>268435456<br />
( &amp; H10000000)</p></td>
<td><p>ユーザーまたはグループは、オブジェクトに対するすべての権限を持っています。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightInsert</strong></p></td>
<td><p>32768<br />
( &amp; H8000)</p></td>
<td><p>ユーザーまたはグループは、オブジェクトを挿入する権限を持っています。<strong>Tables</strong> などのオブジェクトでは、ユーザーはデータをテーブルに挿入する権限を持っています。</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightMaximumAllowed</strong></p></td>
<td><p>33554432 ( &amp; H2000000)</p></td>
<td><p>ユーザーまたはグループは、プロバイダーによって許可される最大数の権限を持っています。指定される権限は、プロバイダーの設定によって決まります。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightNone</strong></p></td>
<td><p>0</p></td>
<td><p>ユーザーまたはグループは、オブジェクトに対する権限を持ちません。</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightRead</strong></p></td>
<td><p>-2147483648<br />
( &amp; H800000000)</p></td>
<td><p>ユーザーまたはグループは、オブジェクトを読み取る権限を持っています。<a href="table-object-adox.md">Tables</a> などのオブジェクトでは、ユーザーはテーブル内のデータを読み取る権限を持っています。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightReadDesign</strong></p></td>
<td><p>1024<br />
( &amp; H400)</p></td>
<td><p>ユーザーまたはグループは、オブジェクトのデザインを読み取る権限を持っています。</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightReadPermissions</strong></p></td>
<td><p>131072<br />
( &amp; H20000)</p></td>
<td><p>ユーザーまたはグループは、カタログ内のオブジェクトの特定の権限を表示することができますが、変更することはできません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightReference</strong></p></td>
<td><p>8192<br />
( &amp; H2000)</p></td>
<td><p>ユーザーまたはグループは、オブジェクトを参照する権限を持っています。</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightUpdate</strong></p></td>
<td><p>1073741824<br />
( &amp; H400000000)</p></td>
<td><p>ユーザーまたはグループは、オブジェクトを更新する権限を持っています。<strong>Tables</strong> などのオブジェクトでは、ユーザーはテーブル内のデータを更新する権限を持っています。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightWithGrant</strong></p></td>
<td><p>4096<br />
( &amp; H1000)</p></td>
<td><p>ユーザーまたはグループは、オブジェクトに対する権限を与える権限を持っています。</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightWriteDesign</strong></p></td>
<td><p>2048<br />
( &amp; H800)</p></td>
<td><p>ユーザーまたはグループは、オブジェクトのデザインを修正する権限を持っています。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightWriteOwner</strong></p></td>
<td><p>524288<br />
( &amp; H80000)</p></td>
<td><p>ユーザーまたはグループは、オブジェクトの所有者を変更する権限を持っています。</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightWritePermissions</strong></p></td>
<td><p>262144<br />
( &amp; H40000)</p></td>
<td><p>ユーザーまたはグループは、カタログ内のオブジェクトに対する特定の権限を変更することができます。</p></td>
</tr>
</tbody>
</table>

