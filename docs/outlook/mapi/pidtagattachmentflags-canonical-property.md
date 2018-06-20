---
title: PidTagAttachmentFlags の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 825f6f1eff94635ca2d0f5226cfc3f421d41bcce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802495"
---
# <a name="pidtagattachmentflags-canonical-property"></a><span data-ttu-id="3ecd7-103">PidTagAttachmentFlags の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="3ecd7-103">PidTagAttachmentFlags Canonical Property</span></span>

  
  
<span data-ttu-id="3ecd7-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3ecd7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3ecd7-105">この添付ファイル オブジェクトに対する特殊な処理を示します。</span><span class="sxs-lookup"><span data-stu-id="3ecd7-105">Indicates special handling for this Attachment object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3ecd7-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="3ecd7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3ecd7-107">PR_ATTACHMENT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="3ecd7-107">PR_ATTACHMENT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="3ecd7-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="3ecd7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3ecd7-109">0x7FFD</span><span class="sxs-lookup"><span data-stu-id="3ecd7-109">0x7FFD</span></span>  <br/> |
|<span data-ttu-id="3ecd7-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="3ecd7-110">Data type:</span></span>  <br/> |<span data-ttu-id="3ecd7-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3ecd7-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3ecd7-112">領域:</span><span class="sxs-lookup"><span data-stu-id="3ecd7-112">Area:</span></span>  <br/> |<span data-ttu-id="3ecd7-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="3ecd7-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3ecd7-114">備考</span><span class="sxs-lookup"><span data-stu-id="3ecd7-114">Remarks</span></span>

<span data-ttu-id="3ecd7-115">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)で説明したように、添付ファイル オブジェクト プロトコル メッセージを拡張する他のプロトコルを指定しないかぎり、0x00000000 をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ecd7-115">Must be 0x00000000, unless overridden by other protocols that extend the Message and Attachment Object Protocol as noted in [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3ecd7-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="3ecd7-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3ecd7-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="3ecd7-117">Protocol specifications</span></span>

<span data-ttu-id="3ecd7-118">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3ecd7-118">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3ecd7-119">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="3ecd7-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="3ecd7-120">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3ecd7-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3ecd7-121">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="3ecd7-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3ecd7-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="3ecd7-122">Header files</span></span>

<span data-ttu-id="3ecd7-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3ecd7-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="3ecd7-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3ecd7-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="3ecd7-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3ecd7-125">Mapitags.h</span></span>
  
> <span data-ttu-id="3ecd7-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3ecd7-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3ecd7-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="3ecd7-127">See also</span></span>



[<span data-ttu-id="3ecd7-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3ecd7-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3ecd7-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3ecd7-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3ecd7-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="3ecd7-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3ecd7-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="3ecd7-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

