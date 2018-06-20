---
title: PidLidFShouldTNEF の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 15354a4a07304913cce06d50564b66abe5062a96
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801998"
---
# <a name="pidlidfshouldtnef-canonical-property"></a><span data-ttu-id="2ce24-103">PidLidFShouldTNEF の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="2ce24-103">PidLidFShouldTNEF Canonical Property</span></span>

  
  
<span data-ttu-id="2ce24-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2ce24-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2ce24-105">トランスポート ニュートラル カプセル化形式 (TNEF) を持つアイテムをエンコードするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="2ce24-105">Indicates whether to encode an item with Transport Neutral Encapsulation Format (TNEF).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2ce24-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="2ce24-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2ce24-107">dispidFShouldTNEF</span><span class="sxs-lookup"><span data-stu-id="2ce24-107">dispidFShouldTNEF</span></span>  <br/> |
|<span data-ttu-id="2ce24-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="2ce24-108">Property set:</span></span>  <br/> |<span data-ttu-id="2ce24-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="2ce24-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="2ce24-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="2ce24-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2ce24-111">0x000085A5</span><span class="sxs-lookup"><span data-stu-id="2ce24-111">0x000085A5</span></span>  <br/> |
|<span data-ttu-id="2ce24-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="2ce24-112">Data type:</span></span>  <br/> |<span data-ttu-id="2ce24-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="2ce24-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="2ce24-114">領域:</span><span class="sxs-lookup"><span data-stu-id="2ce24-114">Area:</span></span>  <br/> |<span data-ttu-id="2ce24-115">実行時の構成</span><span class="sxs-lookup"><span data-stu-id="2ce24-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ce24-116">備考</span><span class="sxs-lookup"><span data-stu-id="2ce24-116">Remarks</span></span>

<span data-ttu-id="2ce24-117">電子メール エディターとして Word を設定し、リッチ テキスト形式 (RTF) のストリームに埋め込まれている OLE オブジェクトを送信するとき、このプロパティが設定されています。</span><span class="sxs-lookup"><span data-stu-id="2ce24-117">This property is set when Microsoft Word is set as the email editor, and it sends an OLE object that is embedded in a Rich Text Format (RTF) stream.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2ce24-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2ce24-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2ce24-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="2ce24-119">Protocol specifications</span></span>

<span data-ttu-id="2ce24-120">[MS OXPROPS]</span><span class="sxs-lookup"><span data-stu-id="2ce24-120">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="2ce24-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="2ce24-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2ce24-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="2ce24-122">Header files</span></span>

<span data-ttu-id="2ce24-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2ce24-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="2ce24-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2ce24-124">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2ce24-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="2ce24-125">See also</span></span>



[<span data-ttu-id="2ce24-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2ce24-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2ce24-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2ce24-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2ce24-128">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="2ce24-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2ce24-129">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="2ce24-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

