---
title: PidTagExtendedRuleSizeLimit の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleSizeLimit
api_type:
- HeaderDef
ms.assetid: 87186764-fb58-4cdf-804d-bb13c5a8cb65
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 01d25614780f10f30d9e1314ea7f60ad3fbb4af0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802742"
---
# <a name="pidtagextendedrulesizelimit-canonical-property"></a><span data-ttu-id="8d30f-103">PidTagExtendedRuleSizeLimit の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="8d30f-103">PidTagExtendedRuleSizeLimit Canonical Property</span></span>

  
  
<span data-ttu-id="8d30f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8d30f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8d30f-105">最大のサイズ (バイト単位)、ユーザーは「拡張」ルールを 1 つに蓄積します。</span><span class="sxs-lookup"><span data-stu-id="8d30f-105">Contains the maximum size, in bytes, the user is allowed to accumulate for a single "extended" rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8d30f-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="8d30f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8d30f-107">PR_EXTENDED_RULE_SIZE_LIMIT</span><span class="sxs-lookup"><span data-stu-id="8d30f-107">PR_EXTENDED_RULE_SIZE_LIMIT</span></span>  <br/> |
|<span data-ttu-id="8d30f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8d30f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8d30f-109">0x0E9B</span><span class="sxs-lookup"><span data-stu-id="8d30f-109">0x0E9B</span></span>  <br/> |
|<span data-ttu-id="8d30f-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="8d30f-110">Data type:</span></span>  <br/> |<span data-ttu-id="8d30f-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8d30f-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8d30f-112">領域:</span><span class="sxs-lookup"><span data-stu-id="8d30f-112">Area:</span></span>  <br/> |<span data-ttu-id="8d30f-113">ルール</span><span class="sxs-lookup"><span data-stu-id="8d30f-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d30f-114">備考</span><span class="sxs-lookup"><span data-stu-id="8d30f-114">Remarks</span></span>

<span data-ttu-id="8d30f-115">ログオン オブジェクトでこのプロパティを設定すると、クライアントはこのプロパティで指定された値] の下の**PR_EXTENDED_RULE_MSG_CONDITION** ([PidTagExtendedRuleMessageCondition](pidtagextendedrulemessagecondition-canonical-property.md)) のプロパティのサイズを維持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d30f-115">If this property is set on the logon object, the client should keep the size of the **PR_EXTENDED_RULE_MSG_CONDITION** ([PidTagExtendedRuleMessageCondition](pidtagextendedrulemessagecondition-canonical-property.md)) property under the value specified by this property.</span></span> <span data-ttu-id="8d30f-116">逆に、クライアントは大きすぎるバイナリ プロパティを設定する場合、サーバーはエラーを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d30f-116">Conversely, the server should return an error if the client does attempt to set a binary property that is too large.</span></span>
  
<span data-ttu-id="8d30f-117">拡張ルールの詳細については、 [[MS OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8d30f-117">For information about extended rules, see [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8d30f-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8d30f-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8d30f-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8d30f-119">Protocol specifications</span></span>

<span data-ttu-id="8d30f-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d30f-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d30f-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="8d30f-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8d30f-122">[[MS OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d30f-122">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d30f-123">コア メッセージのストア オブジェクトの許可された操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="8d30f-123">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8d30f-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8d30f-124">Header files</span></span>

<span data-ttu-id="8d30f-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8d30f-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="8d30f-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8d30f-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="8d30f-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8d30f-127">Mapitags.h</span></span>
  
> <span data-ttu-id="8d30f-128">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8d30f-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8d30f-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="8d30f-129">See also</span></span>



[<span data-ttu-id="8d30f-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8d30f-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8d30f-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8d30f-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8d30f-132">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="8d30f-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8d30f-133">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="8d30f-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

