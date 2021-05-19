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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420025"
---
# <a name="mapioffline_adviseinfo"></a><span data-ttu-id="9f283-103">MAPIOFFLINE_ADVISEINFO</span><span class="sxs-lookup"><span data-stu-id="9f283-103">MAPIOFFLINE_ADVISEINFO</span></span>
 
<span data-ttu-id="9f283-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f283-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f283-105">**[IMAPIOfflineMgr::Advise に](imapiofflinemgr-advise.md)** オフライン オブジェクトのコールバックを登録するための情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="9f283-105">Provides information to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** to register callback for an offline object.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="9f283-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="9f283-106">Quick info</span></span>

<span data-ttu-id="9f283-107">**「IMAPIOfflineMgr::Advise」を参照してください**。</span><span class="sxs-lookup"><span data-stu-id="9f283-107">See **IMAPIOfflineMgr::Advise**.</span></span> 
  
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

## <a name="members"></a><span data-ttu-id="9f283-108">Members</span><span class="sxs-lookup"><span data-stu-id="9f283-108">Members</span></span>

<span data-ttu-id="9f283-109">_ulSize_: サイズ **は** MAPIOFFLINE_ADVISEINFO です。</span><span class="sxs-lookup"><span data-stu-id="9f283-109">_ulSize_: The size of **MAPIOFFLINE_ADVISEINFO**.</span></span> 
    
<span data-ttu-id="9f283-110">_ulClientToken_: コールバックに関するクライアントによって定義されたトークン。</span><span class="sxs-lookup"><span data-stu-id="9f283-110">_ulClientToken_: A token defined by the client about a callback.</span></span> <span data-ttu-id="9f283-111">*IMAPIOfflineNotify::Notify* **[](mapioffline_notify.md)** に渡MAPIOFFLINE_NOTIFY構造の **[ulClientToken メンバーです](imapiofflinenotify-notify.md)**。</span><span class="sxs-lookup"><span data-stu-id="9f283-111">It is the *ulClientToken* member of the **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** structure passed to **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)**.</span></span> 
    
<span data-ttu-id="9f283-112">_CallbackType_: 作成するコールバックの種類。</span><span class="sxs-lookup"><span data-stu-id="9f283-112">_CallbackType_: Type of callback to make.</span></span>
    
   -  <span data-ttu-id="9f283-113">MAPIOFFLINE_CALLBACK_TYPE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="9f283-113">MAPIOFFLINE_CALLBACK_TYPE_NOTIFY</span></span> 
    
   - <span data-ttu-id="9f283-114">コールバックの種類は通知別です。</span><span class="sxs-lookup"><span data-stu-id="9f283-114">The type of callback is by notification.</span></span> <span data-ttu-id="9f283-115">これは、サポートされているコールバックの唯一の種類です。</span><span class="sxs-lookup"><span data-stu-id="9f283-115">This is the only supported type of callback.</span></span>  <span data-ttu-id="9f283-116">*pCallback は*  、インターフェイス **[IMAPIOfflineNotify を示す必要があります](imapiofflinenotifyiunknown.md)**。</span><span class="sxs-lookup"><span data-stu-id="9f283-116">*pCallback*  must indicate the interface **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
<span data-ttu-id="9f283-117">_pCallback_: コールバックに使用するインターフェイス。</span><span class="sxs-lookup"><span data-stu-id="9f283-117">_pCallback_: Interface to use for callback.</span></span> <span data-ttu-id="9f283-118">これは **[、IMAPIOfflineNotify のクライアントの実装です](imapiofflinenotifyiunknown.md)**。</span><span class="sxs-lookup"><span data-stu-id="9f283-118">This is the client's implementation of **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
<span data-ttu-id="9f283-119">_ulAdviseTypes_: アドバイスの種類 。アドバイスの条件によって識別されます。</span><span class="sxs-lookup"><span data-stu-id="9f283-119">_ulAdviseTypes_: The types of advise, as identified by the condition for advising.</span></span> <span data-ttu-id="9f283-120">サポートされている唯一の型は、MAPIOFFLINE_ADVISE_TYPE_STATECHANGE。</span><span class="sxs-lookup"><span data-stu-id="9f283-120">The only supported type is MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.</span></span>
    
<span data-ttu-id="9f283-121">_ulStateMask_: サポートされている唯一の状態は、MAPIOFFLINE_STATE_ALL。</span><span class="sxs-lookup"><span data-stu-id="9f283-121">_ulStateMask_: The only supported state is MAPIOFFLINE_STATE_ALL.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9f283-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="9f283-122">See also</span></span>

- [<span data-ttu-id="9f283-123">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="9f283-123">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)
- [<span data-ttu-id="9f283-124">オフライン状態 API について</span><span class="sxs-lookup"><span data-stu-id="9f283-124">About the Offline State API</span></span>](about-the-offline-state-api.md) 
- [<span data-ttu-id="9f283-125">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="9f283-125">MAPI Constants</span></span>](mapi-constants.md) 
- [<span data-ttu-id="9f283-126">MAPIOFFLINE_CALLBACK_TYPE</span><span class="sxs-lookup"><span data-stu-id="9f283-126">MAPIOFFLINE_CALLBACK_TYPE</span></span>](mapioffline_callback_type.md)

