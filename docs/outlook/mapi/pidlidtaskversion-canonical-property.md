---
title: PidLidTaskVersion の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a31e2862aa3a6265f1dd9f8036abe329cf556276
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802245"
---
# <a name="pidlidtaskversion-canonical-property"></a><span data-ttu-id="f25e2-103">PidLidTaskVersion の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="f25e2-103">PidLidTaskVersion Canonical Property</span></span>

  
  
<span data-ttu-id="f25e2-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f25e2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f25e2-105">どのコピーが、タスクの最新の更新プログラムであることを示します。</span><span class="sxs-lookup"><span data-stu-id="f25e2-105">Indicates which copy is the latest update of a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f25e2-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="f25e2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f25e2-107">dispidTaskVersion</span><span class="sxs-lookup"><span data-stu-id="f25e2-107">dispidTaskVersion</span></span>  <br/> |
|<span data-ttu-id="f25e2-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="f25e2-108">Property set:</span></span>  <br/> |<span data-ttu-id="f25e2-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="f25e2-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="f25e2-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="f25e2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f25e2-111">0x00008112</span><span class="sxs-lookup"><span data-stu-id="f25e2-111">0x00008112</span></span>  <br/> |
|<span data-ttu-id="f25e2-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="f25e2-112">Data type:</span></span>  <br/> |<span data-ttu-id="f25e2-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f25e2-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f25e2-114">領域:</span><span class="sxs-lookup"><span data-stu-id="f25e2-114">Area:</span></span>  <br/> |<span data-ttu-id="f25e2-115">タスク</span><span class="sxs-lookup"><span data-stu-id="f25e2-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f25e2-116">備考</span><span class="sxs-lookup"><span data-stu-id="f25e2-116">Remarks</span></span>

<span data-ttu-id="f25e2-117">タスクよりも低いバージョンでの更新は無視されます。</span><span class="sxs-lookup"><span data-stu-id="f25e2-117">Updates with lower versions than the task are ignored.</span></span> 
  
<span data-ttu-id="f25e2-118">タスクのタスクの通信に埋め込み、クライアントはタスクの通信も同様に、埋め込まれたタスクの現在のバージョンを設定します。</span><span class="sxs-lookup"><span data-stu-id="f25e2-118">When embedding a task in a task communication, the client sets the current version of the embedded task on the task communication as well.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f25e2-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f25e2-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f25e2-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f25e2-120">Protocol specifications</span></span>

<span data-ttu-id="f25e2-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f25e2-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f25e2-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="f25e2-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f25e2-123">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f25e2-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f25e2-124">タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="f25e2-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f25e2-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f25e2-125">Header files</span></span>

<span data-ttu-id="f25e2-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f25e2-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="f25e2-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f25e2-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f25e2-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="f25e2-128">See also</span></span>



[<span data-ttu-id="f25e2-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f25e2-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f25e2-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f25e2-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f25e2-131">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="f25e2-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f25e2-132">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="f25e2-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

