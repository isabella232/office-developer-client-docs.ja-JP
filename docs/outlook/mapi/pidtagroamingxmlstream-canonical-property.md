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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3e7ce1f810a1dd37cd4370ceb423b664d75878a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359543"
---
# <a name="pidtagroamingxmlstream-canonical-property"></a><span data-ttu-id="fa302-103">PidTagRoamingXmlStream 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fa302-103">PidTagRoamingXmlStream Canonical Property</span></span>

  
  
<span data-ttu-id="fa302-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa302-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa302-105">任意の XML ストリームが格納されています。</span><span class="sxs-lookup"><span data-stu-id="fa302-105">Contains an arbitrary XML stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fa302-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="fa302-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fa302-107">PR_ROAMING_XMLSTREAM</span><span class="sxs-lookup"><span data-stu-id="fa302-107">PR_ROAMING_XMLSTREAM</span></span>  <br/> |
|<span data-ttu-id="fa302-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="fa302-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fa302-109">0x7C08</span><span class="sxs-lookup"><span data-stu-id="fa302-109">0x7C08</span></span>  <br/> |
|<span data-ttu-id="fa302-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="fa302-110">Data type:</span></span>  <br/> |<span data-ttu-id="fa302-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fa302-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fa302-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="fa302-112">Area:</span></span>  <br/> |<span data-ttu-id="fa302-113">構成</span><span class="sxs-lookup"><span data-stu-id="fa302-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa302-114">解説</span><span class="sxs-lookup"><span data-stu-id="fa302-114">Remarks</span></span>

<span data-ttu-id="fa302-115">このプロパティには、XML データの任意のストリームが含まれています。</span><span class="sxs-lookup"><span data-stu-id="fa302-115">This property contains an arbitrary stream of XML data.</span></span> <span data-ttu-id="fa302-116">メッセージ内の他のプロパティは、このプロパティで使用する特定のスキーマを示している場合があります。</span><span class="sxs-lookup"><span data-stu-id="fa302-116">Other properties in the message may imply specific schemas to use in this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fa302-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="fa302-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fa302-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="fa302-118">Protocol specifications</span></span>

<span data-ttu-id="fa302-119">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fa302-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fa302-120">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="fa302-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fa302-121">[[OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fa302-121">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fa302-122">カテゴリの共有リストや稼働時間など、クライアントおよびサーバーの構成データの場所とプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="fa302-122">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fa302-123">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="fa302-123">Header files</span></span>

<span data-ttu-id="fa302-124">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fa302-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="fa302-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="fa302-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="fa302-126">Mapitags</span><span class="sxs-lookup"><span data-stu-id="fa302-126">Mapitags.h</span></span>
  
> <span data-ttu-id="fa302-127">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="fa302-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fa302-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="fa302-128">See also</span></span>



[<span data-ttu-id="fa302-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="fa302-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fa302-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fa302-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fa302-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="fa302-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fa302-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="fa302-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

