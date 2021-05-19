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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ad8d6934b5e57429de5039e9420742caa9dd4294
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356729"
---
# <a name="pidtagicon-canonical-property"></a><span data-ttu-id="08cbb-103">PidTagIcon 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="08cbb-103">PidTagIcon Canonical Property</span></span>

  
  
<span data-ttu-id="08cbb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08cbb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08cbb-105">フォームのフル サイズ アイコンのビットマップを含む。</span><span class="sxs-lookup"><span data-stu-id="08cbb-105">Contains a bitmap of a full size icon for a form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="08cbb-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="08cbb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="08cbb-107">PR_ICON</span><span class="sxs-lookup"><span data-stu-id="08cbb-107">PR_ICON</span></span>  <br/> |
|<span data-ttu-id="08cbb-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="08cbb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="08cbb-109">0x0FFD</span><span class="sxs-lookup"><span data-stu-id="08cbb-109">0x0FFD</span></span>  <br/> |
|<span data-ttu-id="08cbb-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="08cbb-110">Data type:</span></span>  <br/> |<span data-ttu-id="08cbb-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="08cbb-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="08cbb-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="08cbb-112">Area:</span></span>  <br/> |<span data-ttu-id="08cbb-113">MAPI 送信不可</span><span class="sxs-lookup"><span data-stu-id="08cbb-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08cbb-114">注釈</span><span class="sxs-lookup"><span data-stu-id="08cbb-114">Remarks</span></span>

<span data-ttu-id="08cbb-115">このプロパティには、アイコンの 32 × 32 ピクセルの画像が含まれる。これは、 の内容と同じです。ICO ファイル。</span><span class="sxs-lookup"><span data-stu-id="08cbb-115">This property contains a 32 × 32 pixel image of an icon, the same as the contents of a .ICO file.</span></span> <span data-ttu-id="08cbb-116">このプロパティは、通常は . からコピーされます。フォーム構成ファイルの適切な [Description] セクションの LargeIcon 行で指定された ICO ファイル。</span><span class="sxs-lookup"><span data-stu-id="08cbb-116">This property is normally copied from the .ICO file specified in the LargeIcon line of the appropriate [Description] section of the form configuration file.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="08cbb-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="08cbb-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="08cbb-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="08cbb-118">Protocol specifications</span></span>

<span data-ttu-id="08cbb-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08cbb-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08cbb-120">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="08cbb-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="08cbb-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="08cbb-121">Header files</span></span>

<span data-ttu-id="08cbb-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="08cbb-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="08cbb-123">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="08cbb-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="08cbb-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="08cbb-124">Mapitags.h</span></span>
  
> <span data-ttu-id="08cbb-125">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="08cbb-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="08cbb-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="08cbb-126">See also</span></span>



[<span data-ttu-id="08cbb-127">PidTagMiniIcon 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="08cbb-127">PidTagMiniIcon Canonical Property</span></span>](pidtagminiicon-canonical-property.md)


[<span data-ttu-id="08cbb-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="08cbb-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="08cbb-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="08cbb-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="08cbb-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="08cbb-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="08cbb-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="08cbb-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

