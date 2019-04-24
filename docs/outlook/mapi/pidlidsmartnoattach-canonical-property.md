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
ms.openlocfilehash: 7dddca6a17b07047d1447a57347fbe47a04471e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331319"
---
# <a name="pidlidsmartnoattach-canonical-property"></a><span data-ttu-id="6e40a-103">PidLidSmartNoAttach 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6e40a-103">PidLidSmartNoAttach Canonical Property</span></span>

  
  
<span data-ttu-id="6e40a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e40a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e40a-105">メッセージの添付ファイルが非表示であると見なされるかどうかを表します。</span><span class="sxs-lookup"><span data-stu-id="6e40a-105">Represents whether the attachments on a message are considered as hidden.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6e40a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="6e40a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6e40a-107">dispidsmartnoattach</span><span class="sxs-lookup"><span data-stu-id="6e40a-107">dispidSmartNoAttach</span></span>  <br/> |
|<span data-ttu-id="6e40a-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="6e40a-108">Property set:</span></span>  <br/> |<span data-ttu-id="6e40a-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="6e40a-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="6e40a-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="6e40a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6e40a-111">0x00008514</span><span class="sxs-lookup"><span data-stu-id="6e40a-111">0x00008514</span></span>  <br/> |
|<span data-ttu-id="6e40a-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="6e40a-112">Data type:</span></span>  <br/> |<span data-ttu-id="6e40a-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="6e40a-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="6e40a-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="6e40a-114">Area:</span></span>  <br/> |<span data-ttu-id="6e40a-115">実行時の構成</span><span class="sxs-lookup"><span data-stu-id="6e40a-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e40a-116">解説</span><span class="sxs-lookup"><span data-stu-id="6e40a-116">Remarks</span></span>

<span data-ttu-id="6e40a-117">このプロパティは、メッセージの添付ファイルが非表示であると見なされる場合に TRUE になります。</span><span class="sxs-lookup"><span data-stu-id="6e40a-117">This property is TRUE if the attachments of the message are considered as hidden.</span></span>
  
<span data-ttu-id="6e40a-118">これは、メッセージオブジェクトにエンドユーザーに表示される添付ファイルがないかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6e40a-118">It indicates whether the message object has no end-user visible attachments.</span></span> <span data-ttu-id="6e40a-119">このプロパティは設定解除できます。その場合は、既定値の FALSE が想定されます。</span><span class="sxs-lookup"><span data-stu-id="6e40a-119">This property may be unset; if so, a default value of FALSE is assumed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6e40a-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6e40a-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6e40a-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6e40a-121">Protocol specifications</span></span>

<span data-ttu-id="6e40a-122">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e40a-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e40a-123">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="6e40a-123">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6e40a-124">[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e40a-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e40a-125">メッセージと添付ファイルオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="6e40a-125">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6e40a-126">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="6e40a-126">Header files</span></span>

<span data-ttu-id="6e40a-127">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6e40a-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="6e40a-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6e40a-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6e40a-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="6e40a-129">See also</span></span>



[<span data-ttu-id="6e40a-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="6e40a-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6e40a-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6e40a-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6e40a-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6e40a-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6e40a-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6e40a-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

