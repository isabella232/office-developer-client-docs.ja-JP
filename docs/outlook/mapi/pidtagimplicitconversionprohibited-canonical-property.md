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
ms.openlocfilehash: a0e18ef529b65317abd9446408ed73638c792809
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346607"
---
# <a name="pidtagimplicitconversionprohibited-canonical-property"></a><span data-ttu-id="1b1ac-103">PidTagImplicitConversionProhibited 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1b1ac-103">PidTagImplicitConversionProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="1b1ac-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b1ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b1ac-105">メッセージ転送エージェント (MTA) が暗黙的なメッセージテキスト変換を行うことが禁止されている場合は、TRUE が含まれます。</span><span class="sxs-lookup"><span data-stu-id="1b1ac-105">Contains TRUE if a message transfer agent (MTA) is prohibited from making implicit message text conversions.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1b1ac-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1b1ac-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1b1ac-107">PR_IMPLICIT_CONVERSION_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="1b1ac-107">PR_IMPLICIT_CONVERSION_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="1b1ac-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1b1ac-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1b1ac-109">0x0016</span><span class="sxs-lookup"><span data-stu-id="1b1ac-109">0x0016</span></span>  <br/> |
|<span data-ttu-id="1b1ac-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1b1ac-110">Data type:</span></span>  <br/> |<span data-ttu-id="1b1ac-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="1b1ac-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="1b1ac-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="1b1ac-112">Area:</span></span>  <br/> |<span data-ttu-id="1b1ac-113">サーバー</span><span class="sxs-lookup"><span data-stu-id="1b1ac-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1b1ac-114">解説</span><span class="sxs-lookup"><span data-stu-id="1b1ac-114">Remarks</span></span>

<span data-ttu-id="1b1ac-115">このプロパティが TRUE の場合、メッセージングシステムは、 **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)) プロパティを使用して受信者ごとに明示的に要求されていない限り、メッセージに対してコンテンツ変換を実行しないでください。</span><span class="sxs-lookup"><span data-stu-id="1b1ac-115">If this property is TRUE, the messaging system must not perform any content conversion on the message unless it is explicitly requested on a per-recipient basis with the **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1b1ac-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1b1ac-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1b1ac-117">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="1b1ac-117">Header files</span></span>

<span data-ttu-id="1b1ac-118">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1b1ac-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="1b1ac-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1b1ac-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="1b1ac-120">Mapitags</span><span class="sxs-lookup"><span data-stu-id="1b1ac-120">Mapitags.h</span></span>
  
> <span data-ttu-id="1b1ac-121">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="1b1ac-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1b1ac-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="1b1ac-122">See also</span></span>



[<span data-ttu-id="1b1ac-123">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="1b1ac-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1b1ac-124">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1b1ac-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1b1ac-125">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1b1ac-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1b1ac-126">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1b1ac-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

