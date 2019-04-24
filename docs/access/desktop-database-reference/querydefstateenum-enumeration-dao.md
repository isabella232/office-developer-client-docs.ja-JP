---
title: querydefstateenum 列挙 (DAO)
TOCTitle: QueryDefStateEnum Enumeration
ms:assetid: edfa3085-f8b4-b813-0828-2ba2a9dc0b9d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836359(v=office.15)
ms:contentKeyID: 48548549
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0ca9923b1604b17c1d7f64d2d968378fec4a8c24
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303319"
---
# <a name="querydefstateenum-enumeration-dao"></a>querydefstateenum 列挙 (DAO)


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
<td><p>1-d</p></td>
<td><p>(既定値) ステートメントが準備されます (つまり、ODBC SQLPrepare API が呼び出されます)。</p></td>
</tr>
<tr class="even">
<td><p>dbQUnprepare</p></td>
<td><p>pbm-2</p></td>
<td><p>ステートメントが準備されません (つまり、ODBC SQLExecDirect API が呼び出されます)。</p></td>
</tr>
</tbody>
</table>

