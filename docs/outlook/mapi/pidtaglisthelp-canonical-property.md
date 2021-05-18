---
title: PidTagListHelp 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListHelp
api_type:
- HeaderDef
ms.assetid: 403324b8-c992-4823-aa0f-0414b283debc
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 588747205ee3922fef7b107dc024f074a6ee527e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279630"
---
# <a name="pidtaglisthelp-canonical-property"></a><span data-ttu-id="ee78d-103">PidTagListHelp 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ee78d-103">PidTagListHelp Canonical Property</span></span>

  
  
<span data-ttu-id="ee78d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee78d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee78d-105">多目的インターネット メール拡張機能 (MIME) メッセージのヘッダー フィールドの値List-Helpします。</span><span class="sxs-lookup"><span data-stu-id="ee78d-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Help header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ee78d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ee78d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ee78d-107">PR_LIST_HELP、PR_LIST_HELP_A、PR_LIST_HELP_W</span><span class="sxs-lookup"><span data-stu-id="ee78d-107">PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W</span></span>  <br/> |
|<span data-ttu-id="ee78d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ee78d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ee78d-109">0x1043</span><span class="sxs-lookup"><span data-stu-id="ee78d-109">0x1043</span></span>  <br/> |
|<span data-ttu-id="ee78d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ee78d-110">Data type:</span></span>  <br/> |<span data-ttu-id="ee78d-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ee78d-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ee78d-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="ee78d-112">Area:</span></span>  <br/> |<span data-ttu-id="ee78d-113">その他</span><span class="sxs-lookup"><span data-stu-id="ee78d-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee78d-114">注釈</span><span class="sxs-lookup"><span data-stu-id="ee78d-114">Remarks</span></span>

<span data-ttu-id="ee78d-115">ヘッダー フィールドをList-Helpするには、クライアントは、PR_LIST_HELPまたは関連付けられているプロパティの **値** を目的の値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee78d-115">To generate a List-Help header field, clients must set the value of **PR_LIST_HELP** or an associated property to the desired value.</span></span> <span data-ttu-id="ee78d-116">MIME ライターは、この値をヘッダー フィールドList-Helpする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee78d-116">MIME writers must copy this value to the List-Help header field.</span></span> 
  
<span data-ttu-id="ee78d-117">これらのリスト サーバー関連のプロパティの値を設定するには、MIME クライアントが次の表で指定したヘッダー フィールドを記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee78d-117">To set the value of these list server-related properties, MIME clients must write the header fields as specified in the following table:</span></span>
  
|<span data-ttu-id="ee78d-118">**Property**</span><span class="sxs-lookup"><span data-stu-id="ee78d-118">**Property**</span></span>|<span data-ttu-id="ee78d-119">**優先ヘッダー フィールド名**</span><span class="sxs-lookup"><span data-stu-id="ee78d-119">**Preferred header field name**</span></span>|<span data-ttu-id="ee78d-120">**代替ヘッダー フィールド名**</span><span class="sxs-lookup"><span data-stu-id="ee78d-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ee78d-121">**PR_LIST_HELP**</span><span class="sxs-lookup"><span data-stu-id="ee78d-121">**PR_LIST_HELP**</span></span> <br/> |<span data-ttu-id="ee78d-122">List-Help</span><span class="sxs-lookup"><span data-stu-id="ee78d-122">List-Help</span></span>  <br/> |<span data-ttu-id="ee78d-123">X-List-Help</span><span class="sxs-lookup"><span data-stu-id="ee78d-123">X-List-Help</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ee78d-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ee78d-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ee78d-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ee78d-125">Protocol specifications</span></span>

<span data-ttu-id="ee78d-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ee78d-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ee78d-127">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="ee78d-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ee78d-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ee78d-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ee78d-129">インターネット標準の電子メール規則からメッセージ オブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="ee78d-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ee78d-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ee78d-130">Header files</span></span>

<span data-ttu-id="ee78d-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ee78d-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="ee78d-132">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ee78d-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="ee78d-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ee78d-133">Mapitags.h</span></span>
  
> <span data-ttu-id="ee78d-134">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="ee78d-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ee78d-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="ee78d-135">See also</span></span>



[<span data-ttu-id="ee78d-136">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="ee78d-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ee78d-137">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ee78d-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ee78d-138">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="ee78d-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ee78d-139">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="ee78d-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

