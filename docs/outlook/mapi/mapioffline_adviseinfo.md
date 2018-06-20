---
title: MAPIOFFLINE_ADVISEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 20a46c69-d6ae-7d17-f8af-12952867d342
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 443644b66ba9c961992e22dbfc260fe8c48fe1b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801503"
---
# <a name="mapiofflineadviseinfo"></a><span data-ttu-id="f4487-103">MAPIOFFLINE_ADVISEINFO</span><span class="sxs-lookup"><span data-stu-id="f4487-103">MAPIOFFLINE_ADVISEINFO</span></span>
 
<span data-ttu-id="f4487-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f4487-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f4487-105">オフライン オブジェクトに対してコールバックを登録するのには**[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** の情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="f4487-105">Provides information to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** to register callback for an offline object.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="f4487-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="f4487-106">Quick info</span></span>

<span data-ttu-id="f4487-107">**IMAPIOfflineMgr::Advise**を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f4487-107">See **IMAPIOfflineMgr::Advise**.</span></span> 
  
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

## <a name="members"></a><span data-ttu-id="f4487-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="f4487-108">Members</span></span>

<span data-ttu-id="f4487-109">_ulSize_: **MAPIOFFLINE_ADVISEINFO**のサイズです。</span><span class="sxs-lookup"><span data-stu-id="f4487-109">_ulSize_: The size of **MAPIOFFLINE_ADVISEINFO**.</span></span> 
    
<span data-ttu-id="f4487-110">_ulClientToken_: コールバックは、クライアントで定義されているトークンです。</span><span class="sxs-lookup"><span data-stu-id="f4487-110">_ulClientToken_: A token defined by the client about a callback.</span></span> <span data-ttu-id="f4487-111">*UlClientToken* 、 **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** 構造体のメンバー **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** に渡されたすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f4487-111">It is the *ulClientToken* member of the **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** structure passed to **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)**.</span></span> 
    
<span data-ttu-id="f4487-112">_CallbackType_: を作成するためのコールバックの種類です。</span><span class="sxs-lookup"><span data-stu-id="f4487-112">_CallbackType_: Type of callback to make.</span></span>
    
   -  <span data-ttu-id="f4487-113">MAPIOFFLINE_CALLBACK_TYPE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="f4487-113">MAPIOFFLINE_CALLBACK_TYPE_NOTIFY</span></span> 
    
   - <span data-ttu-id="f4487-114">コールバックの種類は、通知されたものです。</span><span class="sxs-lookup"><span data-stu-id="f4487-114">The type of callback is by notification.</span></span> <span data-ttu-id="f4487-115">これは、コールバックの唯一のサポートされている型です。</span><span class="sxs-lookup"><span data-stu-id="f4487-115">This is the only supported type of callback.</span></span>  <span data-ttu-id="f4487-116">*pCallback*は、 **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** インタ フェースを示す必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4487-116">*pCallback*  must indicate the interface **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
<span data-ttu-id="f4487-117">_pCallback_: コールバックを使用するインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="f4487-117">_pCallback_: Interface to use for callback.</span></span> <span data-ttu-id="f4487-118">これは、 **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** のクライアントの実装です。</span><span class="sxs-lookup"><span data-stu-id="f4487-118">This is the client's implementation of **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
<span data-ttu-id="f4487-119">_ulAdviseTypes_: のアドバイズ、通知の条件で識別される型。</span><span class="sxs-lookup"><span data-stu-id="f4487-119">_ulAdviseTypes_: The types of advise, as identified by the condition for advising.</span></span> <span data-ttu-id="f4487-120">のみサポートされている型は、MAPIOFFLINE_ADVISE_TYPE_STATECHANGE です。</span><span class="sxs-lookup"><span data-stu-id="f4487-120">The only supported type is MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.</span></span>
    
<span data-ttu-id="f4487-121">_ulStateMask_: MAPIOFFLINE_STATE_ALL は、唯一サポートされている状態です。</span><span class="sxs-lookup"><span data-stu-id="f4487-121">_ulStateMask_: The only supported state is MAPIOFFLINE_STATE_ALL.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f4487-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="f4487-122">See also</span></span>

- [<span data-ttu-id="f4487-123">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="f4487-123">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)
- [<span data-ttu-id="f4487-124">オフラインの状態の API について</span><span class="sxs-lookup"><span data-stu-id="f4487-124">About the Offline State API</span></span>](about-the-offline-state-api.md) 
- [<span data-ttu-id="f4487-125">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="f4487-125">MAPI Constants</span></span>](mapi-constants.md) 
- [<span data-ttu-id="f4487-126">MAPIOFFLINE_CALLBACK_TYPE</span><span class="sxs-lookup"><span data-stu-id="f4487-126">MAPIOFFLINE_CALLBACK_TYPE</span></span>](mapioffline_callback_type.md)

