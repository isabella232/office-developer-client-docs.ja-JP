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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: da90347f5aacdb2fcac8547eddd5b89a0a44820d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385824"
---
# <a name="pidtagexpirynumber-canonical-property"></a><span data-ttu-id="2cf64-103">PidTagExpiryNumber 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2cf64-103">PidTagExpiryNumber Canonical Property</span></span>

  
  
<span data-ttu-id="2cf64-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2cf64-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2cf64-105">**PR_EXPIRY_UNITS** ([PidTagExpiryUnits](pidtagexpiryunits-canonical-property.md)) のプロパティと組み合わせて、送信期限を定義します。</span><span class="sxs-lookup"><span data-stu-id="2cf64-105">Defines the expiry send time in conjunction with the **PR_EXPIRY_UNITS** ([PidTagExpiryUnits](pidtagexpiryunits-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2cf64-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2cf64-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2cf64-107">PR_EXPIRY_NUMBER</span><span class="sxs-lookup"><span data-stu-id="2cf64-107">PR_EXPIRY_NUMBER</span></span>  <br/> |
|<span data-ttu-id="2cf64-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="2cf64-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2cf64-109">0x3FED</span><span class="sxs-lookup"><span data-stu-id="2cf64-109">0x3FED</span></span>  <br/> |
|<span data-ttu-id="2cf64-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2cf64-110">Data type:</span></span>  <br/> |<span data-ttu-id="2cf64-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2cf64-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2cf64-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="2cf64-112">Area:</span></span>  <br/> |<span data-ttu-id="2cf64-113">MAPI のステータス</span><span class="sxs-lookup"><span data-stu-id="2cf64-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2cf64-114">備考</span><span class="sxs-lookup"><span data-stu-id="2cf64-114">Remarks</span></span>

<span data-ttu-id="2cf64-115">存在する場合、このプロパティの値は 0 から 999 の範囲の間で設定しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="2cf64-115">This property's value must be set between 0 and 999 inclusive, if it is present.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2cf64-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2cf64-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2cf64-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="2cf64-117">Protocol specifications</span></span>

<span data-ttu-id="2cf64-118">[[MS OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2cf64-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2cf64-119">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="2cf64-119">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2cf64-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="2cf64-120">Header files</span></span>

<span data-ttu-id="2cf64-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2cf64-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="2cf64-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2cf64-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="2cf64-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2cf64-123">Mapitags.h</span></span>
  
> <span data-ttu-id="2cf64-124">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2cf64-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2cf64-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="2cf64-125">See also</span></span>



[<span data-ttu-id="2cf64-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2cf64-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2cf64-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2cf64-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2cf64-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2cf64-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2cf64-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2cf64-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

