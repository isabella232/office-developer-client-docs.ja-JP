---
title: 十分な TempDB 領域の確保
TOCTitle: Ensuring sufficient TempDB space
ms:assetid: 2729c118-ec8b-1fcb-4a90-56b57823b24c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249034(v=office.15)
ms:contentKeyID: 48543830
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6414c9dd4c3218c2c2bf90f39d0cfb950e6e1018
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293575"
---
# <a name="ensuring-sufficient-tempdb-space"></a><span data-ttu-id="70318-102">十分な TempDB 領域の確保</span><span class="sxs-lookup"><span data-stu-id="70318-102">Ensuring sufficient TempDB space</span></span>


<span data-ttu-id="70318-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="70318-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="70318-p101">Microsoft SQL Server 6.5 において処理領域が必要な [Recordset](recordset-object-ado.md) オブジェクトを処理している際にエラーが発生した場合は、TempDB のサイズを増やす必要があります (一部のクエリは、一時的な処理領域を必要とします。たとえば、ORDER BY 句のあるクエリでは **Recordset** のソートが必要ですが、これには一時的な処理領域が必要です)。</span><span class="sxs-lookup"><span data-stu-id="70318-p101">If errors occur while handling [Recordset](recordset-object-ado.md) objects that need processing space on Microsoft SQL Server 6.5, you may need to increase the size of the TempDB. (Some queries require temporary processing space; for example, a query with an ORDER BY clause requires a sort of the **Recordset**, which requires some temporary space.)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="70318-106">[!重要] 一度展開したデバイスは簡単には圧縮できないので、実行前に以下の手順をよく読んでください。</span><span class="sxs-lookup"><span data-stu-id="70318-106">Read through this procedure before performing the actions because it isn't as easy to shrink a device once it is expanded.</span></span>

> [!NOTE]
> <span data-ttu-id="70318-p102">[!メモ] 既定では、Microsoft SQL Server 7.0 以降のバージョンでは、TempDB は必要に応じて自動的に拡大できるように設定されます。したがって、この手順が必要なのは、7.0 より前のバージョンを実行するサーバーだけです。</span><span class="sxs-lookup"><span data-stu-id="70318-p102">By default in Microsoft SQL Server 7.0 and later, TempDB is set to automatically grow as needed. Therefore, this procedure may only be necessary on servers running versions earlier than 7.0.</span></span>



<span data-ttu-id="70318-109">**SQL Server 6.5 の TempDB 領域を拡大するには**</span><span class="sxs-lookup"><span data-stu-id="70318-109">**To increase the TempDB space on SQL Server 6.5**</span></span>

1.  <span data-ttu-id="70318-110">Microsoft SQL Server Enterprise Manager を起動し、サーバーのツリーを開き、次にデータベース デバイスのツリーを開きます。</span><span class="sxs-lookup"><span data-stu-id="70318-110">Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Database Devices tree.</span></span>

2.  <span data-ttu-id="70318-p103">Select a (physical) device to expand, such as Master, and double-click the device to open the **Edit Database Device** dialog box. This dialog box shows how much space the current databases are using.</span><span class="sxs-lookup"><span data-stu-id="70318-p103">Select a (physical) device to expand, such as Master, and double-click the device to open the **Edit Database Device** dialog box. This dialog box shows how much space the current databases are using.</span></span>

3.  <span data-ttu-id="70318-113">In the **Size** box, increase the device to the desired amount (for example, 50 megabytes (MB) of hard disk space).</span><span class="sxs-lookup"><span data-stu-id="70318-113">In the **Size** box, increase the device to the desired amount (for example, 50 megabytes (MB) of hard disk space).</span></span>

4.  <span data-ttu-id="70318-114">[すぐに変更] をクリックして、論理 TempDB の拡張可能領域を増やします。</span><span class="sxs-lookup"><span data-stu-id="70318-114">Click **Change Now** to increase the amount of space to which the (logical) TempDB can expand.</span></span>

5.  <span data-ttu-id="70318-p104">サーバーのデータベース ツリーを開き、[TempDB] をダブルクリックして [データベースの編集] ダイアログ ボックスを開きます。[データベース] タブには、TempDB に現在割り当てられている領域の大きさ ([データ サイズ]) が表示されます。既定では、この大きさは 2 MB です。</span><span class="sxs-lookup"><span data-stu-id="70318-p104">Open the Databases tree on the server, and then double-click **TempDB** to open the **Edit Database** dialog box. The **Database** tab lists the amount of space currently allocated to TempDB (**Data Size**). By default, this is 2 MB.</span></span>

6.  <span data-ttu-id="70318-p105">Under the **Size** group, click **Expand**. The graphs show the available and allocated space on each of the physical devices. The bars in maroon color represent available space.</span><span class="sxs-lookup"><span data-stu-id="70318-p105">Under the **Size** group, click **Expand**. The graphs show the available and allocated space on each of the physical devices. The bars in maroon color represent available space.</span></span>

7.  <span data-ttu-id="70318-121">Select a **Log Device**, such as Master, to display the available size in the **Size (MB)** box.</span><span class="sxs-lookup"><span data-stu-id="70318-121">Select a **Log Device**, such as Master, to display the available size in the **Size (MB)** box.</span></span>

8.  <span data-ttu-id="70318-p106">Click **Expand Now** to allocate that space to the TempDB database. The **Edit Database** dialog box displays the new allocated size for TempDB.</span><span class="sxs-lookup"><span data-stu-id="70318-p106">Click **Expand Now** to allocate that space to the TempDB database. The **Edit Database** dialog box displays the new allocated size for TempDB.</span></span>

<span data-ttu-id="70318-124">このトピックの詳細については、Microsoft SQL Server Enterprise Manager ヘルプの「データベースのサイズを拡張する方法」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="70318-124">For more information about this topic, search the Microsoft SQL Server Enterprise Manager Help file for "Expand Database dialog box."</span></span>

