---
title: TempDB 用に十分な空き領域を確保する
TOCTitle: Ensuring Sufficient TempDB Space
ms:assetid: 2729c118-ec8b-1fcb-4a90-56b57823b24c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249034(v=office.15)
ms:contentKeyID: 48543830
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5d049a098a7f7cfd826c6c5945c71831acbceb04
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863053"
---
# <a name="ensuring-sufficient-tempdb-space"></a><span data-ttu-id="a7f37-102">TempDB 用に十分な空き領域を確保する</span><span class="sxs-lookup"><span data-stu-id="a7f37-102">Ensuring Sufficient TempDB Space</span></span>


<span data-ttu-id="a7f37-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="a7f37-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a7f37-p101">Microsoft SQL Server 6.5 において処理領域が必要な [Recordset](recordset-object-ado.md) オブジェクトを処理している際にエラーが発生した場合は、TempDB のサイズを増やす必要があります (一部のクエリは、一時的な処理領域を必要とします。たとえば、ORDER BY 句のあるクエリでは **Recordset** のソートが必要ですが、これには一時的な処理領域が必要です)。</span><span class="sxs-lookup"><span data-stu-id="a7f37-p101">If errors occur while handling [Recordset](recordset-object-ado.md) objects that need processing space on Microsoft SQL Server 6.5, you may need to increase the size of the TempDB. (Some queries require temporary processing space; for example, a query with an ORDER BY clause requires a sort of the **Recordset**, which requires some temporary space.)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a7f37-106">[!重要] 一度展開したデバイスは簡単には圧縮できないので、実行前に以下の手順をよく読んでください。</span><span class="sxs-lookup"><span data-stu-id="a7f37-106">Read through this procedure before performing the actions because it isn't as easy to shrink a device once it is expanded.</span></span>

> [!NOTE]
> <span data-ttu-id="a7f37-p102">[!メモ] 既定では、Microsoft SQL Server 7.0 以降のバージョンでは、TempDB は必要に応じて自動的に拡大できるように設定されます。したがって、この手順が必要なのは、7.0 より前のバージョンを実行するサーバーだけです。</span><span class="sxs-lookup"><span data-stu-id="a7f37-p102">By default in Microsoft SQL Server 7.0 and later, TempDB is set to automatically grow as needed. Therefore, this procedure may only be necessary on servers running versions earlier than 7.0.</span></span>



<span data-ttu-id="a7f37-109">**SQL Server 6.5 の TempDB 領域を拡大するには**</span><span class="sxs-lookup"><span data-stu-id="a7f37-109">**To increase the TempDB space on SQL Server 6.5**</span></span>

1.  <span data-ttu-id="a7f37-110">Microsoft® SQL Server Enterprise Manager を起動し、サーバーのツリーを開き、次にデータベース デバイス ツリーを開きます。</span><span class="sxs-lookup"><span data-stu-id="a7f37-110">Start Microsoft® SQL Server Enterprise Manager, open the tree for the Server, and then open the Database Devices tree.</span></span>

2.  <span data-ttu-id="a7f37-111">マスターなどの拡張を (物理的な) デバイスを選択し、デバイスを開くには、[**データベース デバイスの編集**] ダイアログ ボックスをダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7f37-111">Select a (physical) device to expand, such as Master, and double-click the device to open the **Edit Database Device** dialog box.</span></span> <span data-ttu-id="a7f37-112">このダイアログ ボックスは、現在のデータベースを使用している容量を表示します。</span><span class="sxs-lookup"><span data-stu-id="a7f37-112">This dialog box shows how much space the current databases are using.</span></span>

3.  <span data-ttu-id="a7f37-113">[**サイズ**] ボックスで、指定したサイズ (たとえば、50 メガバイト (MB) のハード_ディスクの空き領域) のデバイスを向上します。</span><span class="sxs-lookup"><span data-stu-id="a7f37-113">In the **Size** box, increase the device to the desired amount (for example, 50 megabytes (MB) of hard disk space).</span></span>

4.  <span data-ttu-id="a7f37-114">**すぐに変更**する (論理) の TempDB の拡張可能領域の量を増やす] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7f37-114">Click **Change Now** to increase the amount of space to which the (logical) TempDB can expand.</span></span>

5.  <span data-ttu-id="a7f37-115">サーバーのデータベース ツリーを開き、 **TempDB** **データベースの編集**] ダイアログ ボックスを開く] をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7f37-115">Open the Databases tree on the server, and then double-click **TempDB** to open the **Edit Database** dialog box.</span></span> <span data-ttu-id="a7f37-116">[**データベース**] タブには、(**データのサイズ**) を TempDB に現在割り当てられている領域の容量が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="a7f37-116">The **Database** tab lists the amount of space currently allocated to TempDB (**Data Size**).</span></span> <span data-ttu-id="a7f37-117">既定では、これは、2 MB です。</span><span class="sxs-lookup"><span data-stu-id="a7f37-117">By default, this is 2 MB.</span></span>

6.  <span data-ttu-id="a7f37-118">[**サイズ**] グループで、[**展開**を] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7f37-118">Under the **Size** group, click **Expand**.</span></span> <span data-ttu-id="a7f37-119">グラフでは、各物理デバイスで使用できる割り当て領域を示しています。</span><span class="sxs-lookup"><span data-stu-id="a7f37-119">The graphs show the available and allocated space on each of the physical devices.</span></span> <span data-ttu-id="a7f37-120">茶色のバーは、使用可能な領域を表します。</span><span class="sxs-lookup"><span data-stu-id="a7f37-120">The bars in maroon color represent available space.</span></span>

7.  <span data-ttu-id="a7f37-121">などの**ログ デバイス\*\*\*\*のサイズ (MB)** ] ボックスで利用可能なサイズを表示するのには、マスター シェイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="a7f37-121">Select a **Log Device**, such as Master, to display the available size in the **Size (MB)** box.</span></span>

8.  <span data-ttu-id="a7f37-122">**すぐに拡張**領域を TempDB データベースを割り当てる] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7f37-122">Click **Expand Now** to allocate that space to the TempDB database.</span></span> <span data-ttu-id="a7f37-123">**データベースの編集**] ダイアログ ボックスでは、TempDB に新規に割り当てられたサイズが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a7f37-123">The **Edit Database** dialog box displays the new allocated size for TempDB.</span></span>

<span data-ttu-id="a7f37-124">このトピックの詳細については、Microsoft SQL Server Enterprise Manager ヘルプの「データベースのサイズを拡張する方法」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a7f37-124">For more information about this topic, search the Microsoft SQL Server Enterprise Manager Help file for "Expand Database dialog box."</span></span>

