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
ms.openlocfilehash: d5cb43bfa3acd912e397644657223c177d6afb30
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589323"
---
# <a name="hrallocadvisesink"></a><span data-ttu-id="36d14-103">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="36d14-103">HrAllocAdviseSink</span></span>

  
  
<span data-ttu-id="36d14-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36d14-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36d14-105">呼び出し元の実装とイベント通知が開始されるようにコールバック関数で指定されたコンテキストを指定、アドバイズ シンク オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="36d14-105">Creates an advise sink object, given a context specified by the calling implementation and a callback function to be triggered by an event notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="36d14-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="36d14-106">Header file:</span></span>  <br/> |<span data-ttu-id="36d14-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="36d14-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="36d14-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="36d14-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="36d14-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="36d14-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="36d14-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="36d14-110">Called by:</span></span>  <br/> |<span data-ttu-id="36d14-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="36d14-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
STDAPI HrAllocAdviseSink(
  LPNOTIFCALLBACK lpfnCallback,
  LPVOID lpvContext,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a><span data-ttu-id="36d14-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="36d14-112">Parameters</span></span>

 <span data-ttu-id="36d14-113">_lpfnCallback_</span><span class="sxs-lookup"><span data-stu-id="36d14-113">_lpfnCallback_</span></span>
  
> <span data-ttu-id="36d14-114">[in]MAPI は、新しく作成されたアドバイズ シンクに通知イベントが発生したときに呼び出される[NOTIFCALLBACK](notifcallback.md)プロトタイプに基づいてコールバック関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="36d14-114">[in] Pointer to a callback function based on the [NOTIFCALLBACK](notifcallback.md) prototype that MAPI is to call when a notification event occurs for the newly created advise sink.</span></span> 
    
 <span data-ttu-id="36d14-115">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="36d14-115">_lpvContext_</span></span>
  
> <span data-ttu-id="36d14-116">[in]呼び出し元のデータへのポインターは、MAPI では、それを呼び出すときに、コールバック関数に渡されます。</span><span class="sxs-lookup"><span data-stu-id="36d14-116">[in] Pointer to caller data passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="36d14-117">呼び出し元のデータには、重要では、クライアント、またはプロバイダーにアドレスを表すことができます。</span><span class="sxs-lookup"><span data-stu-id="36d14-117">The caller data can represent an address of significance to the client or provider.</span></span> <span data-ttu-id="36d14-118">通常、C++ コードでは、 _lpvContext_パラメーターのポインターを表しますオブジェクトのアドレスにします。</span><span class="sxs-lookup"><span data-stu-id="36d14-118">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to the address of an object.</span></span> 
    
 <span data-ttu-id="36d14-119">_lppAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="36d14-119">_lppAdviseSink_</span></span>
  
> <span data-ttu-id="36d14-120">[out]アドバイズ シンク オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="36d14-120">[out] Pointer to a pointer to an advise sink object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="36d14-121">Return value</span><span class="sxs-lookup"><span data-stu-id="36d14-121">Return value</span></span>

<span data-ttu-id="36d14-122">なし。</span><span class="sxs-lookup"><span data-stu-id="36d14-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="36d14-123">注釈</span><span class="sxs-lookup"><span data-stu-id="36d14-123">Remarks</span></span>

<span data-ttu-id="36d14-124">**HrAllocAdviseSink**関数を使用するには、クライアント アプリケーションまたはサービス プロバイダーに通知を受け取るオブジェクトを作成、そのオブジェクトを使用する[NOTIFCALLBACK](notifcallback.md)関数のプロトタイプに基づく通知のコールバック関数を作成および_lpvContext_の値として**HrAllocAdviseSink**関数内のオブジェクトへのポインターをパスします。</span><span class="sxs-lookup"><span data-stu-id="36d14-124">To use the **HrAllocAdviseSink** function, a client application or service provider creates an object to receive notifications, creates a notification callback function based on the [NOTIFCALLBACK](notifcallback.md) function prototype that goes with that object, and passes a pointer to the object in the **HrAllocAdviseSink** function as the  _lpvContext_ value.</span></span> <span data-ttu-id="36d14-125">通知; を実行してこれを行う通知プロセスの一環としては、MAPI はコンテキストとオブジェクトへのポインターでコールバック関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="36d14-125">Doing so performs a notification; and as part of the notification process, MAPI calls the callback function with the object pointer as the context.</span></span> 
  
<span data-ttu-id="36d14-126">MAPI では、その通知エンジンを非同期的に実装します。</span><span class="sxs-lookup"><span data-stu-id="36d14-126">MAPI implements its notification engine asynchronously.</span></span> <span data-ttu-id="36d14-127">C++ では、通知コールバック オブジェクトのメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="36d14-127">In C++, the notification callback can be an object method.</span></span> <span data-ttu-id="36d14-128">通知を生成するオブジェクトがクライアントに提供、または通知を要求するプロバイダーは、オブジェクトのためには、そのオブジェクトの個別の参照カウントを保つ必要があるではない場合は、シンクを案内します。</span><span class="sxs-lookup"><span data-stu-id="36d14-128">If the object generating the notification is not present, the client or provider requesting notification must keep a separate reference count for that object for the object's advise sink.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="36d14-129">**HrAllocAdviseSink**に限って使ってください。クライアント独自のアドバイズ シンクを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="36d14-129">**HrAllocAdviseSink** should be used sparingly; it is safer for clients to create their own advise sinks.</span></span> 
  

