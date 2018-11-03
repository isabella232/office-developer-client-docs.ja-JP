---
title: ログ ファイル領域の使用量を最小限に抑える
TOCTitle: Minimizing log file space usage
ms:assetid: d527c313-35ad-c30e-6ea1-ddfeff1fe890
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250073(v=office.15)
ms:contentKeyID: 48547960
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2c462641616c126c7732433fc8b7d23bb137b06a
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944768"
---
# <a name="minimizing-log-file-space-usage"></a><span data-ttu-id="679fb-102">ログ ファイル領域の使用量を最小限に抑える</span><span class="sxs-lookup"><span data-stu-id="679fb-102">Minimizing log file space usage</span></span>

<span data-ttu-id="679fb-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="679fb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="679fb-104">ログ ファイルがすぐにいっぱいことがあります (したがって、サーバーを停止する) 大量の SQL Server データベース上のアクティビティがある場合。</span><span class="sxs-lookup"><span data-stu-id="679fb-104">A log file may fill quickly (thus halting the server) if there is a large volume of activity on an SQL Server database.</span></span> <span data-ttu-id="679fb-105">ログ ファイルを設定するには **[チェックポイント時の切り捨て**はデータベースのログ ファイルのライフ サイクルを大幅に拡張します。</span><span class="sxs-lookup"><span data-stu-id="679fb-105">You can set the log file to **Truncate on Checkpoint** to significantly extend the life of the log file for a database.</span></span>

<span data-ttu-id="679fb-106">**Microsoft SQL Server 6.5 でチェックポイント時のログの切り捨てを有効にするには**</span><span class="sxs-lookup"><span data-stu-id="679fb-106">**To enable Truncate on Checkpoint in Microsoft SQL Server 6.5**</span></span>

1.  <span data-ttu-id="679fb-107">Microsoft SQL Server Enterprise Manager を起動し、サーバーのツリーを開き、次にデータベース デバイスのツリーを開きます。</span><span class="sxs-lookup"><span data-stu-id="679fb-107">Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Database Devices tree.</span></span>

2.  <span data-ttu-id="679fb-108">この機能を有効にするデータベースの名前をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="679fb-108">Double-click the name of the database on which this feature will be enabled.</span></span>

3.  <span data-ttu-id="679fb-109">[**データベース**] タブで、**削除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="679fb-109">From the **Database** tab, select **Truncate**.</span></span>

4.  <span data-ttu-id="679fb-110">**オプション**] タブから **[チェックポイント時のログの切り捨て]** を選択し、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="679fb-110">From the **Options** tab, select **Truncate Log on Checkpoint**, and then click **OK**.</span></span>

<span data-ttu-id="679fb-111">**Microsoft SQL Server 7.0 でチェックポイント時のログの切り捨てを有効にするには**</span><span class="sxs-lookup"><span data-stu-id="679fb-111">**To enable Truncate on Checkpoint in Microsoft SQL Server 7.0**</span></span>

1.  <span data-ttu-id="679fb-112">Microsoft SQL Server Enterprise Manager を起動し、サーバーのツリーを開き、次にデータベースのツリーを開きます。</span><span class="sxs-lookup"><span data-stu-id="679fb-112">Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Databases tree.</span></span>

2.  <span data-ttu-id="679fb-113">データベースにこの機能が有効になります、[**プロパティ**] の名前を右クリックします。</span><span class="sxs-lookup"><span data-stu-id="679fb-113">Right-click the name of the database on which this feature will be enabled and choose **Properties**.</span></span>

3.  <span data-ttu-id="679fb-114">**オプション**] タブから **[チェックポイント時のログの切り捨て]** を選択し、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="679fb-114">From the **Options** tab, select **Truncate Log on Checkpoint**, and then click **OK**.</span></span>

<span data-ttu-id="679fb-115">**チェックポイントの削除**機能の詳細については、Microsoft SQL Server のマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="679fb-115">For more information about the **Truncate on Checkpoint** feature, see the Microsoft SQL Server documentation.</span></span>

