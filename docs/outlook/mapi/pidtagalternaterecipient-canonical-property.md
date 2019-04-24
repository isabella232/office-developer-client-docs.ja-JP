---
title: PidTagAlternateRecipient 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAlternateRecipient
api_type:
- HeaderDef
ms.assetid: df787b60-2f53-42ac-89b5-1b52c906f472
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7c304de3184e49044d3f83cef1f1ebaac019b2ee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360097"
---
# <a name="pidtagalternaterecipient-canonical-property"></a><span data-ttu-id="9e02e-103">PidTagAlternateRecipient 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9e02e-103">PidTagAlternateRecipient Canonical Property</span></span>

  
  
<span data-ttu-id="9e02e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e02e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e02e-105">元の受信者によって指定された代替受信者のエントリ識別子の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9e02e-105">Contains a list of entry identifiers for alternate recipients designated by the original recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9e02e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9e02e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9e02e-107">PR_ALTERNATE_RECIPIENT</span><span class="sxs-lookup"><span data-stu-id="9e02e-107">PR_ALTERNATE_RECIPIENT</span></span>  <br/> |
|<span data-ttu-id="9e02e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="9e02e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9e02e-109">0x3a01</span><span class="sxs-lookup"><span data-stu-id="9e02e-109">0x3A01</span></span>  <br/> |
|<span data-ttu-id="9e02e-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9e02e-110">Data type:</span></span>  <br/> |<span data-ttu-id="9e02e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9e02e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9e02e-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="9e02e-112">Area:</span></span>  <br/> |<span data-ttu-id="9e02e-113">Address</span><span class="sxs-lookup"><span data-stu-id="9e02e-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9e02e-114">解説</span><span class="sxs-lookup"><span data-stu-id="9e02e-114">Remarks</span></span>

<span data-ttu-id="9e02e-115">このプロパティは、自動転送されるメッセージに使用されます。</span><span class="sxs-lookup"><span data-stu-id="9e02e-115">This property is used for auto forwarded messages.</span></span> <span data-ttu-id="9e02e-116">代替受信者の[FLATENTRYLIST](flatentrylist.md)構造が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9e02e-116">It contains a [FLATENTRYLIST](flatentrylist.md) structure of alternate recipients.</span></span> <span data-ttu-id="9e02e-117">自動転送が許可されていない場合、または代替受信者が指定されていない場合は、配信不能レポートが生成されます。</span><span class="sxs-lookup"><span data-stu-id="9e02e-117">If autoforwarding is not permitted or if no alternate recipient has been designated, a nondelivery report is generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9e02e-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9e02e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9e02e-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="9e02e-119">Protocol specifications</span></span>

<span data-ttu-id="9e02e-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e02e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e02e-121">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="9e02e-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9e02e-122">[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e02e-122">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e02e-123">クライアントとサーバー間のデータ転送の順序と流れを処理します。</span><span class="sxs-lookup"><span data-stu-id="9e02e-123">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="9e02e-124">[[OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e02e-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e02e-125">IETF RFC2445、RFC2446、RFC2447、予定および会議の各オブジェクトを変換します。</span><span class="sxs-lookup"><span data-stu-id="9e02e-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="9e02e-126">[[OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e02e-126">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e02e-127">メッセージと添付ファイルオブジェクトをエンコードし、効率的なストリーム表現にデコードします。</span><span class="sxs-lookup"><span data-stu-id="9e02e-127">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9e02e-128">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="9e02e-128">Header files</span></span>

<span data-ttu-id="9e02e-129">Mapitags</span><span class="sxs-lookup"><span data-stu-id="9e02e-129">Mapitags.h</span></span>
  
> <span data-ttu-id="9e02e-130">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9e02e-130">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="9e02e-131">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9e02e-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="9e02e-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9e02e-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9e02e-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="9e02e-133">See also</span></span>



[<span data-ttu-id="9e02e-134">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="9e02e-134">FLATENTRYLIST</span></span>](flatentrylist.md)


[<span data-ttu-id="9e02e-135">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="9e02e-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9e02e-136">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9e02e-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9e02e-137">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9e02e-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9e02e-138">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9e02e-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

