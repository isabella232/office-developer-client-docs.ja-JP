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
ms.openlocfilehash: 9e3a30dad433b255573e4e3f041e6475b9227a54
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398025"
---
# <a name="pidtagdeferredsendnumber-canonical-property"></a><span data-ttu-id="47b0f-103">PidTagDeferredSendNumber 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="47b0f-103">PidTagDeferredSendNumber Canonical Property</span></span>

  
  
<span data-ttu-id="47b0f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47b0f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47b0f-105">メッセージの送信の繰延を計算するために使用できる番号が含まれています。</span><span class="sxs-lookup"><span data-stu-id="47b0f-105">Contains a number that can be used to compute the deferment of sending a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="47b0f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="47b0f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="47b0f-107">PR_DEFERRED_SEND_NUMBER</span><span class="sxs-lookup"><span data-stu-id="47b0f-107">PR_DEFERRED_SEND_NUMBER</span></span>  <br/> |
|<span data-ttu-id="47b0f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="47b0f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="47b0f-109">0x3FEB</span><span class="sxs-lookup"><span data-stu-id="47b0f-109">0x3FEB</span></span>  <br/> |
|<span data-ttu-id="47b0f-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="47b0f-110">Data type:</span></span>  <br/> |<span data-ttu-id="47b0f-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="47b0f-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="47b0f-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="47b0f-112">Area:</span></span>  <br/> |<span data-ttu-id="47b0f-113">MAPI のステータス</span><span class="sxs-lookup"><span data-stu-id="47b0f-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="47b0f-114">備考</span><span class="sxs-lookup"><span data-stu-id="47b0f-114">Remarks</span></span>

<span data-ttu-id="47b0f-115">このプロパティは、ファイルが存在しない場合は、 **PR_DEFERRED_SEND_TIME** ([PidTagDeferredSendTime](pidtagdeferredsendtime-canonical-property.md)) のプロパティを計算するために使用します。</span><span class="sxs-lookup"><span data-stu-id="47b0f-115">This property is used for computing the **PR_DEFERRED_SEND_TIME** ([PidTagDeferredSendTime](pidtagdeferredsendtime-canonical-property.md)) property when it is not present.</span></span> <span data-ttu-id="47b0f-116">**PR_DEFERRED_SEND_TIME**プロパティが存在しない場合、メッセージの送信が遅延すると、 **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) のプロパティと**PR_DEFERRED_SEND_NUMBER**プロパティを設定してください。</span><span class="sxs-lookup"><span data-stu-id="47b0f-116">When sending a message is deferred, the **PR_DEFERRED_SEND_NUMBER** property should be set along with the **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) property, if the **PR_DEFERRED_SEND_TIME** property is absent.</span></span> 
  
<span data-ttu-id="47b0f-117">**PR_DEFERRED_SEND_NUMBER**値は、0 から 999 の間で設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="47b0f-117">The **PR_DEFERRED_SEND_NUMBER** value must be set between 0 and 999.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="47b0f-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="47b0f-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="47b0f-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="47b0f-119">Protocol specifications</span></span>

<span data-ttu-id="47b0f-120">[[MS OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47b0f-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47b0f-121">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="47b0f-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="47b0f-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="47b0f-122">Header files</span></span>

<span data-ttu-id="47b0f-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="47b0f-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="47b0f-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="47b0f-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="47b0f-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="47b0f-125">Mapitags.h</span></span>
  
> <span data-ttu-id="47b0f-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="47b0f-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="47b0f-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="47b0f-127">See also</span></span>



[<span data-ttu-id="47b0f-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="47b0f-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="47b0f-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="47b0f-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="47b0f-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="47b0f-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="47b0f-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="47b0f-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

