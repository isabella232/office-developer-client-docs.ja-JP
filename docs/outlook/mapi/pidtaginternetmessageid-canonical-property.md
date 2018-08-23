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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7b0af907fd5346de5b818c9c75a3d115e598b5e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802883"
---
# <a name="pidtaginternetmessageid-canonical-property"></a><span data-ttu-id="e022a-103">PidTagInternetMessageId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e022a-103">PidTagInternetMessageId Canonical Property</span></span>

  
  
<span data-ttu-id="e022a-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e022a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e022a-105">[RFC2822] で指定されているメッセージ ID] フィールドに対応します。</span><span class="sxs-lookup"><span data-stu-id="e022a-105">Corresponds to the message ID field as specified in [RFC2822].</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e022a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e022a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e022a-107">PR_INTERNET_MESSAGE_ID、PR_INTERNET_MESSAGE_ID_A、PR_INTERNET_MESSAGE_ID_W</span><span class="sxs-lookup"><span data-stu-id="e022a-107">PR_INTERNET_MESSAGE_ID, PR_INTERNET_MESSAGE_ID_A, PR_INTERNET_MESSAGE_ID_W</span></span>  <br/> |
|<span data-ttu-id="e022a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e022a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e022a-109">0x1035</span><span class="sxs-lookup"><span data-stu-id="e022a-109">0x1035</span></span>  <br/> |
|<span data-ttu-id="e022a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e022a-110">Data type:</span></span>  <br/> |<span data-ttu-id="e022a-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e022a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e022a-112">領域:</span><span class="sxs-lookup"><span data-stu-id="e022a-112">Area:</span></span>  <br/> |<span data-ttu-id="e022a-113">MIME</span><span class="sxs-lookup"><span data-stu-id="e022a-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e022a-114">注釈</span><span class="sxs-lookup"><span data-stu-id="e022a-114">Remarks</span></span>

<span data-ttu-id="e022a-115">これらのプロパティは、すべての電子メール メッセージに含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="e022a-115">These properties should be present on all email messages.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e022a-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e022a-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e022a-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e022a-117">Protocol specifications</span></span>

<span data-ttu-id="e022a-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e022a-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e022a-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e022a-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e022a-120">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e022a-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e022a-121">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e022a-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e022a-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e022a-122">Header files</span></span>

<span data-ttu-id="e022a-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e022a-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="e022a-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e022a-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="e022a-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e022a-125">Mapitags.h</span></span>
  
> <span data-ttu-id="e022a-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e022a-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e022a-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="e022a-127">See also</span></span>



[<span data-ttu-id="e022a-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e022a-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e022a-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e022a-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e022a-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e022a-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e022a-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e022a-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

