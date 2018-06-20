---
title: PidLidTaskOrdinal の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskOrdinal
api_type:
- COM
ms.assetid: 1021860e-4c40-4c22-aa68-b568d046aaf7
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 033bc038988373b11f3eac863a256717624999f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802225"
---
# <a name="pidlidtaskordinal-canonical-property"></a><span data-ttu-id="9bb5e-103">PidLidTaskOrdinal の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="9bb5e-103">PidLidTaskOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="9bb5e-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9bb5e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9bb5e-105">カスタムの並べ替え操作を支援するために用意されています。</span><span class="sxs-lookup"><span data-stu-id="9bb5e-105">Provides an aid to custom sorting tasks.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9bb5e-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="9bb5e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9bb5e-107">dispidTaskOrdinal</span><span class="sxs-lookup"><span data-stu-id="9bb5e-107">dispidTaskOrdinal</span></span>  <br/> |
|<span data-ttu-id="9bb5e-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="9bb5e-108">Property set:</span></span>  <br/> |<span data-ttu-id="9bb5e-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="9bb5e-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="9bb5e-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="9bb5e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9bb5e-111">0x00008123</span><span class="sxs-lookup"><span data-stu-id="9bb5e-111">0x00008123</span></span>  <br/> |
|<span data-ttu-id="9bb5e-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="9bb5e-112">Data type:</span></span>  <br/> |<span data-ttu-id="9bb5e-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9bb5e-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9bb5e-114">領域:</span><span class="sxs-lookup"><span data-stu-id="9bb5e-114">Area:</span></span>  <br/> |<span data-ttu-id="9bb5e-115">タスク</span><span class="sxs-lookup"><span data-stu-id="9bb5e-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9bb5e-116">備考</span><span class="sxs-lookup"><span data-stu-id="9bb5e-116">Remarks</span></span>

<span data-ttu-id="9bb5e-117">このプロパティは未設定のままに可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9bb5e-117">This property may be left unset.</span></span> <span data-ttu-id="9bb5e-118">かどうかこのオプションを設定すると、その値より大きくなければなりません"0x800186A0"(-2,147,383,648) とより小さい"0x7FFE7960"(2,147,383,648) と、同じフォルダー内のタスクの間で一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="9bb5e-118">If set, its value must be greater than "0x800186A0" (-2,147,383,648) and less than "0x7FFE7960" (2,147,383,648) and must be unique among tasks in the same folder.</span></span>
  
<span data-ttu-id="9bb5e-119">少ない数に負の数よりも、 **PR_ORDINAL_MOST** ([PidTagOrdinalMost](pidtagordinalmost-canonical-property.md)) のプロパティ、フォルダーの現在の値のクライアントがこのプロパティを設定すると、常に、クライアントはフォルダーの**PR_ORDINAL_MOST**も更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9bb5e-119">Whenever the client sets this property to a number less than the negative of the current value of the **PR_ORDINAL_MOST** ([PidTagOrdinalMost](pidtagordinalmost-canonical-property.md)) property of the folder, the client must also update **PR_ORDINAL_MOST** on the folder.</span></span> 
  
<span data-ttu-id="9bb5e-120">フォルダーの**PR_ORDINAL_MOST**プロパティには、同じフォルダー内のタスクの間で一意の値を決定する効率的な方法が用意されています。</span><span class="sxs-lookup"><span data-stu-id="9bb5e-120">The **PR_ORDINAL_MOST** property of the folder provides an efficient way to determine a unique value among tasks in the same folder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9bb5e-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9bb5e-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9bb5e-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="9bb5e-122">Protocol specifications</span></span>

<span data-ttu-id="9bb5e-123">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9bb5e-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9bb5e-124">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="9bb5e-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9bb5e-125">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9bb5e-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9bb5e-126">タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="9bb5e-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="9bb5e-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="9bb5e-127">Header files</span></span>

<span data-ttu-id="9bb5e-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9bb5e-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="9bb5e-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9bb5e-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9bb5e-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="9bb5e-130">See also</span></span>



[<span data-ttu-id="9bb5e-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9bb5e-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9bb5e-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9bb5e-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9bb5e-133">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="9bb5e-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9bb5e-134">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="9bb5e-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

