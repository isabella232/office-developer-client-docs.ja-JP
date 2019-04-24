---
title: PidTagXCoordinate 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagXCoordinate
api_type:
- COM
ms.assetid: 030d5c21-ab02-4047-bf2d-9a402a1e9102
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 87df676dccdb067302d62da2bd1fda6b634ed4f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350660"
---
# <a name="pidtagxcoordinate-canonical-property"></a><span data-ttu-id="80067-103">PidTagXCoordinate 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="80067-103">PidTagXCoordinate Canonical Property</span></span>

  
  
<span data-ttu-id="80067-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80067-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80067-105">ダイアログボックスコントロールの開始位置 (左上隅) の x 座標を、標準の Windows ダイアログ単位で格納します。</span><span class="sxs-lookup"><span data-stu-id="80067-105">Contains the x coordinate of the starting position (the upper-left corner) of a dialog box control, in standard Windows dialog units.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="80067-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="80067-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="80067-107">PR_XPOS</span><span class="sxs-lookup"><span data-stu-id="80067-107">PR_XPOS</span></span>  <br/> |
|<span data-ttu-id="80067-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="80067-108">Identifier:</span></span>  <br/> |<span data-ttu-id="80067-109">0x3f05</span><span class="sxs-lookup"><span data-stu-id="80067-109">0x3F05</span></span>  <br/> |
|<span data-ttu-id="80067-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="80067-110">Data type:</span></span>  <br/> |<span data-ttu-id="80067-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="80067-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="80067-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="80067-112">Area:</span></span>  <br/> |<span data-ttu-id="80067-113">MAPI 表示テーブル</span><span class="sxs-lookup"><span data-stu-id="80067-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="80067-114">解説</span><span class="sxs-lookup"><span data-stu-id="80067-114">Remarks</span></span>

<span data-ttu-id="80067-115">このプロパティ、 **PR_YPOS** ([PidTagYCoordinate](pidtagycoordinate-canonical-property.md))、 **PR_DELTAX** ([PidTagDeltaX](pidtagdeltax-canonical-property.md))、および**PR_DELTAY** ([PidTagDeltaY](pidtagdeltay-canonical-property.md)) の各プロパティは、ダイアログボックスコントロールの位置とサイズを設定します。</span><span class="sxs-lookup"><span data-stu-id="80067-115">This property, **PR_YPOS** ([PidTagYCoordinate](pidtagycoordinate-canonical-property.md)), **PR_DELTAX** ([PidTagDeltaX](pidtagdeltax-canonical-property.md)), and **PR_DELTAY** ([PidTagDeltaY](pidtagdeltay-canonical-property.md)) properties position and size the dialog box control.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="80067-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="80067-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="80067-117">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="80067-117">Header files</span></span>

<span data-ttu-id="80067-118">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="80067-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="80067-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="80067-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="80067-120">Mapitags</span><span class="sxs-lookup"><span data-stu-id="80067-120">Mapitags.h</span></span>
  
> <span data-ttu-id="80067-121">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="80067-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="80067-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="80067-122">See also</span></span>



[<span data-ttu-id="80067-123">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="80067-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="80067-124">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="80067-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="80067-125">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="80067-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="80067-126">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="80067-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

