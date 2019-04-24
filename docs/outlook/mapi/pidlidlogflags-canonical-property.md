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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a407c065a51870ba9908fbd9b626d7f287a1df4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336947"
---
# <a name="pidlidlogflags-canonical-property"></a><span data-ttu-id="65cdc-103">PidLidLogFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="65cdc-103">PidLidLogFlags Canonical Property</span></span>

  
  
<span data-ttu-id="65cdc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65cdc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65cdc-105">ジャーナルに関するメタデータを格納します。</span><span class="sxs-lookup"><span data-stu-id="65cdc-105">Contains metadata about the journal.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="65cdc-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="65cdc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="65cdc-107">dispidlogflags</span><span class="sxs-lookup"><span data-stu-id="65cdc-107">dispidLogFlags</span></span>  <br/> |
|<span data-ttu-id="65cdc-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="65cdc-108">Property set:</span></span>  <br/> |<span data-ttu-id="65cdc-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="65cdc-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="65cdc-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="65cdc-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="65cdc-111">0x0000870c</span><span class="sxs-lookup"><span data-stu-id="65cdc-111">0x0000870C</span></span>  <br/> |
|<span data-ttu-id="65cdc-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="65cdc-112">Data type:</span></span>  <br/> |<span data-ttu-id="65cdc-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="65cdc-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="65cdc-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="65cdc-114">Area:</span></span>  <br/> |<span data-ttu-id="65cdc-115">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="65cdc-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="65cdc-116">解説</span><span class="sxs-lookup"><span data-stu-id="65cdc-116">Remarks</span></span>

<span data-ttu-id="65cdc-117">ジャーナルに関するメタデータを含むビットフィールドは、0または "0x40000000" である必要があります。</span><span class="sxs-lookup"><span data-stu-id="65cdc-117">The bit field that contains metadata about the journal must be either zero or "0x40000000".</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="65cdc-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="65cdc-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="65cdc-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="65cdc-119">Protocol specifications</span></span>

<span data-ttu-id="65cdc-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="65cdc-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="65cdc-121">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="65cdc-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="65cdc-122">[[OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="65cdc-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="65cdc-123">仕訳帳に対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="65cdc-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="65cdc-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="65cdc-124">Header files</span></span>

<span data-ttu-id="65cdc-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="65cdc-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="65cdc-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="65cdc-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="65cdc-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="65cdc-127">See also</span></span>



[<span data-ttu-id="65cdc-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="65cdc-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="65cdc-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="65cdc-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="65cdc-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="65cdc-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="65cdc-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="65cdc-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

