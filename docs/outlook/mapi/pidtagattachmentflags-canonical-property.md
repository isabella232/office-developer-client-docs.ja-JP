---
title: PidTagAttachmentFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachmentFlags
api_type:
- HeaderDef
ms.assetid: 42981aac-f9e7-45dd-91a2-15d9784f30aa
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d494f1f14daff75be55e910da56204ecb3dbcf83
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400713"
---
# <a name="pidtagattachmentflags-canonical-property"></a><span data-ttu-id="bf040-103">PidTagAttachmentFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bf040-103">PidTagAttachmentFlags Canonical Property</span></span>

  
  
<span data-ttu-id="bf040-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf040-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf040-105">この添付ファイル オブジェクトに対する特殊な処理を示します。</span><span class="sxs-lookup"><span data-stu-id="bf040-105">Indicates special handling for this Attachment object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bf040-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="bf040-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bf040-107">PR_ATTACHMENT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="bf040-107">PR_ATTACHMENT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="bf040-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="bf040-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bf040-109">0x7FFD</span><span class="sxs-lookup"><span data-stu-id="bf040-109">0x7FFD</span></span>  <br/> |
|<span data-ttu-id="bf040-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="bf040-110">Data type:</span></span>  <br/> |<span data-ttu-id="bf040-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="bf040-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="bf040-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="bf040-112">Area:</span></span>  <br/> |<span data-ttu-id="bf040-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="bf040-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf040-114">備考</span><span class="sxs-lookup"><span data-stu-id="bf040-114">Remarks</span></span>

<span data-ttu-id="bf040-115">[[MS OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)で説明したように、添付ファイル オブジェクト プロトコル メッセージを拡張する他のプロトコルを指定しないかぎり、0x00000000 をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="bf040-115">Must be 0x00000000, unless overridden by other protocols that extend the Message and Attachment Object Protocol as noted in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bf040-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bf040-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bf040-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="bf040-117">Protocol specifications</span></span>

<span data-ttu-id="bf040-118">[[MS OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bf040-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bf040-119">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="bf040-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="bf040-120">[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bf040-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bf040-121">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="bf040-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bf040-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="bf040-122">Header files</span></span>

<span data-ttu-id="bf040-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bf040-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="bf040-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bf040-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="bf040-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bf040-125">Mapitags.h</span></span>
  
> <span data-ttu-id="bf040-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bf040-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bf040-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="bf040-127">See also</span></span>



[<span data-ttu-id="bf040-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="bf040-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bf040-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="bf040-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bf040-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="bf040-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bf040-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="bf040-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

