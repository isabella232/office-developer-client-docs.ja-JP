---
title: QueryDefStateEnum 列挙 (DAO)
TOCTitle: QueryDefStateEnum Enumeration
ms:assetid: edfa3085-f8b4-b813-0828-2ba2a9dc0b9d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836359(v=office.15)
ms:contentKeyID: 48548549
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b368079aeb668c9ae72e3955f55159ab2c72a53e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882568"
---
# <a name="querydefstateenum-enumeration-dao"></a>QueryDefStateEnum 列挙 (DAO)


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

