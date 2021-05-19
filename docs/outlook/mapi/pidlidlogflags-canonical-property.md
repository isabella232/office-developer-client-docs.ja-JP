---
title: PidLidLogFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogFlags
api_type:
- COM
ms.assetid: 3174d931-e045-44db-a203-a27c9c00f4fc
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a407c065a51870ba9908fbd9b626d7f287a1df4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336947"
---
# <a name="pidlidlogflags-canonical-property"></a><span data-ttu-id="7abb3-103">PidLidLogFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7abb3-103">PidLidLogFlags Canonical Property</span></span>

  
  
<span data-ttu-id="7abb3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7abb3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7abb3-105">ジャーナルに関するメタデータが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7abb3-105">Contains metadata about the journal.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7abb3-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7abb3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7abb3-107">dispidLogFlags</span><span class="sxs-lookup"><span data-stu-id="7abb3-107">dispidLogFlags</span></span>  <br/> |
|<span data-ttu-id="7abb3-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="7abb3-108">Property set:</span></span>  <br/> |<span data-ttu-id="7abb3-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="7abb3-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="7abb3-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="7abb3-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7abb3-111">0x0000870C</span><span class="sxs-lookup"><span data-stu-id="7abb3-111">0x0000870C</span></span>  <br/> |
|<span data-ttu-id="7abb3-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="7abb3-112">Data type:</span></span>  <br/> |<span data-ttu-id="7abb3-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7abb3-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7abb3-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="7abb3-114">Area:</span></span>  <br/> |<span data-ttu-id="7abb3-115">ジャーナル</span><span class="sxs-lookup"><span data-stu-id="7abb3-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7abb3-116">注釈</span><span class="sxs-lookup"><span data-stu-id="7abb3-116">Remarks</span></span>

<span data-ttu-id="7abb3-117">ジャーナルに関するメタデータを含むビット フィールドは、ゼロまたは "0x40000000" である必要があります。</span><span class="sxs-lookup"><span data-stu-id="7abb3-117">The bit field that contains metadata about the journal must be either zero or "0x40000000".</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7abb3-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7abb3-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7abb3-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7abb3-119">Protocol specifications</span></span>

<span data-ttu-id="7abb3-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7abb3-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7abb3-121">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="7abb3-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7abb3-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7abb3-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7abb3-123">ジャーナルに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="7abb3-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7abb3-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="7abb3-124">Header files</span></span>

<span data-ttu-id="7abb3-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7abb3-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="7abb3-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7abb3-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7abb3-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="7abb3-127">See also</span></span>



[<span data-ttu-id="7abb3-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="7abb3-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7abb3-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7abb3-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7abb3-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="7abb3-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7abb3-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="7abb3-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

