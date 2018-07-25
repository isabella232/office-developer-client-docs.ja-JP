---
title: Excel クラスター コネクタ関数
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65927ef9-29f7-499a-a1c1-6f672c09bb6b
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4a069aa4ed3ee17320ac65ab793ea8812153cc18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798800"
---
# <a name="excel-cluster-connector-functions"></a><span data-ttu-id="bd918-103">Excel クラスター コネクタ関数</span><span class="sxs-lookup"><span data-stu-id="bd918-103">Excel Cluster Connector Functions</span></span>

 <span data-ttu-id="bd918-104">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bd918-104">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="bd918-105">Microsoft Excel 2013 クラスター コネクタ DLL は、このセクションで取り上げる関数を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bd918-105">Microsoft Excel 2013 cluster connector DLLs must implement the functions described in this section.</span></span>
  
<span data-ttu-id="bd918-106">このセクションの参照トピックで言及されている戻り値は、SDK インクルード ファイル (xlcall.h) で定義されています。</span><span class="sxs-lookup"><span data-stu-id="bd918-106">The return values mentioned in reference topics in this section are defined in the SDK include file, xlcall.h.</span></span>
  
## <a name="cluster-connector-architecture"></a><span data-ttu-id="bd918-107">クラスター コネクタのアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="bd918-107">Cluster Connector Architecture</span></span>

<span data-ttu-id="bd918-108">Excel は、クラスター コネクタのエントリ ポイントを呼び出して、ユーザー定義関数呼び出しを高パフォーマンスのコンピューティング クラスターに転送し、クラスター セッション管理を行います。</span><span class="sxs-lookup"><span data-stu-id="bd918-108">Excel calls entry points in a cluster connector to transfer user-defined function calls to a high-performance compute cluster, and for cluster session management.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="bd918-109">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="bd918-109">In this section</span></span>

[<span data-ttu-id="bd918-110">CallUDF</span><span class="sxs-lookup"><span data-stu-id="bd918-110">CallUDF</span></span>](calludf.md)
  
[<span data-ttu-id="bd918-111">CancelOutstandingRequests</span><span class="sxs-lookup"><span data-stu-id="bd918-111">CancelOutstandingRequests</span></span>](canceloutstandingrequests.md)
  
[<span data-ttu-id="bd918-112">CloseSession</span><span class="sxs-lookup"><span data-stu-id="bd918-112">CloseSession</span></span>](closesession.md)
  
[<span data-ttu-id="bd918-113">OpenSession</span><span class="sxs-lookup"><span data-stu-id="bd918-113">OpenSession</span></span>](opensession.md)
  
[<span data-ttu-id="bd918-114">PingSession</span><span class="sxs-lookup"><span data-stu-id="bd918-114">PingSession</span></span>](pingsession.md)
  
[<span data-ttu-id="bd918-115">ShowOptions</span><span class="sxs-lookup"><span data-stu-id="bd918-115">ShowOptions</span></span>](showoptions.md)
  
## <a name="see-also"></a><span data-ttu-id="bd918-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="bd918-116">See also</span></span>



[<span data-ttu-id="bd918-117">Excel クラスター コネクタの開発</span><span class="sxs-lookup"><span data-stu-id="bd918-117">Developing Excel Cluster Connectors</span></span>](developing-excel-cluster-connectors.md)
  
[<span data-ttu-id="bd918-118">クラスター セーフ関数</span><span class="sxs-lookup"><span data-stu-id="bd918-118">Cluster Safe Functions</span></span>](cluster-safe-functions.md)

