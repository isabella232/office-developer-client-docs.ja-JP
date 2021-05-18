---
title: PidTagResponseRequested 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResponseRequested
api_type:
- COM
ms.assetid: e52bb48c-7107-4ac4-b030-885409759ee7
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 77c724affd2057ca6347d752323c5ba0a3094ecf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330157"
---
# <a name="pidtagresponserequested-canonical-property"></a><span data-ttu-id="1745b-103">PidTagResponseRequested 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1745b-103">PidTagResponseRequested Canonical Property</span></span>

  
  
<span data-ttu-id="1745b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1745b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1745b-105">メッセージ送信者が会議出席依頼への応答を望む場合は TRUE を含む。</span><span class="sxs-lookup"><span data-stu-id="1745b-105">Contains TRUE if the message sender wants a response to a meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1745b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1745b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1745b-107">PR_RESPONSE_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="1745b-107">PR_RESPONSE_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="1745b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1745b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1745b-109">0x0063</span><span class="sxs-lookup"><span data-stu-id="1745b-109">0x0063</span></span>  <br/> |
|<span data-ttu-id="1745b-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1745b-110">Data type:</span></span>  <br/> |<span data-ttu-id="1745b-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="1745b-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="1745b-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="1745b-112">Area:</span></span>  <br/> |<span data-ttu-id="1745b-113">MAPI 封筒</span><span class="sxs-lookup"><span data-stu-id="1745b-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1745b-114">注釈</span><span class="sxs-lookup"><span data-stu-id="1745b-114">Remarks</span></span>

<span data-ttu-id="1745b-115">このプロパティは、会議出席依頼に使用されます。</span><span class="sxs-lookup"><span data-stu-id="1745b-115">This property is used for meeting requests.</span></span> <span data-ttu-id="1745b-116">受信側のクライアント アプリケーションは、ユーザーに要求の承諾または拒否を求めるメッセージを表示し、この応答を送信者に返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="1745b-116">The receiving client application should prompt the user to accept or decline the request and then send this response back to the sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1745b-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1745b-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1745b-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1745b-118">Protocol specifications</span></span>

<span data-ttu-id="1745b-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1745b-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1745b-120">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="1745b-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1745b-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1745b-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1745b-122">電子メール メッセージで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="1745b-122">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="1745b-123">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1745b-123">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1745b-124">フラグに関連するプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="1745b-124">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="1745b-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1745b-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1745b-126">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="1745b-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1745b-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="1745b-127">Header files</span></span>

<span data-ttu-id="1745b-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1745b-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="1745b-129">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1745b-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="1745b-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1745b-130">Mapitags.h</span></span>
  
> <span data-ttu-id="1745b-131">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="1745b-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1745b-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="1745b-132">See also</span></span>



[<span data-ttu-id="1745b-133">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="1745b-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1745b-134">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1745b-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1745b-135">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="1745b-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1745b-136">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="1745b-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

