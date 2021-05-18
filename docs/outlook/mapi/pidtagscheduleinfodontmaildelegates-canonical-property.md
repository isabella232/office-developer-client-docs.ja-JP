---
title: PidTagScheduleInfoDontMailDelegates 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDontMailDelegates
api_type:
- COM
ms.assetid: e932966e-cb7a-4d8b-8f06-6406fce1b3e6
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f5965d75e72cecf11216ae785632f7e830a98178
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330108"
---
# <a name="pidtagscheduleinfodontmaildelegates-canonical-property"></a><span data-ttu-id="e0097-103">PidTagScheduleInfoDontMailDelegates 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e0097-103">PidTagScheduleInfoDontMailDelegates Canonical Property</span></span>

  
  
<span data-ttu-id="e0097-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0097-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0097-105">代理人が更新プログラムを受信しない場合は TRUE を含む。</span><span class="sxs-lookup"><span data-stu-id="e0097-105">Contains TRUE if the delegate does not want to receive updates.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e0097-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e0097-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e0097-107">PR_SCHDINFO_DONT_MAIL_DELEGATES</span><span class="sxs-lookup"><span data-stu-id="e0097-107">PR_SCHDINFO_DONT_MAIL_DELEGATES</span></span>  <br/> |
|<span data-ttu-id="e0097-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e0097-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e0097-109">0x6843</span><span class="sxs-lookup"><span data-stu-id="e0097-109">0x6843</span></span>  <br/> |
|<span data-ttu-id="e0097-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e0097-110">Data type:</span></span>  <br/> |<span data-ttu-id="e0097-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e0097-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="e0097-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="e0097-112">Area:</span></span>  <br/> |<span data-ttu-id="e0097-113">空き時間情報</span><span class="sxs-lookup"><span data-stu-id="e0097-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0097-114">注釈</span><span class="sxs-lookup"><span data-stu-id="e0097-114">Remarks</span></span>

<span data-ttu-id="e0097-115">このプロパティは、デリゲート情報オブジェクトで設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0097-115">This property must be set in the delegate information object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e0097-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e0097-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e0097-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e0097-117">Protocol specifications</span></span>

<span data-ttu-id="e0097-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0097-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0097-119">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="e0097-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e0097-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0097-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0097-121">ユーザーまたはリソースの可用性を公開します。</span><span class="sxs-lookup"><span data-stu-id="e0097-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e0097-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e0097-122">Header files</span></span>

<span data-ttu-id="e0097-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e0097-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="e0097-124">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e0097-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="e0097-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e0097-125">Mapitags.h</span></span>
  
> <span data-ttu-id="e0097-126">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="e0097-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e0097-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="e0097-127">See also</span></span>



[<span data-ttu-id="e0097-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e0097-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e0097-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e0097-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e0097-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="e0097-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e0097-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="e0097-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

