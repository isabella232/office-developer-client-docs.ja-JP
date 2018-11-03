---
title: 可能 (DAO) の列挙
TOCTitle: QueryDefStateEnum Enumeration
ms:assetid: edfa3085-f8b4-b813-0828-2ba2a9dc0b9d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836359(v=office.15)
ms:contentKeyID: 48548549
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7a2163caf8b0c6f7b17d0a551d95d18d0883e183
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945475"
---
# <a name="querydefstateenum-enumeration-dao"></a>可能 (DAO) の列挙


**適用されます**Access 2013、Office 2013。

**Prepare** プロパティで、クエリの準備方法の指定に使用されるメソッドを指定するために使用します。

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
<td><p>dbQPrepare</p></td>
<td><p>1</p></td>
<td><p>(既定値) ステートメントが準備されます (つまり、ODBC SQLPrepare API が呼び出されます)。</p></td>
</tr>
<tr class="even">
<td><p>dbQUnprepare</p></td>
<td><p>2</p></td>
<td><p>ステートメントが準備されません (つまり、ODBC SQLExecDirect API が呼び出されます)。</p></td>
</tr>
</tbody>
</table>

