---
title: カーソルの列挙 (DAO)
TOCTitle: CursorDriverEnum enumeration
ms:assetid: d0312ece-c30a-7d61-d5f3-75edf0d0afc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834707(v=office.15)
ms:contentKeyID: 48547832
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2f2bf52943a84d6f2e60891d63810bc0bbb6ecb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295248"
---
# <a name="cursordriverenum-enumeration-dao"></a>カーソルの列挙 (DAO)

**適用先:** Access 2013、Office 2013

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
<td><p>1/3</p></td>
<td><p>常に FoxPro カーソル ライブラリを使用します。一括更新を実行する場合には、このオプションを必ず指定する必要があります。</p></td>
</tr>
<tr class="even">
<td><p>dbusedefaultcursor</p></td>
<td><p>-1</p></td>
<td><p>(既定値) サーバーがサーバー側カーソルをサポートする場合は、サーバー側カーソルを使用します。それ以外の場合は、ODBC カーソル ライブラリを使用します。</p></td>
</tr>
<tr class="odd">
<td><p>dbUseNoCursor</p></td>
<td><p>2/4</p></td>
<td><p>すべてのカーソル (つまり <strong>Recordset</strong> オブジェクト) を、行セットのサイズが 1 である前方のみの読み取り専用カーソルとして開きます。 カーソルの少ない&quot;クエリとも呼ばれます。&quot;</p></td>
</tr>
<tr class="even">
<td><p>dbUseODBCCursor</p></td>
<td><p>1-d</p></td>
<td><p>常に ODBC カーソル ライブラリを使用します。このオプションは、結果セットが小さい場合にはパフォーマンスが高くなりますが、結果セットが大きくなるとパフォーマンスが急激に低下します。</p></td>
</tr>
<tr class="odd">
<td><p>dbuseservercursor</p></td>
<td><p>pbm-2</p></td>
<td><p>常にサーバー側カーソルを使用します。大規模な操作のほとんどでは、このオプションによって高いパフォーマンスが得られますが、ネットワーク トラフィックが増える可能性があります。</p></td>
</tr>
</tbody>
</table>

