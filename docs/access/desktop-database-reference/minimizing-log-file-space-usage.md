---
title: ログファイルの使用領域を最小化する
TOCTitle: Minimizing Log File Space Usage
ms:assetid: d527c313-35ad-c30e-6ea1-ddfeff1fe890
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250073(v=office.15)
ms:contentKeyID: 48547960
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 119e4bc607296d1a68aef6f85d44f15718940b42
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25866986"
---
# <a name="minimizing-log-file-space-usage"></a><span data-ttu-id="627bb-102">ログファイルの使用領域を最小化する</span><span class="sxs-lookup"><span data-stu-id="627bb-102">Minimizing Log File Space Usage</span></span>


<span data-ttu-id="627bb-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="627bb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="627bb-104">ログ ファイルがすぐにいっぱいことがあります (したがって、サーバーを停止する) 大量の SQL Server データベース上のアクティビティがある場合。</span><span class="sxs-lookup"><span data-stu-id="627bb-104">A log file may fill quickly (thus halting the server) if there is a large volume of activity on an SQL Server database.</span></span> <span data-ttu-id="627bb-105">ログ ファイルを設定するには **[チェックポイント時の切り捨て**はデータベースのログ ファイルのライフ サイクルを大幅に拡張します。</span><span class="sxs-lookup"><span data-stu-id="627bb-105">You can set the log file to **Truncate on Checkpoint** to significantly extend the life of the log file for a database.</span></span>

<span data-ttu-id="627bb-106">**Microsoft SQL Server 6.5 でチェックポイント時のログの切り捨てを有効にするには**</span><span class="sxs-lookup"><span data-stu-id="627bb-106">**To enable Truncate on Checkpoint in Microsoft SQL Server 6.5**</span></span>

1.  <span data-ttu-id="627bb-107">Microsoft SQL Server Enterprise Manager を起動し、サーバーのツリーを開き、次にデータベース デバイスのツリーを開きます。</span><span class="sxs-lookup"><span data-stu-id="627bb-107">Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Database Devices tree.</span></span>

2.  <span data-ttu-id="627bb-108">この機能を有効にするデータベースの名前をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="627bb-108">Double-click the name of the database on which this feature will be enabled.</span></span>

3.  <span data-ttu-id="627bb-109">[**データベース**] タブで、**削除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="627bb-109">From the **Database** tab, select **Truncate**.</span></span>

4.  <span data-ttu-id="627bb-110">**オプション**] タブから **[チェックポイント時のログの切り捨て]** を選択し、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="627bb-110">From the **Options** tab, select **Truncate Log on Checkpoint**, and then click **OK**.</span></span>

<span data-ttu-id="627bb-111">**Microsoft SQL Server 7.0 でチェックポイント時のログの切り捨てを有効にするには**</span><span class="sxs-lookup"><span data-stu-id="627bb-111">**To enable Truncate on Checkpoint in Microsoft SQL Server 7.0**</span></span>

1.  <span data-ttu-id="627bb-112">Microsoft SQL Server Enterprise Manager を起動し、サーバーのツリーを開き、次にデータベースのツリーを開きます。</span><span class="sxs-lookup"><span data-stu-id="627bb-112">Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Databases tree.</span></span>

2.  <span data-ttu-id="627bb-113">データベースにこの機能が有効になります、[**プロパティ**] の名前を右クリックします。</span><span class="sxs-lookup"><span data-stu-id="627bb-113">Right-click the name of the database on which this feature will be enabled and choose **Properties**.</span></span>

3.  <span data-ttu-id="627bb-114">**オプション**] タブから **[チェックポイント時のログの切り捨て]** を選択し、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="627bb-114">From the **Options** tab, select **Truncate Log on Checkpoint**, and then click **OK**.</span></span>

<span data-ttu-id="627bb-115">**チェックポイントの削除**機能の詳細については、Microsoft SQL Server のマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="627bb-115">For more information about the **Truncate on Checkpoint** feature, see the Microsoft SQL Server documentation.</span></span>

