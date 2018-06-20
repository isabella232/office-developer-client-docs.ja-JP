---
title: PidTagIcon の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIcon
api_type:
- HeaderDef
ms.assetid: 815dabf3-3cac-40e1-b6ff-51db2ff5096a
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0aa5873d98b7ae9dea1bdaffc37f7996262b6062
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802832"
---
# <a name="pidtagicon-canonical-property"></a><span data-ttu-id="31cc5-103">PidTagIcon の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="31cc5-103">PidTagIcon Canonical Property</span></span>

  
  
<span data-ttu-id="31cc5-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="31cc5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="31cc5-105">フォームのフル サイズのアイコンのビットマップが含まれています。</span><span class="sxs-lookup"><span data-stu-id="31cc5-105">Contains a bitmap of a full size icon for a form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="31cc5-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="31cc5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="31cc5-107">PR_ICON</span><span class="sxs-lookup"><span data-stu-id="31cc5-107">PR_ICON</span></span>  <br/> |
|<span data-ttu-id="31cc5-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="31cc5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="31cc5-109">0x0FFD</span><span class="sxs-lookup"><span data-stu-id="31cc5-109">0x0FFD</span></span>  <br/> |
|<span data-ttu-id="31cc5-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="31cc5-110">Data type:</span></span>  <br/> |<span data-ttu-id="31cc5-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="31cc5-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="31cc5-112">領域:</span><span class="sxs-lookup"><span data-stu-id="31cc5-112">Area:</span></span>  <br/> |<span data-ttu-id="31cc5-113">MAPI 以外から送信できます。</span><span class="sxs-lookup"><span data-stu-id="31cc5-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="31cc5-114">備考</span><span class="sxs-lookup"><span data-stu-id="31cc5-114">Remarks</span></span>

<span data-ttu-id="31cc5-115">このプロパティには、内容と同じアイコンの 32 × 32 ピクセルのイメージが含まれているのです。ICO ファイルです。</span><span class="sxs-lookup"><span data-stu-id="31cc5-115">This property contains a 32 × 32 pixel image of an icon, the same as the contents of a .ICO file.</span></span> <span data-ttu-id="31cc5-116">このプロパティは通常からコピーします。ICO ファイルがフォーム構成ファイルの該当する [説明] セクションの LargeIcon 行で指定します。</span><span class="sxs-lookup"><span data-stu-id="31cc5-116">This property is normally copied from the .ICO file specified in the LargeIcon line of the appropriate [Description] section of the form configuration file.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="31cc5-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="31cc5-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="31cc5-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="31cc5-118">Protocol specifications</span></span>

<span data-ttu-id="31cc5-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="31cc5-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="31cc5-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="31cc5-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="31cc5-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="31cc5-121">Header files</span></span>

<span data-ttu-id="31cc5-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="31cc5-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="31cc5-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="31cc5-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="31cc5-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="31cc5-124">Mapitags.h</span></span>
  
> <span data-ttu-id="31cc5-125">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="31cc5-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="31cc5-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="31cc5-126">See also</span></span>



[<span data-ttu-id="31cc5-127">PidTagMiniIcon の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="31cc5-127">PidTagMiniIcon Canonical Property</span></span>](pidtagminiicon-canonical-property.md)


[<span data-ttu-id="31cc5-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="31cc5-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="31cc5-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="31cc5-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="31cc5-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="31cc5-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="31cc5-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="31cc5-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

