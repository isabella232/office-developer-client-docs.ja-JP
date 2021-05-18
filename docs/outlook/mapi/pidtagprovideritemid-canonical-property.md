---
title: PidTagProviderItemId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderItemId
api_type:
- COM
ms.assetid: fadbf1af-32c2-43ea-8475-15b31b2a9e68
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 48653b86d625da963b655dbd1acc01a46f4687dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412122"
---
# <a name="pidtagprovideritemid-canonical-property"></a><span data-ttu-id="ff6da-103">PidTagProviderItemId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ff6da-103">PidTagProviderItemId Canonical Property</span></span>

  
  
<span data-ttu-id="ff6da-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff6da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff6da-105">フォルダーまたはストア内のアイテムの識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="ff6da-105">Specifies an identifier for a folder or an item in a store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ff6da-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ff6da-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ff6da-107">PR_PROVIDER_ITEMID</span><span class="sxs-lookup"><span data-stu-id="ff6da-107">PR_PROVIDER_ITEMID</span></span>  <br/> |
|<span data-ttu-id="ff6da-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ff6da-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ff6da-109">0x0EA3</span><span class="sxs-lookup"><span data-stu-id="ff6da-109">0x0EA3</span></span>  <br/> |
|<span data-ttu-id="ff6da-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ff6da-110">Data type:</span></span>  <br/> |<span data-ttu-id="ff6da-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ff6da-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ff6da-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="ff6da-112">Area:</span></span>  <br/> |<span data-ttu-id="ff6da-113">MapiNonTransmittable</span><span class="sxs-lookup"><span data-stu-id="ff6da-113">MapiNonTransmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff6da-114">注釈</span><span class="sxs-lookup"><span data-stu-id="ff6da-114">Remarks</span></span>

<span data-ttu-id="ff6da-115">ストア プロバイダーは、フォルダーまたはアイテムに対してこのプロパティの値を指定できますが、セッション間で値を同じに保つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff6da-115">Store providers can specify a value for this property for a folder or an item, but should keep the value the same between sessions.</span></span> <span data-ttu-id="ff6da-116">ストア プロバイダーは、このプロパティを使用して、検索エンジンから返される検索結果を識別します。</span><span class="sxs-lookup"><span data-stu-id="ff6da-116">Store providers use this property to identify search results returned from a search engine.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ff6da-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ff6da-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ff6da-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ff6da-118">Header files</span></span>

<span data-ttu-id="ff6da-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ff6da-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="ff6da-120">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ff6da-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="ff6da-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ff6da-121">Mapitags.h</span></span>
  
> <span data-ttu-id="ff6da-122">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="ff6da-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ff6da-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="ff6da-123">See also</span></span>



[<span data-ttu-id="ff6da-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="ff6da-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ff6da-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ff6da-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ff6da-126">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="ff6da-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ff6da-127">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="ff6da-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

