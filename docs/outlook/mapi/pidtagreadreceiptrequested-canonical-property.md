---
title: PidTagReadReceiptRequested 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReadReceiptRequested
api_type:
- COM
ms.assetid: 7db0645b-f3ab-4fc4-b865-68c952aeb359
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0e49b73c777988ad3559a442af920af3d8f4bdbb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356470"
---
# <a name="pidtagreadreceiptrequested-canonical-property"></a><span data-ttu-id="35d36-103">PidTagReadReceiptRequested 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="35d36-103">PidTagReadReceiptRequested Canonical Property</span></span>

  
  
<span data-ttu-id="35d36-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35d36-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35d36-105">受信者がメッセージを読み取ったときにメッセージ送信者がメッセージ システムに読み取りレポートを生成する場合は TRUE を含む。</span><span class="sxs-lookup"><span data-stu-id="35d36-105">Contains TRUE if a message sender wants the messaging system to generate a read report when the recipient has read a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="35d36-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="35d36-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="35d36-107">PR_READ_RECEIPT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="35d36-107">PR_READ_RECEIPT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="35d36-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="35d36-108">Identifier:</span></span>  <br/> |<span data-ttu-id="35d36-109">0x0029</span><span class="sxs-lookup"><span data-stu-id="35d36-109">0x0029</span></span>  <br/> |
|<span data-ttu-id="35d36-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="35d36-110">Data type:</span></span>  <br/> |<span data-ttu-id="35d36-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="35d36-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="35d36-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="35d36-112">Area:</span></span>  <br/> |<span data-ttu-id="35d36-113">メール</span><span class="sxs-lookup"><span data-stu-id="35d36-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="35d36-114">注釈</span><span class="sxs-lookup"><span data-stu-id="35d36-114">Remarks</span></span>

<span data-ttu-id="35d36-115">**PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md)) および PR_READ_RECEIPT_SEARCH_KEY ([PidTagReadReceiptSearchKey](pidtagreadreceiptsearchkey-canonical-property.md)) プロパティの値を検証するには、このプロパティを **TRUE** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="35d36-115">This property must be set to TRUE to validate the values in the **PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md)) and **PR_READ_RECEIPT_SEARCH_KEY** ([PidTagReadReceiptSearchKey](pidtagreadreceiptsearchkey-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="35d36-116">メッセージング システムが **読み取りレポートを生成する前** に、PR_READ_RECEIPT_REQUESTEDを含むメッセージが削除または期限切れになった場合は、読み取り以外のレポートが生成されます。</span><span class="sxs-lookup"><span data-stu-id="35d36-116">If a message with **PR_READ_RECEIPT_REQUESTED** set is deleted or expires before the messaging system can generate a read report, a nonread report is generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="35d36-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="35d36-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="35d36-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="35d36-118">Protocol specifications</span></span>

<span data-ttu-id="35d36-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="35d36-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="35d36-120">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="35d36-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="35d36-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="35d36-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="35d36-122">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="35d36-122">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="35d36-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="35d36-123">Header files</span></span>

<span data-ttu-id="35d36-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="35d36-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="35d36-125">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="35d36-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="35d36-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="35d36-126">Mapitags.h</span></span>
  
> <span data-ttu-id="35d36-127">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="35d36-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="35d36-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="35d36-128">See also</span></span>



[<span data-ttu-id="35d36-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="35d36-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="35d36-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="35d36-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="35d36-131">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="35d36-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="35d36-132">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="35d36-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

