---
title: PidTagRulesTable 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: fc520720-8190-4dff-8f6c-1bebf7080b57
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e1c670cd566e838104ae3d5480c2297f8632d899
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428502"
---
# <a name="pidtagrulestable-canonical-property"></a><span data-ttu-id="66a0a-103">PidTagRulesTable 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="66a0a-103">PidTagRulesTable Canonical Property</span></span>

  
  
<span data-ttu-id="66a0a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66a0a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66a0a-105">フォルダーに適用されるすべてのルールを含むテーブルが含まれる。</span><span class="sxs-lookup"><span data-stu-id="66a0a-105">Contains a table with all rules applied to a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="66a0a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="66a0a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="66a0a-107">PR_RULES_TABLE</span><span class="sxs-lookup"><span data-stu-id="66a0a-107">PR_RULES_TABLE</span></span>  <br/> |
|<span data-ttu-id="66a0a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="66a0a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="66a0a-109">0x3FE1</span><span class="sxs-lookup"><span data-stu-id="66a0a-109">0x3FE1</span></span>  <br/> |
|<span data-ttu-id="66a0a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="66a0a-110">Data type:</span></span>  <br/> |<span data-ttu-id="66a0a-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="66a0a-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="66a0a-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="66a0a-112">Area:</span></span>  <br/> |<span data-ttu-id="66a0a-113">サーバー側のルール</span><span class="sxs-lookup"><span data-stu-id="66a0a-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66a0a-114">注釈</span><span class="sxs-lookup"><span data-stu-id="66a0a-114">Remarks</span></span>

<span data-ttu-id="66a0a-115">このプロパティは、ルールを持つオブジェクト上Exchange Serverに存在します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-115">This property is present on all folder objects on an Exchange Server that have rules.</span></span> <span data-ttu-id="66a0a-116">このプロパティに含まれる値は、ルールの読み取りおよび変更に使用されます。</span><span class="sxs-lookup"><span data-stu-id="66a0a-116">Values included in this property are used for reading and modifying rules.</span></span> <span data-ttu-id="66a0a-117">[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを **IID_IExchangeModifyTable** インターフェイス識別子と一緒に使用して [、IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)インターフェイスをフォルダーのルール テーブルに取得できます。</span><span class="sxs-lookup"><span data-stu-id="66a0a-117">You can use the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with the **IID_IExchangeModifyTable** interface identifier to obtain an [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to the rules table on a folder.</span></span> <span data-ttu-id="66a0a-118">このインターフェイスを使用して、これらのルールを読み取り、変更できます。</span><span class="sxs-lookup"><span data-stu-id="66a0a-118">You can use this interface to read and modify those rules.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="66a0a-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="66a0a-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="66a0a-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="66a0a-120">Header files</span></span>

<span data-ttu-id="66a0a-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="66a0a-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="66a0a-122">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="66a0a-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="66a0a-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="66a0a-123">Mapitags.h</span></span>
  
> <span data-ttu-id="66a0a-124">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="66a0a-124">Contains definitions of properties listed as associated properties.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="66a0a-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="66a0a-125">See also</span></span>



[<span data-ttu-id="66a0a-126">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="66a0a-126">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="66a0a-127">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="66a0a-127">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)


[<span data-ttu-id="66a0a-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="66a0a-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="66a0a-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="66a0a-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="66a0a-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="66a0a-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="66a0a-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="66a0a-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

