---
title: IIS での仮想サーバーの構成
TOCTitle: Configuring virtual servers on IIS
ms:assetid: 0a8057a2-c90b-d0b5-21c8-5343e80708ce
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248837(v=office.15)
ms:contentKeyID: 48543154
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a9c7f5782885aafd43e365ddc4f08dedd0975234
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719316"
---
# <a name="configuring-virtual-servers-on-iis"></a><span data-ttu-id="3e2ec-102">IIS での仮想サーバーの構成</span><span class="sxs-lookup"><span data-stu-id="3e2ec-102">Configuring virtual servers on IIS</span></span>

<span data-ttu-id="3e2ec-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="3e2ec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3e2ec-104">Internet Information Services 4.0 で仮想サーバーを作成する場合、その仮想サーバーが RDS と共に動作するように設定するには、さらに次の 2 つの手順が必要です。</span><span class="sxs-lookup"><span data-stu-id="3e2ec-104">When creating virtual servers in Internet Information Services 4.0, the following two extra steps are needed in order to configure the virtual server to work with RDS:</span></span>

1.  <span data-ttu-id="3e2ec-105">サーバーをセットアップするときに、[実行アクセスを許可する (スクリプトのアクセスを含む)] チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="3e2ec-105">When setting up the server, check "Allow Execute Access."</span></span>

2.  <span data-ttu-id="3e2ec-106">Msadcs.dll を*vroot*に移動\\msadc、 *vroot*が、仮想サーバーのホーム ディレクトリにあります。</span><span class="sxs-lookup"><span data-stu-id="3e2ec-106">Move msadcs.dll to *vroot*\\msadc, where *vroot* is the home directory of your virtual server.</span></span>

