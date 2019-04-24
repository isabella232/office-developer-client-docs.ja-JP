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
ms.openlocfilehash: 2dac2cb1d40fadbe0cad67b144891b0ece54aae9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341112"
---
# <a name="pidtagrecipientreassignmentprohibited-canonical-property"></a><span data-ttu-id="9a14a-103">PidTagRecipientReassignmentProhibited 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9a14a-103">PidTagRecipientReassignmentProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="9a14a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a14a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a14a-105">メッセージを転送するときに、電子メールメッセージに対して受信者を追加することを禁止するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="9a14a-105">Specifies whether adding additional recipients, when forwarding the message, is prohibited for the email message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9a14a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9a14a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9a14a-107">PR_RECIPIENT_REASSIGNMENT_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="9a14a-107">PR_RECIPIENT_REASSIGNMENT_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="9a14a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="9a14a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9a14a-109">0x002b</span><span class="sxs-lookup"><span data-stu-id="9a14a-109">0x002B</span></span>  <br/> |
|<span data-ttu-id="9a14a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9a14a-110">Data type:</span></span>  <br/> |<span data-ttu-id="9a14a-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="9a14a-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="9a14a-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="9a14a-112">Area:</span></span>  <br/> |<span data-ttu-id="9a14a-113">MAPI エンベロープ</span><span class="sxs-lookup"><span data-stu-id="9a14a-113">MAPI Envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9a14a-114">解説</span><span class="sxs-lookup"><span data-stu-id="9a14a-114">Remarks</span></span>

<span data-ttu-id="9a14a-115">このプロパティは、電子メールメッセージの**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) 値に基づいて設定されます。</span><span class="sxs-lookup"><span data-stu-id="9a14a-115">This property is set based on the email message's **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) value.</span></span> <span data-ttu-id="9a14a-116">**PR_SENSITIVITY**が "0x00000000" (標準) または "0x00000003" (confidential) に設定されている場合は、このプロパティを "0x00" に設定するか、または電子メールメッセージに別の受信者を追加できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a14a-116">If **PR_SENSITIVITY** is set to "0x00000000" (normal) or "0x00000003" (confidential), this property must be set to "0x00" or absent meaning that adding additional or different recipients to the email message is allowed.</span></span> <span data-ttu-id="9a14a-117">電子メールオブジェクトの**PR_SENSITIVITY**が "0x00000001" (personal) または "0x00000002" (private) に設定されている場合は、このプロパティを "0x01" に設定して、転送によってこの電子メールの受信者を追加したり、別の受信者を追加したりしないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a14a-117">If the email object's **PR_SENSITIVITY** is set to "0x00000001" (personal) or "0x00000002" (private), this property must be set "0x01" to prevent adding additional or different recipients of this email through forwarding.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9a14a-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9a14a-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9a14a-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="9a14a-119">Protocol specifications</span></span>

<span data-ttu-id="9a14a-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9a14a-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9a14a-121">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="9a14a-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9a14a-122">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9a14a-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9a14a-123">電子メールメッセージに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="9a14a-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9a14a-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="9a14a-124">Header files</span></span>

<span data-ttu-id="9a14a-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9a14a-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="9a14a-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9a14a-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="9a14a-127">Mapitags</span><span class="sxs-lookup"><span data-stu-id="9a14a-127">Mapitags.h</span></span>
  
> <span data-ttu-id="9a14a-128">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9a14a-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9a14a-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="9a14a-129">See also</span></span>



[<span data-ttu-id="9a14a-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="9a14a-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9a14a-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9a14a-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9a14a-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9a14a-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9a14a-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9a14a-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

