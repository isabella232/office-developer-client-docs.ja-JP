---
title: PidTagHasAttachments 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagHasAttachments
api_type:
- HeaderDef
ms.assetid: fd236d74-2868-46a8-bb3d-17f8365931b6
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 505f9bb80c86b956cd920348f2120f7fc8494d8b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587503"
---
# <a name="pidtaghasattachments-canonical-property"></a><span data-ttu-id="1a7f6-103">PidTagHasAttachments 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1a7f6-103">PidTagHasAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="1a7f6-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a7f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a7f6-105">メッセージには、少なくとも 1 つの添付ファイルが含まれている場合、TRUE が格納されます。</span><span class="sxs-lookup"><span data-stu-id="1a7f6-105">Contains TRUE if a message contains at least one attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1a7f6-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1a7f6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1a7f6-107">PR_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="1a7f6-107">PR_HASATTACH</span></span>  <br/> |
|<span data-ttu-id="1a7f6-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1a7f6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1a7f6-109">0x0E1B</span><span class="sxs-lookup"><span data-stu-id="1a7f6-109">0x0E1B</span></span>  <br/> |
|<span data-ttu-id="1a7f6-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1a7f6-110">Data type:</span></span>  <br/> |<span data-ttu-id="1a7f6-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="1a7f6-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="1a7f6-112">領域:</span><span class="sxs-lookup"><span data-stu-id="1a7f6-112">Area:</span></span>  <br/> |<span data-ttu-id="1a7f6-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="1a7f6-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a7f6-114">注釈</span><span class="sxs-lookup"><span data-stu-id="1a7f6-114">Remarks</span></span>

<span data-ttu-id="1a7f6-115">メッセージ ・ ストアでは、 **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) のプロパティの**MSGFLAG_HASATTACH**フラグのこのプロパティをコピーします。</span><span class="sxs-lookup"><span data-stu-id="1a7f6-115">The message store copies this property from the **MSGFLAG_HASATTACH** flag of the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="1a7f6-116">クライアント アプリケーションは、メッセージ ビューアーで、メッセージの添付ファイルを並べ替えるには、 **PR_HASATTACH**を使用できます。</span><span class="sxs-lookup"><span data-stu-id="1a7f6-116">A client application can then use **PR_HASATTACH** to sort on message attachments in a message viewer.</span></span> 
  
<span data-ttu-id="1a7f6-117">[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを使用してこのプロパティを更新する値です。</span><span class="sxs-lookup"><span data-stu-id="1a7f6-117">The value this property is updated with the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1a7f6-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1a7f6-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1a7f6-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1a7f6-119">Protocol specifications</span></span>

<span data-ttu-id="1a7f6-120">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a7f6-120">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a7f6-121">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="1a7f6-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1a7f6-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="1a7f6-122">Header files</span></span>

<span data-ttu-id="1a7f6-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1a7f6-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="1a7f6-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1a7f6-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="1a7f6-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1a7f6-125">Mapitags.h</span></span>
  
> <span data-ttu-id="1a7f6-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1a7f6-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1a7f6-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="1a7f6-127">See also</span></span>



[<span data-ttu-id="1a7f6-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1a7f6-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1a7f6-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1a7f6-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1a7f6-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1a7f6-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1a7f6-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1a7f6-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

