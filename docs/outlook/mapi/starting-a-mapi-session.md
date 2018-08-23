---
title: MAPI セッションの開始
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7935ebed-f252-482c-ad8c-757aa2d8501d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d683d5fc959b219569417c74494cb47d7c2c059e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804000"
---
# <a name="starting-a-mapi-session"></a><span data-ttu-id="4e7b5-103">MAPI セッションの開始</span><span class="sxs-lookup"><span data-stu-id="4e7b5-103">Starting a MAPI Session</span></span>

  
  
<span data-ttu-id="4e7b5-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4e7b5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4e7b5-105">セッション開始時に実行される作業のかなりの量ですが、必要な作業は最小限にします。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-105">Although there is a significant amount of work performed during session start up, the required tasks are minimal.</span></span> <span data-ttu-id="4e7b5-106">この作業の大半は、MAPI で作業が[生じます](mapiinitialize.md)し、 [MAPILogonEx](mapilogonex.md)の呼び出しの処理です。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-106">Much of this work is done in the MAPI processing of the [MAPIInitialize](mapiinitialize.md) and [MAPILogonEx](mapilogonex.md) calls.</span></span> <span data-ttu-id="4e7b5-107">どちらの関数は、セッション通知の処理とユーザー インターフェイスなどの側面を制御するための入力パラメーターとしてフラグを受け入れます。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-107">Both of these functions accept flags as input parameters for controlling aspects of the session such as notification handling and the user interface.</span></span> <span data-ttu-id="4e7b5-108">MAPI ライブラリを初期化するために**生じます**し、MAPI サブシステムにログオンする**MAPILogonEx**を呼び出すときに、これらのフラグを設定することの影響をよく理解するのには重要です。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-108">It is important to understand the consequences of setting each of these flags when calling **MAPIInitialize** to initialize the MAPI libraries and **MAPILogonEx** to log on to the MAPI subsystem.</span></span> 
  
 <span data-ttu-id="4e7b5-109">**MAPI セッションを開始するには**</span><span class="sxs-lookup"><span data-stu-id="4e7b5-109">**To start a MAPI session**</span></span>
  
1. <span data-ttu-id="4e7b5-110">MAPI ライブラリの標準セットを初期化するために**生じます**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-110">Call **MAPIInitialize** to initialize the standard set of MAPI libraries.</span></span> 
    
2. <span data-ttu-id="4e7b5-111">OLE ライブラリを使用する場合は、 [OleInitialize](http://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx)の OLE 関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-111">If you need to use the OLE libraries, call the OLE function [OleInitialize](http://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx).</span></span>
    
3. <span data-ttu-id="4e7b5-112">MAPI ユーティリティ ライブラリを使用する場合は、 [ScInitMapiUtil](scinitmapiutil.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-112">If you need to use the MAPI utility library, call [ScInitMapiUtil](scinitmapiutil.md).</span></span>
    
4. <span data-ttu-id="4e7b5-113">**MAPILogonEx**は、MAPI サブシステムにログオンするための有効なプロファイルを使用して呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-113">Call **MAPILogonEx** with a valid profile to log on to the MAPI subsystem.</span></span> <span data-ttu-id="4e7b5-114">**MAPILogonEx**では、各プロファイルに含まれているメッセージ サービスのサービス プロバイダーを必要と考えられる場合の詳細についてユーザーに確認の構成を確認します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-114">**MAPILogonEx** verifies the configuration of each of the service providers in the message services included in the profile, prompting the user for additional information if necessary and possible.</span></span> <span data-ttu-id="4e7b5-115">**MAPILogonEx**が完了すると、構成済みのサービス プロバイダーは、サービスの準備が完了です。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-115">When **MAPILogonEx** completes, the configured service providers are ready for service.</span></span> 
    
## <a name="in-this-section"></a><span data-ttu-id="4e7b5-116">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="4e7b5-116">In this section</span></span>

[<span data-ttu-id="4e7b5-117">MAPI の初期化</span><span class="sxs-lookup"><span data-stu-id="4e7b5-117">Initializing MAPI</span></span>](initializing-mapi.md)
  
> <span data-ttu-id="4e7b5-118">セッションの MAPI を初期化する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-118">Describes how to initialize MAPI for a session.</span></span>
    
[<span data-ttu-id="4e7b5-119">OLE for MAPI の初期化</span><span class="sxs-lookup"><span data-stu-id="4e7b5-119">Initializing OLE for MAPI</span></span>](initializing-ole-for-mapi.md)
  
> <span data-ttu-id="4e7b5-120">MAPI を使用するための OLE を初期化するための呼び出しについて説明します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-120">Describes the calls to make to initialize OLE for use with MAPI.</span></span>
    
[<span data-ttu-id="4e7b5-121">MAPI ユーティリティの初期化</span><span class="sxs-lookup"><span data-stu-id="4e7b5-121">Initializing the MAPI Utilities</span></span>](initializing-the-mapi-utilities.md)
  
> <span data-ttu-id="4e7b5-122">MAPI ユーティリティを初期化する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-122">Describes how to initialize MAPI utilities.</span></span>
    
[<span data-ttu-id="4e7b5-123">MAPI へのログオン</span><span class="sxs-lookup"><span data-stu-id="4e7b5-123">Logging on to MAPI</span></span>](logging-on-to-mapi.md)
  
> <span data-ttu-id="4e7b5-124">クライアント アプリケーションが MAPI サブシステムにログオンする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4e7b5-124">Describes how client applications log on to the MAPI sub system.</span></span>
    

