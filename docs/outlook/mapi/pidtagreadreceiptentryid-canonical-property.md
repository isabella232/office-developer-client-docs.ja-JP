---
title: PidTagReadReceiptEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReadReceiptEntryId
api_type:
- COM
ms.assetid: 141d49c8-87cf-4d80-a33b-ccbf3eeae19e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 662c191f36f9ca30dcdf0f559ea5385bfe5fd305
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356515"
---
# <a name="pidtagreadreceiptentryid-canonical-property"></a><span data-ttu-id="bb531-103">PidTagReadReceiptEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bb531-103">PidTagReadReceiptEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="bb531-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb531-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb531-105">メッセージング システムがこのメッセージの読み取りレポートを指示する必要があるメッセージング ユーザーのエントリ識別子が含まれる。</span><span class="sxs-lookup"><span data-stu-id="bb531-105">Contains an entry identifier for the messaging user where the messaging system should direct a read report for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bb531-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="bb531-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bb531-107">PR_READ_RECEIPT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="bb531-107">PR_READ_RECEIPT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="bb531-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="bb531-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bb531-109">0x0046</span><span class="sxs-lookup"><span data-stu-id="bb531-109">0x0046</span></span>  <br/> |
|<span data-ttu-id="bb531-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="bb531-110">Data type:</span></span>  <br/> |<span data-ttu-id="bb531-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bb531-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bb531-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="bb531-112">Area:</span></span>  <br/> |<span data-ttu-id="bb531-113">MAPI 封筒</span><span class="sxs-lookup"><span data-stu-id="bb531-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb531-114">注釈</span><span class="sxs-lookup"><span data-stu-id="bb531-114">Remarks</span></span>

<span data-ttu-id="bb531-115">このプロパティは **、PR_READ_RECEIPT_REQUESTED** プロパティ ([PidTagReadReceiptRequested ) プロパティ ( PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) が TRUE に設定されていない限り、無視されます。</span><span class="sxs-lookup"><span data-stu-id="bb531-115">This property is ignored unless the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set to TRUE.</span></span>
  
<span data-ttu-id="bb531-116">クライアント アプリケーションが読み取りレポート自体を受信する場合は、このプロパティを設定解除するか、メッセージ送信時に **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) プロパティに含まれるエントリ識別子に設定できます。</span><span class="sxs-lookup"><span data-stu-id="bb531-116">If a client application wants to receive read reports itself, it can leave this property unset or set it to the entry identifier contained in the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property at message submission time.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bb531-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bb531-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bb531-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="bb531-118">Protocol specifications</span></span>

<span data-ttu-id="bb531-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb531-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb531-120">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="bb531-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bb531-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb531-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb531-122">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="bb531-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bb531-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="bb531-123">Header files</span></span>

<span data-ttu-id="bb531-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bb531-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="bb531-125">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bb531-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="bb531-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bb531-126">Mapitags.h</span></span>
  
> <span data-ttu-id="bb531-127">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="bb531-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bb531-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="bb531-128">See also</span></span>



[<span data-ttu-id="bb531-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="bb531-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bb531-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bb531-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bb531-131">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="bb531-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bb531-132">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="bb531-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

