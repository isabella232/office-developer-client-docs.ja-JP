---
title: LockTypeEnum 列挙 (DAO)
TOCTitle: LockTypeEnum Enumeration
ms:assetid: d40f984c-b37f-72f7-7b05-752f106b6029
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834802(v=office.15)
ms:contentKeyID: 48547925
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 82a09db7baff93ba7fd51de593bc4d1dfff41dc1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477755"
---
# <a name="locktypeenum-enumeration-dao"></a>LockTypeEnum 列挙 (DAO)


**適用されます**Access 2013 |。Office 2013

レコードセットを開くときに使用されるレコード ロックの種類を指定します。

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
<td><p>dbOptimistic</p></td>
<td><p>3</p></td>
<td><p>レコード ID に基づく共有的同時ロック。カーソルは古いレコードと新しいレコードのレコード ID を比較し、そのレコードへのアクセスが最後に行われてから変更が加えられたかどうか判断します。</p></td>
</tr>
<tr class="even">
<td><p>dbOptimisticBatch</p></td>
<td><p>5</p></td>
<td><p>共有的バッチ更新を可能にします (ODBCDirect ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p>dbOptimisticValue</p></td>
<td><p>1</p></td>
<td><p>レコード値に基づく共有的同時ロック。カーソルは古いレコードと新しいレコードのデータ値を比較し、そのレコードへのアクセスが最後に行われてから変更が加えられたかどうか判断します (ODBCDirect ワークスペースのみ)。</p>

> [!NOTE]
> <P>[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</P>


</td>
</tr>
<tr class="even">
<td><p>dbPessimistic</p></td>
<td><p>2</p></td>
<td><p>排他的同時ロック。カーソルは、レコードが更新可能であることを保証するために必要な最低限のロックを使用します。</p></td>
</tr>
</tbody>
</table>

