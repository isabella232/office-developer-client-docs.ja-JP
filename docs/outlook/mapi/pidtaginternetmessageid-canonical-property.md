---
title: PidTagInternetMessageId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInternetMessageId
api_type:
- HeaderDef
ms.assetid: 5c93d00c-a199-4d45-9bf6-87bd2ffe4784
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c2cc0eabd9c329953d9b0d252418549ea1c588a1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358569"
---
# <a name="pidtaginternetmessageid-canonical-property"></a><span data-ttu-id="7dc39-103">PidTagInternetMessageId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7dc39-103">PidTagInternetMessageId Canonical Property</span></span>

  
  
<span data-ttu-id="7dc39-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7dc39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7dc39-105">[RFC2822] で指定されているメッセージ ID フィールドに対応します。</span><span class="sxs-lookup"><span data-stu-id="7dc39-105">Corresponds to the message ID field as specified in [RFC2822].</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7dc39-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7dc39-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7dc39-107">PR_INTERNET_MESSAGE_ID、PR_INTERNET_MESSAGE_ID_A、PR_INTERNET_MESSAGE_ID_W</span><span class="sxs-lookup"><span data-stu-id="7dc39-107">PR_INTERNET_MESSAGE_ID, PR_INTERNET_MESSAGE_ID_A, PR_INTERNET_MESSAGE_ID_W</span></span>  <br/> |
|<span data-ttu-id="7dc39-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7dc39-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7dc39-109">0x1035</span><span class="sxs-lookup"><span data-stu-id="7dc39-109">0x1035</span></span>  <br/> |
|<span data-ttu-id="7dc39-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="7dc39-110">Data type:</span></span>  <br/> |<span data-ttu-id="7dc39-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7dc39-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7dc39-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="7dc39-112">Area:</span></span>  <br/> |<span data-ttu-id="7dc39-113">MIME</span><span class="sxs-lookup"><span data-stu-id="7dc39-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7dc39-114">注釈</span><span class="sxs-lookup"><span data-stu-id="7dc39-114">Remarks</span></span>

<span data-ttu-id="7dc39-115">これらのプロパティは、すべての電子メール メッセージに存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7dc39-115">These properties should be present on all email messages.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7dc39-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7dc39-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7dc39-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7dc39-117">Protocol specifications</span></span>

<span data-ttu-id="7dc39-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7dc39-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7dc39-119">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="7dc39-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7dc39-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7dc39-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7dc39-121">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="7dc39-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7dc39-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="7dc39-122">Header files</span></span>

<span data-ttu-id="7dc39-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7dc39-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="7dc39-124">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7dc39-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="7dc39-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7dc39-125">Mapitags.h</span></span>
  
> <span data-ttu-id="7dc39-126">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="7dc39-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7dc39-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="7dc39-127">See also</span></span>



[<span data-ttu-id="7dc39-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="7dc39-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7dc39-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7dc39-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7dc39-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="7dc39-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7dc39-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="7dc39-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

