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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d494f1f14daff75be55e910da56204ecb3dbcf83
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345802"
---
# <a name="pidtagattachmentflags-canonical-property"></a><span data-ttu-id="79884-103">PidTagAttachmentFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="79884-103">PidTagAttachmentFlags Canonical Property</span></span>

  
  
<span data-ttu-id="79884-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79884-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79884-105">この Attachment オブジェクトの特別な処理を示します。</span><span class="sxs-lookup"><span data-stu-id="79884-105">Indicates special handling for this Attachment object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="79884-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="79884-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="79884-107">PR_ATTACHMENT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="79884-107">PR_ATTACHMENT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="79884-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="79884-108">Identifier:</span></span>  <br/> |<span data-ttu-id="79884-109">0x7FFD</span><span class="sxs-lookup"><span data-stu-id="79884-109">0x7FFD</span></span>  <br/> |
|<span data-ttu-id="79884-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="79884-110">Data type:</span></span>  <br/> |<span data-ttu-id="79884-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="79884-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="79884-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="79884-112">Area:</span></span>  <br/> |<span data-ttu-id="79884-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="79884-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="79884-114">注釈</span><span class="sxs-lookup"><span data-stu-id="79884-114">Remarks</span></span>

<span data-ttu-id="79884-115">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)で0x00000000メッセージおよび添付ファイル オブジェクト プロトコルを拡張する他のプロトコルによってオーバーライドされない限り、このプロトコルを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="79884-115">Must be 0x00000000, unless overridden by other protocols that extend the Message and Attachment Object Protocol as noted in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="79884-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="79884-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="79884-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="79884-117">Protocol specifications</span></span>

<span data-ttu-id="79884-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="79884-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="79884-119">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="79884-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="79884-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="79884-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="79884-121">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="79884-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="79884-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="79884-122">Header files</span></span>

<span data-ttu-id="79884-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="79884-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="79884-124">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="79884-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="79884-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="79884-125">Mapitags.h</span></span>
  
> <span data-ttu-id="79884-126">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="79884-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="79884-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="79884-127">See also</span></span>



[<span data-ttu-id="79884-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="79884-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="79884-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="79884-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="79884-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="79884-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="79884-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="79884-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

