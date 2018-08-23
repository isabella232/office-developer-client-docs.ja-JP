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
ms.openlocfilehash: 15354a4a07304913cce06d50564b66abe5062a96
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801998"
---
# <a name="pidlidfshouldtnef-canonical-property"></a><span data-ttu-id="5bfd6-103">PidLidFShouldTNEF 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5bfd6-103">PidLidFShouldTNEF Canonical Property</span></span>

  
  
<span data-ttu-id="5bfd6-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5bfd6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5bfd6-105">トランスポート ニュートラル カプセル化形式 (TNEF) を持つアイテムをエンコードするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5bfd6-105">Indicates whether to encode an item with Transport Neutral Encapsulation Format (TNEF).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5bfd6-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5bfd6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5bfd6-107">dispidFShouldTNEF</span><span class="sxs-lookup"><span data-stu-id="5bfd6-107">dispidFShouldTNEF</span></span>  <br/> |
|<span data-ttu-id="5bfd6-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="5bfd6-108">Property set:</span></span>  <br/> |<span data-ttu-id="5bfd6-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="5bfd6-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="5bfd6-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="5bfd6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5bfd6-111">0x000085A5</span><span class="sxs-lookup"><span data-stu-id="5bfd6-111">0x000085A5</span></span>  <br/> |
|<span data-ttu-id="5bfd6-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5bfd6-112">Data type:</span></span>  <br/> |<span data-ttu-id="5bfd6-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5bfd6-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5bfd6-114">領域:</span><span class="sxs-lookup"><span data-stu-id="5bfd6-114">Area:</span></span>  <br/> |<span data-ttu-id="5bfd6-115">実行時の構成</span><span class="sxs-lookup"><span data-stu-id="5bfd6-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5bfd6-116">注釈</span><span class="sxs-lookup"><span data-stu-id="5bfd6-116">Remarks</span></span>

<span data-ttu-id="5bfd6-117">電子メール エディターとして Word を設定し、リッチ テキスト形式 (RTF) のストリームに埋め込まれている OLE オブジェクトを送信するとき、このプロパティが設定されています。</span><span class="sxs-lookup"><span data-stu-id="5bfd6-117">This property is set when Microsoft Word is set as the email editor, and it sends an OLE object that is embedded in a Rich Text Format (RTF) stream.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5bfd6-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5bfd6-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5bfd6-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5bfd6-119">Protocol specifications</span></span>

<span data-ttu-id="5bfd6-120">[MS OXPROPS]</span><span class="sxs-lookup"><span data-stu-id="5bfd6-120">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="5bfd6-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="5bfd6-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5bfd6-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5bfd6-122">Header files</span></span>

<span data-ttu-id="5bfd6-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5bfd6-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="5bfd6-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5bfd6-124">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5bfd6-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="5bfd6-125">See also</span></span>



[<span data-ttu-id="5bfd6-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5bfd6-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5bfd6-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5bfd6-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5bfd6-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5bfd6-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5bfd6-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5bfd6-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

