---
title: PidLidSmartNoAttach の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 43e10652a7dccdf0da6592df0f9fc2daf5ea9bee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802166"
---
# <a name="pidlidsmartnoattach-canonical-property"></a><span data-ttu-id="feaeb-103">PidLidSmartNoAttach の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="feaeb-103">PidLidSmartNoAttach Canonical Property</span></span>

  
  
<span data-ttu-id="feaeb-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="feaeb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="feaeb-105">メッセージの添付ファイルと見なされますかどうかを非表示にします。</span><span class="sxs-lookup"><span data-stu-id="feaeb-105">Represents whether the attachments on a message are considered as hidden.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="feaeb-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="feaeb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="feaeb-107">dispidSmartNoAttach</span><span class="sxs-lookup"><span data-stu-id="feaeb-107">dispidSmartNoAttach</span></span>  <br/> |
|<span data-ttu-id="feaeb-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="feaeb-108">Property set:</span></span>  <br/> |<span data-ttu-id="feaeb-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="feaeb-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="feaeb-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="feaeb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="feaeb-111">0x00008514</span><span class="sxs-lookup"><span data-stu-id="feaeb-111">0x00008514</span></span>  <br/> |
|<span data-ttu-id="feaeb-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="feaeb-112">Data type:</span></span>  <br/> |<span data-ttu-id="feaeb-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="feaeb-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="feaeb-114">領域:</span><span class="sxs-lookup"><span data-stu-id="feaeb-114">Area:</span></span>  <br/> |<span data-ttu-id="feaeb-115">実行時の構成</span><span class="sxs-lookup"><span data-stu-id="feaeb-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="feaeb-116">備考</span><span class="sxs-lookup"><span data-stu-id="feaeb-116">Remarks</span></span>

<span data-ttu-id="feaeb-117">メッセージの添付ファイルと見なされる場合は、このプロパティは TRUE を非表示にします。</span><span class="sxs-lookup"><span data-stu-id="feaeb-117">This property is TRUE if the attachments of the message are considered as hidden.</span></span>
  
<span data-ttu-id="feaeb-118">これは、メッセージ オブジェクトのエンド ・ ユーザーに表示されている添付ファイルがないかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="feaeb-118">It indicates whether the message object has no end-user visible attachments.</span></span> <span data-ttu-id="feaeb-119">このプロパティが設定ではない可能性があります。既定値は FALSE と見なされます。</span><span class="sxs-lookup"><span data-stu-id="feaeb-119">This property may be unset; if so, a default value of FALSE is assumed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="feaeb-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="feaeb-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="feaeb-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="feaeb-121">Protocol specifications</span></span>

<span data-ttu-id="feaeb-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="feaeb-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="feaeb-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="feaeb-123">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="feaeb-124">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="feaeb-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="feaeb-125">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="feaeb-125">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="feaeb-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="feaeb-126">Header files</span></span>

<span data-ttu-id="feaeb-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="feaeb-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="feaeb-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="feaeb-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="feaeb-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="feaeb-129">See also</span></span>



[<span data-ttu-id="feaeb-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="feaeb-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="feaeb-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="feaeb-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="feaeb-132">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="feaeb-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="feaeb-133">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="feaeb-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

