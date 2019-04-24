---
title: PidTagFlagCompleteTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFlagCompleteTime
api_type:
- HeaderDef
ms.assetid: effc738a-30f4-4a5e-b21d-04b50dad1f45
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 5dd0d4c19f30e189218b1aeddd333df58e42102a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316290"
---
# <a name="pidtagflagcompletetime-canonical-property"></a><span data-ttu-id="1006f-103">PidTagFlagCompleteTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1006f-103">PidTagFlagCompleteTime Canonical Property</span></span>

  
  
<span data-ttu-id="1006f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1006f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1006f-105">メッセージオブジェクトに完了のフラグが設定された日付と時刻を協定世界時 (UTC) で指定します。</span><span class="sxs-lookup"><span data-stu-id="1006f-105">Specifies the date and time in Coordinated Universal Time (UTC) that the message object was flagged as completed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1006f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1006f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1006f-107">PR_FLAG_COMPLETE_TIME</span><span class="sxs-lookup"><span data-stu-id="1006f-107">PR_FLAG_COMPLETE_TIME</span></span>  <br/> |
|<span data-ttu-id="1006f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1006f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1006f-109">0x1091</span><span class="sxs-lookup"><span data-stu-id="1006f-109">0x1091</span></span>  <br/> |
|<span data-ttu-id="1006f-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1006f-110">Data type:</span></span>  <br/> |<span data-ttu-id="1006f-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="1006f-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="1006f-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="1006f-112">Area:</span></span>  <br/> |<span data-ttu-id="1006f-113">その他</span><span class="sxs-lookup"><span data-stu-id="1006f-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1006f-114">解説</span><span class="sxs-lookup"><span data-stu-id="1006f-114">Remarks</span></span>

<span data-ttu-id="1006f-115">このプロパティは、メッセージオブジェクトのフラグが設定されていない場合は削除されます。</span><span class="sxs-lookup"><span data-stu-id="1006f-115">This property is deleted if the message object is not flagged complete.</span></span> <span data-ttu-id="1006f-116">時間の最小解像度は分である必要があります (値は6億の倍数である必要があります)。</span><span class="sxs-lookup"><span data-stu-id="1006f-116">The time's smallest resolution must be minutes (the value must be a multiple of 600,000,000).</span></span> <span data-ttu-id="1006f-117">このプロパティは、オブジェクトが会議関連オブジェクトであり、task オブジェクトに存在してはならない場合は、存在してはなりません。</span><span class="sxs-lookup"><span data-stu-id="1006f-117">This property must not exist if the object is a meeting-related object, and it should not exist on a task object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1006f-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1006f-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1006f-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1006f-119">Protocol specifications</span></span>

<span data-ttu-id="1006f-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1006f-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1006f-121">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="1006f-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1006f-122">[[OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1006f-122">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1006f-123">フラグに関連するプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="1006f-123">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1006f-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="1006f-124">Header files</span></span>

<span data-ttu-id="1006f-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1006f-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="1006f-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1006f-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="1006f-127">Mapitags</span><span class="sxs-lookup"><span data-stu-id="1006f-127">Mapitags.h</span></span>
  
> <span data-ttu-id="1006f-128">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1006f-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1006f-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="1006f-129">See also</span></span>



[<span data-ttu-id="1006f-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="1006f-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1006f-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1006f-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1006f-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1006f-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1006f-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1006f-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

