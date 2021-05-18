---
title: PidTagListSubscribe 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListSubscribe
api_type:
- HeaderDef
ms.assetid: 97387a82-8e40-4c76-818c-2229fac12e01
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: bee11c495d7f1ef21f9af70e6aa89f8c0d0f78b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279658"
---
# <a name="pidtaglistsubscribe-canonical-property"></a><span data-ttu-id="b7b85-103">PidTagListSubscribe 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b7b85-103">PidTagListSubscribe Canonical Property</span></span>

  
  
<span data-ttu-id="b7b85-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7b85-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7b85-105">多目的インターネット メール拡張機能 (MIME) メッセージのヘッダー フィールドの値List-Subscribeします。</span><span class="sxs-lookup"><span data-stu-id="b7b85-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Subscribe header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b7b85-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b7b85-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b7b85-107">PR_LIST_SUBSCRIBE、PR_LIST_SUBSCRIBE_A、PR_LIST_SUBSCRIBE_W</span><span class="sxs-lookup"><span data-stu-id="b7b85-107">PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A, PR_LIST_SUBSCRIBE_W</span></span>  <br/> |
|<span data-ttu-id="b7b85-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b7b85-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b7b85-109">0x1044</span><span class="sxs-lookup"><span data-stu-id="b7b85-109">0x1044</span></span>  <br/> |
|<span data-ttu-id="b7b85-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b7b85-110">Data type:</span></span>  <br/> |<span data-ttu-id="b7b85-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b7b85-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b7b85-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="b7b85-112">Area:</span></span>  <br/> |<span data-ttu-id="b7b85-113">その他</span><span class="sxs-lookup"><span data-stu-id="b7b85-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7b85-114">注釈</span><span class="sxs-lookup"><span data-stu-id="b7b85-114">Remarks</span></span>

<span data-ttu-id="b7b85-115">ヘッダー フィールドをList-Subscribeするには、クライアントがこれらのプロパティの値を目的の値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7b85-115">To generate a List-Subscribe header field, clients must set the value of these properties to the desired value.</span></span> <span data-ttu-id="b7b85-116">MIME ライターは、これらのプロパティの値をヘッダー フィールドのList-Subscribeする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7b85-116">MIME writers must copy the value of these properties to the List-Subscribe header field.</span></span>
  
<span data-ttu-id="b7b85-117">このようなサーバー関連のプロパティの値を設定するには、MIME クライアントが次の表で指定したヘッダー フィールドを記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7b85-117">To set the value of server-related properties like these, MIME clients must write the header fields as specified in the following table.</span></span>
  
|<span data-ttu-id="b7b85-118">**Property**</span><span class="sxs-lookup"><span data-stu-id="b7b85-118">**Property**</span></span>|<span data-ttu-id="b7b85-119">**優先ヘッダー フィールド名**</span><span class="sxs-lookup"><span data-stu-id="b7b85-119">**Preferred header field name**</span></span>|<span data-ttu-id="b7b85-120">**代替ヘッダー フィールド名**</span><span class="sxs-lookup"><span data-stu-id="b7b85-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b7b85-121">**PidTagListSubscribe**</span><span class="sxs-lookup"><span data-stu-id="b7b85-121">**PidTagListSubscribe**</span></span> <br/> |<span data-ttu-id="b7b85-122">List-Subscribe</span><span class="sxs-lookup"><span data-stu-id="b7b85-122">List-Subscribe</span></span>  <br/> |<span data-ttu-id="b7b85-123">X-List-Subscribe</span><span class="sxs-lookup"><span data-stu-id="b7b85-123">X-List-Subscribe</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b7b85-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b7b85-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b7b85-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b7b85-125">Protocol specifications</span></span>

<span data-ttu-id="b7b85-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7b85-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7b85-127">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="b7b85-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b7b85-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7b85-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7b85-129">インターネット標準の電子メール規則からメッセージ オブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="b7b85-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b7b85-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b7b85-130">Header files</span></span>

<span data-ttu-id="b7b85-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b7b85-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="b7b85-132">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b7b85-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="b7b85-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b7b85-133">Mapitags.h</span></span>
  
> <span data-ttu-id="b7b85-134">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="b7b85-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b7b85-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="b7b85-135">See also</span></span>



[<span data-ttu-id="b7b85-136">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="b7b85-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b7b85-137">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b7b85-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b7b85-138">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="b7b85-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b7b85-139">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="b7b85-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

