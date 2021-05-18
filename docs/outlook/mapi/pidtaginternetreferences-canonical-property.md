---
title: PidTagInternetReferences 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInternetReferences
api_type:
- HeaderDef
ms.assetid: 645fe61d-414a-455e-b034-db3cfd003b9d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 431a212b6e024d695fe2de084080996d8b1054d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360411"
---
# <a name="pidtaginternetreferences-canonical-property"></a><span data-ttu-id="eefa4-103">PidTagInternetReferences 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="eefa4-103">PidTagInternetReferences Canonical Property</span></span>

  
  
<span data-ttu-id="eefa4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eefa4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eefa4-105">多目的インターネット メール拡張機能 (MIME) メッセージの [参照] ヘッダー フィールドの値を格納します。</span><span class="sxs-lookup"><span data-stu-id="eefa4-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's References header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eefa4-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="eefa4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="eefa4-107">PR_INTERNET_REFERENCES、PR_INTERNET_REFERENCES_A、PR_INTERNET_REFERENCES_W</span><span class="sxs-lookup"><span data-stu-id="eefa4-107">PR_INTERNET_REFERENCES, PR_INTERNET_REFERENCES_A, PR_INTERNET_REFERENCES_W</span></span>  <br/> |
|<span data-ttu-id="eefa4-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="eefa4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="eefa4-109">0x1039</span><span class="sxs-lookup"><span data-stu-id="eefa4-109">0x1039</span></span>  <br/> |
|<span data-ttu-id="eefa4-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="eefa4-110">Data type:</span></span>  <br/> |<span data-ttu-id="eefa4-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="eefa4-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="eefa4-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="eefa4-112">Area:</span></span>  <br/> |<span data-ttu-id="eefa4-113">MIME</span><span class="sxs-lookup"><span data-stu-id="eefa4-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eefa4-114">注釈</span><span class="sxs-lookup"><span data-stu-id="eefa4-114">Remarks</span></span>

<span data-ttu-id="eefa4-115">参照ヘッダー フィールドを生成するには、クライアントがこれらのプロパティを目的の値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eefa4-115">To generate a References header field, clients must set these properties to the desired value.</span></span> <span data-ttu-id="eefa4-116">MIME ライターは、これらのプロパティの値を References ヘッダー フィールドにコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="eefa4-116">MIME writers must copy the value of these properties to the References header field.</span></span>
  
<span data-ttu-id="eefa4-117">これらのプロパティの値を設定するには、MIME クライアントが目的の値を References ヘッダー フィールドに書き込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="eefa4-117">To set the value of these properties, MIME clients must write the desired value to a References header field.</span></span> <span data-ttu-id="eefa4-118">MIME リーダーは、参照ヘッダー フィールドの値をこれらのプロパティにコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="eefa4-118">MIME readers must copy the value of the References header field to these properties.</span></span> <span data-ttu-id="eefa4-119">MIME リーダーの長さが 64 KB を超えると、これらのプロパティの値が切り詰められることがあります。</span><span class="sxs-lookup"><span data-stu-id="eefa4-119">MIME readers may truncate the value of these properties if it exceeds 64KB in length.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="eefa4-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="eefa4-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="eefa4-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="eefa4-121">Protocol specifications</span></span>

<span data-ttu-id="eefa4-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eefa4-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eefa4-123">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="eefa4-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="eefa4-124">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eefa4-124">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eefa4-125">インターネット標準の電子メール規則からメッセージ オブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="eefa4-125">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="eefa4-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="eefa4-126">Header files</span></span>

<span data-ttu-id="eefa4-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eefa4-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="eefa4-128">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="eefa4-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="eefa4-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="eefa4-129">Mapitags.h</span></span>
  
> <span data-ttu-id="eefa4-130">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="eefa4-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eefa4-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="eefa4-131">See also</span></span>



[<span data-ttu-id="eefa4-132">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="eefa4-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="eefa4-133">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="eefa4-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="eefa4-134">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="eefa4-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="eefa4-135">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="eefa4-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

