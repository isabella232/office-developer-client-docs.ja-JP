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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: de31fe7d472b143ed8f3c108dca84a019b5ce103
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357296"
---
# <a name="mapiinit_0"></a><span data-ttu-id="b1456-103">MAPIINIT_0</span><span class="sxs-lookup"><span data-stu-id="b1456-103">MAPIINIT_0</span></span>

  
  
<span data-ttu-id="b1456-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1456-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1456-105">[MAPIInitialize 関数にオプションを伝達](mapiinitialize.md)します。</span><span class="sxs-lookup"><span data-stu-id="b1456-105">Conveys options to the [MAPIInitialize](mapiinitialize.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b1456-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="b1456-106">Header file:</span></span>  <br/> |<span data-ttu-id="b1456-107">MAPIX。H</span><span class="sxs-lookup"><span data-stu-id="b1456-107">MAPIX.H</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG ulVersion;
  ULONG ulFlags;
} MAPIINIT_0, FAR *LPMAPIINIT_0;

```

## <a name="members"></a><span data-ttu-id="b1456-108">Members</span><span class="sxs-lookup"><span data-stu-id="b1456-108">Members</span></span>

 <span data-ttu-id="b1456-109">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="b1456-109">**ulVersion**</span></span>
  
> <span data-ttu-id="b1456-110">指定した構造体のバージョン番号を表す **MAPIINIT_0** 値。</span><span class="sxs-lookup"><span data-stu-id="b1456-110">An integer value that represents the version number of the **MAPIINIT_0** structure.</span></span> <span data-ttu-id="b1456-111">**ulVersion メンバー** は将来の拡張用であり、MAPI インターフェイスのバージョンを表すのではありません。</span><span class="sxs-lookup"><span data-stu-id="b1456-111">The **ulVersion** member is for future expansion and does not represent the version of the MAPI interface.</span></span> <span data-ttu-id="b1456-112">現時点では **、ulVersion** を設定する必要MAPI_INIT_VERSION。</span><span class="sxs-lookup"><span data-stu-id="b1456-112">Currently, **ulVersion** must be set to MAPI_INIT_VERSION.</span></span> 
    
 <span data-ttu-id="b1456-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="b1456-113">**ulFlags**</span></span>
  
> <span data-ttu-id="b1456-114">MAPI セッションの初期化を制御するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="b1456-114">The bitmask of flags used to control the initialization of the MAPI session.</span></span> <span data-ttu-id="b1456-115">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="b1456-115">The following flags can be set:</span></span>
    
<span data-ttu-id="b1456-116">MAPI_MULTITHREAD_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="b1456-116">MAPI_MULTITHREAD_NOTIFICATIONS</span></span> 
  
> <span data-ttu-id="b1456-117">MAPI は、MAPIInitialize を呼び出す最初のスレッドではなく、通知処理専用のスレッドを使用して通知 **を生成する必要があります**。</span><span class="sxs-lookup"><span data-stu-id="b1456-117">MAPI should generate notifications using a thread dedicated to notification handling instead of the first thread used to call **MAPIInitialize**.</span></span>
    
<span data-ttu-id="b1456-118">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="b1456-118">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="b1456-119">呼び出し元は、Windowsサービスとして実行されています。</span><span class="sxs-lookup"><span data-stu-id="b1456-119">The caller is running as a Windows service.</span></span> <span data-ttu-id="b1456-120">サービスとして実行されていない呼び出し元Windowsこのフラグを設定する必要があります。サービスとして実行されている呼び出し元は、このフラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1456-120">Callers that are not running as a Windows service should not set this flag; callers that are running as a service must set this flag.</span></span>
    
<span data-ttu-id="b1456-121">MAPI_NO_COINIT</span><span class="sxs-lookup"><span data-stu-id="b1456-121">MAPI_NO_COINIT</span></span>
  
> <span data-ttu-id="b1456-122">**MAPIInitialize** MAPI_NO_COINT呼び出しで COM を初期化しようとしないので、このフラグを [設定します](https://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="b1456-122">Set the MAPI_NO_COINT flag so that **MAPIInitialize** does not try to initialize COM with a call to [CoInitialize](https://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx).</span></span> <span data-ttu-id="b1456-123">MAPIINIT_0 構造体 **が** **mapiInitialize** に渡され  _、ulFlags_ が MAPI_NO_COINIT に設定されている場合、MAPI は COM が既に初期化済みであり **、CoInitialize** への呼び出しをバイパスすると想定します。</span><span class="sxs-lookup"><span data-stu-id="b1456-123">If a **MAPIINIT_0** structure is passed into **MAPIInitialize** with  _ulFlags_ set to MAPI_NO_COINIT, MAPI will assume that COM has already been initialized and will bypass the call to **CoInitialize**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b1456-124">注釈</span><span class="sxs-lookup"><span data-stu-id="b1456-124">Remarks</span></span>

<span data-ttu-id="b1456-125">マルチスレッド クライアントは、このフラグを設定MAPI_MULTITHREAD_NOTIFICATIONS必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1456-125">Multithreaded clients should set the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> <span data-ttu-id="b1456-126">フラグが設定されていない場合 **、MAPIInitialize** の最初の呼び出しに使用されるスレッドで通知が生成されます。</span><span class="sxs-lookup"><span data-stu-id="b1456-126">If the flag is not set, notifications are generated on the thread used to make the first call to **MAPIInitialize**.</span></span> 
  
<span data-ttu-id="b1456-127">このフラグを設定する場合と、クライアントでスレッドセーフを実装する方法の詳細については、「MAPI でのスレッド処理 [」を参照してください](threading-in-mapi.md)。</span><span class="sxs-lookup"><span data-stu-id="b1456-127">For more information about when to set this flag and how to implement thread safety in a client, see [Threading in MAPI](threading-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b1456-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="b1456-128">See also</span></span>



[<span data-ttu-id="b1456-129">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="b1456-129">MAPIInitialize</span></span>](mapiinitialize.md)


[<span data-ttu-id="b1456-130">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="b1456-130">MAPI Structures</span></span>](mapi-structures.md)

