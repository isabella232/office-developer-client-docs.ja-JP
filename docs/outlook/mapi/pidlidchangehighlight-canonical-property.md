---
title: PidLidChangeHighlight 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidChangeHighlight
api_type:
- COM
ms.assetid: cd57a5be-5550-4492-acb9-52255fac9014
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: bbac700c2bf5a0e17967cbf94b68b03627a47256
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344941"
---
# <a name="pidlidchangehighlight-canonical-property"></a><span data-ttu-id="8772a-103">PidLidChangeHighlight 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8772a-103">PidLidChangeHighlight Canonical Property</span></span>

  
  
<span data-ttu-id="8772a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8772a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8772a-105">会議オブジェクトがどのように変更されたかを示すビットフィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="8772a-105">Specifies a bit field that indicates how the meeting object changed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8772a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8772a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8772a-107">dispidchangehighlight 表示</span><span class="sxs-lookup"><span data-stu-id="8772a-107">dispidChangeHighlight</span></span>  <br/> |
|<span data-ttu-id="8772a-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="8772a-108">Property set:</span></span>  <br/> |<span data-ttu-id="8772a-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="8772a-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="8772a-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="8772a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8772a-111">0x00008204</span><span class="sxs-lookup"><span data-stu-id="8772a-111">0x00008204</span></span>  <br/> |
|<span data-ttu-id="8772a-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8772a-112">Data type:</span></span>  <br/> |<span data-ttu-id="8772a-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8772a-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8772a-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="8772a-114">Area:</span></span>  <br/> |<span data-ttu-id="8772a-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="8772a-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8772a-116">解説</span><span class="sxs-lookup"><span data-stu-id="8772a-116">Remarks</span></span>

<span data-ttu-id="8772a-117">このプロパティは必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="8772a-117">This property is not required.</span></span> <span data-ttu-id="8772a-118">設定できる各フラグの詳細については、「 [[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)」を参考にしてください。</span><span class="sxs-lookup"><span data-stu-id="8772a-118">The individual flags that can be set are detailed in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8772a-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8772a-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8772a-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8772a-120">Protocol specifications</span></span>

<span data-ttu-id="8772a-121">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8772a-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8772a-122">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="8772a-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8772a-123">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8772a-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8772a-124">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="8772a-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8772a-125">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="8772a-125">Header files</span></span>

<span data-ttu-id="8772a-126">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8772a-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="8772a-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8772a-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8772a-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="8772a-128">See also</span></span>



[<span data-ttu-id="8772a-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="8772a-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8772a-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8772a-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8772a-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8772a-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8772a-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8772a-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

