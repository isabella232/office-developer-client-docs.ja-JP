---
title: PidTagExpiryNumber 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExpiryNumber
api_type:
- HeaderDef
ms.assetid: 644e8d3d-1792-4417-95a1-e978d0e6cd8e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: da90347f5aacdb2fcac8547eddd5b89a0a44820d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316367"
---
# <a name="pidtagexpirynumber-canonical-property"></a><span data-ttu-id="a17d9-103">PidTagExpiryNumber 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a17d9-103">PidTagExpiryNumber Canonical Property</span></span>

  
  
<span data-ttu-id="a17d9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a17d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a17d9-105">有効期限の送信時間を、PR_EXPIRY_UNITS **(** [PidTagExpiryUnits](pidtagexpiryunits-canonical-property.md)) プロパティと組み合わせて定義します。</span><span class="sxs-lookup"><span data-stu-id="a17d9-105">Defines the expiry send time in conjunction with the **PR_EXPIRY_UNITS** ([PidTagExpiryUnits](pidtagexpiryunits-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a17d9-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a17d9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a17d9-107">PR_EXPIRY_NUMBER</span><span class="sxs-lookup"><span data-stu-id="a17d9-107">PR_EXPIRY_NUMBER</span></span>  <br/> |
|<span data-ttu-id="a17d9-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a17d9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a17d9-109">0x3FED</span><span class="sxs-lookup"><span data-stu-id="a17d9-109">0x3FED</span></span>  <br/> |
|<span data-ttu-id="a17d9-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a17d9-110">Data type:</span></span>  <br/> |<span data-ttu-id="a17d9-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a17d9-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a17d9-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="a17d9-112">Area:</span></span>  <br/> |<span data-ttu-id="a17d9-113">MAPI の状態</span><span class="sxs-lookup"><span data-stu-id="a17d9-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a17d9-114">注釈</span><span class="sxs-lookup"><span data-stu-id="a17d9-114">Remarks</span></span>

<span data-ttu-id="a17d9-115">このプロパティの値が存在する場合は、0 ~ 999 を含む値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a17d9-115">This property's value must be set between 0 and 999 inclusive, if it is present.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a17d9-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a17d9-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a17d9-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a17d9-117">Protocol specifications</span></span>

<span data-ttu-id="a17d9-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a17d9-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a17d9-119">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="a17d9-119">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a17d9-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="a17d9-120">Header files</span></span>

<span data-ttu-id="a17d9-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a17d9-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="a17d9-122">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a17d9-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="a17d9-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a17d9-123">Mapitags.h</span></span>
  
> <span data-ttu-id="a17d9-124">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="a17d9-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a17d9-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="a17d9-125">See also</span></span>



[<span data-ttu-id="a17d9-126">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a17d9-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a17d9-127">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a17d9-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a17d9-128">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="a17d9-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a17d9-129">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="a17d9-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

