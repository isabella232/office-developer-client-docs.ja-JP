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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 588747205ee3922fef7b107dc024f074a6ee527e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387210"
---
# <a name="pidtaglisthelp-canonical-property"></a><span data-ttu-id="0114b-103">PidTagListHelp 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0114b-103">PidTagListHelp Canonical Property</span></span>

  
  
<span data-ttu-id="0114b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0114b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0114b-105">多目的インターネット メール拡張 (MIME) メッセージの一覧ヘルプ ヘッダー フィールドの値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0114b-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Help header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0114b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="0114b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0114b-107">PR_LIST_HELP、PR_LIST_HELP_A、PR_LIST_HELP_W</span><span class="sxs-lookup"><span data-stu-id="0114b-107">PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W</span></span>  <br/> |
|<span data-ttu-id="0114b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="0114b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0114b-109">0x1043</span><span class="sxs-lookup"><span data-stu-id="0114b-109">0x1043</span></span>  <br/> |
|<span data-ttu-id="0114b-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="0114b-110">Data type:</span></span>  <br/> |<span data-ttu-id="0114b-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0114b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0114b-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="0114b-112">Area:</span></span>  <br/> |<span data-ttu-id="0114b-113">その他</span><span class="sxs-lookup"><span data-stu-id="0114b-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0114b-114">備考</span><span class="sxs-lookup"><span data-stu-id="0114b-114">Remarks</span></span>

<span data-ttu-id="0114b-115">リスト ヘルプ ヘッダー フィールドを生成するには、クライアントは、目的の値を**PR_LIST_HELP**または関連付けられたプロパティの値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0114b-115">To generate a List-Help header field, clients must set the value of **PR_LIST_HELP** or an associated property to the desired value.</span></span> <span data-ttu-id="0114b-116">MIME ライターは、リスト ヘルプ ヘッダー フィールドにこの値をコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0114b-116">MIME writers must copy this value to the List-Help header field.</span></span> 
  
<span data-ttu-id="0114b-117">これらの一覧のサーバーに関連するプロパティの値を設定するのには MIME クライアントは次の表で指定されているヘッダー フィールドを書き込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="0114b-117">To set the value of these list server-related properties, MIME clients must write the header fields as specified in the following table:</span></span>
  
|<span data-ttu-id="0114b-118">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="0114b-118">**Property**</span></span>|<span data-ttu-id="0114b-119">**優先のヘッダ ・ フィールド名**</span><span class="sxs-lookup"><span data-stu-id="0114b-119">**Preferred header field name**</span></span>|<span data-ttu-id="0114b-120">**別のヘッダ ・ フィールド名**</span><span class="sxs-lookup"><span data-stu-id="0114b-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0114b-121">**PR_LIST_HELP**</span><span class="sxs-lookup"><span data-stu-id="0114b-121">**PR_LIST_HELP**</span></span> <br/> |<span data-ttu-id="0114b-122">リスト ヘルプ</span><span class="sxs-lookup"><span data-stu-id="0114b-122">List-Help</span></span>  <br/> |<span data-ttu-id="0114b-123">X のヘルプ一覧</span><span class="sxs-lookup"><span data-stu-id="0114b-123">X-List-Help</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="0114b-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="0114b-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0114b-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="0114b-125">Protocol specifications</span></span>

<span data-ttu-id="0114b-126">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0114b-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0114b-127">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="0114b-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0114b-128">[[MS OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0114b-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0114b-129">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="0114b-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0114b-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="0114b-130">Header files</span></span>

<span data-ttu-id="0114b-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0114b-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="0114b-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="0114b-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="0114b-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0114b-133">Mapitags.h</span></span>
  
> <span data-ttu-id="0114b-134">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0114b-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0114b-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="0114b-135">See also</span></span>



[<span data-ttu-id="0114b-136">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0114b-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0114b-137">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0114b-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0114b-138">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0114b-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0114b-139">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0114b-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

