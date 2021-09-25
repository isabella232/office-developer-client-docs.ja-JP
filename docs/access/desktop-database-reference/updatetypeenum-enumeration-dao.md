---
title: UpdateTypeEnum 列挙 (DAO)
TOCTitle: UpdateTypeEnum Enumeration
ms:assetid: 7ac38bae-27fc-f3d0-5b75-569bce547954
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196186(v=office.15)
ms:contentKeyID: 48545800
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: fe9c9873f244568a7f48faae0a012b53649cf308
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576850"
---
# <a name="updatetypeenum-enumeration-dao"></a>UpdateTypeEnum 列挙 (DAO)


**適用先:** Access 2013、Office 2013

**Update** メソッドで、ディスクに書き込む更新を指定するために使用します。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>値</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>dbUpdateBatch</p></td>
<td><p>4 </p></td>
<td><p>更新キャッシュ内の保留中のすべての変更をディスクに書き込みます。</p></td>
</tr>
<tr class="even">
<td><p>dbUpdateCurrentRecord</p></td>
<td><p>2</p></td>
<td><p>現在のレコードの保留中の変更のみをディスクに書き込みます。</p></td>
</tr>
<tr class="odd">
<td><p>dbUpdateRegular</p></td>
<td><p>1</p></td>
<td><p>(既定値) 保留中の変更をキャッシュせず、ディスクに直ちに書き込みます。</p></td>
</tr>
</tbody>
</table>

