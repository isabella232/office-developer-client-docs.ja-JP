---
title: PidTagScheduleInfoDontMailDelegates の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 6bcda9c6281e25f3bae2f9c1dda2f8defb024b57
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803470"
---
# <a name="pidtagscheduleinfodontmaildelegates-canonical-property"></a><span data-ttu-id="770bb-103">PidTagScheduleInfoDontMailDelegates の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="770bb-103">PidTagScheduleInfoDontMailDelegates Canonical Property</span></span>

  
  
<span data-ttu-id="770bb-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="770bb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="770bb-105">代理人が更新を受信しない場合、TRUE が格納されます。</span><span class="sxs-lookup"><span data-stu-id="770bb-105">Contains TRUE if the delegate does not want to receive updates.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="770bb-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="770bb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="770bb-107">PR_SCHDINFO_DONT_MAIL_DELEGATES</span><span class="sxs-lookup"><span data-stu-id="770bb-107">PR_SCHDINFO_DONT_MAIL_DELEGATES</span></span>  <br/> |
|<span data-ttu-id="770bb-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="770bb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="770bb-109">0x6843</span><span class="sxs-lookup"><span data-stu-id="770bb-109">0x6843</span></span>  <br/> |
|<span data-ttu-id="770bb-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="770bb-110">Data type:</span></span>  <br/> |<span data-ttu-id="770bb-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="770bb-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="770bb-112">領域:</span><span class="sxs-lookup"><span data-stu-id="770bb-112">Area:</span></span>  <br/> |<span data-ttu-id="770bb-113">空き/予約済み</span><span class="sxs-lookup"><span data-stu-id="770bb-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="770bb-114">備考</span><span class="sxs-lookup"><span data-stu-id="770bb-114">Remarks</span></span>

<span data-ttu-id="770bb-115">代理人の情報オブジェクトにこのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="770bb-115">This property must be set in the delegate information object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="770bb-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="770bb-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="770bb-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="770bb-117">Protocol specifications</span></span>

<span data-ttu-id="770bb-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="770bb-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="770bb-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="770bb-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="770bb-120">[[MS OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="770bb-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="770bb-121">ユーザーまたはリソースの可用性を発行します。</span><span class="sxs-lookup"><span data-stu-id="770bb-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="770bb-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="770bb-122">Header files</span></span>

<span data-ttu-id="770bb-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="770bb-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="770bb-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="770bb-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="770bb-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="770bb-125">Mapitags.h</span></span>
  
> <span data-ttu-id="770bb-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="770bb-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="770bb-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="770bb-127">See also</span></span>



[<span data-ttu-id="770bb-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="770bb-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="770bb-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="770bb-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="770bb-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="770bb-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="770bb-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="770bb-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

