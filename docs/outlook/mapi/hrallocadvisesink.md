---
title: HrAllocAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrAllocAdviseSink
api_type:
- HeaderDef
ms.assetid: 1dd460e6-ce95-4fef-bb5e-8d778c9716d5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7f9873fe8e1825c68d4540cc1d093171e9f95727
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348217"
---
# <a name="hrallocadvisesink"></a><span data-ttu-id="d40a4-103">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="d40a4-103">HrAllocAdviseSink</span></span>

  
  
<span data-ttu-id="d40a4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d40a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d40a4-105">呼び出し側の実装によって指定されたコンテキストと、イベント通知によってトリガーされるコールバック関数を指定して、アドバイズシンクオブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="d40a4-105">Creates an advise sink object, given a context specified by the calling implementation and a callback function to be triggered by an event notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d40a4-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="d40a4-106">Header file:</span></span>  <br/> |<span data-ttu-id="d40a4-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="d40a4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d40a4-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="d40a4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d40a4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d40a4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d40a4-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="d40a4-110">Called by:</span></span>  <br/> |<span data-ttu-id="d40a4-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="d40a4-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
STDAPI HrAllocAdviseSink(
  LPNOTIFCALLBACK lpfnCallback,
  LPVOID lpvContext,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a><span data-ttu-id="d40a4-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d40a4-112">Parameters</span></span>

 <span data-ttu-id="d40a4-113">_lpfnCallback_</span><span class="sxs-lookup"><span data-stu-id="d40a4-113">_lpfnCallback_</span></span>
  
> <span data-ttu-id="d40a4-114">順番新しく作成されたアドバイズシンクに対して通知イベントが発生したときに MAPI が呼び出す[NOTIFCALLBACK](notifcallback.md)プロトタイプに基づく、コールバック関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d40a4-114">[in] Pointer to a callback function based on the [NOTIFCALLBACK](notifcallback.md) prototype that MAPI is to call when a notification event occurs for the newly created advise sink.</span></span> 
    
 <span data-ttu-id="d40a4-115">_lpvcontext_</span><span class="sxs-lookup"><span data-stu-id="d40a4-115">_lpvContext_</span></span>
  
> <span data-ttu-id="d40a4-116">順番MAPI がコールバック関数に渡す、呼び出し元データへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d40a4-116">[in] Pointer to caller data passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="d40a4-117">発信者データは、クライアントまたはプロバイダーの重要度のアドレスを表すことができます。</span><span class="sxs-lookup"><span data-stu-id="d40a4-117">The caller data can represent an address of significance to the client or provider.</span></span> <span data-ttu-id="d40a4-118">通常、C++ コードの場合、 _lpvcontext_パラメーターはオブジェクトのアドレスへのポインターを表します。</span><span class="sxs-lookup"><span data-stu-id="d40a4-118">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to the address of an object.</span></span> 
    
 <span data-ttu-id="d40a4-119">_lppAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="d40a4-119">_lppAdviseSink_</span></span>
  
> <span data-ttu-id="d40a4-120">読み上げアドバイズシンクオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d40a4-120">[out] Pointer to a pointer to an advise sink object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d40a4-121">Return value</span><span class="sxs-lookup"><span data-stu-id="d40a4-121">Return value</span></span>

<span data-ttu-id="d40a4-122">なし。</span><span class="sxs-lookup"><span data-stu-id="d40a4-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d40a4-123">解説</span><span class="sxs-lookup"><span data-stu-id="d40a4-123">Remarks</span></span>

<span data-ttu-id="d40a4-124">**HrAllocAdviseSink**関数を使用するために、クライアントアプリケーションまたはサービスプロバイダーは通知を受信するオブジェクトを作成し、そのオブジェクトに含まれる[NOTIFCALLBACK](notifcallback.md)関数プロトタイプに基づいて通知コールバック関数を作成します。を指定し、 **HrAllocAdviseSink**関数内のオブジェクトへのポインターを_lpvcontext_値として渡します。</span><span class="sxs-lookup"><span data-stu-id="d40a4-124">To use the **HrAllocAdviseSink** function, a client application or service provider creates an object to receive notifications, creates a notification callback function based on the [NOTIFCALLBACK](notifcallback.md) function prototype that goes with that object, and passes a pointer to the object in the **HrAllocAdviseSink** function as the  _lpvContext_ value.</span></span> <span data-ttu-id="d40a4-125">これにより通知が行われます。通知処理の一環として、MAPI はオブジェクトポインターをコンテキストとしてコールバック関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d40a4-125">Doing so performs a notification; and as part of the notification process, MAPI calls the callback function with the object pointer as the context.</span></span> 
  
<span data-ttu-id="d40a4-126">MAPI は、通知エンジンを非同期的に実装します。</span><span class="sxs-lookup"><span data-stu-id="d40a4-126">MAPI implements its notification engine asynchronously.</span></span> <span data-ttu-id="d40a4-127">C++ では、通知コールバックはオブジェクトメソッドにすることができます。</span><span class="sxs-lookup"><span data-stu-id="d40a4-127">In C++, the notification callback can be an object method.</span></span> <span data-ttu-id="d40a4-128">通知を生成するオブジェクトが存在しない場合は、通知を要求しているクライアントまたはプロバイダーは、オブジェクトのアドバイズシンクに対して、そのオブジェクトに対して個別の参照カウントを保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d40a4-128">If the object generating the notification is not present, the client or provider requesting notification must keep a separate reference count for that object for the object's advise sink.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="d40a4-129">**HrAllocAdviseSink**は控えめに使用する必要があります。クライアントが独自のアドバイズシンクを作成することは安全です。</span><span class="sxs-lookup"><span data-stu-id="d40a4-129">**HrAllocAdviseSink** should be used sparingly; it is safer for clients to create their own advise sinks.</span></span> 
  

