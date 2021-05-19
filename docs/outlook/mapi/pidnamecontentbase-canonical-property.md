---
title: PidNameContentBase 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameContentBase
api_type:
- COM
ms.assetid: ab197ace-6e7d-4ec5-9f6d-4a63a1eda11c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 501b54cfb7846a91aec7172cbe1d846c24704923
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331501"
---
# <a name="pidnamecontentbase-canonical-property"></a><span data-ttu-id="50c1e-103">PidNameContentBase 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="50c1e-103">PidNameContentBase Canonical Property</span></span>

  
  
<span data-ttu-id="50c1e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50c1e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50c1e-105">[RFC3282] Content-Base ヘッダー フィールドの値を含む。</span><span class="sxs-lookup"><span data-stu-id="50c1e-105">Contains an [RFC3282] Content-Base header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="50c1e-106">分名:</span><span class="sxs-lookup"><span data-stu-id="50c1e-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="50c1e-107">BodyContentBase</span><span class="sxs-lookup"><span data-stu-id="50c1e-107">BodyContentBase</span></span>  <br/> |
|<span data-ttu-id="50c1e-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="50c1e-108">Property set:</span></span>  <br/> |<span data-ttu-id="50c1e-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="50c1e-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="50c1e-110">プロパティ名:</span><span class="sxs-lookup"><span data-stu-id="50c1e-110">Property name:</span></span>  <br/> |<span data-ttu-id="50c1e-111">Content-Base</span><span class="sxs-lookup"><span data-stu-id="50c1e-111">Content-Base</span></span>  <br/> |
|<span data-ttu-id="50c1e-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="50c1e-112">Data type:</span></span>  <br/> |<span data-ttu-id="50c1e-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="50c1e-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="50c1e-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="50c1e-114">Area:</span></span>  <br/> |<span data-ttu-id="50c1e-115">メール</span><span class="sxs-lookup"><span data-stu-id="50c1e-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50c1e-116">注釈</span><span class="sxs-lookup"><span data-stu-id="50c1e-116">Remarks</span></span>

<span data-ttu-id="50c1e-117">このプロパティの値を設定するには、メッセージ本文にマップする MIME エンティティの Content-Base ヘッダー フィールドに目的の値を書き込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="50c1e-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write the desired value to a Content-Base header field on a MIME entity that maps to a message body.</span></span> <span data-ttu-id="50c1e-118">MIME リーダーは、このような MIME エンティティの Content-Base ヘッダー フィールドの値をこのプロパティの値にコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="50c1e-118">MIME readers must copy the value of a Content-Base header field on such a MIME entity to the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="50c1e-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="50c1e-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="50c1e-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="50c1e-120">Protocol specifications</span></span>

<span data-ttu-id="50c1e-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50c1e-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="50c1e-122">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="50c1e-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="50c1e-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50c1e-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="50c1e-124">インターネット標準の電子メール規則からメッセージ オブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="50c1e-124">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="50c1e-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="50c1e-125">Header files</span></span>

<span data-ttu-id="50c1e-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="50c1e-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="50c1e-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="50c1e-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="50c1e-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="50c1e-128">See also</span></span>



[<span data-ttu-id="50c1e-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="50c1e-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="50c1e-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="50c1e-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="50c1e-131">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="50c1e-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="50c1e-132">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="50c1e-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

