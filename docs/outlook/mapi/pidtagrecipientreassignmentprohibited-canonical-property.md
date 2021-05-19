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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2dac2cb1d40fadbe0cad67b144891b0ece54aae9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341112"
---
# <a name="pidtagrecipientreassignmentprohibited-canonical-property"></a><span data-ttu-id="907e6-103">PidTagRecipientReassignmentProhibited 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="907e6-103">PidTagRecipientReassignmentProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="907e6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="907e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="907e6-105">電子メール メッセージに対して、メッセージを転送するときに受信者を追加することを禁止するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="907e6-105">Specifies whether adding additional recipients, when forwarding the message, is prohibited for the email message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="907e6-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="907e6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="907e6-107">PR_RECIPIENT_REASSIGNMENT_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="907e6-107">PR_RECIPIENT_REASSIGNMENT_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="907e6-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="907e6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="907e6-109">0x002B</span><span class="sxs-lookup"><span data-stu-id="907e6-109">0x002B</span></span>  <br/> |
|<span data-ttu-id="907e6-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="907e6-110">Data type:</span></span>  <br/> |<span data-ttu-id="907e6-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="907e6-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="907e6-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="907e6-112">Area:</span></span>  <br/> |<span data-ttu-id="907e6-113">MAPI 封筒</span><span class="sxs-lookup"><span data-stu-id="907e6-113">MAPI Envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="907e6-114">注釈</span><span class="sxs-lookup"><span data-stu-id="907e6-114">Remarks</span></span>

<span data-ttu-id="907e6-115">このプロパティは、電子メール メッセージの値 ([PidTagSensitivity](pidtagsensitivity-canonical-property.md) **)** PR_SENSITIVITYに基づいて設定されます。</span><span class="sxs-lookup"><span data-stu-id="907e6-115">This property is set based on the email message's **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) value.</span></span> <span data-ttu-id="907e6-116">PR_SENSITIVITYが "0x00000000" (標準) または "0x00000003" (機密) に設定されている場合、このプロパティを "0x00" に設定するか、電子メール メッセージに別の受信者を追加できます。</span><span class="sxs-lookup"><span data-stu-id="907e6-116">If **PR_SENSITIVITY** is set to "0x00000000" (normal) or "0x00000003" (confidential), this property must be set to "0x00" or absent meaning that adding additional or different recipients to the email message is allowed.</span></span> <span data-ttu-id="907e6-117">電子メール オブジェクトの **PR_SENSITIVITY** が "0x00000001" (個人用) または "0x00000002" (プライベート) に設定されている場合、転送によってこのメールの受信者が追加または異なって追加されるのを防ぐために、このプロパティを "0x01" に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="907e6-117">If the email object's **PR_SENSITIVITY** is set to "0x00000001" (personal) or "0x00000002" (private), this property must be set "0x01" to prevent adding additional or different recipients of this email through forwarding.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="907e6-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="907e6-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="907e6-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="907e6-119">Protocol specifications</span></span>

<span data-ttu-id="907e6-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="907e6-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="907e6-121">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="907e6-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="907e6-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="907e6-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="907e6-123">電子メール メッセージで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="907e6-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="907e6-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="907e6-124">Header files</span></span>

<span data-ttu-id="907e6-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="907e6-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="907e6-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="907e6-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="907e6-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="907e6-127">Mapitags.h</span></span>
  
> <span data-ttu-id="907e6-128">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="907e6-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="907e6-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="907e6-129">See also</span></span>



[<span data-ttu-id="907e6-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="907e6-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="907e6-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="907e6-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="907e6-132">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="907e6-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="907e6-133">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="907e6-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

