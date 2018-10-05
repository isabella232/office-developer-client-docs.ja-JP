---
title: PidLidLogEnd 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogEnd
api_type:
- COM
ms.assetid: 621459ea-adf5-4420-9f0f-6f31b9b95508
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: bed1692a4860d59ba7a6c297ab8e88645b023a86
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398942"
---
# <a name="pidlidlogend-canonical-property"></a><span data-ttu-id="dc1af-103">PidLidLogEnd 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="dc1af-103">PidLidLogEnd Canonical Property</span></span>

  
  
<span data-ttu-id="dc1af-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc1af-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc1af-105">ジャーナル メッセージの終了日時を表します。</span><span class="sxs-lookup"><span data-stu-id="dc1af-105">Represents the end date and time for the journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dc1af-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="dc1af-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dc1af-107">dispidLogEnd</span><span class="sxs-lookup"><span data-stu-id="dc1af-107">dispidLogEnd</span></span>  <br/> |
|<span data-ttu-id="dc1af-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="dc1af-108">Property set:</span></span>  <br/> |<span data-ttu-id="dc1af-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="dc1af-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="dc1af-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="dc1af-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="dc1af-111">0x00008708</span><span class="sxs-lookup"><span data-stu-id="dc1af-111">0x00008708</span></span>  <br/> |
|<span data-ttu-id="dc1af-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="dc1af-112">Data type:</span></span>  <br/> |<span data-ttu-id="dc1af-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="dc1af-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="dc1af-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="dc1af-114">Area:</span></span>  <br/> |<span data-ttu-id="dc1af-115">ジャーナル</span><span class="sxs-lookup"><span data-stu-id="dc1af-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dc1af-116">備考</span><span class="sxs-lookup"><span data-stu-id="dc1af-116">Remarks</span></span>

<span data-ttu-id="dc1af-117">時間活動が終了したときに世界協定時刻の (UTC)、 **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) プロパティに等しい、以上の**dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) のプロパティにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc1af-117">The time when the activity ended in Coordinated Universal Time The (UTC), which must be equal to the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property and greater than or equal to **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="dc1af-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="dc1af-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dc1af-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="dc1af-119">Protocol specifications</span></span>

<span data-ttu-id="dc1af-120">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc1af-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dc1af-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="dc1af-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dc1af-122">[[MS OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc1af-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dc1af-123">プロパティとは、仕訳帳の許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="dc1af-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dc1af-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="dc1af-124">Header files</span></span>

<span data-ttu-id="dc1af-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dc1af-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="dc1af-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="dc1af-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dc1af-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="dc1af-127">See also</span></span>



[<span data-ttu-id="dc1af-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="dc1af-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dc1af-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="dc1af-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dc1af-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="dc1af-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dc1af-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="dc1af-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

