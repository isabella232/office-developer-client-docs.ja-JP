---
title: PidTagReadReceiptSearchKey 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReadReceiptSearchKey
api_type:
- COM
ms.assetid: a0ea5628-1393-4ab8-bc34-a58cf130db51
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: aa92e224f10fd652078b965c8e3a0b5ab59cc388
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398732"
---
# <a name="pidtagreadreceiptsearchkey-canonical-property"></a><span data-ttu-id="3c218-103">PidTagReadReceiptSearchKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3c218-103">PidTagReadReceiptSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="3c218-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c218-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c218-105">メッセージング システムがメッセージの開封レポートを送信する必要があります、メッセージング ユーザーのための検索キーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="3c218-105">Contains a search key for the messaging user to which the messaging system should direct a read report for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3c218-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="3c218-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3c218-107">PR_READ_RECEIPT_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="3c218-107">PR_READ_RECEIPT_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="3c218-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="3c218-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3c218-109">0x0053</span><span class="sxs-lookup"><span data-stu-id="3c218-109">0x0053</span></span>  <br/> |
|<span data-ttu-id="3c218-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="3c218-110">Data type:</span></span>  <br/> |<span data-ttu-id="3c218-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3c218-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3c218-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="3c218-112">Area:</span></span>  <br/> |<span data-ttu-id="3c218-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="3c218-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3c218-114">備考</span><span class="sxs-lookup"><span data-stu-id="3c218-114">Remarks</span></span>

<span data-ttu-id="3c218-115">**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) プロパティが TRUE に設定されていない限り、このプロパティは無視されます。</span><span class="sxs-lookup"><span data-stu-id="3c218-115">This property is ignored unless the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set to TRUE.</span></span>
  
<span data-ttu-id="3c218-116">クライアント アプリケーションは、受信を希望する場合自体には、レポートを読んで、このプロパティを設定しないままにしたり、メッセージの送信時に、 **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) のプロパティに含まれる検索キーに設定できます。</span><span class="sxs-lookup"><span data-stu-id="3c218-116">If a client application wants to receive read reports itself, it can leave this property unset or set it to the search key contained in the **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) property at message submission time.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3c218-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="3c218-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3c218-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="3c218-118">Protocol specifications</span></span>

<span data-ttu-id="3c218-119">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3c218-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3c218-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="3c218-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3c218-121">[[MS OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3c218-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3c218-122">プロパティは、電子メール メッセージの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="3c218-122">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3c218-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="3c218-123">Header files</span></span>

<span data-ttu-id="3c218-124">Mapidef.h</span><span class="sxs-lookup"><span data-stu-id="3c218-124">Mapidef.h</span></span>
  
> <span data-ttu-id="3c218-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3c218-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="3c218-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3c218-126">Mapitags.h</span></span>
  
> <span data-ttu-id="3c218-127">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3c218-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3c218-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="3c218-128">See also</span></span>



[<span data-ttu-id="3c218-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3c218-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3c218-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3c218-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3c218-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="3c218-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3c218-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="3c218-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

