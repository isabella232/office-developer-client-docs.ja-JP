---
title: PidLidSmartNoAttach 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSmartNoAttach
api_type:
- COM
ms.assetid: 60299c1b-1b46-4c3a-8fb9-a2b4d3383aac
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e4a0e87b24789e3ee4cb5ed6684d508b62e65b30
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575974"
---
# <a name="pidlidsmartnoattach-canonical-property"></a><span data-ttu-id="4b975-103">PidLidSmartNoAttach 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4b975-103">PidLidSmartNoAttach Canonical Property</span></span>

  
  
<span data-ttu-id="4b975-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b975-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b975-105">メッセージの添付ファイルと見なされますかどうかを非表示にします。</span><span class="sxs-lookup"><span data-stu-id="4b975-105">Represents whether the attachments on a message are considered as hidden.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4b975-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4b975-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4b975-107">dispidSmartNoAttach</span><span class="sxs-lookup"><span data-stu-id="4b975-107">dispidSmartNoAttach</span></span>  <br/> |
|<span data-ttu-id="4b975-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="4b975-108">Property set:</span></span>  <br/> |<span data-ttu-id="4b975-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="4b975-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="4b975-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="4b975-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4b975-111">0x00008514</span><span class="sxs-lookup"><span data-stu-id="4b975-111">0x00008514</span></span>  <br/> |
|<span data-ttu-id="4b975-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4b975-112">Data type:</span></span>  <br/> |<span data-ttu-id="4b975-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="4b975-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="4b975-114">領域:</span><span class="sxs-lookup"><span data-stu-id="4b975-114">Area:</span></span>  <br/> |<span data-ttu-id="4b975-115">実行時の構成</span><span class="sxs-lookup"><span data-stu-id="4b975-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4b975-116">注釈</span><span class="sxs-lookup"><span data-stu-id="4b975-116">Remarks</span></span>

<span data-ttu-id="4b975-117">メッセージの添付ファイルと見なされる場合は、このプロパティは TRUE を非表示にします。</span><span class="sxs-lookup"><span data-stu-id="4b975-117">This property is TRUE if the attachments of the message are considered as hidden.</span></span>
  
<span data-ttu-id="4b975-118">これは、メッセージ オブジェクトのエンド ・ ユーザーに表示されている添付ファイルがないかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="4b975-118">It indicates whether the message object has no end-user visible attachments.</span></span> <span data-ttu-id="4b975-119">このプロパティが設定ではない可能性があります。既定値は FALSE と見なされます。</span><span class="sxs-lookup"><span data-stu-id="4b975-119">This property may be unset; if so, a default value of FALSE is assumed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4b975-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4b975-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4b975-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="4b975-121">Protocol specifications</span></span>

<span data-ttu-id="4b975-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b975-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b975-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="4b975-123">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4b975-124">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b975-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b975-125">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="4b975-125">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4b975-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="4b975-126">Header files</span></span>

<span data-ttu-id="4b975-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4b975-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="4b975-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4b975-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4b975-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="4b975-129">See also</span></span>



[<span data-ttu-id="4b975-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4b975-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4b975-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4b975-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4b975-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4b975-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4b975-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4b975-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

