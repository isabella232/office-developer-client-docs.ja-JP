---
title: RDS オブジェクト モデルの概要
TOCTitle: RDS Object Model Summary
ms:assetid: 0355d62a-dabb-8643-5c43-1e98ccf7f3b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248800(v=office.15)
ms:contentKeyID: 48542981
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4afb0309018b12267f29c23bcde740fdb5a9664e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478109"
---
# <a name="rds-object-model-summary"></a>RDS オブジェクト モデルの概要


**適用されます**Access 2013 |。Office 2013

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>オブジェクト</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="dataspace-object-rds.md">RDS.インスタンス</a></p></td>
<td><p>このオブジェクトには、サーバー プロキシを取得するためのメソッドが含まれます。プロキシは、既定のサーバー プログラムの場合と、カスタム サーバー プログラム (ビジネス オブジェクト) の場合があります。サーバー プログラムは、インターネット、イントラネット、またはローカル エリア ネットワークを介して呼び出すこと、またはローカルなダイナミック リンク ライブラリとすることができます。</p></td>
</tr>
<tr class="even">
<td><p><a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a></p></td>
<td><p>このオブジェクトは、既定のサーバー プログラムを表します。RDS データの既定の取得動作および更新動作を実行します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="datacontrol-object-rds.md">RDS.DataControl</a></p></td>
<td><p>このオブジェクトは、<strong>RDS.DataSpace</strong> オブジェクトおよび <strong>RDSServer.DataFactory</strong> オブジェクトを、自動的に呼び出すことができます。
 既定の RDS データ取得動作または更新動作を呼び出すには、このオブジェクトを使用します。 また、このオブジェクトは、返された <strong>Recordset</strong> オブジェクトにアクセスするビジュアル コントロールを提供します。</p></td>
</tr>
</tbody>
</table>

