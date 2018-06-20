---
title: PidTagImplicitConversionProhibited の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: dcfaf9f4e71a13a8697da0cac98f7ea9cc3d8708
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802855"
---
# <a name="pidtagimplicitconversionprohibited-canonical-property"></a><span data-ttu-id="074ca-103">PidTagImplicitConversionProhibited の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="074ca-103">PidTagImplicitConversionProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="074ca-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="074ca-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="074ca-105">メッセージ転送エージェント (MTA) が暗黙的なメッセージのテキストの変換をすることから禁止されている場合 TRUE が含まれています。</span><span class="sxs-lookup"><span data-stu-id="074ca-105">Contains TRUE if a message transfer agent (MTA) is prohibited from making implicit message text conversions.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="074ca-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="074ca-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="074ca-107">PR_IMPLICIT_CONVERSION_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="074ca-107">PR_IMPLICIT_CONVERSION_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="074ca-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="074ca-108">Identifier:</span></span>  <br/> |<span data-ttu-id="074ca-109">0x0016</span><span class="sxs-lookup"><span data-stu-id="074ca-109">0x0016</span></span>  <br/> |
|<span data-ttu-id="074ca-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="074ca-110">Data type:</span></span>  <br/> |<span data-ttu-id="074ca-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="074ca-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="074ca-112">領域:</span><span class="sxs-lookup"><span data-stu-id="074ca-112">Area:</span></span>  <br/> |<span data-ttu-id="074ca-113">Server</span><span class="sxs-lookup"><span data-stu-id="074ca-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="074ca-114">備考</span><span class="sxs-lookup"><span data-stu-id="074ca-114">Remarks</span></span>

<span data-ttu-id="074ca-115">このプロパティが TRUE の場合は、メッセージング システムする必要がありますで実行できません、コンテンツを変換、メッセージは、 **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)) プロパティを使用して受信者ごとの単位で明示的に要求された場合を除き。</span><span class="sxs-lookup"><span data-stu-id="074ca-115">If this property is TRUE, the messaging system must not perform any content conversion on the message unless it is explicitly requested on a per-recipient basis with the **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="074ca-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="074ca-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="074ca-117">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="074ca-117">Header files</span></span>

<span data-ttu-id="074ca-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="074ca-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="074ca-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="074ca-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="074ca-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="074ca-120">Mapitags.h</span></span>
  
> <span data-ttu-id="074ca-121">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="074ca-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="074ca-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="074ca-122">See also</span></span>



[<span data-ttu-id="074ca-123">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="074ca-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="074ca-124">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="074ca-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="074ca-125">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="074ca-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="074ca-126">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="074ca-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

