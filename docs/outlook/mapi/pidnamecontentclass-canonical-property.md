---
title: PidNameContentClass 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameContentClass
api_type:
- COM
ms.assetid: 6f623345-b30e-452f-a822-9308b455697a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 51788a49d1c0d01ef7ff5daca853000a8f1e34a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356351"
---
# <a name="pidnamecontentclass-canonical-property"></a><span data-ttu-id="76313-103">PidNameContentClass 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="76313-103">PidNameContentClass Canonical Property</span></span>

  
  
<span data-ttu-id="76313-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76313-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76313-105">[RFC3282] Content-Class ヘッダー フィールドの値を含む。</span><span class="sxs-lookup"><span data-stu-id="76313-105">Contains an [RFC3282] Content-Class header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="76313-106">分名:</span><span class="sxs-lookup"><span data-stu-id="76313-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="76313-107">なし</span><span class="sxs-lookup"><span data-stu-id="76313-107">None</span></span>  <br/> |
|<span data-ttu-id="76313-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="76313-108">Property set:</span></span>  <br/> |<span data-ttu-id="76313-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="76313-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="76313-110">プロパティ名:</span><span class="sxs-lookup"><span data-stu-id="76313-110">Property name:</span></span>  <br/> |<span data-ttu-id="76313-111">Content-Class</span><span class="sxs-lookup"><span data-stu-id="76313-111">Content-Class</span></span>  <br/> |
|<span data-ttu-id="76313-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="76313-112">Data type:</span></span>  <br/> |<span data-ttu-id="76313-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="76313-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="76313-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="76313-114">Area:</span></span>  <br/> |<span data-ttu-id="76313-115">メール</span><span class="sxs-lookup"><span data-stu-id="76313-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76313-116">注釈</span><span class="sxs-lookup"><span data-stu-id="76313-116">Remarks</span></span>

<span data-ttu-id="76313-117">このプロパティの値を設定するには、Multipurpose Internet Message Extensions (MIME) クライアントが目的の値を持つ Content-Class ヘッダー フィールドを記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="76313-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write a Content-Class header field with the desired value.</span></span> <span data-ttu-id="76313-118">MIME リーダーは、Content-Class ヘッダー フィールドの値をこのプロパティの値にコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="76313-118">MIME readers must copy the value of a Content-Class header field to the value of this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="76313-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="76313-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="76313-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="76313-120">Protocol specifications</span></span>

<span data-ttu-id="76313-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76313-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76313-122">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="76313-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="76313-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76313-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76313-124">インターネット標準の電子メール規則からメッセージ オブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="76313-124">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="76313-125">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76313-125">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76313-126">権限で管理されたエンコードされたメッセージのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="76313-126">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="76313-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="76313-127">Header files</span></span>

<span data-ttu-id="76313-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="76313-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="76313-129">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="76313-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="76313-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="76313-130">See also</span></span>



[<span data-ttu-id="76313-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="76313-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="76313-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="76313-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="76313-133">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="76313-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="76313-134">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="76313-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

