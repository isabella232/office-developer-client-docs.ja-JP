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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 48653b86d625da963b655dbd1acc01a46f4687dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286475"
---
# <a name="pidtagprovideritemid-canonical-property"></a><span data-ttu-id="2460f-103">PidTagProviderItemId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2460f-103">PidTagProviderItemId Canonical Property</span></span>

  
  
<span data-ttu-id="2460f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2460f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2460f-105">フォルダーまたはストア内のアイテムの識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="2460f-105">Specifies an identifier for a folder or an item in a store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2460f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2460f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2460f-107">PR_PROVIDER_ITEMID</span><span class="sxs-lookup"><span data-stu-id="2460f-107">PR_PROVIDER_ITEMID</span></span>  <br/> |
|<span data-ttu-id="2460f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="2460f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2460f-109">0x0EA3</span><span class="sxs-lookup"><span data-stu-id="2460f-109">0x0EA3</span></span>  <br/> |
|<span data-ttu-id="2460f-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2460f-110">Data type:</span></span>  <br/> |<span data-ttu-id="2460f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2460f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2460f-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="2460f-112">Area:</span></span>  <br/> |<span data-ttu-id="2460f-113">mapinonたテーブル</span><span class="sxs-lookup"><span data-stu-id="2460f-113">MapiNonTransmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2460f-114">解説</span><span class="sxs-lookup"><span data-stu-id="2460f-114">Remarks</span></span>

<span data-ttu-id="2460f-115">ストアプロバイダーは、フォルダーまたはアイテムに対してこのプロパティの値を指定できますが、セッション間では同じ値を保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2460f-115">Store providers can specify a value for this property for a folder or an item, but should keep the value the same between sessions.</span></span> <span data-ttu-id="2460f-116">ストアプロバイダー検索エンジンから返される検索結果を識別するには、このプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="2460f-116">Store providers use this property to identify search results returned from a search engine.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2460f-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2460f-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2460f-118">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="2460f-118">Header files</span></span>

<span data-ttu-id="2460f-119">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2460f-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="2460f-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2460f-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="2460f-121">Mapitags</span><span class="sxs-lookup"><span data-stu-id="2460f-121">Mapitags.h</span></span>
  
> <span data-ttu-id="2460f-122">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2460f-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2460f-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="2460f-123">See also</span></span>



[<span data-ttu-id="2460f-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="2460f-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2460f-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2460f-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2460f-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2460f-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2460f-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2460f-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

