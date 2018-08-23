---
title: PidTagProviderParentItemId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderParentItemId
api_type:
- COM
ms.assetid: 6adb8e85-ae56-4542-8b19-ed3cfe7fe522
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 96a9d153fadbe8b4c8baa8532b8c99771b1d7987
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803210"
---
# <a name="pidtagproviderparentitemid-canonical-property"></a><span data-ttu-id="11c98-103">PidTagProviderParentItemId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="11c98-103">PidTagProviderParentItemId Canonical Property</span></span>

  
  
<span data-ttu-id="11c98-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="11c98-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="11c98-105">フォルダーまたはストア内のアイテムの親の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="11c98-105">Specifies an identifier for the parent of a folder or an item in a store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="11c98-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="11c98-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="11c98-107">PR_PROVIDER_PARENT_ITEMID</span><span class="sxs-lookup"><span data-stu-id="11c98-107">PR_PROVIDER_PARENT_ITEMID</span></span>  <br/> |
|<span data-ttu-id="11c98-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="11c98-108">Identifier:</span></span>  <br/> |<span data-ttu-id="11c98-109">0x0EA4</span><span class="sxs-lookup"><span data-stu-id="11c98-109">0x0EA4</span></span>  <br/> |
|<span data-ttu-id="11c98-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="11c98-110">Data type:</span></span>  <br/> |<span data-ttu-id="11c98-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="11c98-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="11c98-112">領域:</span><span class="sxs-lookup"><span data-stu-id="11c98-112">Area:</span></span>  <br/> |<span data-ttu-id="11c98-113">MAPI 以外から送信できます。</span><span class="sxs-lookup"><span data-stu-id="11c98-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="11c98-114">注釈</span><span class="sxs-lookup"><span data-stu-id="11c98-114">Remarks</span></span>

<span data-ttu-id="11c98-115">ストア プロバイダーは、フォルダーまたはアイテムの親に対してこのプロパティの値を指定できますが、セッション間で同じように値が保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="11c98-115">Store providers can specify a value for this property for a parent of a folder or an item, but should keep the value the same between sessions.</span></span> <span data-ttu-id="11c98-116">ストア プロバイダーは、検索エンジンから返される検索結果を識別するのには、このプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="11c98-116">Store providers use this property to identify search results returned from a search engine.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="11c98-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="11c98-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="11c98-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="11c98-118">Header files</span></span>

<span data-ttu-id="11c98-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="11c98-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="11c98-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="11c98-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="11c98-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="11c98-121">Mapitags.h</span></span>
  
> <span data-ttu-id="11c98-122">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="11c98-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="11c98-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="11c98-123">See also</span></span>



[<span data-ttu-id="11c98-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="11c98-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="11c98-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="11c98-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="11c98-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="11c98-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="11c98-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="11c98-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

