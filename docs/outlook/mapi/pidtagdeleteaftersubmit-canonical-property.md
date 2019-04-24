---
title: PidTagDeleteAfterSubmit 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeleteAfterSubmit
api_type:
- HeaderDef
ms.assetid: ba69a557-120c-4b1e-bbb7-0e901e7d1ebf
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2708d89e2572e8820de0b525b4f53ccd309ae2a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359914"
---
# <a name="pidtagdeleteaftersubmit-canonical-property"></a><span data-ttu-id="11c5d-103">PidTagDeleteAfterSubmit 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="11c5d-103">PidTagDeleteAfterSubmit Canonical Property</span></span>

  
  
<span data-ttu-id="11c5d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11c5d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11c5d-105">クライアントアプリケーションが、送信後に関連付けられたメッセージを MAPI で削除する場合は、TRUE が含まれます。</span><span class="sxs-lookup"><span data-stu-id="11c5d-105">Contains TRUE if a client application wants MAPI to delete the associated message after submission.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="11c5d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="11c5d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="11c5d-107">PR_DELETE_AFTER_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="11c5d-107">PR_DELETE_AFTER_SUBMIT</span></span>  <br/> |
|<span data-ttu-id="11c5d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="11c5d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="11c5d-109">0x0e01</span><span class="sxs-lookup"><span data-stu-id="11c5d-109">0x0E01</span></span>  <br/> |
|<span data-ttu-id="11c5d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="11c5d-110">Data type:</span></span>  <br/> |<span data-ttu-id="11c5d-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="11c5d-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="11c5d-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="11c5d-112">Area:</span></span>  <br/> |<span data-ttu-id="11c5d-113">MAPI ノンノンアウトテーブル</span><span class="sxs-lookup"><span data-stu-id="11c5d-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="11c5d-114">解説</span><span class="sxs-lookup"><span data-stu-id="11c5d-114">Remarks</span></span>

<span data-ttu-id="11c5d-115">クライアントアプリケーションは、このプロパティを**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) プロパティと共に使用して、メッセージが送信された後の処理を制御します。</span><span class="sxs-lookup"><span data-stu-id="11c5d-115">A client application uses this property with the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property to control what happens to a message after it is submitted.</span></span> <span data-ttu-id="11c5d-116">どちらか一方を設定する必要がありますが、両方を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="11c5d-116">Either one or the other should be set, but not both.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="11c5d-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="11c5d-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="11c5d-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="11c5d-118">Protocol specifications</span></span>

<span data-ttu-id="11c5d-119">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11c5d-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11c5d-120">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="11c5d-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="11c5d-121">[[OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11c5d-121">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11c5d-122">コアメッセージストアオブジェクトに対する許容される操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="11c5d-122">Specifies permissible operations for the core message store objects.</span></span>
    
<span data-ttu-id="11c5d-123">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11c5d-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11c5d-124">電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="11c5d-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="11c5d-125">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="11c5d-125">Header files</span></span>

<span data-ttu-id="11c5d-126">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="11c5d-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="11c5d-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="11c5d-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="11c5d-128">Mapitags</span><span class="sxs-lookup"><span data-stu-id="11c5d-128">Mapitags.h</span></span>
  
> <span data-ttu-id="11c5d-129">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="11c5d-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="11c5d-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="11c5d-130">See also</span></span>



[<span data-ttu-id="11c5d-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="11c5d-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="11c5d-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="11c5d-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="11c5d-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="11c5d-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="11c5d-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="11c5d-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

