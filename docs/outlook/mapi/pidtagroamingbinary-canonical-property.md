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
ms.openlocfilehash: ead7c9c33c92240ba5e458b68635b766caaa9760
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359564"
---
# <a name="pidtagroamingbinary-canonical-property"></a><span data-ttu-id="fcafd-103">PidTagRoamingBinary 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fcafd-103">PidTagRoamingBinary Canonical Property</span></span>

  
  
<span data-ttu-id="fcafd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fcafd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fcafd-105">IPM のサブクラスに関連付けられたメッセージストリームを含み**ます。構成**クラス。</span><span class="sxs-lookup"><span data-stu-id="fcafd-105">Contains a message stream associated with a subclass of the **IPM.Configuration** class.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fcafd-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="fcafd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fcafd-107">PR_ROAMING_BINARYSTREAM</span><span class="sxs-lookup"><span data-stu-id="fcafd-107">PR_ROAMING_BINARYSTREAM</span></span>  <br/> |
|<span data-ttu-id="fcafd-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="fcafd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fcafd-109">0x7C09</span><span class="sxs-lookup"><span data-stu-id="fcafd-109">0x7C09</span></span>  <br/> |
|<span data-ttu-id="fcafd-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="fcafd-110">Data type:</span></span>  <br/> |<span data-ttu-id="fcafd-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fcafd-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fcafd-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="fcafd-112">Area:</span></span>  <br/> |<span data-ttu-id="fcafd-113">構成</span><span class="sxs-lookup"><span data-stu-id="fcafd-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fcafd-114">解説</span><span class="sxs-lookup"><span data-stu-id="fcafd-114">Remarks</span></span>

<span data-ttu-id="fcafd-115">このプロパティには、IPM に関連付けられているデータストリームが含まれ**ます。構成**メッセージクラスメッセージ。</span><span class="sxs-lookup"><span data-stu-id="fcafd-115">This property contains the data stream associated with an **IPM.Configuration** message class message.</span></span> <span data-ttu-id="fcafd-116">stream の形式は、メッセージクラスに依存します。</span><span class="sxs-lookup"><span data-stu-id="fcafd-116">The format of the stream depends on the message class.</span></span> <span data-ttu-id="fcafd-117">たとえば、クラスの種類が IPM であるメッセージ **。構成。オートコンプリート**は、[オートコンプリートストリーム](autocomplete-stream.md)として書式設定されます。</span><span class="sxs-lookup"><span data-stu-id="fcafd-117">For instance, a message of class type **IPM.Configuration.Autocomplete** would be formatted as an [Autocomplete Stream](autocomplete-stream.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fcafd-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="fcafd-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fcafd-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="fcafd-119">Protocol specifications</span></span>

<span data-ttu-id="fcafd-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fcafd-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fcafd-121">関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="fcafd-121">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fcafd-122">[[OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fcafd-122">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fcafd-123">カテゴリの共有リストや稼働時間など、クライアントおよびサーバーの構成データの場所とプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="fcafd-123">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fcafd-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="fcafd-124">Header files</span></span>

<span data-ttu-id="fcafd-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fcafd-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="fcafd-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="fcafd-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="fcafd-127">Mapitags</span><span class="sxs-lookup"><span data-stu-id="fcafd-127">Mapitags.h</span></span>
  
> <span data-ttu-id="fcafd-128">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="fcafd-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fcafd-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="fcafd-129">See also</span></span>



[<span data-ttu-id="fcafd-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="fcafd-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fcafd-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fcafd-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fcafd-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="fcafd-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fcafd-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="fcafd-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

