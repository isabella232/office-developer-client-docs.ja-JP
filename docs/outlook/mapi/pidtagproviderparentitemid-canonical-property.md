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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0f99cf38e65c75ce1ba74bf72d88e19f4fbfa03a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433417"
---
# <a name="pidtagproviderparentitemid-canonical-property"></a><span data-ttu-id="8fc50-103">PidTagProviderParentItemId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8fc50-103">PidTagProviderParentItemId Canonical Property</span></span>

  
  
<span data-ttu-id="8fc50-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8fc50-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8fc50-105">フォルダーの親またはストア内のアイテムの識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="8fc50-105">Specifies an identifier for the parent of a folder or an item in a store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8fc50-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8fc50-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8fc50-107">PR_PROVIDER_PARENT_ITEMID</span><span class="sxs-lookup"><span data-stu-id="8fc50-107">PR_PROVIDER_PARENT_ITEMID</span></span>  <br/> |
|<span data-ttu-id="8fc50-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8fc50-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8fc50-109">0x0EA4</span><span class="sxs-lookup"><span data-stu-id="8fc50-109">0x0EA4</span></span>  <br/> |
|<span data-ttu-id="8fc50-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8fc50-110">Data type:</span></span>  <br/> |<span data-ttu-id="8fc50-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8fc50-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8fc50-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="8fc50-112">Area:</span></span>  <br/> |<span data-ttu-id="8fc50-113">MAPI 送信不可</span><span class="sxs-lookup"><span data-stu-id="8fc50-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8fc50-114">注釈</span><span class="sxs-lookup"><span data-stu-id="8fc50-114">Remarks</span></span>

<span data-ttu-id="8fc50-115">ストア プロバイダーは、フォルダーまたはアイテムの親に対してこのプロパティの値を指定できますが、セッション間で値を同じに保つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="8fc50-115">Store providers can specify a value for this property for a parent of a folder or an item, but should keep the value the same between sessions.</span></span> <span data-ttu-id="8fc50-116">ストア プロバイダーは、このプロパティを使用して、検索エンジンから返される検索結果を識別します。</span><span class="sxs-lookup"><span data-stu-id="8fc50-116">Store providers use this property to identify search results returned from a search engine.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8fc50-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8fc50-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8fc50-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8fc50-118">Header files</span></span>

<span data-ttu-id="8fc50-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8fc50-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="8fc50-120">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8fc50-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="8fc50-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8fc50-121">Mapitags.h</span></span>
  
> <span data-ttu-id="8fc50-122">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="8fc50-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8fc50-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="8fc50-123">See also</span></span>



[<span data-ttu-id="8fc50-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="8fc50-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8fc50-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8fc50-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8fc50-126">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="8fc50-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8fc50-127">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="8fc50-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

