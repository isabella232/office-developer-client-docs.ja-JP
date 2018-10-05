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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: bee11c495d7f1ef21f9af70e6aa89f8c0d0f78b4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389604"
---
# <a name="pidtaglistsubscribe-canonical-property"></a><span data-ttu-id="2938c-103">PidTagListSubscribe 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2938c-103">PidTagListSubscribe Canonical Property</span></span>

  
  
<span data-ttu-id="2938c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2938c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2938c-105">多目的インターネット メール拡張 (MIME) メッセージのリストの購読のヘッダー フィールドの値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2938c-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Subscribe header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2938c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2938c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2938c-107">PR_LIST_SUBSCRIBE、PR_LIST_SUBSCRIBE_A、PR_LIST_SUBSCRIBE_W</span><span class="sxs-lookup"><span data-stu-id="2938c-107">PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A, PR_LIST_SUBSCRIBE_W</span></span>  <br/> |
|<span data-ttu-id="2938c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="2938c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2938c-109">0x1044</span><span class="sxs-lookup"><span data-stu-id="2938c-109">0x1044</span></span>  <br/> |
|<span data-ttu-id="2938c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2938c-110">Data type:</span></span>  <br/> |<span data-ttu-id="2938c-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2938c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2938c-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="2938c-112">Area:</span></span>  <br/> |<span data-ttu-id="2938c-113">その他</span><span class="sxs-lookup"><span data-stu-id="2938c-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2938c-114">備考</span><span class="sxs-lookup"><span data-stu-id="2938c-114">Remarks</span></span>

<span data-ttu-id="2938c-115">リスト購読ヘッダー フィールドを生成するには、クライアントは、目的の値にこれらのプロパティの値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2938c-115">To generate a List-Subscribe header field, clients must set the value of these properties to the desired value.</span></span> <span data-ttu-id="2938c-116">MIME ライターは、購読リストのヘッダー フィールドにこれらのプロパティの値をコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2938c-116">MIME writers must copy the value of these properties to the List-Subscribe header field.</span></span>
  
<span data-ttu-id="2938c-117">上記のようなサーバー関連のプロパティの値を設定するのには MIME クライアントは次の表で指定されているヘッダー フィールドを書き込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="2938c-117">To set the value of server-related properties like these, MIME clients must write the header fields as specified in the following table.</span></span>
  
|<span data-ttu-id="2938c-118">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="2938c-118">**Property**</span></span>|<span data-ttu-id="2938c-119">**優先のヘッダ ・ フィールド名**</span><span class="sxs-lookup"><span data-stu-id="2938c-119">**Preferred header field name**</span></span>|<span data-ttu-id="2938c-120">**別のヘッダ ・ フィールド名**</span><span class="sxs-lookup"><span data-stu-id="2938c-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2938c-121">**PidTagListSubscribe**</span><span class="sxs-lookup"><span data-stu-id="2938c-121">**PidTagListSubscribe**</span></span> <br/> |<span data-ttu-id="2938c-122">リスト購読</span><span class="sxs-lookup"><span data-stu-id="2938c-122">List-Subscribe</span></span>  <br/> |<span data-ttu-id="2938c-123">X リスト購読</span><span class="sxs-lookup"><span data-stu-id="2938c-123">X-List-Subscribe</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="2938c-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2938c-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2938c-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="2938c-125">Protocol specifications</span></span>

<span data-ttu-id="2938c-126">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2938c-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2938c-127">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="2938c-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2938c-128">[[MS OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2938c-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2938c-129">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="2938c-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2938c-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="2938c-130">Header files</span></span>

<span data-ttu-id="2938c-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2938c-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="2938c-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2938c-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="2938c-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2938c-133">Mapitags.h</span></span>
  
> <span data-ttu-id="2938c-134">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2938c-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2938c-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="2938c-135">See also</span></span>



[<span data-ttu-id="2938c-136">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2938c-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2938c-137">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2938c-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2938c-138">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2938c-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2938c-139">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2938c-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

