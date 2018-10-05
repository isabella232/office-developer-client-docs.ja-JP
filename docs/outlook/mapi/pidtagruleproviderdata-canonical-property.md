---
title: PidTagRuleProviderData 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleProviderData
api_type:
- COM
ms.assetid: b04a277c-b483-4f54-b360-311034b9a7ee
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e4d209c4f185ff253476beb04913e6a64884f9b6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388022"
---
# <a name="pidtagruleproviderdata-canonical-property"></a><span data-ttu-id="1fa61-103">PidTagRuleProviderData 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1fa61-103">PidTagRuleProviderData Canonical Property</span></span>

  
  
<span data-ttu-id="1fa61-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1fa61-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1fa61-105">クライアントの設定は、クライアントが排他的に使用する不透明なプロパティです。</span><span class="sxs-lookup"><span data-stu-id="1fa61-105">An opaque property that the client sets for the exclusive use of the client.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1fa61-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1fa61-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1fa61-107">PR_RULE_PROVIDER_DATA</span><span class="sxs-lookup"><span data-stu-id="1fa61-107">PR_RULE_PROVIDER_DATA</span></span>  <br/> |
|<span data-ttu-id="1fa61-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1fa61-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1fa61-109">0x6684</span><span class="sxs-lookup"><span data-stu-id="1fa61-109">0x6684</span></span>  <br/> |
|<span data-ttu-id="1fa61-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1fa61-110">Data type:</span></span>  <br/> |<span data-ttu-id="1fa61-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1fa61-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1fa61-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="1fa61-112">Area:</span></span>  <br/> |<span data-ttu-id="1fa61-113">サーバー側のルール</span><span class="sxs-lookup"><span data-stu-id="1fa61-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1fa61-114">備考</span><span class="sxs-lookup"><span data-stu-id="1fa61-114">Remarks</span></span>

<span data-ttu-id="1fa61-115">サーバーは、クライアントが設定されている場合、このプロパティの値を保持する必要がありますが、ルールの評価および処理中にその内容を無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fa61-115">The server must preserve the value of this property if it was set by the client but must ignore its contents during rule evaluation and processing.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1fa61-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1fa61-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1fa61-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1fa61-117">Protocol specifications</span></span>

<span data-ttu-id="1fa61-118">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1fa61-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1fa61-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="1fa61-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1fa61-120">[[MS OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1fa61-120">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1fa61-121">サーバー上の受信電子メール メッセージを操作します。</span><span class="sxs-lookup"><span data-stu-id="1fa61-121">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1fa61-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="1fa61-122">Header files</span></span>

<span data-ttu-id="1fa61-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1fa61-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="1fa61-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1fa61-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="1fa61-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1fa61-125">Mapitags.h</span></span>
  
> <span data-ttu-id="1fa61-126">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1fa61-126">Contains definitions of properties listed as associated properties.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="1fa61-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="1fa61-127">See also</span></span>



[<span data-ttu-id="1fa61-128">PidTagRuleProvider 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1fa61-128">PidTagRuleProvider Canonical Property</span></span>](pidtagruleprovider-canonical-property.md)


[<span data-ttu-id="1fa61-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1fa61-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1fa61-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1fa61-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1fa61-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1fa61-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1fa61-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1fa61-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

