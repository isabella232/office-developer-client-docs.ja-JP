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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7f9873fe8e1825c68d4540cc1d093171e9f95727
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428901"
---
# <a name="hrallocadvisesink"></a><span data-ttu-id="7bf0b-103">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="7bf0b-103">HrAllocAdviseSink</span></span>

  
  
<span data-ttu-id="7bf0b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7bf0b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7bf0b-105">呼び出し元の実装で指定されたコンテキストと、イベント通知によってトリガーされるコールバック関数を指定して、アアドバイス シンク オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="7bf0b-105">Creates an advise sink object, given a context specified by the calling implementation and a callback function to be triggered by an event notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7bf0b-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="7bf0b-106">Header file:</span></span>  <br/> |<span data-ttu-id="7bf0b-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="7bf0b-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7bf0b-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="7bf0b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7bf0b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7bf0b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7bf0b-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="7bf0b-110">Called by:</span></span>  <br/> |<span data-ttu-id="7bf0b-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="7bf0b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
STDAPI HrAllocAdviseSink(
  LPNOTIFCALLBACK lpfnCallback,
  LPVOID lpvContext,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a><span data-ttu-id="7bf0b-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7bf0b-112">Parameters</span></span>

 <span data-ttu-id="7bf0b-113">_lpfnCallback_</span><span class="sxs-lookup"><span data-stu-id="7bf0b-113">_lpfnCallback_</span></span>
  
> <span data-ttu-id="7bf0b-114">[in]新しく作成されたアアドバイス シンクの通知イベントが発生した場合に MAPI が呼び出す [NOTIFCALLBACK](notifcallback.md) プロトタイプに基づくコールバック関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7bf0b-114">[in] Pointer to a callback function based on the [NOTIFCALLBACK](notifcallback.md) prototype that MAPI is to call when a notification event occurs for the newly created advise sink.</span></span> 
    
 <span data-ttu-id="7bf0b-115">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="7bf0b-115">_lpvContext_</span></span>
  
> <span data-ttu-id="7bf0b-116">[in]MAPI がコールバック関数を呼び出す際にコールバック関数に渡される呼び出し元データへのポインター。</span><span class="sxs-lookup"><span data-stu-id="7bf0b-116">[in] Pointer to caller data passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="7bf0b-117">呼び出し元データは、クライアントまたはプロバイダーにとって重要なアドレスを表すことができます。</span><span class="sxs-lookup"><span data-stu-id="7bf0b-117">The caller data can represent an address of significance to the client or provider.</span></span> <span data-ttu-id="7bf0b-118">通常、C++ コードの場合  _、lpvContext_ パラメーターはオブジェクトのアドレスへのポインターを表します。</span><span class="sxs-lookup"><span data-stu-id="7bf0b-118">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to the address of an object.</span></span> 
    
 <span data-ttu-id="7bf0b-119">_lppAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="7bf0b-119">_lppAdviseSink_</span></span>
  
> <span data-ttu-id="7bf0b-120">[out]アアドバイス シンク オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="7bf0b-120">[out] Pointer to a pointer to an advise sink object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7bf0b-121">Return value</span><span class="sxs-lookup"><span data-stu-id="7bf0b-121">Return value</span></span>

<span data-ttu-id="7bf0b-122">なし。</span><span class="sxs-lookup"><span data-stu-id="7bf0b-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7bf0b-123">注釈</span><span class="sxs-lookup"><span data-stu-id="7bf0b-123">Remarks</span></span>

<span data-ttu-id="7bf0b-124">**HrAllocAdviseSink** 関数を使用するには、クライアント アプリケーションまたはサービス プロバイダーが通知を受け取るオブジェクトを作成し、そのオブジェクトに対応する [NOTIFCALLBACK](notifcallback.md)関数プロトタイプに基づいて通知コールバック関数を作成し **、HrAllocAdviseSink** 関数内のオブジェクトへのポインターを _lpvContext_ 値として渡します。</span><span class="sxs-lookup"><span data-stu-id="7bf0b-124">To use the **HrAllocAdviseSink** function, a client application or service provider creates an object to receive notifications, creates a notification callback function based on the [NOTIFCALLBACK](notifcallback.md) function prototype that goes with that object, and passes a pointer to the object in the **HrAllocAdviseSink** function as the  _lpvContext_ value.</span></span> <span data-ttu-id="7bf0b-125">通知を実行します。通知プロセスの一部として、MAPI はオブジェクト ポインターをコンテキストとしてコールバック関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7bf0b-125">Doing so performs a notification; and as part of the notification process, MAPI calls the callback function with the object pointer as the context.</span></span> 
  
<span data-ttu-id="7bf0b-126">MAPI は、通知エンジンを非同期的に実装します。</span><span class="sxs-lookup"><span data-stu-id="7bf0b-126">MAPI implements its notification engine asynchronously.</span></span> <span data-ttu-id="7bf0b-127">C++ では、通知コールバックにはオブジェクト メソッドを指定できます。</span><span class="sxs-lookup"><span data-stu-id="7bf0b-127">In C++, the notification callback can be an object method.</span></span> <span data-ttu-id="7bf0b-128">通知を生成するオブジェクトが存在しない場合、通知を要求するクライアントまたはプロバイダーは、オブジェクトのアアドバイス シンクに対して、そのオブジェクトの個別の参照カウントを保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0b-128">If the object generating the notification is not present, the client or provider requesting notification must keep a separate reference count for that object for the object's advise sink.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="7bf0b-129">**HrAllocAdviseSink を** 使用する必要があります。クライアントが独自のアドバイス シンクを作成する方が安全です。</span><span class="sxs-lookup"><span data-stu-id="7bf0b-129">**HrAllocAdviseSink** should be used sparingly; it is safer for clients to create their own advise sinks.</span></span> 
  

