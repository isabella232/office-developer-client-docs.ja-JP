---
title: MAPIOFFLINE_ADVISEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 20a46c69-d6ae-7d17-f8af-12952867d342
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3cb110fdcbbd88e494c44ba2ed73cc26674638ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270036"
---
# <a name="mapiofflineadviseinfo"></a><span data-ttu-id="a3315-103">MAPIOFFLINE_ADVISEINFO</span><span class="sxs-lookup"><span data-stu-id="a3315-103">MAPIOFFLINE_ADVISEINFO</span></span>
 
<span data-ttu-id="a3315-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3315-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3315-105">**[IMAPIOfflineMgr::](imapiofflinemgr-advise.md)** 通知して、オフラインオブジェクトのコールバックを登録するようにアドバイスします。</span><span class="sxs-lookup"><span data-stu-id="a3315-105">Provides information to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** to register callback for an offline object.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="a3315-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="a3315-106">Quick info</span></span>

<span data-ttu-id="a3315-107">「 **IMAPIOfflineMgr:: Advise**」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3315-107">See **IMAPIOfflineMgr::Advise**.</span></span> 
  
```cpp
typedef struct 
{ 
      ULONG                   ulSize; 
      ULONG                   ulClientToken; 
      MAPIOFFLINE_CALLBACK_TYPE     CallbackType; 
      IUnknown*               pCallback; 
      ULONG                   ulAdviseTypes; 
      ULONG                   ulStateMask; 
} MAPIOFFLINE_ADVISEINFO;
```

## <a name="members"></a><span data-ttu-id="a3315-108">Members</span><span class="sxs-lookup"><span data-stu-id="a3315-108">Members</span></span>

<span data-ttu-id="a3315-109">_ulsize_: **MAPIOFFLINE_ADVISEINFO**のサイズ。</span><span class="sxs-lookup"><span data-stu-id="a3315-109">_ulSize_: The size of **MAPIOFFLINE_ADVISEINFO**.</span></span> 
    
<span data-ttu-id="a3315-110">_ulclienttoken_: クライアントによってコールバックに対して定義されたトークン。</span><span class="sxs-lookup"><span data-stu-id="a3315-110">_ulClientToken_: A token defined by the client about a callback.</span></span> <span data-ttu-id="a3315-111">これは、 **[IMAPIOfflineNotify:: NOTIFY](imapiofflinenotify-notify.md)** に渡される**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** 構造の*ulclienttoken*メンバーです。</span><span class="sxs-lookup"><span data-stu-id="a3315-111">It is the *ulClientToken* member of the **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** structure passed to **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)**.</span></span> 
    
<span data-ttu-id="a3315-112">/_テキスト_: 作成するコールバックの種類。</span><span class="sxs-lookup"><span data-stu-id="a3315-112">_CallbackType_: Type of callback to make.</span></span>
    
   -  <span data-ttu-id="a3315-113">MAPIOFFLINE_CALLBACK_TYPE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="a3315-113">MAPIOFFLINE_CALLBACK_TYPE_NOTIFY</span></span> 
    
   - <span data-ttu-id="a3315-114">コールバックの種類は、通知によって行います。</span><span class="sxs-lookup"><span data-stu-id="a3315-114">The type of callback is by notification.</span></span> <span data-ttu-id="a3315-115">これは、サポートされている唯一の種類のコールバックです。</span><span class="sxs-lookup"><span data-stu-id="a3315-115">This is the only supported type of callback.</span></span>  <span data-ttu-id="a3315-116">*pcallback*は、インターフェイス**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** を示す必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3315-116">*pCallback*  must indicate the interface **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
<span data-ttu-id="a3315-117">_pcallback_: コールバックに使用するインターフェイス。</span><span class="sxs-lookup"><span data-stu-id="a3315-117">_pCallback_: Interface to use for callback.</span></span> <span data-ttu-id="a3315-118">これは、クライアントによる**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** の実装です。</span><span class="sxs-lookup"><span data-stu-id="a3315-118">This is the client's implementation of **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
<span data-ttu-id="a3315-119">_ulAdviseTypes_: アドバイスの条件で識別される、アドバイスの種類。</span><span class="sxs-lookup"><span data-stu-id="a3315-119">_ulAdviseTypes_: The types of advise, as identified by the condition for advising.</span></span> <span data-ttu-id="a3315-120">サポートされている唯一の種類は MAPIOFFLINE_ADVISE_TYPE_STATECHANGE です。</span><span class="sxs-lookup"><span data-stu-id="a3315-120">The only supported type is MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.</span></span>
    
<span data-ttu-id="a3315-121">_ulStateMask_: サポートされている唯一の状態は、MAPIOFFLINE_STATE_ALL です。</span><span class="sxs-lookup"><span data-stu-id="a3315-121">_ulStateMask_: The only supported state is MAPIOFFLINE_STATE_ALL.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a3315-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="a3315-122">See also</span></span>

- [<span data-ttu-id="a3315-123">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="a3315-123">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)
- [<span data-ttu-id="a3315-124">オフライン状態 API について</span><span class="sxs-lookup"><span data-stu-id="a3315-124">About the Offline State API</span></span>](about-the-offline-state-api.md) 
- [<span data-ttu-id="a3315-125">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="a3315-125">MAPI Constants</span></span>](mapi-constants.md) 
- [<span data-ttu-id="a3315-126">MAPIOFFLINE_CALLBACK_TYPE</span><span class="sxs-lookup"><span data-stu-id="a3315-126">MAPIOFFLINE_CALLBACK_TYPE</span></span>](mapioffline_callback_type.md)

