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
ms.openlocfilehash: 5138f5d255f6a90d2891fe2cf5ce92513463fa31
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389800"
---
# <a name="pidtagaccesslevel-canonical-property"></a><span data-ttu-id="a8f47-103">PidTagAccessLevel 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a8f47-103">PidTagAccessLevel Canonical Property</span></span>

  
  
<span data-ttu-id="a8f47-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8f47-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8f47-105">オブジェクトへのクライアントのアクセス レベルを示します。</span><span class="sxs-lookup"><span data-stu-id="a8f47-105">Indicates the client's access level to the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a8f47-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a8f47-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a8f47-107">PR_ACCESS_LEVEL</span><span class="sxs-lookup"><span data-stu-id="a8f47-107">PR_ACCESS_LEVEL</span></span>  <br/> |
|<span data-ttu-id="a8f47-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a8f47-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a8f47-109">0x0FF7</span><span class="sxs-lookup"><span data-stu-id="a8f47-109">0x0FF7</span></span>  <br/> |
|<span data-ttu-id="a8f47-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a8f47-110">Data type:</span></span>  <br/> |<span data-ttu-id="a8f47-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a8f47-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a8f47-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="a8f47-112">Area:</span></span>  <br/> |<span data-ttu-id="a8f47-113">コントロール プロパティにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="a8f47-113">Access Control Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a8f47-114">備考</span><span class="sxs-lookup"><span data-stu-id="a8f47-114">Remarks</span></span>

<span data-ttu-id="a8f47-115">このプロパティは、クライアントに対しては読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="a8f47-115">This property is read-only for the client.</span></span> <span data-ttu-id="a8f47-116">次の値のいずれかを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a8f47-116">It must be one of the following values:</span></span>
  
|<span data-ttu-id="a8f47-117">**値**</span><span class="sxs-lookup"><span data-stu-id="a8f47-117">**Value**</span></span>|<span data-ttu-id="a8f47-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="a8f47-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a8f47-119">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8f47-119">0x00000000</span></span>  <br/> |<span data-ttu-id="a8f47-120">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="a8f47-120">Read-Only</span></span>  <br/> |
|<span data-ttu-id="a8f47-121">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a8f47-121">0x00000001</span></span>  <br/> |<span data-ttu-id="a8f47-122">Modify</span><span class="sxs-lookup"><span data-stu-id="a8f47-122">Modify</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="a8f47-123">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a8f47-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a8f47-124">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a8f47-124">Protocol specifications</span></span>

<span data-ttu-id="a8f47-125">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a8f47-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a8f47-126">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="a8f47-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a8f47-127">[[MS OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a8f47-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a8f47-128">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="a8f47-128">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a8f47-129">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="a8f47-129">Header files</span></span>

<span data-ttu-id="a8f47-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a8f47-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="a8f47-131">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a8f47-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="a8f47-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a8f47-132">Mapitags.h</span></span>
  
> <span data-ttu-id="a8f47-133">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a8f47-133">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a8f47-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="a8f47-134">See also</span></span>



[<span data-ttu-id="a8f47-135">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a8f47-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a8f47-136">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a8f47-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a8f47-137">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a8f47-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a8f47-138">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a8f47-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

