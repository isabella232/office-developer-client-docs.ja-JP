---
title: PidTagImplicitConversionProhibited 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagImplicitConversionProhibited
api_type:
- HeaderDef
ms.assetid: c6cb5a86-0105-4743-9f8e-b832e898da52
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7635dd24f4fbc5128d3d96556802ab2e3fe56e35
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571844"
---
# <a name="pidtagimplicitconversionprohibited-canonical-property"></a><span data-ttu-id="0c3b5-103">PidTagImplicitConversionProhibited 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0c3b5-103">PidTagImplicitConversionProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="0c3b5-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c3b5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c3b5-105">メッセージ転送エージェント (MTA) が暗黙的なメッセージのテキストの変換をすることから禁止されている場合 TRUE が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0c3b5-105">Contains TRUE if a message transfer agent (MTA) is prohibited from making implicit message text conversions.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0c3b5-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="0c3b5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0c3b5-107">PR_IMPLICIT_CONVERSION_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="0c3b5-107">PR_IMPLICIT_CONVERSION_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="0c3b5-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="0c3b5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0c3b5-109">0x0016</span><span class="sxs-lookup"><span data-stu-id="0c3b5-109">0x0016</span></span>  <br/> |
|<span data-ttu-id="0c3b5-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="0c3b5-110">Data type:</span></span>  <br/> |<span data-ttu-id="0c3b5-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="0c3b5-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="0c3b5-112">領域:</span><span class="sxs-lookup"><span data-stu-id="0c3b5-112">Area:</span></span>  <br/> |<span data-ttu-id="0c3b5-113">Server</span><span class="sxs-lookup"><span data-stu-id="0c3b5-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0c3b5-114">注釈</span><span class="sxs-lookup"><span data-stu-id="0c3b5-114">Remarks</span></span>

<span data-ttu-id="0c3b5-115">このプロパティが TRUE の場合は、メッセージング システムする必要がありますで実行できません、コンテンツを変換、メッセージは、 **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)) プロパティを使用して受信者ごとの単位で明示的に要求された場合を除き。</span><span class="sxs-lookup"><span data-stu-id="0c3b5-115">If this property is TRUE, the messaging system must not perform any content conversion on the message unless it is explicitly requested on a per-recipient basis with the **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0c3b5-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="0c3b5-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0c3b5-117">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="0c3b5-117">Header files</span></span>

<span data-ttu-id="0c3b5-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0c3b5-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="0c3b5-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="0c3b5-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="0c3b5-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0c3b5-120">Mapitags.h</span></span>
  
> <span data-ttu-id="0c3b5-121">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0c3b5-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0c3b5-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="0c3b5-122">See also</span></span>



[<span data-ttu-id="0c3b5-123">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0c3b5-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0c3b5-124">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0c3b5-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0c3b5-125">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0c3b5-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0c3b5-126">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0c3b5-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

