---
title: PidTagReportTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportTime
api_type:
- COM
ms.assetid: b3646505-a9f0-4a72-8277-b238c909f66f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 95972d53f20f432bc8007f8bbc6734889773f938
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803351"
---
# <a name="pidtagreporttime-canonical-property"></a><span data-ttu-id="303c9-103">PidTagReportTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="303c9-103">PidTagReportTime Canonical Property</span></span>

  
  
<span data-ttu-id="303c9-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="303c9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="303c9-105">メッセージング システムにレポートが生成されたときの日時が含まれています。</span><span class="sxs-lookup"><span data-stu-id="303c9-105">Contains the date and time when the messaging system generated a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="303c9-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="303c9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="303c9-107">PR_REPORT_TIME</span><span class="sxs-lookup"><span data-stu-id="303c9-107">PR_REPORT_TIME</span></span>  <br/> |
|<span data-ttu-id="303c9-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="303c9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="303c9-109">0x0032</span><span class="sxs-lookup"><span data-stu-id="303c9-109">0x0032</span></span>  <br/> |
|<span data-ttu-id="303c9-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="303c9-110">Data type:</span></span>  <br/> |<span data-ttu-id="303c9-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="303c9-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="303c9-112">領域:</span><span class="sxs-lookup"><span data-stu-id="303c9-112">Area:</span></span>  <br/> |<span data-ttu-id="303c9-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="303c9-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="303c9-114">注釈</span><span class="sxs-lookup"><span data-stu-id="303c9-114">Remarks</span></span>

<span data-ttu-id="303c9-115">このプロパティは、配信し、配信不能レポートの受信者ごとのプロパティとレポートの読み取りと nonread のメッセージごとのプロパティを表します。</span><span class="sxs-lookup"><span data-stu-id="303c9-115">This property represents a per-recipient property on delivery and nondelivery reports and a per-message property on read and nonread reports.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="303c9-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="303c9-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="303c9-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="303c9-117">Protocol specifications</span></span>

<span data-ttu-id="303c9-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="303c9-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="303c9-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="303c9-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="303c9-120">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="303c9-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="303c9-121">プロパティは、電子メール メッセージの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="303c9-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="303c9-122">[[MS OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="303c9-122">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="303c9-123">許可/禁止リストの処理、迷惑メール メッセージの決定を可能にします。</span><span class="sxs-lookup"><span data-stu-id="303c9-123">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="303c9-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="303c9-124">Header files</span></span>

<span data-ttu-id="303c9-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="303c9-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="303c9-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="303c9-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="303c9-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="303c9-127">Mapitags.h</span></span>
  
> <span data-ttu-id="303c9-128">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="303c9-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="303c9-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="303c9-129">See also</span></span>



[<span data-ttu-id="303c9-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="303c9-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="303c9-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="303c9-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="303c9-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="303c9-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="303c9-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="303c9-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

