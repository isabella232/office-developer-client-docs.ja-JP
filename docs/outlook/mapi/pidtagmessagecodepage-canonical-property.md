---
title: PidTagMessageCodepage 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageCodepage
api_type:
- HeaderDef
ms.assetid: eef73e34-470c-4c37-94ce-ea95fe83bc10
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f75a5e10a59d7c6db4e43d2552a38d523b537790
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580202"
---
# <a name="pidtagmessagecodepage-canonical-property"></a><span data-ttu-id="e2bc4-103">PidTagMessageCodepage 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e2bc4-103">PidTagMessageCodepage Canonical Property</span></span>

  
  
<span data-ttu-id="e2bc4-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2bc4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2bc4-105">メッセージに使用されるコード ページが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e2bc4-105">Contains the code page that is used for the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e2bc4-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e2bc4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e2bc4-107">PR_MESSAGE_CODEPAGE</span><span class="sxs-lookup"><span data-stu-id="e2bc4-107">PR_MESSAGE_CODEPAGE</span></span>  <br/> |
|<span data-ttu-id="e2bc4-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e2bc4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e2bc4-109">0x3FFD</span><span class="sxs-lookup"><span data-stu-id="e2bc4-109">0x3FFD</span></span>  <br/> |
|<span data-ttu-id="e2bc4-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e2bc4-110">Data type:</span></span>  <br/> |<span data-ttu-id="e2bc4-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e2bc4-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e2bc4-112">領域:</span><span class="sxs-lookup"><span data-stu-id="e2bc4-112">Area:</span></span>  <br/> |<span data-ttu-id="e2bc4-113">Common</span><span class="sxs-lookup"><span data-stu-id="e2bc4-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2bc4-114">注釈</span><span class="sxs-lookup"><span data-stu-id="e2bc4-114">Remarks</span></span>

<span data-ttu-id="e2bc4-115">このプロパティをゼロ (0) に設定されている場合、フォルダーのオブジェクトのコード ページが使用されます。</span><span class="sxs-lookup"><span data-stu-id="e2bc4-115">The folder object code page is used if this property is set to zero (0).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e2bc4-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e2bc4-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e2bc4-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e2bc4-117">Protocol specifications</span></span>

<span data-ttu-id="e2bc4-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2bc4-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2bc4-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e2bc4-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e2bc4-120">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2bc4-120">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2bc4-121">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="e2bc4-121">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="e2bc4-122">[[MS OXPFOAB]](http://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2bc4-122">[[MS-OXPFOAB]](http://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2bc4-123">オフライン アドレス帳 (OAB) のデータをサーバーからクライアントに配信する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="e2bc4-123">Specifies the method of delivering offline address book (OAB) data from server to client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e2bc4-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e2bc4-124">Header files</span></span>

<span data-ttu-id="e2bc4-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e2bc4-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="e2bc4-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e2bc4-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="e2bc4-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e2bc4-127">Mapitags.h</span></span>
  
> <span data-ttu-id="e2bc4-128">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e2bc4-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e2bc4-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="e2bc4-129">See also</span></span>



[<span data-ttu-id="e2bc4-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e2bc4-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e2bc4-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e2bc4-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e2bc4-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e2bc4-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e2bc4-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e2bc4-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

