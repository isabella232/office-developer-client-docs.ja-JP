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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a88f05bab3f3effc60c0bcca24910106e6849903
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576809"
---
# <a name="pidtagscheduleinfodontmaildelegates-canonical-property"></a><span data-ttu-id="c7474-103">PidTagScheduleInfoDontMailDelegates 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c7474-103">PidTagScheduleInfoDontMailDelegates Canonical Property</span></span>

  
  
<span data-ttu-id="c7474-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7474-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7474-105">代理人が更新を受信しない場合、TRUE が格納されます。</span><span class="sxs-lookup"><span data-stu-id="c7474-105">Contains TRUE if the delegate does not want to receive updates.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c7474-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c7474-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c7474-107">PR_SCHDINFO_DONT_MAIL_DELEGATES</span><span class="sxs-lookup"><span data-stu-id="c7474-107">PR_SCHDINFO_DONT_MAIL_DELEGATES</span></span>  <br/> |
|<span data-ttu-id="c7474-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c7474-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c7474-109">0x6843</span><span class="sxs-lookup"><span data-stu-id="c7474-109">0x6843</span></span>  <br/> |
|<span data-ttu-id="c7474-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c7474-110">Data type:</span></span>  <br/> |<span data-ttu-id="c7474-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c7474-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="c7474-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="c7474-112">Area:</span></span>  <br/> |<span data-ttu-id="c7474-113">空き/予約済み</span><span class="sxs-lookup"><span data-stu-id="c7474-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c7474-114">注釈</span><span class="sxs-lookup"><span data-stu-id="c7474-114">Remarks</span></span>

<span data-ttu-id="c7474-115">代理人の情報オブジェクトにこのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c7474-115">This property must be set in the delegate information object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c7474-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c7474-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c7474-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c7474-117">Protocol specifications</span></span>

<span data-ttu-id="c7474-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c7474-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c7474-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="c7474-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c7474-120">[[MS OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c7474-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c7474-121">ユーザーまたはリソースの可用性を発行します。</span><span class="sxs-lookup"><span data-stu-id="c7474-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c7474-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c7474-122">Header files</span></span>

<span data-ttu-id="c7474-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c7474-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="c7474-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c7474-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="c7474-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c7474-125">Mapitags.h</span></span>
  
> <span data-ttu-id="c7474-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c7474-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c7474-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="c7474-127">See also</span></span>



[<span data-ttu-id="c7474-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c7474-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c7474-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c7474-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c7474-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c7474-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c7474-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c7474-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

