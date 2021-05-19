---
title: PidNameCrossReference 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameCrossReference
api_type:
- COM
ms.assetid: d16e1adf-c911-427e-9c98-678a303e6791
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8f8706ec3db36cddbe7be7420ba27683c190cd43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331445"
---
# <a name="pidnamecrossreference-canonical-property"></a><span data-ttu-id="78e69-103">PidNameCrossReference 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="78e69-103">PidNameCrossReference Canonical Property</span></span>

  
  
<span data-ttu-id="78e69-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78e69-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78e69-105">[RFC3282] 外部参照ヘッダー フィールドの値を含む。</span><span class="sxs-lookup"><span data-stu-id="78e69-105">Contains an [RFC3282] Xref header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="78e69-106">分名:</span><span class="sxs-lookup"><span data-stu-id="78e69-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="78e69-107">なし</span><span class="sxs-lookup"><span data-stu-id="78e69-107">None</span></span>  <br/> |
|<span data-ttu-id="78e69-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="78e69-108">Property set:</span></span>  <br/> |<span data-ttu-id="78e69-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="78e69-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="78e69-110">プロパティ名:</span><span class="sxs-lookup"><span data-stu-id="78e69-110">Property name:</span></span>  <br/> |<span data-ttu-id="78e69-111">Xref</span><span class="sxs-lookup"><span data-stu-id="78e69-111">Xref</span></span>  <br/> |
|<span data-ttu-id="78e69-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="78e69-112">Data type:</span></span>  <br/> |<span data-ttu-id="78e69-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="78e69-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="78e69-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="78e69-114">Area:</span></span>  <br/> |<span data-ttu-id="78e69-115">メール</span><span class="sxs-lookup"><span data-stu-id="78e69-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="78e69-116">注釈</span><span class="sxs-lookup"><span data-stu-id="78e69-116">Remarks</span></span>

<span data-ttu-id="78e69-117">このプロパティの値を設定するには、Multipurpose Internet Message Extensions (MIME) クライアントが目的の値を XRef ヘッダー フィールドに書き込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="78e69-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write the desired value to an XRef header field.</span></span> <span data-ttu-id="78e69-118">MIME リーダーは、XRef ヘッダー フィールドの値をこのプロパティの値にコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="78e69-118">MIME readers must copy the value of an XRef header field to the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="78e69-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="78e69-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="78e69-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="78e69-120">Protocol specifications</span></span>

<span data-ttu-id="78e69-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="78e69-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="78e69-122">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="78e69-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="78e69-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="78e69-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="78e69-124">インターネット標準の電子メール規則からメッセージ オブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="78e69-124">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="78e69-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="78e69-125">Header files</span></span>

<span data-ttu-id="78e69-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="78e69-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="78e69-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="78e69-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="78e69-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="78e69-128">See also</span></span>



[<span data-ttu-id="78e69-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="78e69-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="78e69-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="78e69-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="78e69-131">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="78e69-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="78e69-132">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="78e69-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

