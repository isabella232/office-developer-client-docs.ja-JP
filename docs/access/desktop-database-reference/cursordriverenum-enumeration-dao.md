---
title: CursorDriverEnum 列挙 (DAO)
TOCTitle: CursorDriverEnum Enumeration
ms:assetid: d0312ece-c30a-7d61-d5f3-75edf0d0afc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834707(v=office.15)
ms:contentKeyID: 48547832
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 25d264c1e91982231e025f17c00db79e47a1d5c6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880741"
---
# <a name="cursordriverenum-enumeration-dao"></a>CursorDriverEnum 列挙 (DAO)


**適用されます**Access 2013、Office 2013。

カーソル ドライバーの種類を指定します。

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
<td><p>dbUseClientBatchCursor</p></td>
<td><p>3</p></td>
<td><p>常に FoxPro カーソル ライブラリを使用します。一括更新を実行する場合には、このオプションを必ず指定する必要があります。</p></td>
</tr>
<tr class="even">
<td><p>dbUseDefaultCursor</p></td>
<td><p>-1</p></td>
<td><p>(既定値) サーバーがサーバー側カーソルをサポートする場合は、サーバー側カーソルを使用します。それ以外の場合は、ODBC カーソル ライブラリを使用します。</p></td>
</tr>
<tr class="odd">
<td><p>dbUseNoCursor</p></td>
<td><p>4</p></td>
<td><p>付けて順方向専用、読み取り専用、行セット サイズが 1 のすべてのカーソル (つまり、<strong>レコード セット</strong>オブジェクト) を開きます。 呼ばれる&quot;カーソルレス クエリします。&quot;</p></td>
</tr>
<tr class="even">
<td><p>dbUseODBCCursor</p></td>
<td><p>1</p></td>
<td><p>常に ODBC カーソル ライブラリを使用します。このオプションは、結果セットが小さい場合にはパフォーマンスが高くなりますが、結果セットが大きくなるとパフォーマンスが急激に低下します。</p></td>
</tr>
<tr class="odd">
<td><p>dbUseServerCursor</p></td>
<td><p>2</p></td>
<td><p>常にサーバー側カーソルを使用します。大規模な操作のほとんどでは、このオプションによって高いパフォーマンスが得られますが、ネットワーク トラフィックが増える可能性があります。</p></td>
</tr>
</tbody>
</table>

