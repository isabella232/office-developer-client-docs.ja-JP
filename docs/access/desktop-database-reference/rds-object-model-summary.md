---
title: RDS オブジェクト モデルの概要
TOCTitle: RDS object model summary
ms:assetid: 0355d62a-dabb-8643-5c43-1e98ccf7f3b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248800(v=office.15)
ms:contentKeyID: 48542981
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 33cbdc6de644592d87b7d49e65a5c5674ad94d5b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718407"
---
# <a name="rds-object-model-summary"></a><span data-ttu-id="4775d-102">RDS オブジェクト モデルの概要</span><span class="sxs-lookup"><span data-stu-id="4775d-102">RDS object model summary</span></span>


<span data-ttu-id="4775d-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="4775d-103">**Applies to**: Access 2013, Office 2013</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4775d-104">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4775d-104">Object</span></span></p></th>
<th><p><span data-ttu-id="4775d-105">説明</span><span class="sxs-lookup"><span data-stu-id="4775d-105">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4775d-106"><a href="dataspace-object-rds.md">RDS.インスタンス</a></span><span class="sxs-lookup"><span data-stu-id="4775d-106"><a href="dataspace-object-rds.md">RDS.DataSpace</a></span></span></p></td>
<td><p><span data-ttu-id="4775d-p101">このオブジェクトには、サーバー プロキシを取得するためのメソッドが含まれます。プロキシは、既定のサーバー プログラムの場合と、カスタム サーバー プログラム (ビジネス オブジェクト) の場合があります。サーバー プログラムは、インターネット、イントラネット、またはローカル エリア ネットワークを介して呼び出すこと、またはローカルなダイナミック リンク ライブラリとすることができます。</span><span class="sxs-lookup"><span data-stu-id="4775d-p101">This object contains a method to obtain a server proxy. The proxy may be the default or a custom server program (business object). The server program may be invoked on the Internet, an intranet, a local area network, or be a local dynamic-link library.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4775d-110"><a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a></span><span class="sxs-lookup"><span data-stu-id="4775d-110"><a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a></span></span></p></td>
<td><p><span data-ttu-id="4775d-p102">このオブジェクトは、既定のサーバー プログラムを表します。RDS データの既定の取得動作および更新動作を実行します。</span><span class="sxs-lookup"><span data-stu-id="4775d-p102">This object represents the default server program. It executes the default RDS data retrieval and update behavior.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4775d-113"><a href="datacontrol-object-rds.md">RDS.DataControl</a></span><span class="sxs-lookup"><span data-stu-id="4775d-113"><a href="datacontrol-object-rds.md">RDS.DataControl</a></span></span></p></td>
<td><p><span data-ttu-id="4775d-114">このオブジェクトは、<strong>RDS.DataSpace</strong> オブジェクトおよび <strong>RDSServer.DataFactory</strong> オブジェクトを、自動的に呼び出すことができます。
</span><span class="sxs-lookup"><span data-stu-id="4775d-114">This object can automatically invoke the <strong>RDS.DataSpace</strong> and <strong>RDSServer.DataFactory</strong> objects.</span></span> <span data-ttu-id="4775d-115">既定の RDS データ取得動作または更新動作を呼び出すには、このオブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="4775d-115">Use this object to invoke the default RDS data retrieval or update behavior.</span></span> <span data-ttu-id="4775d-116">また、このオブジェクトは、返された <strong>Recordset</strong> オブジェクトにアクセスするビジュアル コントロールを提供します。</span><span class="sxs-lookup"><span data-stu-id="4775d-116">This object also provides the means for visual controls to access the returned <strong>Recordset</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>

