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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 77c724affd2057ca6347d752323c5ba0a3094ecf
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396744"
---
# <a name="pidtagresponserequested-canonical-property"></a><span data-ttu-id="5b7a8-103">PidTagResponseRequested 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5b7a8-103">PidTagResponseRequested Canonical Property</span></span>

  
  
<span data-ttu-id="5b7a8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b7a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b7a8-105">メッセージの送信者は、会議出席依頼への応答を希望する場合は TRUE が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5b7a8-105">Contains TRUE if the message sender wants a response to a meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5b7a8-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5b7a8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5b7a8-107">PR_RESPONSE_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="5b7a8-107">PR_RESPONSE_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="5b7a8-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="5b7a8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5b7a8-109">0x0063</span><span class="sxs-lookup"><span data-stu-id="5b7a8-109">0x0063</span></span>  <br/> |
|<span data-ttu-id="5b7a8-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5b7a8-110">Data type:</span></span>  <br/> |<span data-ttu-id="5b7a8-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5b7a8-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5b7a8-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="5b7a8-112">Area:</span></span>  <br/> |<span data-ttu-id="5b7a8-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="5b7a8-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b7a8-114">備考</span><span class="sxs-lookup"><span data-stu-id="5b7a8-114">Remarks</span></span>

<span data-ttu-id="5b7a8-115">会議出席依頼には、このプロパティが使用されます。</span><span class="sxs-lookup"><span data-stu-id="5b7a8-115">This property is used for meeting requests.</span></span> <span data-ttu-id="5b7a8-116">受信側のクライアント アプリケーションでユーザーが承諾または辞退し、送信者に戻るには、この応答を送信し、メッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="5b7a8-116">The receiving client application should prompt the user to accept or decline the request and then send this response back to the sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5b7a8-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5b7a8-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5b7a8-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5b7a8-118">Protocol specifications</span></span>

<span data-ttu-id="5b7a8-119">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b7a8-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b7a8-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="5b7a8-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5b7a8-121">[[MS OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b7a8-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b7a8-122">プロパティは、電子メール メッセージの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="5b7a8-122">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="5b7a8-123">[[MS OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b7a8-123">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b7a8-124">プロパティ フラグに関連する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="5b7a8-124">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="5b7a8-125">[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b7a8-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b7a8-126">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="5b7a8-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5b7a8-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5b7a8-127">Header files</span></span>

<span data-ttu-id="5b7a8-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5b7a8-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="5b7a8-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5b7a8-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="5b7a8-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5b7a8-130">Mapitags.h</span></span>
  
> <span data-ttu-id="5b7a8-131">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5b7a8-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5b7a8-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="5b7a8-132">See also</span></span>



[<span data-ttu-id="5b7a8-133">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5b7a8-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5b7a8-134">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5b7a8-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5b7a8-135">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5b7a8-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5b7a8-136">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5b7a8-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

