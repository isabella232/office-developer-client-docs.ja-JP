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
ms.openlocfilehash: e1c670cd566e838104ae3d5480c2297f8632d899
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348560"
---
# <a name="pidtagrulestable-canonical-property"></a><span data-ttu-id="1cd45-103">PidTagRulesTable 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1cd45-103">PidTagRulesTable Canonical Property</span></span>

  
  
<span data-ttu-id="1cd45-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1cd45-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1cd45-105">フォルダーに適用されているすべてのルールを含むテーブルを含みます。</span><span class="sxs-lookup"><span data-stu-id="1cd45-105">Contains a table with all rules applied to a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1cd45-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1cd45-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1cd45-107">PR_RULES_TABLE</span><span class="sxs-lookup"><span data-stu-id="1cd45-107">PR_RULES_TABLE</span></span>  <br/> |
|<span data-ttu-id="1cd45-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1cd45-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1cd45-109">0x3fe1</span><span class="sxs-lookup"><span data-stu-id="1cd45-109">0x3FE1</span></span>  <br/> |
|<span data-ttu-id="1cd45-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1cd45-110">Data type:</span></span>  <br/> |<span data-ttu-id="1cd45-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="1cd45-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="1cd45-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="1cd45-112">Area:</span></span>  <br/> |<span data-ttu-id="1cd45-113">サーバー側のルール</span><span class="sxs-lookup"><span data-stu-id="1cd45-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1cd45-114">解説</span><span class="sxs-lookup"><span data-stu-id="1cd45-114">Remarks</span></span>

<span data-ttu-id="1cd45-115">このプロパティは、ルールが設定されている Exchange サーバー上のすべての folder オブジェクトに存在します。</span><span class="sxs-lookup"><span data-stu-id="1cd45-115">This property is present on all folder objects on an Exchange Server that have rules.</span></span> <span data-ttu-id="1cd45-116">このプロパティに含まれる値は、ルールの読み取りと変更に使用されます。</span><span class="sxs-lookup"><span data-stu-id="1cd45-116">Values included in this property are used for reading and modifying rules.</span></span> <span data-ttu-id="1cd45-117">**IID_IExchangeModifyTable**インターフェイス識別子を使用して[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを使用すると、フォルダーの rules テーブルに対して[IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md)インターフェイスを取得できます。</span><span class="sxs-lookup"><span data-stu-id="1cd45-117">You can use the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with the **IID_IExchangeModifyTable** interface identifier to obtain an [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to the rules table on a folder.</span></span> <span data-ttu-id="1cd45-118">このインターフェイスを使用して、これらのルールを読み取りおよび変更できます。</span><span class="sxs-lookup"><span data-stu-id="1cd45-118">You can use this interface to read and modify those rules.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1cd45-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1cd45-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1cd45-120">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="1cd45-120">Header files</span></span>

<span data-ttu-id="1cd45-121">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1cd45-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="1cd45-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1cd45-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="1cd45-123">Mapitags</span><span class="sxs-lookup"><span data-stu-id="1cd45-123">Mapitags.h</span></span>
  
> <span data-ttu-id="1cd45-124">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="1cd45-124">Contains definitions of properties listed as associated properties.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="1cd45-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="1cd45-125">See also</span></span>



[<span data-ttu-id="1cd45-126">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1cd45-126">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="1cd45-127">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="1cd45-127">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)


[<span data-ttu-id="1cd45-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="1cd45-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1cd45-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1cd45-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1cd45-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1cd45-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1cd45-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1cd45-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

