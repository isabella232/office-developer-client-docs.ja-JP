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
ms.openlocfilehash: 7a9a5d090babce8105fab43bf8401448373777cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802957"
---
# <a name="pidtaglisthelp-canonical-property"></a><span data-ttu-id="0db8c-103">PidTagListHelp 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0db8c-103">PidTagListHelp Canonical Property</span></span>

  
  
<span data-ttu-id="0db8c-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0db8c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0db8c-105">多目的インターネット メール拡張 (MIME) メッセージの一覧ヘルプ ヘッダー フィールドの値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0db8c-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Help header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0db8c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="0db8c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0db8c-107">PR_LIST_HELP、PR_LIST_HELP_A、PR_LIST_HELP_W</span><span class="sxs-lookup"><span data-stu-id="0db8c-107">PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W</span></span>  <br/> |
|<span data-ttu-id="0db8c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="0db8c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0db8c-109">0x1043</span><span class="sxs-lookup"><span data-stu-id="0db8c-109">0x1043</span></span>  <br/> |
|<span data-ttu-id="0db8c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="0db8c-110">Data type:</span></span>  <br/> |<span data-ttu-id="0db8c-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0db8c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0db8c-112">領域:</span><span class="sxs-lookup"><span data-stu-id="0db8c-112">Area:</span></span>  <br/> |<span data-ttu-id="0db8c-113">その他</span><span class="sxs-lookup"><span data-stu-id="0db8c-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0db8c-114">注釈</span><span class="sxs-lookup"><span data-stu-id="0db8c-114">Remarks</span></span>

<span data-ttu-id="0db8c-115">リスト ヘルプ ヘッダー フィールドを生成するには、クライアントは、目的の値を**PR_LIST_HELP**または関連付けられたプロパティの値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0db8c-115">To generate a List-Help header field, clients must set the value of **PR_LIST_HELP** or an associated property to the desired value.</span></span> <span data-ttu-id="0db8c-116">MIME ライターは、リスト ヘルプ ヘッダー フィールドにこの値をコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0db8c-116">MIME writers must copy this value to the List-Help header field.</span></span> 
  
<span data-ttu-id="0db8c-117">これらの一覧のサーバーに関連するプロパティの値を設定するのには MIME クライアントは次の表で指定されているヘッダー フィールドを書き込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="0db8c-117">To set the value of these list server-related properties, MIME clients must write the header fields as specified in the following table:</span></span>
  
|<span data-ttu-id="0db8c-118">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="0db8c-118">**Property**</span></span>|<span data-ttu-id="0db8c-119">**優先のヘッダ ・ フィールド名**</span><span class="sxs-lookup"><span data-stu-id="0db8c-119">**Preferred header field name**</span></span>|<span data-ttu-id="0db8c-120">**別のヘッダ ・ フィールド名**</span><span class="sxs-lookup"><span data-stu-id="0db8c-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0db8c-121">**PR_LIST_HELP**</span><span class="sxs-lookup"><span data-stu-id="0db8c-121">**PR_LIST_HELP**</span></span> <br/> |<span data-ttu-id="0db8c-122">リスト ヘルプ</span><span class="sxs-lookup"><span data-stu-id="0db8c-122">List-Help</span></span>  <br/> |<span data-ttu-id="0db8c-123">X のヘルプ一覧</span><span class="sxs-lookup"><span data-stu-id="0db8c-123">X-List-Help</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="0db8c-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="0db8c-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0db8c-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="0db8c-125">Protocol specifications</span></span>

<span data-ttu-id="0db8c-126">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0db8c-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0db8c-127">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="0db8c-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0db8c-128">[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0db8c-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0db8c-129">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="0db8c-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0db8c-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="0db8c-130">Header files</span></span>

<span data-ttu-id="0db8c-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0db8c-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="0db8c-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="0db8c-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="0db8c-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0db8c-133">Mapitags.h</span></span>
  
> <span data-ttu-id="0db8c-134">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0db8c-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0db8c-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="0db8c-135">See also</span></span>



[<span data-ttu-id="0db8c-136">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0db8c-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0db8c-137">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0db8c-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0db8c-138">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0db8c-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0db8c-139">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0db8c-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

