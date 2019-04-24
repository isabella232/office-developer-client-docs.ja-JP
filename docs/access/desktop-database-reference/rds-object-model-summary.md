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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300876"
---
# <a name="rds-object-model-summary"></a><span data-ttu-id="bffbe-102">RDS オブジェクト モデルの概要</span><span class="sxs-lookup"><span data-stu-id="bffbe-102">RDS object model summary</span></span>


<span data-ttu-id="bffbe-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="bffbe-103">**Applies to**: Access 2013, Office 2013</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bffbe-104">Object</span><span class="sxs-lookup"><span data-stu-id="bffbe-104">Object</span></span></p></th>
<th><p><span data-ttu-id="bffbe-105">説明</span><span class="sxs-lookup"><span data-stu-id="bffbe-105">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bffbe-106"><a href="dataspace-object-rds.md">章.スペース</a></span><span class="sxs-lookup"><span data-stu-id="bffbe-106"><a href="dataspace-object-rds.md">RDS.DataSpace</a></span></span></p></td>
<td><p><span data-ttu-id="bffbe-p101">このオブジェクトには、サーバー プロキシを取得するためのメソッドが含まれます。プロキシは、既定のサーバー プログラムの場合と、カスタム サーバー プログラム (ビジネス オブジェクト) の場合があります。サーバー プログラムは、インターネット、イントラネット、またはローカル エリア ネットワークを介して呼び出すこと、またはローカルなダイナミック リンク ライブラリとすることができます。</span><span class="sxs-lookup"><span data-stu-id="bffbe-p101">This object contains a method to obtain a server proxy. The proxy may be the default or a custom server program (business object). The server program may be invoked on the Internet, an intranet, a local area network, or be a local dynamic-link library.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bffbe-110"><a href="datafactory-object-rdsserver.md">rdsserver.datafactory DataFactory</a></span><span class="sxs-lookup"><span data-stu-id="bffbe-110"><a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a></span></span></p></td>
<td><p><span data-ttu-id="bffbe-111">このオブジェクトは、既定のサーバー プログラムを表します。</span><span class="sxs-lookup"><span data-stu-id="bffbe-111">This object represents the default server program.</span></span> <span data-ttu-id="bffbe-112">RDS データの既定の取得動作および更新動作を実行します。</span><span class="sxs-lookup"><span data-stu-id="bffbe-112">It executes the default RDS data retrieval and update behavior.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bffbe-113"><a href="datacontrol-object-rds.md">章.DataControl</a></span><span class="sxs-lookup"><span data-stu-id="bffbe-113"><a href="datacontrol-object-rds.md">RDS.DataControl</a></span></span></p></td>
<td><p><span data-ttu-id="bffbe-114">このオブジェクトは、<strong>RDS.DataSpace</strong> オブジェクトおよび <strong>RDSServer.DataFactory</strong> オブジェクトを、自動的に呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="bffbe-114">This object can automatically invoke the <strong>RDS.DataSpace</strong> and <strong>RDSServer.DataFactory</strong> objects.</span></span> <span data-ttu-id="bffbe-115">既定の RDS データ取得動作または更新動作を呼び出すには、このオブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="bffbe-115">Use this object to invoke the default RDS data retrieval or update behavior.</span></span> <span data-ttu-id="bffbe-116">また、このオブジェクトは、返された <strong>Recordset</strong> オブジェクトにアクセスするビジュアル コントロールを提供します。</span><span class="sxs-lookup"><span data-stu-id="bffbe-116">This object also provides the means for visual controls to access the returned <strong>Recordset</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>

