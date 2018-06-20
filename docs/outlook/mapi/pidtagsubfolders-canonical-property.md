---
title: PidTagSubfolders の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: acde7f18324d5642f7b8f8b5aa25721c4019ce3a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803604"
---
# <a name="pidtagsubfolders-canonical-property"></a><span data-ttu-id="6241c-103">PidTagSubfolders の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="6241c-103">PidTagSubfolders Canonical Property</span></span>

  
  
<span data-ttu-id="6241c-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6241c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6241c-105">フォルダーにサブフォルダーが含まれている場合、TRUE が格納されます。</span><span class="sxs-lookup"><span data-stu-id="6241c-105">Contains TRUE if a folder contains subfolders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6241c-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="6241c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6241c-107">PR_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="6241c-107">PR_SUBFOLDERS</span></span>  <br/> |
|<span data-ttu-id="6241c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="6241c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6241c-109">0x360A</span><span class="sxs-lookup"><span data-stu-id="6241c-109">0x360A</span></span>  <br/> |
|<span data-ttu-id="6241c-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="6241c-110">Data type:</span></span>  <br/> |<span data-ttu-id="6241c-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="6241c-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="6241c-112">領域:</span><span class="sxs-lookup"><span data-stu-id="6241c-112">Area:</span></span>  <br/> |<span data-ttu-id="6241c-113">MAPI のコンテナー</span><span class="sxs-lookup"><span data-stu-id="6241c-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6241c-114">備考</span><span class="sxs-lookup"><span data-stu-id="6241c-114">Remarks</span></span>

<span data-ttu-id="6241c-115">メッセージ ・ ストアは、すべてのフォルダーに対してこのプロパティを指定しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="6241c-115">Message stores must supply this property for all folders.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6241c-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6241c-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6241c-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6241c-117">Protocol specifications</span></span>

<span data-ttu-id="6241c-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6241c-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6241c-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="6241c-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6241c-120">[[MS OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6241c-120">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6241c-121">フォルダーの操作を処理します。</span><span class="sxs-lookup"><span data-stu-id="6241c-121">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6241c-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="6241c-122">Header files</span></span>

<span data-ttu-id="6241c-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6241c-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="6241c-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6241c-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="6241c-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6241c-125">Mapitags.h</span></span>
  
> <span data-ttu-id="6241c-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6241c-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6241c-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="6241c-127">See also</span></span>



[<span data-ttu-id="6241c-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6241c-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6241c-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6241c-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6241c-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="6241c-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6241c-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="6241c-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

