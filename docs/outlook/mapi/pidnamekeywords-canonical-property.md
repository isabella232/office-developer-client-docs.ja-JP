---
title: PidNameKeywords 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameKeywords
api_type:
- COM
ms.assetid: bcc0cda0-02bc-49a5-9fb9-850b4c2867c1
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 90e5b370dace12dbe529465259b8551516fda491
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338060"
---
# <a name="pidnamekeywords-canonical-property"></a><span data-ttu-id="141c8-103">PidNameKeywords 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="141c8-103">PidNameKeywords Canonical Property</span></span>

  
  
<span data-ttu-id="141c8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="141c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="141c8-105">メッセージ オブジェクトのキーワードまたはカテゴリを含む。</span><span class="sxs-lookup"><span data-stu-id="141c8-105">Contains keywords or categories for the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="141c8-106">分名:</span><span class="sxs-lookup"><span data-stu-id="141c8-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="141c8-107">なし</span><span class="sxs-lookup"><span data-stu-id="141c8-107">None</span></span>  <br/> |
|<span data-ttu-id="141c8-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="141c8-108">Property set:</span></span>  <br/> |<span data-ttu-id="141c8-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="141c8-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="141c8-110">プロパティ名:</span><span class="sxs-lookup"><span data-stu-id="141c8-110">Property name:</span></span>  <br/> |<span data-ttu-id="141c8-111">キーワード</span><span class="sxs-lookup"><span data-stu-id="141c8-111">Keywords</span></span>  <br/> |
|<span data-ttu-id="141c8-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="141c8-112">Data type:</span></span>  <br/> |<span data-ttu-id="141c8-113">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="141c8-113">PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="141c8-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="141c8-114">Area:</span></span>  <br/> |<span data-ttu-id="141c8-115">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="141c8-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="141c8-116">注釈</span><span class="sxs-lookup"><span data-stu-id="141c8-116">Remarks</span></span>

<span data-ttu-id="141c8-117">このプロパティの複数値文字列内の各文字列の長さである、メッセージ オブジェクトのカテゴリを指定する複数文字列値は、256 未満である必要があります。</span><span class="sxs-lookup"><span data-stu-id="141c8-117">A multi-string value that specifies the categories for a message object, the length of each string within this property multi-value string, must be less than 256.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="141c8-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="141c8-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="141c8-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="141c8-119">Protocol specifications</span></span>

<span data-ttu-id="141c8-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="141c8-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="141c8-121">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="141c8-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="141c8-122">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="141c8-122">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="141c8-123">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="141c8-123">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="141c8-124">[[MS-OXODOC]](https://msdn.microsoft.com/library/103007c8-5066-4bed-84e3-4465907af098%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="141c8-124">[[MS-OXODOC]](https://msdn.microsoft.com/library/103007c8-5066-4bed-84e3-4465907af098%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="141c8-125">ドキュメントで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="141c8-125">Specifies the properties and operations that are permissible on documents.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="141c8-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="141c8-126">Header files</span></span>

<span data-ttu-id="141c8-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="141c8-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="141c8-128">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="141c8-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="141c8-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="141c8-129">See also</span></span>



[<span data-ttu-id="141c8-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="141c8-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="141c8-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="141c8-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="141c8-132">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="141c8-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="141c8-133">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="141c8-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

