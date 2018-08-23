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
ms.openlocfilehash: f85fdc701a29f5865700c6519d589212a06fd0af
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585781"
---
# <a name="pidlidlogflags-canonical-property"></a><span data-ttu-id="33f24-103">PidLidLogFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="33f24-103">PidLidLogFlags Canonical Property</span></span>

  
  
<span data-ttu-id="33f24-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33f24-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33f24-105">仕訳帳についてのメタデータが含まれています。</span><span class="sxs-lookup"><span data-stu-id="33f24-105">Contains metadata about the journal.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="33f24-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="33f24-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="33f24-107">dispidLogFlags</span><span class="sxs-lookup"><span data-stu-id="33f24-107">dispidLogFlags</span></span>  <br/> |
|<span data-ttu-id="33f24-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="33f24-108">Property set:</span></span>  <br/> |<span data-ttu-id="33f24-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="33f24-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="33f24-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="33f24-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="33f24-111">0x0000870C</span><span class="sxs-lookup"><span data-stu-id="33f24-111">0x0000870C</span></span>  <br/> |
|<span data-ttu-id="33f24-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="33f24-112">Data type:</span></span>  <br/> |<span data-ttu-id="33f24-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="33f24-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="33f24-114">領域:</span><span class="sxs-lookup"><span data-stu-id="33f24-114">Area:</span></span>  <br/> |<span data-ttu-id="33f24-115">ジャーナル</span><span class="sxs-lookup"><span data-stu-id="33f24-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33f24-116">注釈</span><span class="sxs-lookup"><span data-stu-id="33f24-116">Remarks</span></span>

<span data-ttu-id="33f24-117">仕訳帳に関するメタデータが含まれたビット フィールドは、0 または「0x40000000」のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="33f24-117">The bit field that contains metadata about the journal must be either zero or "0x40000000".</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="33f24-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="33f24-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="33f24-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="33f24-119">Protocol specifications</span></span>

<span data-ttu-id="33f24-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33f24-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33f24-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="33f24-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="33f24-122">[[MS OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33f24-122">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33f24-123">プロパティとは、仕訳帳の許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="33f24-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="33f24-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="33f24-124">Header files</span></span>

<span data-ttu-id="33f24-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="33f24-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="33f24-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="33f24-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="33f24-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="33f24-127">See also</span></span>



[<span data-ttu-id="33f24-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="33f24-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="33f24-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="33f24-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="33f24-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="33f24-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="33f24-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="33f24-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

