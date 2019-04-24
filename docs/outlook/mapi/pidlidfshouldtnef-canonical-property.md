---
title: PidLidFShouldTNEF 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFShouldTNEF
api_type:
- COM
ms.assetid: 3cab23b6-f0e3-4703-a83b-12a617537651
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a8f88e4b41ab455c55bfd1cb36b73ce7ef0383b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348994"
---
# <a name="pidlidfshouldtnef-canonical-property"></a><span data-ttu-id="23908-103">PidLidFShouldTNEF 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="23908-103">PidLidFShouldTNEF Canonical Property</span></span>

  
  
<span data-ttu-id="23908-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23908-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23908-105">アイテムをトランスポートニュートラルカプセル化形式 (TNEF) でエンコードするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="23908-105">Indicates whether to encode an item with Transport Neutral Encapsulation Format (TNEF).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="23908-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="23908-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="23908-107">dispidfid tnef</span><span class="sxs-lookup"><span data-stu-id="23908-107">dispidFShouldTNEF</span></span>  <br/> |
|<span data-ttu-id="23908-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="23908-108">Property set:</span></span>  <br/> |<span data-ttu-id="23908-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="23908-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="23908-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="23908-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="23908-111">0x000085a5</span><span class="sxs-lookup"><span data-stu-id="23908-111">0x000085A5</span></span>  <br/> |
|<span data-ttu-id="23908-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="23908-112">Data type:</span></span>  <br/> |<span data-ttu-id="23908-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="23908-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="23908-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="23908-114">Area:</span></span>  <br/> |<span data-ttu-id="23908-115">実行時の構成</span><span class="sxs-lookup"><span data-stu-id="23908-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23908-116">解説</span><span class="sxs-lookup"><span data-stu-id="23908-116">Remarks</span></span>

<span data-ttu-id="23908-117">このプロパティは、Microsoft Word が電子メールエディターとして設定されているときに設定され、リッチテキスト形式 (RTF) のストリームに埋め込まれている OLE オブジェクトを送信します。</span><span class="sxs-lookup"><span data-stu-id="23908-117">This property is set when Microsoft Word is set as the email editor, and it sends an OLE object that is embedded in a Rich Text Format (RTF) stream.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="23908-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="23908-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="23908-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="23908-119">Protocol specifications</span></span>

<span data-ttu-id="23908-120">[[OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="23908-120">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="23908-121">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="23908-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="23908-122">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="23908-122">Header files</span></span>

<span data-ttu-id="23908-123">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="23908-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="23908-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="23908-124">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="23908-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="23908-125">See also</span></span>



[<span data-ttu-id="23908-126">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="23908-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="23908-127">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="23908-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="23908-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="23908-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="23908-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="23908-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

