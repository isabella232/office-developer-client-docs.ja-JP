---
title: RecordCreateOptionsEnum
TOCTitle: RecordCreateOptionsEnum
ms:assetid: 153dc8ff-680c-1482-d386-4c4b33ffc589
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248917(v=office.15)
ms:contentKeyID: 48543405
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3cd855adb62a1b97f99cdc34a9c27ee539ab1c2b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884221"
---
# <a name="recordcreateoptionsenum"></a>RecordCreateOptionsEnum


**適用されます**Access 2013、Office 2013。

**Record** オブジェクトの **Open** メソッドに対し、既存の [Record](record-object-ado.md) を開くか、新しい [Record](open-method-ado-record.md) を作成するかを表します。これらの値は AND 演算子で結合できます。

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
<td><p><strong>adCreateCollection</strong></p></td>
<td><p>0x2000</p></td>
<td><p>既存の <strong>Record</strong> を開かずに、<em>Source</em> パラメーターで指定したノードに新しい <strong>Record</strong> を作成します。ソースが既存のノードを指定している場合、<strong>adCreateCollection</strong> が <strong>adOpenIfExists</strong> または <strong>adCreateOverwrite</strong> と組み合わせて使用されていない限り、実行時エラーになります。</p></td>
</tr>
<tr class="even">
<td><p><strong>adCreateNonCollection</strong></p></td>
<td><p>0</p></td>
<td><p>種類が <a href="recordtypeenum.md">adSimpleRecord</a> の新しい <strong>Record</strong> を作成します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCreateOverwrite</strong></p></td>
<td><p>0x4000000</p></td>
<td><p>作成フラグ <strong>adCreateCollection</strong>、<strong>adCreateNonCollection</strong>、および <strong>adCreateStructDoc</strong> を修飾します。この値と作成フラグの値の 1 つが OR を使って連結されている場合、ソース URL が既存のノードまたは <strong>Record</strong> を指定していると、既存のものが上書きされ、新しい <strong>Record</strong> が作成されます。この値は、<strong>adOpenIfExists</strong> とは併用できません。</p></td>
</tr>
<tr class="even">
<td><p><strong>adCreateStructDoc</strong></p></td>
<td><p>0x80000000</p></td>
<td><p>既存の <strong>Record</strong> を開かずに、種類が <a href="recordtypeenum.md">adStructDoc</a> の新しい <strong>Record</strong> を作成します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFailIfNotExists</strong></p></td>
<td><p>-1</p></td>
<td><p>既定値。<em>Source</em> が存在しないノードを指定していると、実行時エラーになります。</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenIfExists</strong></p></td>
<td><p>0x2000000</p></td>
<td><p>作成フラグ <strong>adCreateCollection</strong>、<strong>adCreateNonCollection</strong>、および <strong>adCreateStructDoc</strong> を修飾します。この値と作成フラグの値の 1 つが OR を使って連結されている場合、ソース URL が既存のノードまたは <strong>Record</strong> オブジェクトを指定していると、プロバイダーは、新しい <strong>Record</strong> を作成せずに、既存のものを開く必要があります。この値は、<strong>adCreateOverwrite</strong> とは併用できません。</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC に相当

これらの定数に ADO/WFC 等価はありません。

