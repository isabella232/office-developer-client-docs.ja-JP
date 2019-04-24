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
ms.openlocfilehash: aca9c9f9c22fc4057f1650d1342492d2ed34653c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316129"
---
# <a name="pidtaghasattachments-canonical-property"></a><span data-ttu-id="94f22-103">PidTagHasAttachments 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="94f22-103">PidTagHasAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="94f22-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94f22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94f22-105">メッセージに添付ファイルが1つ以上含まれている場合は、TRUE が含まれます。</span><span class="sxs-lookup"><span data-stu-id="94f22-105">Contains TRUE if a message contains at least one attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="94f22-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="94f22-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="94f22-107">PR_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="94f22-107">PR_HASATTACH</span></span>  <br/> |
|<span data-ttu-id="94f22-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="94f22-108">Identifier:</span></span>  <br/> |<span data-ttu-id="94f22-109">0x0e1b</span><span class="sxs-lookup"><span data-stu-id="94f22-109">0x0E1B</span></span>  <br/> |
|<span data-ttu-id="94f22-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="94f22-110">Data type:</span></span>  <br/> |<span data-ttu-id="94f22-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="94f22-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="94f22-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="94f22-112">Area:</span></span>  <br/> |<span data-ttu-id="94f22-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="94f22-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="94f22-114">解説</span><span class="sxs-lookup"><span data-stu-id="94f22-114">Remarks</span></span>

<span data-ttu-id="94f22-115">メッセージストアは、このプロパティを**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティの**MSGFLAG_HASATTACH**フラグからコピーします。</span><span class="sxs-lookup"><span data-stu-id="94f22-115">The message store copies this property from the **MSGFLAG_HASATTACH** flag of the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="94f22-116">その後、クライアントアプリケーションは**PR_HASATTACH**を使用して、メッセージビューアーのメッセージの添付ファイルを並べ替えることができます。</span><span class="sxs-lookup"><span data-stu-id="94f22-116">A client application can then use **PR_HASATTACH** to sort on message attachments in a message viewer.</span></span> 
  
<span data-ttu-id="94f22-117">このプロパティの値は、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを使用して更新されます。</span><span class="sxs-lookup"><span data-stu-id="94f22-117">The value this property is updated with the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="94f22-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="94f22-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="94f22-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="94f22-119">Protocol specifications</span></span>

<span data-ttu-id="94f22-120">[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94f22-120">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94f22-121">電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="94f22-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="94f22-122">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="94f22-122">Header files</span></span>

<span data-ttu-id="94f22-123">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="94f22-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="94f22-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="94f22-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="94f22-125">Mapitags</span><span class="sxs-lookup"><span data-stu-id="94f22-125">Mapitags.h</span></span>
  
> <span data-ttu-id="94f22-126">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="94f22-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="94f22-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="94f22-127">See also</span></span>



[<span data-ttu-id="94f22-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="94f22-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="94f22-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="94f22-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="94f22-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="94f22-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="94f22-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="94f22-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

