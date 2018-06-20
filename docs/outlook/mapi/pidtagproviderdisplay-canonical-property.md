---
title: PidTagProviderDisplay の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1546ee1aa970be71d853dba59ce0fab7cc5a4dac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803207"
---
# <a name="pidtagproviderdisplay-canonical-property"></a><span data-ttu-id="3ec90-103">PidTagProviderDisplay の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="3ec90-103">PidTagProviderDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="3ec90-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3ec90-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3ec90-105">サービス プロバイダーのベンダー定義の表示名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3ec90-105">Contains the vendor-defined display name for a service provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3ec90-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="3ec90-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3ec90-107">PR_PROVIDER_DISPLAY、PR_PROVIDER_DISPLAY_A、PR_PROVIDER_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="3ec90-107">PR_PROVIDER_DISPLAY, PR_PROVIDER_DISPLAY_A, PR_PROVIDER_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="3ec90-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="3ec90-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3ec90-109">0x3006</span><span class="sxs-lookup"><span data-stu-id="3ec90-109">0x3006</span></span>  <br/> |
|<span data-ttu-id="3ec90-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="3ec90-110">Data type:</span></span>  <br/> |<span data-ttu-id="3ec90-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3ec90-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3ec90-112">領域:</span><span class="sxs-lookup"><span data-stu-id="3ec90-112">Area:</span></span>  <br/> |<span data-ttu-id="3ec90-113">一般的な MAPI</span><span class="sxs-lookup"><span data-stu-id="3ec90-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3ec90-114">備考</span><span class="sxs-lookup"><span data-stu-id="3ec90-114">Remarks</span></span>

<span data-ttu-id="3ec90-115">これらのプロパティと**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) は、サービス プロバイダーに属するプロファイル セクションでのみ定義されます。</span><span class="sxs-lookup"><span data-stu-id="3ec90-115">These properties and **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) are defined only on profile sections belonging to service providers.</span></span> <span data-ttu-id="3ec90-116">MAPISVC.INF に存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ec90-116">They must be present in MAPISVC.INF.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3ec90-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="3ec90-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="3ec90-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="3ec90-118">Header files</span></span>

<span data-ttu-id="3ec90-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3ec90-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="3ec90-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3ec90-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="3ec90-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3ec90-121">Mapitags.h</span></span>
  
> <span data-ttu-id="3ec90-122">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3ec90-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3ec90-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="3ec90-123">See also</span></span>



[<span data-ttu-id="3ec90-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3ec90-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3ec90-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3ec90-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3ec90-126">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="3ec90-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3ec90-127">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="3ec90-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

