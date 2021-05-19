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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8de14542c0d2a4e6d95fb4258697b827f82b8d06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339250"
---
# <a name="pidtagsubfolders-canonical-property"></a><span data-ttu-id="9423b-103">PidTagSubfolders 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9423b-103">PidTagSubfolders Canonical Property</span></span>

  
  
<span data-ttu-id="9423b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9423b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9423b-105">フォルダーにサブフォルダーが含まれている場合は TRUE を含む。</span><span class="sxs-lookup"><span data-stu-id="9423b-105">Contains TRUE if a folder contains subfolders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9423b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9423b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9423b-107">PR_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="9423b-107">PR_SUBFOLDERS</span></span>  <br/> |
|<span data-ttu-id="9423b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="9423b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9423b-109">0x360A</span><span class="sxs-lookup"><span data-stu-id="9423b-109">0x360A</span></span>  <br/> |
|<span data-ttu-id="9423b-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9423b-110">Data type:</span></span>  <br/> |<span data-ttu-id="9423b-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="9423b-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="9423b-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="9423b-112">Area:</span></span>  <br/> |<span data-ttu-id="9423b-113">MAPI コンテナー</span><span class="sxs-lookup"><span data-stu-id="9423b-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9423b-114">注釈</span><span class="sxs-lookup"><span data-stu-id="9423b-114">Remarks</span></span>

<span data-ttu-id="9423b-115">メッセージ ストアは、すべてのフォルダーに対してこのプロパティを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9423b-115">Message stores must supply this property for all folders.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9423b-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9423b-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9423b-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="9423b-117">Protocol specifications</span></span>

<span data-ttu-id="9423b-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9423b-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9423b-119">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="9423b-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9423b-120">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9423b-120">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9423b-121">フォルダー操作を処理します。</span><span class="sxs-lookup"><span data-stu-id="9423b-121">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9423b-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="9423b-122">Header files</span></span>

<span data-ttu-id="9423b-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9423b-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="9423b-124">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9423b-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="9423b-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9423b-125">Mapitags.h</span></span>
  
> <span data-ttu-id="9423b-126">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="9423b-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9423b-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="9423b-127">See also</span></span>



[<span data-ttu-id="9423b-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="9423b-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9423b-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9423b-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9423b-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="9423b-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9423b-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="9423b-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

