---
title: PidTagRoamingBinary 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f06bf063-fc95-46f9-b5fa-3f127a59ebda
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 717c456024dd98495550f1377edc6a53f82ee042
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572411"
---
# <a name="pidtagroamingbinary-canonical-property"></a><span data-ttu-id="6e116-103">PidTagRoamingBinary 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6e116-103">PidTagRoamingBinary Canonical Property</span></span>

  
  
<span data-ttu-id="6e116-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e116-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e116-105">**IPM のサブクラスに関連付けられているメッセージ ストリームが含まれています。構成**クラス。</span><span class="sxs-lookup"><span data-stu-id="6e116-105">Contains a message stream associated with a subclass of the **IPM.Configuration** class.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6e116-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="6e116-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6e116-107">PR_ROAMING_BINARYSTREAM</span><span class="sxs-lookup"><span data-stu-id="6e116-107">PR_ROAMING_BINARYSTREAM</span></span>  <br/> |
|<span data-ttu-id="6e116-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="6e116-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6e116-109">0x7C09</span><span class="sxs-lookup"><span data-stu-id="6e116-109">0x7C09</span></span>  <br/> |
|<span data-ttu-id="6e116-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="6e116-110">Data type:</span></span>  <br/> |<span data-ttu-id="6e116-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6e116-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6e116-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="6e116-112">Area:</span></span>  <br/> |<span data-ttu-id="6e116-113">Configuration</span><span class="sxs-lookup"><span data-stu-id="6e116-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e116-114">注釈</span><span class="sxs-lookup"><span data-stu-id="6e116-114">Remarks</span></span>

<span data-ttu-id="6e116-115">このプロパティには、IPM、**に関連付けられているデータ ストリームが含まれています。構成**メッセージ クラスのメッセージです。</span><span class="sxs-lookup"><span data-stu-id="6e116-115">This property contains the data stream associated with an **IPM.Configuration** message class message.</span></span> <span data-ttu-id="6e116-116">ストリームの形式は、メッセージ クラスによって異なります。</span><span class="sxs-lookup"><span data-stu-id="6e116-116">The format of the stream depends on the message class.</span></span> <span data-ttu-id="6e116-117">たとえば、クラス型 IPM の**のメッセージです。Configuration.Autocomplete**ように、[オートコンプリートのストリーム](autocomplete-stream.md)としてフォーマットされます。</span><span class="sxs-lookup"><span data-stu-id="6e116-117">For instance, a message of class type **IPM.Configuration.Autocomplete** would be formatted as an [Autocomplete Stream](autocomplete-stream.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6e116-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6e116-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6e116-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6e116-119">Protocol specifications</span></span>

<span data-ttu-id="6e116-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e116-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e116-121">関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="6e116-121">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6e116-122">[[MS OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e116-122">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e116-123">場所と共有カテゴリのリストおよび作業時間など、クライアントとサーバーの構成データのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="6e116-123">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6e116-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="6e116-124">Header files</span></span>

<span data-ttu-id="6e116-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6e116-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="6e116-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6e116-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="6e116-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6e116-127">Mapitags.h</span></span>
  
> <span data-ttu-id="6e116-128">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6e116-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6e116-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="6e116-129">See also</span></span>



[<span data-ttu-id="6e116-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6e116-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6e116-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6e116-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6e116-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6e116-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6e116-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6e116-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

