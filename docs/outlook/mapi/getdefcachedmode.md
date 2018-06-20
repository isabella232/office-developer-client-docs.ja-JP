---
title: GetDefCachedMode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 325b6b47-b6a6-503e-e9bb-65ef7b73d659
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 7595fac4346a537eed86550432f56a761c27c0ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800190"
---
# <a name="getdefcachedmode"></a><span data-ttu-id="b79f5-103">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="b79f5-103">GetDefCachedMode</span></span>

  
  
<span data-ttu-id="b79f5-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b79f5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b79f5-105">プライベートの Exchange ストアの Exchange キャッシュ モードが有効になっているかどうか、ポリシーによって適用されるには、これかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b79f5-105">Indicates whether Cached Exchange Mode for the private Exchange store is enabled, and whether this is enforced by policy.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b79f5-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="b79f5-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b79f5-107">によってエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="b79f5-107">Exported by:</span></span>  <br/> |<span data-ttu-id="b79f5-108">msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="b79f5-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="b79f5-109">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b79f5-109">Called by:</span></span>  <br/> |<span data-ttu-id="b79f5-110">クライアント</span><span class="sxs-lookup"><span data-stu-id="b79f5-110">Client</span></span>  <br/> |
|<span data-ttu-id="b79f5-111">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="b79f5-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="b79f5-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="b79f5-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="b79f5-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="b79f5-113">Parameters</span></span>

 <span data-ttu-id="b79f5-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="b79f5-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="b79f5-115">[out]**true**でない場合、ポリシーでは、 **false を指定**して、戻り値が設定されている場合です。</span><span class="sxs-lookup"><span data-stu-id="b79f5-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="b79f5-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="b79f5-116">Return values</span></span>

 <span data-ttu-id="b79f5-117">**true**</span><span class="sxs-lookup"><span data-stu-id="b79f5-117">**true**</span></span>
  
- <span data-ttu-id="b79f5-118">キャッシュを有効にします。</span><span class="sxs-lookup"><span data-stu-id="b79f5-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="b79f5-119">**false**</span><span class="sxs-lookup"><span data-stu-id="b79f5-119">**false**</span></span>
  
- <span data-ttu-id="b79f5-120">キャッシュを無効にします。</span><span class="sxs-lookup"><span data-stu-id="b79f5-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b79f5-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="b79f5-121">See also</span></span>



[<span data-ttu-id="b79f5-122">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="b79f5-122">GetDefCachedModeDownloadPubFoldFavs</span></span>](getdefcachedmodedownloadpubfoldfavs.md)

