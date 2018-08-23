---
title: PidTagListUnsubscribe 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListUnsubscribe
api_type:
- HeaderDef
ms.assetid: 4e6bfbc7-7586-43cc-9380-daa0fe3d85a5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 87f5c3fc8475f9795847e4680babb26682608a5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802947"
---
# <a name="pidtaglistunsubscribe-canonical-property"></a><span data-ttu-id="aa604-103">PidTagListUnsubscribe 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="aa604-103">PidTagListUnsubscribe Canonical Property</span></span>

  
  
<span data-ttu-id="aa604-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aa604-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aa604-105">多目的インターネット メール拡張 (MIME) メッセージのリストの購読中止のヘッダー フィールドの値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="aa604-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Unsubscribe header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aa604-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="aa604-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aa604-107">PR_LIST_UNSUBSCRIBE、PR_LIST_UNSUBSCRIBE_A、PR_LIST_UNSUBSCRIBE_W</span><span class="sxs-lookup"><span data-stu-id="aa604-107">PR_LIST_UNSUBSCRIBE, PR_LIST_UNSUBSCRIBE_A, PR_LIST_UNSUBSCRIBE_W</span></span>  <br/> |
|<span data-ttu-id="aa604-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="aa604-108">Identifier:</span></span>  <br/> |<span data-ttu-id="aa604-109">0x1045</span><span class="sxs-lookup"><span data-stu-id="aa604-109">0x1045</span></span>  <br/> |
|<span data-ttu-id="aa604-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="aa604-110">Data type:</span></span>  <br/> |<span data-ttu-id="aa604-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="aa604-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="aa604-112">領域:</span><span class="sxs-lookup"><span data-stu-id="aa604-112">Area:</span></span>  <br/> |<span data-ttu-id="aa604-113">その他</span><span class="sxs-lookup"><span data-stu-id="aa604-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aa604-114">注釈</span><span class="sxs-lookup"><span data-stu-id="aa604-114">Remarks</span></span>

<span data-ttu-id="aa604-115">リストの購読中止のヘッダー フィールドを生成するためにクライアントは、目的の値にこれらのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa604-115">To generate a List-Unsubscribe header field, clients must set these properties to the desired value.</span></span> <span data-ttu-id="aa604-116">MIME ライターは、リストの購読中止のヘッダー フィールドにこれらのプロパティの値をコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa604-116">MIME writers must copy the value of these properties to the List-Unsubscribe header field.</span></span>
  
<span data-ttu-id="aa604-117">これらの一覧のサーバーに関連するプロパティの値を設定するのには MIME クライアントは次の表で指定されているヘッダー フィールドを書き込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa604-117">To set the value of these list server-related properties, MIME clients must write the header fields as specified in the following table.</span></span>
  
|<span data-ttu-id="aa604-118">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="aa604-118">**Property**</span></span>|<span data-ttu-id="aa604-119">**優先のヘッダ ・ フィールド名**</span><span class="sxs-lookup"><span data-stu-id="aa604-119">**Preferred header field name**</span></span>|<span data-ttu-id="aa604-120">**別のヘッダ ・ フィールド名**</span><span class="sxs-lookup"><span data-stu-id="aa604-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="aa604-121">**PR_LIST_UNSUBSCRIBE**</span><span class="sxs-lookup"><span data-stu-id="aa604-121">**PR_LIST_UNSUBSCRIBE**</span></span> <br/> |<span data-ttu-id="aa604-122">リストの購読を解除</span><span class="sxs-lookup"><span data-stu-id="aa604-122">List-Unsubscribe</span></span>  <br/> |<span data-ttu-id="aa604-123">X リストの購読中止</span><span class="sxs-lookup"><span data-stu-id="aa604-123">X-List-Unsubscribe</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="aa604-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="aa604-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="aa604-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="aa604-125">Protocol specifications</span></span>

<span data-ttu-id="aa604-126">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aa604-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aa604-127">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="aa604-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="aa604-128">[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aa604-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aa604-129">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="aa604-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="aa604-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="aa604-130">Header files</span></span>

<span data-ttu-id="aa604-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aa604-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="aa604-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="aa604-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="aa604-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="aa604-133">Mapitags.h</span></span>
  
> <span data-ttu-id="aa604-134">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="aa604-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aa604-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="aa604-135">See also</span></span>



[<span data-ttu-id="aa604-136">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="aa604-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aa604-137">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="aa604-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aa604-138">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="aa604-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aa604-139">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="aa604-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

