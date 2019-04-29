---
title: GetDefCachedMode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 325b6b47-b6a6-503e-e9bb-65ef7b73d659
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8e8a6ac07e14af52337b6e280fa58274df453c65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412745"
---
# <a name="getdefcachedmode"></a><span data-ttu-id="dfb78-103">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="dfb78-103">GetDefCachedMode</span></span>

  
  
<span data-ttu-id="dfb78-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dfb78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dfb78-105">プライベート exchange ストアの exchange キャッシュモードを有効にするかどうか、およびポリシーによってこれを強制するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="dfb78-105">Indicates whether Cached Exchange Mode for the private Exchange store is enabled, and whether this is enforced by policy.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="dfb78-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="dfb78-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dfb78-107">エクスポート対象:</span><span class="sxs-lookup"><span data-stu-id="dfb78-107">Exported by:</span></span>  <br/> |<span data-ttu-id="dfb78-108">msmapi32</span><span class="sxs-lookup"><span data-stu-id="dfb78-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="dfb78-109">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="dfb78-109">Called by:</span></span>  <br/> |<span data-ttu-id="dfb78-110">クライアント</span><span class="sxs-lookup"><span data-stu-id="dfb78-110">Client</span></span>  <br/> |
|<span data-ttu-id="dfb78-111">実装元:</span><span class="sxs-lookup"><span data-stu-id="dfb78-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="dfb78-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="dfb78-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="dfb78-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="dfb78-113">Parameters</span></span>

 <span data-ttu-id="dfb78-114">_pfpolicy_</span><span class="sxs-lookup"><span data-stu-id="dfb78-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="dfb78-115">読み上げ戻り値がポリシーによって適用される場合は**true** 、それ以外の場合は**false** 。</span><span class="sxs-lookup"><span data-stu-id="dfb78-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="dfb78-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="dfb78-116">Return values</span></span>

 <span data-ttu-id="dfb78-117">**false**</span><span class="sxs-lookup"><span data-stu-id="dfb78-117">**true**</span></span>
  
- <span data-ttu-id="dfb78-118">キャッシュが有効になります。</span><span class="sxs-lookup"><span data-stu-id="dfb78-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="dfb78-119">**false**</span><span class="sxs-lookup"><span data-stu-id="dfb78-119">**false**</span></span>
  
- <span data-ttu-id="dfb78-120">キャッシュが無効になります。</span><span class="sxs-lookup"><span data-stu-id="dfb78-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dfb78-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="dfb78-121">See also</span></span>



[<span data-ttu-id="dfb78-122">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="dfb78-122">GetDefCachedModeDownloadPubFoldFavs</span></span>](getdefcachedmodedownloadpubfoldfavs.md)

