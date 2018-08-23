---
title: PidTagRuleUserFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleUserFlags
api_type:
- COM
ms.assetid: c5dfb21f-b35e-4521-bf2b-e3d03d98d75d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d2fb648de0c974c9b54ad925c271dd5eb7276b71
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585515"
---
# <a name="pidtagruleuserflags-canonical-property"></a><span data-ttu-id="08c48-103">PidTagRuleUserFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="08c48-103">PidTagRuleUserFlags Canonical Property</span></span>

  
  
<span data-ttu-id="08c48-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08c48-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08c48-105">このプロパティは、クライアントが排他的に使用のためにクライアントによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="08c48-105">This property is set by the client for the exclusive use of the client.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="08c48-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="08c48-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="08c48-107">PR_RULE_USER_FLAGS</span><span class="sxs-lookup"><span data-stu-id="08c48-107">PR_RULE_USER_FLAGS</span></span>  <br/> |
|<span data-ttu-id="08c48-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="08c48-108">Identifier:</span></span>  <br/> |<span data-ttu-id="08c48-109">0x6678</span><span class="sxs-lookup"><span data-stu-id="08c48-109">0x6678</span></span>  <br/> |
|<span data-ttu-id="08c48-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="08c48-110">Data type:</span></span>  <br/> |<span data-ttu-id="08c48-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="08c48-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="08c48-112">領域:</span><span class="sxs-lookup"><span data-stu-id="08c48-112">Area:</span></span>  <br/> |<span data-ttu-id="08c48-113">サーバー側のルール</span><span class="sxs-lookup"><span data-stu-id="08c48-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08c48-114">注釈</span><span class="sxs-lookup"><span data-stu-id="08c48-114">Remarks</span></span>

<span data-ttu-id="08c48-115">サーバーはクライアントが設定されている場合このプロパティの値を保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="08c48-115">The server must preserve the value of this property if it was set by the client.</span></span> <span data-ttu-id="08c48-116">サーバーを評価し、処理中に無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="08c48-116">The server must ignore it during rule evaluation and processing.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="08c48-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="08c48-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="08c48-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="08c48-118">Protocol specifications</span></span>

<span data-ttu-id="08c48-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08c48-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08c48-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="08c48-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="08c48-121">[[MS OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08c48-121">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08c48-122">サーバー上の受信電子メール メッセージを操作します。</span><span class="sxs-lookup"><span data-stu-id="08c48-122">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="08c48-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="08c48-123">Header files</span></span>

<span data-ttu-id="08c48-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="08c48-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="08c48-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="08c48-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="08c48-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="08c48-126">Mapitags.h</span></span>
  
> <span data-ttu-id="08c48-127">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="08c48-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="08c48-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="08c48-128">See also</span></span>



[<span data-ttu-id="08c48-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="08c48-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="08c48-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="08c48-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="08c48-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="08c48-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="08c48-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="08c48-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

