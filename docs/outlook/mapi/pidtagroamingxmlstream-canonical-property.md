---
title: PidTagRoamingXmlStream 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRoamingXmlStream
api_type:
- COM
ms.assetid: ce55b50e-3dbf-4690-9102-c08f35ada82e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3e7ce1f810a1dd37cd4370ceb423b664d75878a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359543"
---
# <a name="pidtagroamingxmlstream-canonical-property"></a><span data-ttu-id="08003-103">PidTagRoamingXmlStream 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="08003-103">PidTagRoamingXmlStream Canonical Property</span></span>

  
  
<span data-ttu-id="08003-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08003-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08003-105">任意の XML ストリームを含みます。</span><span class="sxs-lookup"><span data-stu-id="08003-105">Contains an arbitrary XML stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="08003-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="08003-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="08003-107">PR_ROAMING_XMLSTREAM</span><span class="sxs-lookup"><span data-stu-id="08003-107">PR_ROAMING_XMLSTREAM</span></span>  <br/> |
|<span data-ttu-id="08003-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="08003-108">Identifier:</span></span>  <br/> |<span data-ttu-id="08003-109">0x7C08</span><span class="sxs-lookup"><span data-stu-id="08003-109">0x7C08</span></span>  <br/> |
|<span data-ttu-id="08003-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="08003-110">Data type:</span></span>  <br/> |<span data-ttu-id="08003-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="08003-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="08003-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="08003-112">Area:</span></span>  <br/> |<span data-ttu-id="08003-113">構成</span><span class="sxs-lookup"><span data-stu-id="08003-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08003-114">注釈</span><span class="sxs-lookup"><span data-stu-id="08003-114">Remarks</span></span>

<span data-ttu-id="08003-115">このプロパティには、XML データの任意のストリームが含まれます。</span><span class="sxs-lookup"><span data-stu-id="08003-115">This property contains an arbitrary stream of XML data.</span></span> <span data-ttu-id="08003-116">メッセージ内の他のプロパティは、このプロパティで使用する特定のスキーマを示している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="08003-116">Other properties in the message may imply specific schemas to use in this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="08003-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="08003-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="08003-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="08003-118">Protocol specifications</span></span>

<span data-ttu-id="08003-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08003-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08003-120">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="08003-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="08003-121">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08003-121">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08003-122">共有カテゴリ リストや作業時間など、クライアントおよびサーバー構成データの場所とプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="08003-122">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="08003-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="08003-123">Header files</span></span>

<span data-ttu-id="08003-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="08003-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="08003-125">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="08003-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="08003-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="08003-126">Mapitags.h</span></span>
  
> <span data-ttu-id="08003-127">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="08003-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="08003-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="08003-128">See also</span></span>



[<span data-ttu-id="08003-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="08003-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="08003-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="08003-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="08003-131">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="08003-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="08003-132">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="08003-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

