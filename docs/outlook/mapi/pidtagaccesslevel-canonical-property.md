---
title: PidTagAccessLevel 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccessLevel
api_type:
- HeaderDef
ms.assetid: 8f7119c7-ffc3-47cf-aa1b-b4e56bcc5a24
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 71c0bbec13c869c1401c60834f30ca61360c8b38
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802411"
---
# <a name="pidtagaccesslevel-canonical-property"></a><span data-ttu-id="be863-103">PidTagAccessLevel 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="be863-103">PidTagAccessLevel Canonical Property</span></span>

  
  
<span data-ttu-id="be863-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="be863-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="be863-105">オブジェクトへのクライアントのアクセス レベルを示します。</span><span class="sxs-lookup"><span data-stu-id="be863-105">Indicates the client's access level to the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="be863-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="be863-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="be863-107">PR_ACCESS_LEVEL</span><span class="sxs-lookup"><span data-stu-id="be863-107">PR_ACCESS_LEVEL</span></span>  <br/> |
|<span data-ttu-id="be863-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="be863-108">Identifier:</span></span>  <br/> |<span data-ttu-id="be863-109">0x0FF7</span><span class="sxs-lookup"><span data-stu-id="be863-109">0x0FF7</span></span>  <br/> |
|<span data-ttu-id="be863-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="be863-110">Data type:</span></span>  <br/> |<span data-ttu-id="be863-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="be863-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="be863-112">領域:</span><span class="sxs-lookup"><span data-stu-id="be863-112">Area:</span></span>  <br/> |<span data-ttu-id="be863-113">コントロール プロパティにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="be863-113">Access Control Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be863-114">注釈</span><span class="sxs-lookup"><span data-stu-id="be863-114">Remarks</span></span>

<span data-ttu-id="be863-115">このプロパティは、クライアントに対しては読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="be863-115">This property is read-only for the client.</span></span> <span data-ttu-id="be863-116">次の値のいずれかを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="be863-116">It must be one of the following values:</span></span>
  
|<span data-ttu-id="be863-117">**値**</span><span class="sxs-lookup"><span data-stu-id="be863-117">**Value**</span></span>|<span data-ttu-id="be863-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="be863-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="be863-119">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be863-119">0x00000000</span></span>  <br/> |<span data-ttu-id="be863-120">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="be863-120">Read-Only</span></span>  <br/> |
|<span data-ttu-id="be863-121">0x00000001</span><span class="sxs-lookup"><span data-stu-id="be863-121">0x00000001</span></span>  <br/> |<span data-ttu-id="be863-122">Modify</span><span class="sxs-lookup"><span data-stu-id="be863-122">Modify</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="be863-123">関連リソース</span><span class="sxs-lookup"><span data-stu-id="be863-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="be863-124">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="be863-124">Protocol specifications</span></span>

<span data-ttu-id="be863-125">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="be863-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="be863-126">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="be863-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="be863-127">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="be863-127">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="be863-128">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="be863-128">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="be863-129">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="be863-129">Header files</span></span>

<span data-ttu-id="be863-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="be863-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="be863-131">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="be863-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="be863-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="be863-132">Mapitags.h</span></span>
  
> <span data-ttu-id="be863-133">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="be863-133">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="be863-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="be863-134">See also</span></span>



[<span data-ttu-id="be863-135">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="be863-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="be863-136">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="be863-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="be863-137">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="be863-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="be863-138">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="be863-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

