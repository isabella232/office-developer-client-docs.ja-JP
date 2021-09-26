---
title: CursorDriverEnum 列挙 (DAO)
TOCTitle: CursorDriverEnum enumeration
ms:assetid: d0312ece-c30a-7d61-d5f3-75edf0d0afc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834707(v=office.15)
ms:contentKeyID: 48547832
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: bf12758f823d656fd2ca1c8d9e867db5a3392e02
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597493"
---
# <a name="cursordriverenum-enumeration-dao"></a>CursorDriverEnum 列挙 (DAO)

**適用先**: Access 2013、Office 2013

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
<td><p>4 </p></td>
<td><p>すべてのカーソル (つまり <strong>Recordset</strong> オブジェクト) を、行セットのサイズが 1 である前方のみの読み取り専用カーソルとして開きます。 カーソルレス &quot; クエリとも呼ばれる。&quot;</p></td>
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

