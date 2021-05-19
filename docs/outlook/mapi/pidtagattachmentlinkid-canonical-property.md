---
title: PidTagAttachmentLinkId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachmentLinkId
api_type:
- HeaderDef
ms.assetid: 5d0daae7-248d-459f-9d96-cb949b86f590
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 623b4195b7128667b9aaa6bc97d03c21d62c690a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345697"
---
# <a name="pidtagattachmentlinkid-canonical-property"></a><span data-ttu-id="e5725-103">PidTagAttachmentLinkId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e5725-103">PidTagAttachmentLinkId Canonical Property</span></span>

  
  
<span data-ttu-id="e5725-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5725-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5725-105">この添付ファイルがリンクされている Message オブジェクトの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="e5725-105">Indicates the type of Message object to which this attachment is linked.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e5725-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e5725-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e5725-107">PR_ATTACHMENT_LINKID</span><span class="sxs-lookup"><span data-stu-id="e5725-107">PR_ATTACHMENT_LINKID</span></span>  <br/> |
|<span data-ttu-id="e5725-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e5725-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e5725-109">0x7FFA</span><span class="sxs-lookup"><span data-stu-id="e5725-109">0x7FFA</span></span>  <br/> |
|<span data-ttu-id="e5725-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e5725-110">Data type:</span></span>  <br/> |<span data-ttu-id="e5725-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e5725-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e5725-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="e5725-112">Area:</span></span>  <br/> |<span data-ttu-id="e5725-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="e5725-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e5725-114">注釈</span><span class="sxs-lookup"><span data-stu-id="e5725-114">Remarks</span></span>

<span data-ttu-id="e5725-115">[[MS-OXCMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)で示されているメッセージ および添付ファイル オブジェクト プロトコルを拡張する他のプロトコルによってオーバーライドされない限り、0 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5725-115">Must be 0, unless overridden by other protocols that extend the Message and Attachment Object Protocol as noted in [[MS-OXCMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e5725-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e5725-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e5725-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e5725-117">Protocol specifications</span></span>

<span data-ttu-id="e5725-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e5725-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e5725-119">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="e5725-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="e5725-120">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e5725-120">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e5725-121">ジャーナル オブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e5725-121">Specifies the properties and operations that are permissible for journal objects.</span></span>
    
<span data-ttu-id="e5725-122">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e5725-122">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e5725-123">メールなどのオブジェクトアラームのプロパティと対話モデルを指定します。</span><span class="sxs-lookup"><span data-stu-id="e5725-123">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e5725-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e5725-124">Header files</span></span>

<span data-ttu-id="e5725-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e5725-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="e5725-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e5725-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="e5725-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e5725-127">Mapitags.h</span></span>
  
> <span data-ttu-id="e5725-128">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="e5725-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e5725-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="e5725-129">See also</span></span>



[<span data-ttu-id="e5725-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e5725-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e5725-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e5725-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e5725-132">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="e5725-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e5725-133">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="e5725-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

