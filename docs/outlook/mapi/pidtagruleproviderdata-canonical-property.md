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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335421"
---
# <a name="pidtagruleproviderdata-canonical-property"></a><span data-ttu-id="b4db1-103">PidTagRuleProviderData 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b4db1-103">PidTagRuleProviderData Canonical Property</span></span>

  
  
<span data-ttu-id="b4db1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4db1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4db1-105">クライアントが排他的にクライアントを使用するために設定する、不透明なプロパティ。</span><span class="sxs-lookup"><span data-stu-id="b4db1-105">An opaque property that the client sets for the exclusive use of the client.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b4db1-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b4db1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b4db1-107">PR_RULE_PROVIDER_DATA</span><span class="sxs-lookup"><span data-stu-id="b4db1-107">PR_RULE_PROVIDER_DATA</span></span>  <br/> |
|<span data-ttu-id="b4db1-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b4db1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b4db1-109">0x6684</span><span class="sxs-lookup"><span data-stu-id="b4db1-109">0x6684</span></span>  <br/> |
|<span data-ttu-id="b4db1-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b4db1-110">Data type:</span></span>  <br/> |<span data-ttu-id="b4db1-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b4db1-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b4db1-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="b4db1-112">Area:</span></span>  <br/> |<span data-ttu-id="b4db1-113">サーバー側のルール</span><span class="sxs-lookup"><span data-stu-id="b4db1-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4db1-114">解説</span><span class="sxs-lookup"><span data-stu-id="b4db1-114">Remarks</span></span>

<span data-ttu-id="b4db1-115">このプロパティがクライアントによって設定されている場合、サーバーはこのプロパティの値を保持する必要がありますが、ルールの評価および処理中にその内容を無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4db1-115">The server must preserve the value of this property if it was set by the client but must ignore its contents during rule evaluation and processing.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b4db1-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b4db1-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b4db1-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b4db1-117">Protocol specifications</span></span>

<span data-ttu-id="b4db1-118">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b4db1-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b4db1-119">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="b4db1-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b4db1-120">[[OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b4db1-120">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b4db1-121">サーバー上の受信電子メールメッセージを操作します。</span><span class="sxs-lookup"><span data-stu-id="b4db1-121">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b4db1-122">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="b4db1-122">Header files</span></span>

<span data-ttu-id="b4db1-123">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b4db1-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="b4db1-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b4db1-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="b4db1-125">Mapitags</span><span class="sxs-lookup"><span data-stu-id="b4db1-125">Mapitags.h</span></span>
  
> <span data-ttu-id="b4db1-126">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b4db1-126">Contains definitions of properties listed as associated properties.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="b4db1-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="b4db1-127">See also</span></span>



[<span data-ttu-id="b4db1-128">PidTagRuleProvider 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b4db1-128">PidTagRuleProvider Canonical Property</span></span>](pidtagruleprovider-canonical-property.md)


[<span data-ttu-id="b4db1-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="b4db1-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b4db1-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b4db1-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b4db1-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b4db1-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b4db1-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b4db1-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

