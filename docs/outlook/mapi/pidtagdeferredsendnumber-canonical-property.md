---
title: PidTagDeferredSendNumber 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendNumber
api_type:
- HeaderDef
ms.assetid: 8ada5c9b-bec5-42d8-bc58-f0411ec4e88b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 30ee7c1a7eb86fd4cdfe90fb6711bd1b295fd5e6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591087"
---
# <a name="pidtagdeferredsendnumber-canonical-property"></a><span data-ttu-id="f741b-103">PidTagDeferredSendNumber 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f741b-103">PidTagDeferredSendNumber Canonical Property</span></span>

  
  
<span data-ttu-id="f741b-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f741b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f741b-105">メッセージの送信の繰延を計算するために使用できる番号が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f741b-105">Contains a number that can be used to compute the deferment of sending a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f741b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f741b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f741b-107">PR_DEFERRED_SEND_NUMBER</span><span class="sxs-lookup"><span data-stu-id="f741b-107">PR_DEFERRED_SEND_NUMBER</span></span>  <br/> |
|<span data-ttu-id="f741b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f741b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f741b-109">0x3FEB</span><span class="sxs-lookup"><span data-stu-id="f741b-109">0x3FEB</span></span>  <br/> |
|<span data-ttu-id="f741b-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f741b-110">Data type:</span></span>  <br/> |<span data-ttu-id="f741b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f741b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f741b-112">領域:</span><span class="sxs-lookup"><span data-stu-id="f741b-112">Area:</span></span>  <br/> |<span data-ttu-id="f741b-113">MAPI のステータス</span><span class="sxs-lookup"><span data-stu-id="f741b-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f741b-114">注釈</span><span class="sxs-lookup"><span data-stu-id="f741b-114">Remarks</span></span>

<span data-ttu-id="f741b-115">このプロパティは、ファイルが存在しない場合は、 **PR_DEFERRED_SEND_TIME** ([PidTagDeferredSendTime](pidtagdeferredsendtime-canonical-property.md)) のプロパティを計算するために使用します。</span><span class="sxs-lookup"><span data-stu-id="f741b-115">This property is used for computing the **PR_DEFERRED_SEND_TIME** ([PidTagDeferredSendTime](pidtagdeferredsendtime-canonical-property.md)) property when it is not present.</span></span> <span data-ttu-id="f741b-116">**PR_DEFERRED_SEND_TIME**プロパティが存在しない場合、メッセージの送信が遅延すると、 **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) のプロパティと**PR_DEFERRED_SEND_NUMBER**プロパティを設定してください。</span><span class="sxs-lookup"><span data-stu-id="f741b-116">When sending a message is deferred, the **PR_DEFERRED_SEND_NUMBER** property should be set along with the **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) property, if the **PR_DEFERRED_SEND_TIME** property is absent.</span></span> 
  
<span data-ttu-id="f741b-117">**PR_DEFERRED_SEND_NUMBER**値は、0 から 999 の間で設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f741b-117">The **PR_DEFERRED_SEND_NUMBER** value must be set between 0 and 999.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f741b-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f741b-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f741b-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f741b-119">Protocol specifications</span></span>

<span data-ttu-id="f741b-120">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f741b-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f741b-121">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="f741b-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f741b-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f741b-122">Header files</span></span>

<span data-ttu-id="f741b-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f741b-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="f741b-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f741b-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="f741b-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f741b-125">Mapitags.h</span></span>
  
> <span data-ttu-id="f741b-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f741b-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f741b-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="f741b-127">See also</span></span>



[<span data-ttu-id="f741b-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f741b-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f741b-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f741b-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f741b-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f741b-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f741b-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f741b-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

