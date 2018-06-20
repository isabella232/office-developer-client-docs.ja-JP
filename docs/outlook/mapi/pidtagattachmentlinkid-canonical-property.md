---
title: PidTagAttachmentLinkId の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e467fb7c05a647265d007429930ee522fd77b2fa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802476"
---
# <a name="pidtagattachmentlinkid-canonical-property"></a><span data-ttu-id="31984-103">PidTagAttachmentLinkId の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="31984-103">PidTagAttachmentLinkId Canonical Property</span></span>

  
  
<span data-ttu-id="31984-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="31984-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="31984-105">この添付ファイルがリンクされているメッセージ オブジェクトの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="31984-105">Indicates the type of Message object to which this attachment is linked.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="31984-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="31984-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="31984-107">PR_ATTACHMENT_LINKID</span><span class="sxs-lookup"><span data-stu-id="31984-107">PR_ATTACHMENT_LINKID</span></span>  <br/> |
|<span data-ttu-id="31984-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="31984-108">Identifier:</span></span>  <br/> |<span data-ttu-id="31984-109">0x7FFA</span><span class="sxs-lookup"><span data-stu-id="31984-109">0x7FFA</span></span>  <br/> |
|<span data-ttu-id="31984-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="31984-110">Data type:</span></span>  <br/> |<span data-ttu-id="31984-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="31984-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="31984-112">領域:</span><span class="sxs-lookup"><span data-stu-id="31984-112">Area:</span></span>  <br/> |<span data-ttu-id="31984-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="31984-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="31984-114">備考</span><span class="sxs-lookup"><span data-stu-id="31984-114">Remarks</span></span>

<span data-ttu-id="31984-115">[[MS OXCMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)で説明したように、添付ファイル オブジェクト プロトコル メッセージを拡張する他のプロトコルによってオーバーライドされない限り、0 を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="31984-115">Must be 0, unless overridden by other protocols that extend the Message and Attachment Object Protocol as noted in [[MS-OXCMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="31984-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="31984-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="31984-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="31984-117">Protocol specifications</span></span>

<span data-ttu-id="31984-118">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="31984-118">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="31984-119">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="31984-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="31984-120">[[MS OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="31984-120">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="31984-121">プロパティとは、仕訳帳のオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="31984-121">Specifies the properties and operations that are permissible for journal objects.</span></span>
    
<span data-ttu-id="31984-122">[[MS OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="31984-122">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="31984-123">電子メールおよびその他のオブジェクトのアラームの操作モデルのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="31984-123">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="31984-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="31984-124">Header files</span></span>

<span data-ttu-id="31984-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="31984-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="31984-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="31984-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="31984-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="31984-127">Mapitags.h</span></span>
  
> <span data-ttu-id="31984-128">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="31984-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="31984-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="31984-129">See also</span></span>



[<span data-ttu-id="31984-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="31984-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="31984-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="31984-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="31984-132">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="31984-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="31984-133">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="31984-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

