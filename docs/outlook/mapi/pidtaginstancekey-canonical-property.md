---
title: PidTagInstanceKey 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInstanceKey
api_type:
- HeaderDef
ms.assetid: 14fc5571-acc0-4d75-8598-964aee5ba01c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c237149c305a80012d1f06ea4373b892d25daec1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396990"
---
# <a name="pidtaginstancekey-canonical-property"></a><span data-ttu-id="69995-103">PidTagInstanceKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="69995-103">PidTagInstanceKey Canonical Property</span></span>

  
  
<span data-ttu-id="69995-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69995-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69995-105">テーブル内の行を一意に識別する値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="69995-105">Contains a value that uniquely identifies a row in a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="69995-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="69995-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="69995-107">PR_INSTANCE_KEY</span><span class="sxs-lookup"><span data-stu-id="69995-107">PR_INSTANCE_KEY</span></span>  <br/> |
|<span data-ttu-id="69995-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="69995-108">Identifier:</span></span>  <br/> |<span data-ttu-id="69995-109">0x0FF6</span><span class="sxs-lookup"><span data-stu-id="69995-109">0x0FF6</span></span>  <br/> |
|<span data-ttu-id="69995-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="69995-110">Data type:</span></span>  <br/> |<span data-ttu-id="69995-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="69995-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="69995-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="69995-112">Area:</span></span>  <br/> |<span data-ttu-id="69995-113">テーブル</span><span class="sxs-lookup"><span data-stu-id="69995-113">Table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69995-114">備考</span><span class="sxs-lookup"><span data-stu-id="69995-114">Remarks</span></span>

<span data-ttu-id="69995-115">このプロパティは、表形式ビュー内の行を一意に識別するバイナリ値です。</span><span class="sxs-lookup"><span data-stu-id="69995-115">This property is a binary value that uniquely identifies a row in a table view.</span></span> <span data-ttu-id="69995-116">ほとんどのテーブルの必要な列があります。</span><span class="sxs-lookup"><span data-stu-id="69995-116">It is a required column in most tables.</span></span> <span data-ttu-id="69995-117">行が 2 つのビューに含まれている場合は、2 つの別のインスタンスのキーがあります。</span><span class="sxs-lookup"><span data-stu-id="69995-117">If a row is included in two views, there are two different instance keys.</span></span> <span data-ttu-id="69995-118">行のインスタンスのキーは、テーブルを開くたびに異なる場合がありますが、テーブルの中に一定に開いています。</span><span class="sxs-lookup"><span data-stu-id="69995-118">The instance key of a row may differ each time the table is opened, but remains constant while the table is open.</span></span> <span data-ttu-id="69995-119">テーブルの使用中に追加された行は、使用していたインスタンスのキーを再利用しません。</span><span class="sxs-lookup"><span data-stu-id="69995-119">Rows added while a table is in use do not reuse an instance key that was previously used.</span></span> 
  
<span data-ttu-id="69995-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) または**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) のプロパティを使用して、拡張のすべての行を関連付けるには。</span><span class="sxs-lookup"><span data-stu-id="69995-120">Use the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) or **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) properties to correlate all the rows of an expansion.</span></span> <span data-ttu-id="69995-121">**PR_INSTANCE_KEY**を使用して、展開内の特定のインスタンスを探します。</span><span class="sxs-lookup"><span data-stu-id="69995-121">Use **PR_INSTANCE_KEY** to locate a particular instance within the expansion.</span></span> 
  
<span data-ttu-id="69995-122">表内の複数値を持つプロパティが拡張されると、行が作成、展開の各インスタンスは、そのプロパティの値ごとに。</span><span class="sxs-lookup"><span data-stu-id="69995-122">When a multivalued property is expanded in a table, a row is created for each instance of the expansion, that is, for each value of that property.</span></span> <span data-ttu-id="69995-123">各行は、展開全体の元の値を保持する他のすべての列に、 **PR_INSTANCE_KEY**プロパティに一意の値を持ちます。</span><span class="sxs-lookup"><span data-stu-id="69995-123">Each row has a unique value for the **PR_INSTANCE_KEY** property, while all the other columns retain their original values throughout the expansion.</span></span> 
  
<span data-ttu-id="69995-124">分類された種類のテーブル、行の実際のデータには対応しない、並べ替えの結果に追加できます。</span><span class="sxs-lookup"><span data-stu-id="69995-124">In a categorized sort of a table, rows not corresponding to actual data can be added to the result of the sort.</span></span> <span data-ttu-id="69995-125">すべてのテーブル内のすべての行と同様に、このような行には、独自の一意のインスタンスのキーがあります。</span><span class="sxs-lookup"><span data-stu-id="69995-125">Each such row, like all rows in all tables, has its own unique instance key.</span></span> 
  
 <span data-ttu-id="69995-126">**PR_INSTANCE_KEY**は、表のイベント通知にも使用されます。</span><span class="sxs-lookup"><span data-stu-id="69995-126">**PR_INSTANCE_KEY** is also used in table event notifications.</span></span> <span data-ttu-id="69995-127">**PropIndex** 、 **propPrior** 、 [TABLE_NOTIFICATION](table_notification.md)構造体のメンバーは、 **PR_INSTANCE_KEY**の値を保持している[SPropValue](spropvalue.md)構造体です。</span><span class="sxs-lookup"><span data-stu-id="69995-127">The **propIndex** and **propPrior** members of the [TABLE_NOTIFICATION](table_notification.md) structure are [SPropValue](spropvalue.md) structures holding **PR_INSTANCE_KEY** values.</span></span> <span data-ttu-id="69995-128">**PropIndex**メンバーは、追加または変更された行を示します。</span><span class="sxs-lookup"><span data-stu-id="69995-128">The **propIndex** member indicates the row that was added or changed.</span></span> <span data-ttu-id="69995-129">**PropPrior**メンバーは、(**PR_NULL**は、最初の行への変更を示します) の追加または変更された行の前に行を示します。</span><span class="sxs-lookup"><span data-stu-id="69995-129">The **propPrior** member indicates the row before the added or changed row (**PR_NULL** indicates a change to the first row).</span></span> 
  
<span data-ttu-id="69995-130">表示された表の一部としては、この値はコピーされません。</span><span class="sxs-lookup"><span data-stu-id="69995-130">This value is not copied as part of the display table.</span></span> 
  
 <span data-ttu-id="69995-131">**PR_INSTANCE_KEY**は、 [MAPIUID](mapiuid.md)構造です。</span><span class="sxs-lookup"><span data-stu-id="69995-131">**PR_INSTANCE_KEY** is a [MAPIUID](mapiuid.md) structure.</span></span> <span data-ttu-id="69995-132">バイナリ値として、すべてのインスタンスのキーを直接比較できます。</span><span class="sxs-lookup"><span data-stu-id="69995-132">All instance keys can be directly compared as binary values.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="69995-133">関連リソース</span><span class="sxs-lookup"><span data-stu-id="69995-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="69995-134">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="69995-134">Protocol specifications</span></span>

<span data-ttu-id="69995-135">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69995-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69995-136">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="69995-136">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="69995-137">[[MS OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69995-137">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69995-138">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="69995-138">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="69995-139">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="69995-139">Header files</span></span>

<span data-ttu-id="69995-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="69995-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="69995-141">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="69995-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="69995-142">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="69995-142">Mapitags.h</span></span>
  
> <span data-ttu-id="69995-143">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="69995-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="69995-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="69995-144">See also</span></span>



[<span data-ttu-id="69995-145">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="69995-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="69995-146">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="69995-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="69995-147">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="69995-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="69995-148">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="69995-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

