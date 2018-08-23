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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 945dabec4ee34d38d2474c918e779d894f4a917c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803427"
---
# <a name="pidtagrulestable-canonical-property"></a><span data-ttu-id="02818-103">PidTagRulesTable 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="02818-103">PidTagRulesTable Canonical Property</span></span>

  
  
<span data-ttu-id="02818-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="02818-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="02818-105">フォルダーに適用されるすべてのルールを持つテーブルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="02818-105">Contains a table with all rules applied to a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="02818-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="02818-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="02818-107">PR_RULES_TABLE</span><span class="sxs-lookup"><span data-stu-id="02818-107">PR_RULES_TABLE</span></span>  <br/> |
|<span data-ttu-id="02818-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="02818-108">Identifier:</span></span>  <br/> |<span data-ttu-id="02818-109">0x3FE1</span><span class="sxs-lookup"><span data-stu-id="02818-109">0x3FE1</span></span>  <br/> |
|<span data-ttu-id="02818-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="02818-110">Data type:</span></span>  <br/> |<span data-ttu-id="02818-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="02818-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="02818-112">領域:</span><span class="sxs-lookup"><span data-stu-id="02818-112">Area:</span></span>  <br/> |<span data-ttu-id="02818-113">サーバー側のルール</span><span class="sxs-lookup"><span data-stu-id="02818-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02818-114">注釈</span><span class="sxs-lookup"><span data-stu-id="02818-114">Remarks</span></span>

<span data-ttu-id="02818-115">このプロパティは、ルールがある、Exchange Server 上のすべてのフォルダー オブジェクト上に存在します。</span><span class="sxs-lookup"><span data-stu-id="02818-115">This property is present on all folder objects on an Exchange Server that have rules.</span></span> <span data-ttu-id="02818-116">このプロパティに含まれる値は、読み取りとルールを変更するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="02818-116">Values included in this property are used for reading and modifying rules.</span></span> <span data-ttu-id="02818-117">**IID_IExchangeModifyTable**インターフェイス識別子を使用して[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを使用するにを取得するのには、 [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md)フォルダーのルール テーブルへのインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="02818-117">You can use the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with the **IID_IExchangeModifyTable** interface identifier to obtain an [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to the rules table on a folder.</span></span> <span data-ttu-id="02818-118">読み取りおよびそれらの規則を変更するには、このインターフェイスを使用します。</span><span class="sxs-lookup"><span data-stu-id="02818-118">You can use this interface to read and modify those rules.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="02818-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="02818-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="02818-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="02818-120">Header files</span></span>

<span data-ttu-id="02818-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="02818-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="02818-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="02818-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="02818-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="02818-123">Mapitags.h</span></span>
  
> <span data-ttu-id="02818-124">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="02818-124">Contains definitions of properties listed as associated properties.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="02818-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="02818-125">See also</span></span>



[<span data-ttu-id="02818-126">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="02818-126">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="02818-127">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="02818-127">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)


[<span data-ttu-id="02818-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="02818-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="02818-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="02818-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="02818-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="02818-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="02818-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="02818-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

