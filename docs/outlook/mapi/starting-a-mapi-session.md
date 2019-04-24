---
title: MAPI セッションの開始
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7935ebed-f252-482c-ad8c-757aa2d8501d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d88ce382b6a6b5f98ec5f88c4deb1565d3b60151
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336345"
---
# <a name="starting-a-mapi-session"></a><span data-ttu-id="ba58c-103">MAPI セッションの開始</span><span class="sxs-lookup"><span data-stu-id="ba58c-103">Starting a MAPI Session</span></span>

  
  
<span data-ttu-id="ba58c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ba58c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ba58c-105">セッションの起動時に大量の作業が実行されますが、必要なタスクは最小限で済みます。</span><span class="sxs-lookup"><span data-stu-id="ba58c-105">Although there is a significant amount of work performed during session start up, the required tasks are minimal.</span></span> <span data-ttu-id="ba58c-106">この作業の多くは、 [MAPIInitialize](mapiinitialize.md)および[MAPILogonEx](mapilogonex.md)呼び出しの MAPI 処理で行われます。</span><span class="sxs-lookup"><span data-stu-id="ba58c-106">Much of this work is done in the MAPI processing of the [MAPIInitialize](mapiinitialize.md) and [MAPILogonEx](mapilogonex.md) calls.</span></span> <span data-ttu-id="ba58c-107">どちらの関数も、通知処理やユーザーインターフェイスなどのセッションの側面を制御するための入力パラメーターとしてフラグを受け入れます。</span><span class="sxs-lookup"><span data-stu-id="ba58c-107">Both of these functions accept flags as input parameters for controlling aspects of the session such as notification handling and the user interface.</span></span> <span data-ttu-id="ba58c-108">**MAPIInitialize**を呼び出して mapi ライブラリと**MAPILogonEx**を初期化し、mapi サブシステムにログオンするときに、これらの各フラグを設定した場合の影響を理解しておくことが重要です。</span><span class="sxs-lookup"><span data-stu-id="ba58c-108">It is important to understand the consequences of setting each of these flags when calling **MAPIInitialize** to initialize the MAPI libraries and **MAPILogonEx** to log on to the MAPI subsystem.</span></span> 
  
 <span data-ttu-id="ba58c-109">**MAPI セッションを開始するには**</span><span class="sxs-lookup"><span data-stu-id="ba58c-109">**To start a MAPI session**</span></span>
  
1. <span data-ttu-id="ba58c-110">**MAPIInitialize**を呼び出して、MAPI ライブラリの標準セットを初期化します。</span><span class="sxs-lookup"><span data-stu-id="ba58c-110">Call **MAPIInitialize** to initialize the standard set of MAPI libraries.</span></span> 
    
2. <span data-ttu-id="ba58c-111">ole ライブラリを使用する必要がある場合は、ole 関数[oleinitialize](https://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ba58c-111">If you need to use the OLE libraries, call the OLE function [OleInitialize](https://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx).</span></span>
    
3. <span data-ttu-id="ba58c-112">MAPI ユーティリティライブラリを使用する必要がある場合は、 [ScInitMapiUtil](scinitmapiutil.md)を呼び出してください。</span><span class="sxs-lookup"><span data-stu-id="ba58c-112">If you need to use the MAPI utility library, call [ScInitMapiUtil](scinitmapiutil.md).</span></span>
    
4. <span data-ttu-id="ba58c-113">有効なプロファイルを使用して**MAPILogonEx**を呼び出して、MAPI サブシステムにログオンします。</span><span class="sxs-lookup"><span data-stu-id="ba58c-113">Call **MAPILogonEx** with a valid profile to log on to the MAPI subsystem.</span></span> <span data-ttu-id="ba58c-114">**MAPILogonEx**は、プロファイルに含まれているメッセージサービスの各サービスプロバイダーの構成を確認し、必要に応じて、ユーザーに追加情報を要求します。</span><span class="sxs-lookup"><span data-stu-id="ba58c-114">**MAPILogonEx** verifies the configuration of each of the service providers in the message services included in the profile, prompting the user for additional information if necessary and possible.</span></span> <span data-ttu-id="ba58c-115">**MAPILogonEx**が完了すると、構成されたサービスプロバイダーがサービスの準備が整います。</span><span class="sxs-lookup"><span data-stu-id="ba58c-115">When **MAPILogonEx** completes, the configured service providers are ready for service.</span></span> 
    
## <a name="in-this-section"></a><span data-ttu-id="ba58c-116">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="ba58c-116">In this section</span></span>

[<span data-ttu-id="ba58c-117">MAPI の初期化</span><span class="sxs-lookup"><span data-stu-id="ba58c-117">Initializing MAPI</span></span>](initializing-mapi.md)
  
> <span data-ttu-id="ba58c-118">セッションの MAPI を初期化する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ba58c-118">Describes how to initialize MAPI for a session.</span></span>
    
[<span data-ttu-id="ba58c-119">OLE for MAPI の初期化</span><span class="sxs-lookup"><span data-stu-id="ba58c-119">Initializing OLE for MAPI</span></span>](initializing-ole-for-mapi.md)
  
> <span data-ttu-id="ba58c-120">MAPI で使用するために OLE を初期化するために必要な呼び出しについて説明します。</span><span class="sxs-lookup"><span data-stu-id="ba58c-120">Describes the calls to make to initialize OLE for use with MAPI.</span></span>
    
[<span data-ttu-id="ba58c-121">MAPI ユーティリティの初期化</span><span class="sxs-lookup"><span data-stu-id="ba58c-121">Initializing the MAPI Utilities</span></span>](initializing-the-mapi-utilities.md)
  
> <span data-ttu-id="ba58c-122">MAPI ユーティリティを初期化する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ba58c-122">Describes how to initialize MAPI utilities.</span></span>
    
[<span data-ttu-id="ba58c-123">MAPI へのログオン</span><span class="sxs-lookup"><span data-stu-id="ba58c-123">Logging on to MAPI</span></span>](logging-on-to-mapi.md)
  
> <span data-ttu-id="ba58c-124">クライアントアプリケーションが MAPI サブシステムにログオンする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ba58c-124">Describes how client applications log on to the MAPI sub system.</span></span>
    

