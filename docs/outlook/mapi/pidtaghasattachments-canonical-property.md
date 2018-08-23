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
ms.openlocfilehash: 3b618e5a79c3b7e3810ea541aa9b905dfa4188a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802800"
---
# <a name="pidtaghasattachments-canonical-property"></a><span data-ttu-id="b53f9-103">PidTagHasAttachments 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b53f9-103">PidTagHasAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="b53f9-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b53f9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b53f9-105">メッセージには、少なくとも 1 つの添付ファイルが含まれている場合、TRUE が格納されます。</span><span class="sxs-lookup"><span data-stu-id="b53f9-105">Contains TRUE if a message contains at least one attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b53f9-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b53f9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b53f9-107">PR_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="b53f9-107">PR_HASATTACH</span></span>  <br/> |
|<span data-ttu-id="b53f9-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b53f9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b53f9-109">0x0E1B</span><span class="sxs-lookup"><span data-stu-id="b53f9-109">0x0E1B</span></span>  <br/> |
|<span data-ttu-id="b53f9-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b53f9-110">Data type:</span></span>  <br/> |<span data-ttu-id="b53f9-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="b53f9-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="b53f9-112">領域:</span><span class="sxs-lookup"><span data-stu-id="b53f9-112">Area:</span></span>  <br/> |<span data-ttu-id="b53f9-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="b53f9-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b53f9-114">注釈</span><span class="sxs-lookup"><span data-stu-id="b53f9-114">Remarks</span></span>

<span data-ttu-id="b53f9-115">メッセージ ・ ストアでは、 **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) のプロパティの**MSGFLAG_HASATTACH**フラグのこのプロパティをコピーします。</span><span class="sxs-lookup"><span data-stu-id="b53f9-115">The message store copies this property from the **MSGFLAG_HASATTACH** flag of the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="b53f9-116">クライアント アプリケーションは、メッセージ ビューアーで、メッセージの添付ファイルを並べ替えるには、 **PR_HASATTACH**を使用できます。</span><span class="sxs-lookup"><span data-stu-id="b53f9-116">A client application can then use **PR_HASATTACH** to sort on message attachments in a message viewer.</span></span> 
  
<span data-ttu-id="b53f9-117">[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを使用してこのプロパティを更新する値です。</span><span class="sxs-lookup"><span data-stu-id="b53f9-117">The value this property is updated with the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b53f9-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b53f9-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b53f9-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b53f9-119">Protocol specifications</span></span>

<span data-ttu-id="b53f9-120">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b53f9-120">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b53f9-121">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="b53f9-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b53f9-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b53f9-122">Header files</span></span>

<span data-ttu-id="b53f9-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b53f9-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="b53f9-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b53f9-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="b53f9-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b53f9-125">Mapitags.h</span></span>
  
> <span data-ttu-id="b53f9-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b53f9-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b53f9-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="b53f9-127">See also</span></span>



[<span data-ttu-id="b53f9-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b53f9-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b53f9-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b53f9-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b53f9-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b53f9-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b53f9-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b53f9-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

