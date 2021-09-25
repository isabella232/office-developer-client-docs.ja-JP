---
title: QueryDefStateEnum 列挙 (DAO)
TOCTitle: QueryDefStateEnum Enumeration
ms:assetid: edfa3085-f8b4-b813-0828-2ba2a9dc0b9d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836359(v=office.15)
ms:contentKeyID: 48548549
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: afed37a05b4598c1f57399162a68f430941d9e93
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558031"
---
# <a name="querydefstateenum-enumeration-dao"></a>QueryDefStateEnum 列挙 (DAO)


**適用先:** Access 2013、Office 2013

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

