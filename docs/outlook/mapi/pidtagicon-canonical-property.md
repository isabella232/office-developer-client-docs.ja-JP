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
ms.openlocfilehash: ad8d6934b5e57429de5039e9420742caa9dd4294
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397696"
---
# <a name="pidtagicon-canonical-property"></a><span data-ttu-id="5d7ea-103">PidTagIcon 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5d7ea-103">PidTagIcon Canonical Property</span></span>

  
  
<span data-ttu-id="5d7ea-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d7ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d7ea-105">フォームのフル サイズのアイコンのビットマップが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5d7ea-105">Contains a bitmap of a full size icon for a form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5d7ea-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5d7ea-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5d7ea-107">PR_ICON</span><span class="sxs-lookup"><span data-stu-id="5d7ea-107">PR_ICON</span></span>  <br/> |
|<span data-ttu-id="5d7ea-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="5d7ea-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5d7ea-109">0x0FFD</span><span class="sxs-lookup"><span data-stu-id="5d7ea-109">0x0FFD</span></span>  <br/> |
|<span data-ttu-id="5d7ea-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5d7ea-110">Data type:</span></span>  <br/> |<span data-ttu-id="5d7ea-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5d7ea-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5d7ea-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="5d7ea-112">Area:</span></span>  <br/> |<span data-ttu-id="5d7ea-113">MAPI 以外から送信できます。</span><span class="sxs-lookup"><span data-stu-id="5d7ea-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d7ea-114">備考</span><span class="sxs-lookup"><span data-stu-id="5d7ea-114">Remarks</span></span>

<span data-ttu-id="5d7ea-115">このプロパティには、内容と同じアイコンの 32 × 32 ピクセルのイメージが含まれているのです。ICO ファイルです。</span><span class="sxs-lookup"><span data-stu-id="5d7ea-115">This property contains a 32 × 32 pixel image of an icon, the same as the contents of a .ICO file.</span></span> <span data-ttu-id="5d7ea-116">このプロパティは通常からコピーします。ICO ファイルがフォーム構成ファイルの該当する [説明] セクションの LargeIcon 行で指定します。</span><span class="sxs-lookup"><span data-stu-id="5d7ea-116">This property is normally copied from the .ICO file specified in the LargeIcon line of the appropriate [Description] section of the form configuration file.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5d7ea-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5d7ea-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5d7ea-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5d7ea-118">Protocol specifications</span></span>

<span data-ttu-id="5d7ea-119">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5d7ea-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5d7ea-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="5d7ea-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5d7ea-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5d7ea-121">Header files</span></span>

<span data-ttu-id="5d7ea-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5d7ea-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="5d7ea-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5d7ea-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="5d7ea-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5d7ea-124">Mapitags.h</span></span>
  
> <span data-ttu-id="5d7ea-125">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5d7ea-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5d7ea-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="5d7ea-126">See also</span></span>



[<span data-ttu-id="5d7ea-127">PidTagMiniIcon 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5d7ea-127">PidTagMiniIcon Canonical Property</span></span>](pidtagminiicon-canonical-property.md)


[<span data-ttu-id="5d7ea-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5d7ea-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5d7ea-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5d7ea-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5d7ea-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5d7ea-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5d7ea-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5d7ea-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

