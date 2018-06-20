---
title: GetDefCachedModeDownloadPubFoldFavs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dd95561-ed8f-8a3b-6532-b53556f16666
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: cb93d9ae4e6660c208d74e43bb26be4dbd55f4e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800189"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a><span data-ttu-id="3c4ec-103">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="3c4ec-103">GetDefCachedModeDownloadPubFoldFavs</span></span>

  
  
<span data-ttu-id="3c4ec-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3c4ec-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3c4ec-105">**パブリック フォルダーのお気に入り**フォルダーの Exchange キャッシュ モードが有効になっているかどうか、ポリシーによって適用されるには、これかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="3c4ec-105">Indicates whether Cached Exchange Mode for the **Public Folder Favorites** folder is enabled, and whether this is enforced by policy.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="3c4ec-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="3c4ec-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c4ec-107">によってエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="3c4ec-107">Exported by:</span></span>  <br/> |<span data-ttu-id="3c4ec-108">msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="3c4ec-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="3c4ec-109">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3c4ec-109">Called by:</span></span>  <br/> |<span data-ttu-id="3c4ec-110">クライアント</span><span class="sxs-lookup"><span data-stu-id="3c4ec-110">Client</span></span>  <br/> |
|<span data-ttu-id="3c4ec-111">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="3c4ec-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="3c4ec-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="3c4ec-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="3c4ec-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="3c4ec-113">Parameters</span></span>

 <span data-ttu-id="3c4ec-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="3c4ec-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="3c4ec-115">[out]**true**でない場合、ポリシーでは、 **false を指定**して、戻り値が設定されている場合です。</span><span class="sxs-lookup"><span data-stu-id="3c4ec-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="3c4ec-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="3c4ec-116">Return values</span></span>

 <span data-ttu-id="3c4ec-117">**true**</span><span class="sxs-lookup"><span data-stu-id="3c4ec-117">**true**</span></span>
  
- <span data-ttu-id="3c4ec-118">キャッシュを有効にします。</span><span class="sxs-lookup"><span data-stu-id="3c4ec-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="3c4ec-119">**false**</span><span class="sxs-lookup"><span data-stu-id="3c4ec-119">**false**</span></span>
  
- <span data-ttu-id="3c4ec-120">キャッシュを無効にします。</span><span class="sxs-lookup"><span data-stu-id="3c4ec-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3c4ec-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="3c4ec-121">See also</span></span>



[<span data-ttu-id="3c4ec-122">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="3c4ec-122">GetDefCachedMode</span></span>](getdefcachedmode.md)

