---
title: PidTagExpiryTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExpiryTime
api_type:
- HeaderDef
ms.assetid: 6e4d4ee9-c6b1-4987-b02e-684c2af3d21c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8d6fa58e61dde30292487c95fb8a74d568a3bbeb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388470"
---
# <a name="pidtagexpirytime-canonical-property"></a><span data-ttu-id="7c055-103">PidTagExpiryTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7c055-103">PidTagExpiryTime Canonical Property</span></span>

  
  
<span data-ttu-id="7c055-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c055-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c055-105">日付と時刻のメッセージング システムがメッセージの内容を無効にするとが含まれています。</span><span class="sxs-lookup"><span data-stu-id="7c055-105">Contains the date and time when the messaging system can invalidate the content of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7c055-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7c055-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7c055-107">PR_EXPIRY_TIME</span><span class="sxs-lookup"><span data-stu-id="7c055-107">PR_EXPIRY_TIME</span></span>  <br/> |
|<span data-ttu-id="7c055-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7c055-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7c055-109">0x0015</span><span class="sxs-lookup"><span data-stu-id="7c055-109">0x0015</span></span>  <br/> |
|<span data-ttu-id="7c055-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="7c055-110">Data type:</span></span>  <br/> |<span data-ttu-id="7c055-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="7c055-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="7c055-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="7c055-112">Area:</span></span>  <br/> |<span data-ttu-id="7c055-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="7c055-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7c055-114">備考</span><span class="sxs-lookup"><span data-stu-id="7c055-114">Remarks</span></span>

<span data-ttu-id="7c055-115">処理でメッセージング システムに配信された個人間のメッセージを送信するこのプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="7c055-115">This property is used to direct the messaging system in handling delivered interpersonal messages.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7c055-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7c055-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7c055-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7c055-117">Protocol specifications</span></span>

<span data-ttu-id="7c055-118">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7c055-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7c055-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="7c055-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7c055-120">[[MS OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7c055-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7c055-121">プロパティは、電子メール メッセージの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="7c055-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7c055-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="7c055-122">Header files</span></span>

<span data-ttu-id="7c055-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7c055-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="7c055-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7c055-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="7c055-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7c055-125">Mapitags.h</span></span>
  
> <span data-ttu-id="7c055-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7c055-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7c055-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="7c055-127">See also</span></span>



[<span data-ttu-id="7c055-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7c055-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7c055-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7c055-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7c055-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7c055-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7c055-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7c055-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

