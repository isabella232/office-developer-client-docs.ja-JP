---
title: PidTagSubfolders 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubfolders
api_type:
- COM
ms.assetid: b456b07b-4d83-46bf-a305-4f322ea7dbd1
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 93e5510802fe5ff0327d7ed3fc702fa61cd3c1c4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565579"
---
# <a name="pidtagsubfolders-canonical-property"></a><span data-ttu-id="7973f-103">PidTagSubfolders 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7973f-103">PidTagSubfolders Canonical Property</span></span>

  
  
<span data-ttu-id="7973f-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7973f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7973f-105">フォルダーにサブフォルダーが含まれている場合、TRUE が格納されます。</span><span class="sxs-lookup"><span data-stu-id="7973f-105">Contains TRUE if a folder contains subfolders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7973f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7973f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7973f-107">PR_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="7973f-107">PR_SUBFOLDERS</span></span>  <br/> |
|<span data-ttu-id="7973f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7973f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7973f-109">0x360A</span><span class="sxs-lookup"><span data-stu-id="7973f-109">0x360A</span></span>  <br/> |
|<span data-ttu-id="7973f-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="7973f-110">Data type:</span></span>  <br/> |<span data-ttu-id="7973f-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="7973f-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="7973f-112">領域:</span><span class="sxs-lookup"><span data-stu-id="7973f-112">Area:</span></span>  <br/> |<span data-ttu-id="7973f-113">MAPI のコンテナー</span><span class="sxs-lookup"><span data-stu-id="7973f-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7973f-114">注釈</span><span class="sxs-lookup"><span data-stu-id="7973f-114">Remarks</span></span>

<span data-ttu-id="7973f-115">メッセージ ・ ストアは、すべてのフォルダーに対してこのプロパティを指定しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="7973f-115">Message stores must supply this property for all folders.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7973f-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7973f-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7973f-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7973f-117">Protocol specifications</span></span>

<span data-ttu-id="7973f-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7973f-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7973f-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="7973f-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7973f-120">[[MS OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7973f-120">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7973f-121">フォルダーの操作を処理します。</span><span class="sxs-lookup"><span data-stu-id="7973f-121">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7973f-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="7973f-122">Header files</span></span>

<span data-ttu-id="7973f-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7973f-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="7973f-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7973f-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="7973f-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7973f-125">Mapitags.h</span></span>
  
> <span data-ttu-id="7973f-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7973f-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7973f-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="7973f-127">See also</span></span>



[<span data-ttu-id="7973f-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7973f-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7973f-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7973f-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7973f-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7973f-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7973f-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7973f-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

