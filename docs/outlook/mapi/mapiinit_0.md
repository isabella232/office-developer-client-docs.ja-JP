---
title: MAPIINIT_0
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIINIT_0
api_type:
- COM
ms.assetid: 70739711-ff43-407d-bc8b-6baf7a476fef
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: de31fe7d472b143ed8f3c108dca84a019b5ce103
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357296"
---
# <a name="mapiinit0"></a><span data-ttu-id="6fa48-103">MAPIINIT_0</span><span class="sxs-lookup"><span data-stu-id="6fa48-103">MAPIINIT_0</span></span>

  
  
<span data-ttu-id="6fa48-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6fa48-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6fa48-105">[MAPIInitialize](mapiinitialize.md)関数にオプションを伝えます。</span><span class="sxs-lookup"><span data-stu-id="6fa48-105">Conveys options to the [MAPIInitialize](mapiinitialize.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6fa48-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="6fa48-106">Header file:</span></span>  <br/> |<span data-ttu-id="6fa48-107">mapix。H</span><span class="sxs-lookup"><span data-stu-id="6fa48-107">MAPIX.H</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG ulVersion;
  ULONG ulFlags;
} MAPIINIT_0, FAR *LPMAPIINIT_0;

```

## <a name="members"></a><span data-ttu-id="6fa48-108">Members</span><span class="sxs-lookup"><span data-stu-id="6fa48-108">Members</span></span>

 <span data-ttu-id="6fa48-109">**ulversion**</span><span class="sxs-lookup"><span data-stu-id="6fa48-109">**ulVersion**</span></span>
  
> <span data-ttu-id="6fa48-110">**MAPIINIT_0**構造体のバージョン番号を表す整数値。</span><span class="sxs-lookup"><span data-stu-id="6fa48-110">An integer value that represents the version number of the **MAPIINIT_0** structure.</span></span> <span data-ttu-id="6fa48-111">**ulversion**メンバは将来の拡張のためのものであり、MAPI インターフェイスのバージョンを表すものではありません。</span><span class="sxs-lookup"><span data-stu-id="6fa48-111">The **ulVersion** member is for future expansion and does not represent the version of the MAPI interface.</span></span> <span data-ttu-id="6fa48-112">現時点では、 **ulversion**を MAPI_INIT_VERSION に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6fa48-112">Currently, **ulVersion** must be set to MAPI_INIT_VERSION.</span></span> 
    
 <span data-ttu-id="6fa48-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="6fa48-113">**ulFlags**</span></span>
  
> <span data-ttu-id="6fa48-114">MAPI セッションの初期化を制御するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="6fa48-114">The bitmask of flags used to control the initialization of the MAPI session.</span></span> <span data-ttu-id="6fa48-115">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="6fa48-115">The following flags can be set:</span></span>
    
<span data-ttu-id="6fa48-116">MAPI_MULTITHREAD_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="6fa48-116">MAPI_MULTITHREAD_NOTIFICATIONS</span></span> 
  
> <span data-ttu-id="6fa48-117">MAPI では、 **MAPIInitialize**を呼び出すために使用される最初のスレッドではなく、通知処理専用のスレッドを使用して通知を生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6fa48-117">MAPI should generate notifications using a thread dedicated to notification handling instead of the first thread used to call **MAPIInitialize**.</span></span>
    
<span data-ttu-id="6fa48-118">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="6fa48-118">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="6fa48-119">発信者が Windows サービスとして実行されている。</span><span class="sxs-lookup"><span data-stu-id="6fa48-119">The caller is running as a Windows service.</span></span> <span data-ttu-id="6fa48-120">Windows サービスとして実行されていない発信者は、このフラグを設定してはなりません。サービスとして実行されている発信者は、このフラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6fa48-120">Callers that are not running as a Windows service should not set this flag; callers that are running as a service must set this flag.</span></span>
    
<span data-ttu-id="6fa48-121">MAPI_NO_COINIT</span><span class="sxs-lookup"><span data-stu-id="6fa48-121">MAPI_NO_COINIT</span></span>
  
> <span data-ttu-id="6fa48-122">MAPI_NO_COINT フラグを設定して、 **MAPIInitialize**が[CoInitialize](https://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx)の呼び出しで COM を初期化しないようにします。</span><span class="sxs-lookup"><span data-stu-id="6fa48-122">Set the MAPI_NO_COINT flag so that **MAPIInitialize** does not try to initialize COM with a call to [CoInitialize](https://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx).</span></span> <span data-ttu-id="6fa48-123">_ulflags_が MAPI_NO_COINIT に設定されている場合、 **MAPIINIT_0**構造体が**MAPIInitialize**に渡されると、MAPI は COM が既に初期化されていると見なし、 **CoInitialize**の呼び出しをバイパスします。</span><span class="sxs-lookup"><span data-stu-id="6fa48-123">If a **MAPIINIT_0** structure is passed into **MAPIInitialize** with  _ulFlags_ set to MAPI_NO_COINIT, MAPI will assume that COM has already been initialized and will bypass the call to **CoInitialize**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6fa48-124">解説</span><span class="sxs-lookup"><span data-stu-id="6fa48-124">Remarks</span></span>

<span data-ttu-id="6fa48-125">マルチスレッドクライアントでは、MAPI_MULTITHREAD_NOTIFICATIONS フラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6fa48-125">Multithreaded clients should set the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> <span data-ttu-id="6fa48-126">フラグが設定されていない場合、 **MAPIInitialize**への最初の呼び出しを行うために使用されるスレッドで通知が生成されます。</span><span class="sxs-lookup"><span data-stu-id="6fa48-126">If the flag is not set, notifications are generated on the thread used to make the first call to **MAPIInitialize**.</span></span> 
  
<span data-ttu-id="6fa48-127">このフラグを設定する状況と、クライアントにスレッドセーフを実装する方法の詳細については、「 [MAPI でのスレッド処理](threading-in-mapi.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6fa48-127">For more information about when to set this flag and how to implement thread safety in a client, see [Threading in MAPI](threading-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6fa48-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="6fa48-128">See also</span></span>



[<span data-ttu-id="6fa48-129">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="6fa48-129">MAPIInitialize</span></span>](mapiinitialize.md)


[<span data-ttu-id="6fa48-130">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="6fa48-130">MAPI Structures</span></span>](mapi-structures.md)

