---
title: GetDefCachedMode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 325b6b47-b6a6-503e-e9bb-65ef7b73d659
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 91a56acf4afc7453496fa89becd905184101c910
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591395"
---
# <a name="getdefcachedmode"></a><span data-ttu-id="0420a-103">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="0420a-103">GetDefCachedMode</span></span>

  
  
<span data-ttu-id="0420a-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0420a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0420a-105">プライベートの Exchange ストアの Exchange キャッシュ モードが有効になっているかどうか、ポリシーによって適用されるには、これかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="0420a-105">Indicates whether Cached Exchange Mode for the private Exchange store is enabled, and whether this is enforced by policy.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="0420a-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="0420a-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0420a-107">によってエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="0420a-107">Exported by:</span></span>  <br/> |<span data-ttu-id="0420a-108">msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="0420a-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="0420a-109">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="0420a-109">Called by:</span></span>  <br/> |<span data-ttu-id="0420a-110">クライアント</span><span class="sxs-lookup"><span data-stu-id="0420a-110">Client</span></span>  <br/> |
|<span data-ttu-id="0420a-111">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="0420a-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="0420a-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="0420a-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="0420a-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0420a-113">Parameters</span></span>

 <span data-ttu-id="0420a-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="0420a-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="0420a-115">[out]**true**でない場合、ポリシーでは、 **false を指定**して、戻り値が設定されている場合です。</span><span class="sxs-lookup"><span data-stu-id="0420a-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="0420a-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="0420a-116">Return values</span></span>

 <span data-ttu-id="0420a-117">**true**</span><span class="sxs-lookup"><span data-stu-id="0420a-117">**true**</span></span>
  
- <span data-ttu-id="0420a-118">キャッシュを有効にします。</span><span class="sxs-lookup"><span data-stu-id="0420a-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="0420a-119">**false**</span><span class="sxs-lookup"><span data-stu-id="0420a-119">**false**</span></span>
  
- <span data-ttu-id="0420a-120">キャッシュを無効にします。</span><span class="sxs-lookup"><span data-stu-id="0420a-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0420a-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="0420a-121">See also</span></span>



[<span data-ttu-id="0420a-122">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="0420a-122">GetDefCachedModeDownloadPubFoldFavs</span></span>](getdefcachedmodedownloadpubfoldfavs.md)

