---
title: PidTagRecipientReassignmentProhibited 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 8636774b-1fff-4b29-bc12-4d0bd63fcba2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0176485ca9b84260176e3be8ec9c8f42cf755cba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803291"
---
# <a name="pidtagrecipientreassignmentprohibited-canonical-property"></a><span data-ttu-id="813b1-103">PidTagRecipientReassignmentProhibited 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="813b1-103">PidTagRecipientReassignmentProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="813b1-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="813b1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="813b1-105">電子メール メッセージのメッセージを転送するときに追加の受信者を追加することが禁止されているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="813b1-105">Specifies whether adding additional recipients, when forwarding the message, is prohibited for the email message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="813b1-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="813b1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="813b1-107">PR_RECIPIENT_REASSIGNMENT_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="813b1-107">PR_RECIPIENT_REASSIGNMENT_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="813b1-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="813b1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="813b1-109">0x002B</span><span class="sxs-lookup"><span data-stu-id="813b1-109">0x002B</span></span>  <br/> |
|<span data-ttu-id="813b1-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="813b1-110">Data type:</span></span>  <br/> |<span data-ttu-id="813b1-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="813b1-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="813b1-112">領域:</span><span class="sxs-lookup"><span data-stu-id="813b1-112">Area:</span></span>  <br/> |<span data-ttu-id="813b1-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="813b1-113">MAPI Envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="813b1-114">注釈</span><span class="sxs-lookup"><span data-stu-id="813b1-114">Remarks</span></span>

<span data-ttu-id="813b1-115">電子メール メッセージの**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) の値に基づいて、このプロパティが設定されます。</span><span class="sxs-lookup"><span data-stu-id="813b1-115">This property is set based on the email message's **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) value.</span></span> <span data-ttu-id="813b1-116">**PR_SENSITIVITY**が (機密) を"0x00"に、または省略することを追加することを意味、このプロパティを設定する必要があります"0x00000000"の (標準) または"0x00000003"に設定されて場合は、電子メール メッセージに受信者を追加または変更が許可されます。</span><span class="sxs-lookup"><span data-stu-id="813b1-116">If **PR_SENSITIVITY** is set to "0x00000000" (normal) or "0x00000003" (confidential), this property must be set to "0x00" or absent meaning that adding additional or different recipients to the email message is allowed.</span></span> <span data-ttu-id="813b1-117">メール オブジェクトの**PR_SENSITIVITY**は、(個人)"0x00000001"または"0x00000002"(プライベート) に設定されている場合は、このプロパティが"0x01"を設定する必要があります転送では、この電子メールの受信者を追加または変更を追加できないようにするのにします。</span><span class="sxs-lookup"><span data-stu-id="813b1-117">If the email object's **PR_SENSITIVITY** is set to "0x00000001" (personal) or "0x00000002" (private), this property must be set "0x01" to prevent adding additional or different recipients of this email through forwarding.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="813b1-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="813b1-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="813b1-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="813b1-119">Protocol specifications</span></span>

<span data-ttu-id="813b1-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="813b1-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="813b1-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="813b1-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="813b1-122">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="813b1-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="813b1-123">プロパティは、電子メール メッセージの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="813b1-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="813b1-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="813b1-124">Header files</span></span>

<span data-ttu-id="813b1-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="813b1-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="813b1-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="813b1-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="813b1-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="813b1-127">Mapitags.h</span></span>
  
> <span data-ttu-id="813b1-128">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="813b1-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="813b1-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="813b1-129">See also</span></span>



[<span data-ttu-id="813b1-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="813b1-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="813b1-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="813b1-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="813b1-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="813b1-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="813b1-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="813b1-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

