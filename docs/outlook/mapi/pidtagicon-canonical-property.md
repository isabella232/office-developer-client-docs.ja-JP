---
title: PidTagIcon 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0aa5873d98b7ae9dea1bdaffc37f7996262b6062
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802832"
---
# <a name="pidtagicon-canonical-property"></a><span data-ttu-id="f7734-103">PidTagIcon 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f7734-103">PidTagIcon Canonical Property</span></span>

  
  
<span data-ttu-id="f7734-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f7734-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f7734-105">フォームのフル サイズのアイコンのビットマップが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f7734-105">Contains a bitmap of a full size icon for a form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f7734-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f7734-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f7734-107">PR_ICON</span><span class="sxs-lookup"><span data-stu-id="f7734-107">PR_ICON</span></span>  <br/> |
|<span data-ttu-id="f7734-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f7734-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f7734-109">0x0FFD</span><span class="sxs-lookup"><span data-stu-id="f7734-109">0x0FFD</span></span>  <br/> |
|<span data-ttu-id="f7734-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f7734-110">Data type:</span></span>  <br/> |<span data-ttu-id="f7734-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f7734-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f7734-112">領域:</span><span class="sxs-lookup"><span data-stu-id="f7734-112">Area:</span></span>  <br/> |<span data-ttu-id="f7734-113">MAPI 以外から送信できます。</span><span class="sxs-lookup"><span data-stu-id="f7734-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f7734-114">注釈</span><span class="sxs-lookup"><span data-stu-id="f7734-114">Remarks</span></span>

<span data-ttu-id="f7734-115">このプロパティには、内容と同じアイコンの 32 × 32 ピクセルのイメージが含まれているのです。ICO ファイルです。</span><span class="sxs-lookup"><span data-stu-id="f7734-115">This property contains a 32 × 32 pixel image of an icon, the same as the contents of a .ICO file.</span></span> <span data-ttu-id="f7734-116">このプロパティは通常からコピーします。ICO ファイルがフォーム構成ファイルの該当する [説明] セクションの LargeIcon 行で指定します。</span><span class="sxs-lookup"><span data-stu-id="f7734-116">This property is normally copied from the .ICO file specified in the LargeIcon line of the appropriate [Description] section of the form configuration file.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f7734-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f7734-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f7734-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f7734-118">Protocol specifications</span></span>

<span data-ttu-id="f7734-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7734-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7734-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="f7734-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f7734-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f7734-121">Header files</span></span>

<span data-ttu-id="f7734-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f7734-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="f7734-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f7734-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="f7734-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f7734-124">Mapitags.h</span></span>
  
> <span data-ttu-id="f7734-125">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f7734-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f7734-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="f7734-126">See also</span></span>



[<span data-ttu-id="f7734-127">PidTagMiniIcon 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f7734-127">PidTagMiniIcon Canonical Property</span></span>](pidtagminiicon-canonical-property.md)


[<span data-ttu-id="f7734-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f7734-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f7734-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f7734-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f7734-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f7734-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f7734-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f7734-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

