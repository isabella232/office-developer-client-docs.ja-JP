---
title: オブジェクトを使用した RDS プログラミング モデル
TOCTitle: RDS Programming Model with Objects
ms:assetid: 207150ec-8eb5-bec5-3059-db37a0e28c19
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248987(v=office.15)
ms:contentKeyID: 48543663
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f6d28373e5d241ae9e87357187894924f27ba78c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873804"
---
# <a name="rds-programming-model-with-objects"></a><span data-ttu-id="5681c-102">オブジェクトを使用した RDS プログラミング モデル</span><span class="sxs-lookup"><span data-stu-id="5681c-102">RDS Programming Model with Objects</span></span>


<span data-ttu-id="5681c-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="5681c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5681c-p101">RDS の目的は、IIS などを中継してデータ ソースに対するアクセスおよび更新を行うことです。プログラミング モデルでは、この目的の達成に必要な一連の操作を指定します。オブジェクト モデルでは、プログラミング モデルに作用するメソッドおよびプロパティを持つオブジェクトを指定します。</span><span class="sxs-lookup"><span data-stu-id="5681c-p101">The goal of RDS is to gain access to and update data sources through an intermediary such as IIS. The programming model specifies the sequence of activities necessary to accomplish this goal. The object model specifies the objects whose methods and properties affect the programming model.</span></span>

<span data-ttu-id="5681c-107">RDS は、次に示す一連の操作を実行する手段を提供します。</span><span class="sxs-lookup"><span data-stu-id="5681c-107">RDS provides the means to perform the following sequence of actions:</span></span>

  - <span data-ttu-id="5681c-108">サーバー上で呼び出すプログラムを指定し、クライアント ([RDS.DataSpace](dataspace-object-rds.md)) がそのプログラムを参照する手段 (プロキシ) を獲得します。</span><span class="sxs-lookup"><span data-stu-id="5681c-108">Specify the program to be invoked on the server, and obtain a way (proxy) to refer to it from the client ([RDS.DataSpace](dataspace-object-rds.md)).</span></span>

  - <span data-ttu-id="5681c-p102">サーバー プログラムを呼び出します。データ ソースおよび発行するコマンドを識別するためのパラメーターをサーバー プログラムに渡します (プロキシまたは [RDS.DataControl](datacontrol-object-rds.md))。</span><span class="sxs-lookup"><span data-stu-id="5681c-p102">Invoke the server program. Pass parameters to the server program that identifies the data source and the command to issue (proxy or [RDS.DataControl](datacontrol-object-rds.md)).</span></span>

  - <span data-ttu-id="5681c-p103">サーバー プログラムは、データ ソースから [Recordset](recordset-object-ado.md) オブジェクトを取得します。通常は、ADO を使用して取得します。また、**Recordset** オブジェクトをサーバー上で処理することもできます ([RDSServer.DataFactory](datafactory-object-rdsserver.md))。</span><span class="sxs-lookup"><span data-stu-id="5681c-p103">The server program obtains a [Recordset](recordset-object-ado.md) object from the data source, typically by using ADO. Optionally, the **Recordset** object is processed on the server ([RDSServer.DataFactory](datafactory-object-rdsserver.md)).</span></span>

  - <span data-ttu-id="5681c-113">サーバー プログラムは、処理結果の **Recordset** オブジェクトをクライアント アプリケーション (プロキシ) に返します。</span><span class="sxs-lookup"><span data-stu-id="5681c-113">The server program returns the final **Recordset** object to the client application (proxy).</span></span>

  - <span data-ttu-id="5681c-114">クライアントでは、返された **Recordset** オブジェクトを、ビジュアル コントロールで使用しやすい形式に変換します (ビジュアル コントロールおよび **RDS.DataControl**)。</span><span class="sxs-lookup"><span data-stu-id="5681c-114">On the client, the **Recordset** object is put into a form that can be easily used by visual controls (visual control and **RDS.DataControl**).</span></span>

  - <span data-ttu-id="5681c-115">**Recordset** オブジェクトに加えられた変更がサーバーに送り返され、その変更がデータ ソースに反映されます (**RDS.DataControl** または **RDSServer.DataFactory**)。</span><span class="sxs-lookup"><span data-stu-id="5681c-115">Changes to the **Recordset** object are sent back to the server and used to update the data source (**RDS.DataControl** or **RDSServer.DataFactory**).</span></span>

