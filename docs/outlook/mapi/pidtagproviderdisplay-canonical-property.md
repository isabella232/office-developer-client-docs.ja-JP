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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9a37382cda1a96025f950d941f83fb5b6a0497bb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565502"
---
# <a name="pidtagproviderdisplay-canonical-property"></a><span data-ttu-id="b37bd-103">PidTagProviderDisplay 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b37bd-103">PidTagProviderDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="b37bd-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b37bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b37bd-105">サービス プロバイダーのベンダー定義の表示名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b37bd-105">Contains the vendor-defined display name for a service provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b37bd-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b37bd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b37bd-107">PR_PROVIDER_DISPLAY、PR_PROVIDER_DISPLAY_A、PR_PROVIDER_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="b37bd-107">PR_PROVIDER_DISPLAY, PR_PROVIDER_DISPLAY_A, PR_PROVIDER_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="b37bd-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b37bd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b37bd-109">0x3006</span><span class="sxs-lookup"><span data-stu-id="b37bd-109">0x3006</span></span>  <br/> |
|<span data-ttu-id="b37bd-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b37bd-110">Data type:</span></span>  <br/> |<span data-ttu-id="b37bd-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b37bd-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b37bd-112">領域:</span><span class="sxs-lookup"><span data-stu-id="b37bd-112">Area:</span></span>  <br/> |<span data-ttu-id="b37bd-113">一般的な MAPI</span><span class="sxs-lookup"><span data-stu-id="b37bd-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b37bd-114">注釈</span><span class="sxs-lookup"><span data-stu-id="b37bd-114">Remarks</span></span>

<span data-ttu-id="b37bd-115">これらのプロパティと**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) は、サービス プロバイダーに属するプロファイル セクションでのみ定義されます。</span><span class="sxs-lookup"><span data-stu-id="b37bd-115">These properties and **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) are defined only on profile sections belonging to service providers.</span></span> <span data-ttu-id="b37bd-116">MAPISVC.INF に存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b37bd-116">They must be present in MAPISVC.INF.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b37bd-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b37bd-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b37bd-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b37bd-118">Header files</span></span>

<span data-ttu-id="b37bd-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b37bd-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="b37bd-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b37bd-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="b37bd-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b37bd-121">Mapitags.h</span></span>
  
> <span data-ttu-id="b37bd-122">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b37bd-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b37bd-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="b37bd-123">See also</span></span>



[<span data-ttu-id="b37bd-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b37bd-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b37bd-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b37bd-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b37bd-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b37bd-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b37bd-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b37bd-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

