---
title: PidLidTaskActualEffort の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0782191010341019ebea71ebf545dec490521520
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802179"
---
# <a name="pidlidtaskactualeffort-canonical-property"></a><span data-ttu-id="e97c5-103">PidLidTaskActualEffort の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="e97c5-103">PidLidTaskActualEffort Canonical Property</span></span>

  
  
<span data-ttu-id="e97c5-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e97c5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e97c5-105">ユーザーがタスクを実行した分の数を示します。</span><span class="sxs-lookup"><span data-stu-id="e97c5-105">Indicates the number of minutes that the user performed a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e97c5-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="e97c5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e97c5-107">dispidTaskActualEffort</span><span class="sxs-lookup"><span data-stu-id="e97c5-107">dispidTaskActualEffort</span></span>  <br/> |
|<span data-ttu-id="e97c5-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="e97c5-108">Property set:</span></span>  <br/> |<span data-ttu-id="e97c5-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="e97c5-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="e97c5-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="e97c5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e97c5-111">0x00008110</span><span class="sxs-lookup"><span data-stu-id="e97c5-111">0x00008110</span></span>  <br/> |
|<span data-ttu-id="e97c5-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="e97c5-112">Data type:</span></span>  <br/> |<span data-ttu-id="e97c5-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e97c5-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e97c5-114">領域:</span><span class="sxs-lookup"><span data-stu-id="e97c5-114">Area:</span></span>  <br/> |<span data-ttu-id="e97c5-115">タスク</span><span class="sxs-lookup"><span data-stu-id="e97c5-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e97c5-116">備考</span><span class="sxs-lookup"><span data-stu-id="e97c5-116">Remarks</span></span>

<span data-ttu-id="e97c5-117">値は、0 以上で 0x5AE980DF (1,525,252,319) より小さい、480 分と等しい 1 日 2400 分と等しい 1 週間 (1 日の作業で、稼働日の 5 日間は 8 時間) をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e97c5-117">The value must be greater than or equal to 0 and less than 0x5AE980DF (1,525,252,319), where 480 minutes equal one day and 2400 minutes equal one week (eight hours in a work day and five days in a work week).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e97c5-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e97c5-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e97c5-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e97c5-119">Protocol specifications</span></span>

<span data-ttu-id="e97c5-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e97c5-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e97c5-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e97c5-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e97c5-122">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e97c5-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e97c5-123">プロパティは、連絡先と個人用配布リスト オブジェクトの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e97c5-123">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e97c5-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e97c5-124">Header files</span></span>

<span data-ttu-id="e97c5-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e97c5-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="e97c5-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e97c5-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e97c5-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="e97c5-127">See also</span></span>



[<span data-ttu-id="e97c5-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e97c5-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e97c5-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e97c5-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e97c5-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="e97c5-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e97c5-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="e97c5-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

