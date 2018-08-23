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
ms.openlocfilehash: b099bf5df657b5516fbf0948e742d1d1b36af2e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803355"
---
# <a name="pidtagresponserequested-canonical-property"></a><span data-ttu-id="567ca-103">PidTagResponseRequested 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="567ca-103">PidTagResponseRequested Canonical Property</span></span>

  
  
<span data-ttu-id="567ca-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="567ca-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="567ca-105">メッセージの送信者は、会議出席依頼への応答を希望する場合は TRUE が含まれています。</span><span class="sxs-lookup"><span data-stu-id="567ca-105">Contains TRUE if the message sender wants a response to a meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="567ca-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="567ca-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="567ca-107">PR_RESPONSE_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="567ca-107">PR_RESPONSE_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="567ca-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="567ca-108">Identifier:</span></span>  <br/> |<span data-ttu-id="567ca-109">0x0063</span><span class="sxs-lookup"><span data-stu-id="567ca-109">0x0063</span></span>  <br/> |
|<span data-ttu-id="567ca-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="567ca-110">Data type:</span></span>  <br/> |<span data-ttu-id="567ca-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="567ca-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="567ca-112">領域:</span><span class="sxs-lookup"><span data-stu-id="567ca-112">Area:</span></span>  <br/> |<span data-ttu-id="567ca-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="567ca-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="567ca-114">注釈</span><span class="sxs-lookup"><span data-stu-id="567ca-114">Remarks</span></span>

<span data-ttu-id="567ca-115">会議出席依頼には、このプロパティが使用されます。</span><span class="sxs-lookup"><span data-stu-id="567ca-115">This property is used for meeting requests.</span></span> <span data-ttu-id="567ca-116">受信側のクライアント アプリケーションでユーザーが承諾または辞退し、送信者に戻るには、この応答を送信し、メッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="567ca-116">The receiving client application should prompt the user to accept or decline the request and then send this response back to the sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="567ca-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="567ca-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="567ca-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="567ca-118">Protocol specifications</span></span>

<span data-ttu-id="567ca-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="567ca-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="567ca-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="567ca-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="567ca-121">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="567ca-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="567ca-122">プロパティは、電子メール メッセージの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="567ca-122">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="567ca-123">[[MS OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="567ca-123">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="567ca-124">プロパティ フラグに関連する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="567ca-124">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="567ca-125">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="567ca-125">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="567ca-126">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="567ca-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="567ca-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="567ca-127">Header files</span></span>

<span data-ttu-id="567ca-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="567ca-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="567ca-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="567ca-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="567ca-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="567ca-130">Mapitags.h</span></span>
  
> <span data-ttu-id="567ca-131">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="567ca-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="567ca-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="567ca-132">See also</span></span>



[<span data-ttu-id="567ca-133">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="567ca-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="567ca-134">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="567ca-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="567ca-135">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="567ca-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="567ca-136">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="567ca-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

