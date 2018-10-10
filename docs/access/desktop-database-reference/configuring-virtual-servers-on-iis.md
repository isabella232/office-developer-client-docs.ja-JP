---
title: IIS で仮想サーバーを構成する
TOCTitle: Configuring Virtual Servers on IIS
ms:assetid: 0a8057a2-c90b-d0b5-21c8-5343e80708ce
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248837(v=office.15)
ms:contentKeyID: 48543154
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1212a5c7e0761cf9c52a21b5abd67b7dd9841aa0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476613"
---
# <a name="configuring-virtual-servers-on-iis"></a><span data-ttu-id="0efff-102">IIS で仮想サーバーを構成する</span><span class="sxs-lookup"><span data-stu-id="0efff-102">Configuring Virtual Servers on IIS</span></span>


<span data-ttu-id="0efff-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="0efff-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0efff-104">Internet Information Services 4.0 で仮想サーバーを作成する場合、その仮想サーバーが RDS と共に動作するように設定するには、さらに次の 2 つの手順が必要です。</span><span class="sxs-lookup"><span data-stu-id="0efff-104">When creating virtual servers in Internet Information Services 4.0, the following two extra steps are needed in order to configure the virtual server to work with RDS:</span></span>

1.  <span data-ttu-id="0efff-105">サーバーをセットアップするときに、[実行アクセスを許可する (スクリプトのアクセスを含む)] チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="0efff-105">When setting up the server, check "Allow Execute Access."</span></span>

2.  <span data-ttu-id="0efff-106">Msadcs.dll を*vroot*に移動\\msadc、 *vroot*が、仮想サーバーのホーム ディレクトリにあります。</span><span class="sxs-lookup"><span data-stu-id="0efff-106">Move msadcs.dll to *vroot*\\msadc, where *vroot* is the home directory of your virtual server.</span></span>
