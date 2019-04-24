---
title: PidLidTaskVersion 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskVersion
api_type:
- COM
ms.assetid: 3ab77f25-ad11-4501-8d35-ef560c07e2f2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3daf8a04afc9cf47d808b46f2cee010e15a33cf9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356494"
---
# <a name="pidlidtaskversion-canonical-property"></a><span data-ttu-id="591a0-103">PidLidTaskVersion 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="591a0-103">PidLidTaskVersion Canonical Property</span></span>

  
  
<span data-ttu-id="591a0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="591a0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="591a0-105">どのコピーがタスクの最新の更新プログラムであるかを示します。</span><span class="sxs-lookup"><span data-stu-id="591a0-105">Indicates which copy is the latest update of a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="591a0-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="591a0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="591a0-107">dispidtaskversion</span><span class="sxs-lookup"><span data-stu-id="591a0-107">dispidTaskVersion</span></span>  <br/> |
|<span data-ttu-id="591a0-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="591a0-108">Property set:</span></span>  <br/> |<span data-ttu-id="591a0-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="591a0-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="591a0-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="591a0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="591a0-111">0x00008112</span><span class="sxs-lookup"><span data-stu-id="591a0-111">0x00008112</span></span>  <br/> |
|<span data-ttu-id="591a0-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="591a0-112">Data type:</span></span>  <br/> |<span data-ttu-id="591a0-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="591a0-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="591a0-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="591a0-114">Area:</span></span>  <br/> |<span data-ttu-id="591a0-115">タスク</span><span class="sxs-lookup"><span data-stu-id="591a0-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="591a0-116">解説</span><span class="sxs-lookup"><span data-stu-id="591a0-116">Remarks</span></span>

<span data-ttu-id="591a0-117">タスクより下位のバージョンの更新は無視されます。</span><span class="sxs-lookup"><span data-stu-id="591a0-117">Updates with lower versions than the task are ignored.</span></span> 
  
<span data-ttu-id="591a0-118">タスクがタスクの通信に埋め込まれている場合、クライアントは現在のバージョンの埋め込みタスクをタスクの通信にも設定します。</span><span class="sxs-lookup"><span data-stu-id="591a0-118">When embedding a task in a task communication, the client sets the current version of the embedded task on the task communication as well.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="591a0-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="591a0-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="591a0-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="591a0-120">Protocol specifications</span></span>

<span data-ttu-id="591a0-121">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="591a0-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="591a0-122">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="591a0-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="591a0-123">[[OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="591a0-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="591a0-124">タスク、タスクの割り当て、およびタスクの更新に相当する電子メールをモデル化する複数のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="591a0-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="591a0-125">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="591a0-125">Header files</span></span>

<span data-ttu-id="591a0-126">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="591a0-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="591a0-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="591a0-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="591a0-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="591a0-128">See also</span></span>



[<span data-ttu-id="591a0-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="591a0-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="591a0-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="591a0-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="591a0-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="591a0-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="591a0-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="591a0-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

