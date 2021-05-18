---
title: PidTagProviderDisplay 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderDisplay
api_type:
- COM
ms.assetid: 62e96db8-4c3e-4f73-b695-99eb4b2396fd
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 58db944720817491420f2bcb1774e51e3842b4a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421593"
---
# <a name="pidtagproviderdisplay-canonical-property"></a><span data-ttu-id="634f3-103">PidTagProviderDisplay 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="634f3-103">PidTagProviderDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="634f3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="634f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="634f3-105">サービス プロバイダーのベンダー定義の表示名を含む。</span><span class="sxs-lookup"><span data-stu-id="634f3-105">Contains the vendor-defined display name for a service provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="634f3-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="634f3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="634f3-107">PR_PROVIDER_DISPLAY、PR_PROVIDER_DISPLAY_A、PR_PROVIDER_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="634f3-107">PR_PROVIDER_DISPLAY, PR_PROVIDER_DISPLAY_A, PR_PROVIDER_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="634f3-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="634f3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="634f3-109">0x3006</span><span class="sxs-lookup"><span data-stu-id="634f3-109">0x3006</span></span>  <br/> |
|<span data-ttu-id="634f3-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="634f3-110">Data type:</span></span>  <br/> |<span data-ttu-id="634f3-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="634f3-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="634f3-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="634f3-112">Area:</span></span>  <br/> |<span data-ttu-id="634f3-113">MAPI 共通</span><span class="sxs-lookup"><span data-stu-id="634f3-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="634f3-114">注釈</span><span class="sxs-lookup"><span data-stu-id="634f3-114">Remarks</span></span>

<span data-ttu-id="634f3-115">これらのプロパティと **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) は、サービス プロバイダーに属するプロファイル セクションでのみ定義されます。</span><span class="sxs-lookup"><span data-stu-id="634f3-115">These properties and **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) are defined only on profile sections belonging to service providers.</span></span> <span data-ttu-id="634f3-116">MAPISVC.INF に存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="634f3-116">They must be present in MAPISVC.INF.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="634f3-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="634f3-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="634f3-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="634f3-118">Header files</span></span>

<span data-ttu-id="634f3-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="634f3-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="634f3-120">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="634f3-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="634f3-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="634f3-121">Mapitags.h</span></span>
  
> <span data-ttu-id="634f3-122">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="634f3-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="634f3-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="634f3-123">See also</span></span>



[<span data-ttu-id="634f3-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="634f3-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="634f3-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="634f3-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="634f3-126">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="634f3-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="634f3-127">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="634f3-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

