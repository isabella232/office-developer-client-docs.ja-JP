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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cd5a6071674dce97215bbeb7027752bfcedc94ea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578074"
---
# <a name="pidtagattachmentlinkid-canonical-property"></a><span data-ttu-id="224b7-103">PidTagAttachmentLinkId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="224b7-103">PidTagAttachmentLinkId Canonical Property</span></span>

  
  
<span data-ttu-id="224b7-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="224b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="224b7-105">この添付ファイルがリンクされているメッセージ オブジェクトの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="224b7-105">Indicates the type of Message object to which this attachment is linked.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="224b7-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="224b7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="224b7-107">PR_ATTACHMENT_LINKID</span><span class="sxs-lookup"><span data-stu-id="224b7-107">PR_ATTACHMENT_LINKID</span></span>  <br/> |
|<span data-ttu-id="224b7-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="224b7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="224b7-109">0x7FFA</span><span class="sxs-lookup"><span data-stu-id="224b7-109">0x7FFA</span></span>  <br/> |
|<span data-ttu-id="224b7-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="224b7-110">Data type:</span></span>  <br/> |<span data-ttu-id="224b7-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="224b7-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="224b7-112">領域:</span><span class="sxs-lookup"><span data-stu-id="224b7-112">Area:</span></span>  <br/> |<span data-ttu-id="224b7-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="224b7-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="224b7-114">注釈</span><span class="sxs-lookup"><span data-stu-id="224b7-114">Remarks</span></span>

<span data-ttu-id="224b7-115">[[MS OXCMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)で説明したように、添付ファイル オブジェクト プロトコル メッセージを拡張する他のプロトコルによってオーバーライドされない限り、0 を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="224b7-115">Must be 0, unless overridden by other protocols that extend the Message and Attachment Object Protocol as noted in [[MS-OXCMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="224b7-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="224b7-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="224b7-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="224b7-117">Protocol specifications</span></span>

<span data-ttu-id="224b7-118">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="224b7-118">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="224b7-119">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="224b7-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="224b7-120">[[MS OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="224b7-120">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="224b7-121">プロパティとは、仕訳帳のオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="224b7-121">Specifies the properties and operations that are permissible for journal objects.</span></span>
    
<span data-ttu-id="224b7-122">[[MS OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="224b7-122">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="224b7-123">電子メールおよびその他のオブジェクトのアラームの操作モデルのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="224b7-123">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="224b7-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="224b7-124">Header files</span></span>

<span data-ttu-id="224b7-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="224b7-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="224b7-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="224b7-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="224b7-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="224b7-127">Mapitags.h</span></span>
  
> <span data-ttu-id="224b7-128">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="224b7-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="224b7-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="224b7-129">See also</span></span>



[<span data-ttu-id="224b7-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="224b7-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="224b7-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="224b7-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="224b7-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="224b7-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="224b7-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="224b7-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

