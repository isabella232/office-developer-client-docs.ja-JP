---
title: PidLidTaskActualEffort 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskActualEffort
api_type:
- COM
ms.assetid: 8e9a9432-bf50-4333-82ec-fba19dff8006
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7eb51396f4575a8f8f9ce15aff84eb894773e979
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382583"
---
# <a name="pidlidtaskactualeffort-canonical-property"></a><span data-ttu-id="50d31-103">PidLidTaskActualEffort 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="50d31-103">PidLidTaskActualEffort Canonical Property</span></span>

  
  
<span data-ttu-id="50d31-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50d31-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50d31-105">ユーザーがタスクを実行した分の数を示します。</span><span class="sxs-lookup"><span data-stu-id="50d31-105">Indicates the number of minutes that the user performed a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="50d31-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="50d31-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="50d31-107">dispidTaskActualEffort</span><span class="sxs-lookup"><span data-stu-id="50d31-107">dispidTaskActualEffort</span></span>  <br/> |
|<span data-ttu-id="50d31-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="50d31-108">Property set:</span></span>  <br/> |<span data-ttu-id="50d31-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="50d31-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="50d31-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="50d31-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="50d31-111">0x00008110</span><span class="sxs-lookup"><span data-stu-id="50d31-111">0x00008110</span></span>  <br/> |
|<span data-ttu-id="50d31-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="50d31-112">Data type:</span></span>  <br/> |<span data-ttu-id="50d31-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="50d31-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="50d31-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="50d31-114">Area:</span></span>  <br/> |<span data-ttu-id="50d31-115">タスク</span><span class="sxs-lookup"><span data-stu-id="50d31-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50d31-116">備考</span><span class="sxs-lookup"><span data-stu-id="50d31-116">Remarks</span></span>

<span data-ttu-id="50d31-117">値は、0 以上で 0x5AE980DF (1,525,252,319) より小さい、480 分と等しい 1 日 2400 分と等しい 1 週間 (1 日の作業で、稼働日の 5 日間は 8 時間) をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="50d31-117">The value must be greater than or equal to 0 and less than 0x5AE980DF (1,525,252,319), where 480 minutes equal one day and 2400 minutes equal one week (eight hours in a work day and five days in a work week).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="50d31-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="50d31-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="50d31-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="50d31-119">Protocol specifications</span></span>

<span data-ttu-id="50d31-120">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50d31-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="50d31-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="50d31-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="50d31-122">[[MS OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50d31-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="50d31-123">プロパティは、連絡先と個人用配布リスト オブジェクトの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="50d31-123">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="50d31-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="50d31-124">Header files</span></span>

<span data-ttu-id="50d31-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="50d31-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="50d31-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="50d31-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="50d31-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="50d31-127">See also</span></span>



[<span data-ttu-id="50d31-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="50d31-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="50d31-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="50d31-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="50d31-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="50d31-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="50d31-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="50d31-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

