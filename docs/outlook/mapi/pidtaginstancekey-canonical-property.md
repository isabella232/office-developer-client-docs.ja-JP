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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358512"
---
# <a name="pidtaginstancekey-canonical-property"></a><span data-ttu-id="e6034-103">PidTagInstanceKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e6034-103">PidTagInstanceKey Canonical Property</span></span>

  
  
<span data-ttu-id="e6034-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6034-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6034-105">テーブル内の行を一意に識別する値を格納します。</span><span class="sxs-lookup"><span data-stu-id="e6034-105">Contains a value that uniquely identifies a row in a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e6034-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e6034-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e6034-107">PR_INSTANCE_KEY</span><span class="sxs-lookup"><span data-stu-id="e6034-107">PR_INSTANCE_KEY</span></span>  <br/> |
|<span data-ttu-id="e6034-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e6034-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e6034-109">0x0ff6</span><span class="sxs-lookup"><span data-stu-id="e6034-109">0x0FF6</span></span>  <br/> |
|<span data-ttu-id="e6034-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e6034-110">Data type:</span></span>  <br/> |<span data-ttu-id="e6034-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e6034-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e6034-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="e6034-112">Area:</span></span>  <br/> |<span data-ttu-id="e6034-113">Table</span><span class="sxs-lookup"><span data-stu-id="e6034-113">Table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e6034-114">解説</span><span class="sxs-lookup"><span data-stu-id="e6034-114">Remarks</span></span>

<span data-ttu-id="e6034-115">このプロパティは、テーブルビューの行を一意に識別するバイナリ値です。</span><span class="sxs-lookup"><span data-stu-id="e6034-115">This property is a binary value that uniquely identifies a row in a table view.</span></span> <span data-ttu-id="e6034-116">ほとんどのテーブルでは必須の列です。</span><span class="sxs-lookup"><span data-stu-id="e6034-116">It is a required column in most tables.</span></span> <span data-ttu-id="e6034-117">行が2つのビューに含まれている場合は、2つの異なるインスタンスキーがあります。</span><span class="sxs-lookup"><span data-stu-id="e6034-117">If a row is included in two views, there are two different instance keys.</span></span> <span data-ttu-id="e6034-118">行のインスタンスキーは、テーブルが開かれるたびに異なる場合がありますが、テーブルを開いている間は一定のままです。</span><span class="sxs-lookup"><span data-stu-id="e6034-118">The instance key of a row may differ each time the table is opened, but remains constant while the table is open.</span></span> <span data-ttu-id="e6034-119">テーブルが使用されている間に追加された行は、以前に使用されていたインスタンスキーを再利用しません。</span><span class="sxs-lookup"><span data-stu-id="e6034-119">Rows added while a table is in use do not reuse an instance key that was previously used.</span></span> 
  
<span data-ttu-id="e6034-120">拡張のすべての行を関連付けるには、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) または**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="e6034-120">Use the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) or **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) properties to correlate all the rows of an expansion.</span></span> <span data-ttu-id="e6034-121">**PR_INSTANCE_KEY**を使用して、拡張内で特定のインスタンスを検索します。</span><span class="sxs-lookup"><span data-stu-id="e6034-121">Use **PR_INSTANCE_KEY** to locate a particular instance within the expansion.</span></span> 
  
<span data-ttu-id="e6034-122">複数値プロパティがテーブルで展開されている場合は、そのプロパティの各値に対して、拡張の各インスタンスに対して1つの行が作成されます。</span><span class="sxs-lookup"><span data-stu-id="e6034-122">When a multivalued property is expanded in a table, a row is created for each instance of the expansion, that is, for each value of that property.</span></span> <span data-ttu-id="e6034-123">各行には、 **PR_INSTANCE_KEY**プロパティの一意の値がありますが、他のすべての列は、拡張全体を通じて元の値を保持します。</span><span class="sxs-lookup"><span data-stu-id="e6034-123">Each row has a unique value for the **PR_INSTANCE_KEY** property, while all the other columns retain their original values throughout the expansion.</span></span> 
  
<span data-ttu-id="e6034-124">表の分類された並べ替えでは、実際のデータに対応していない行は、並べ替えの結果に追加できます。</span><span class="sxs-lookup"><span data-stu-id="e6034-124">In a categorized sort of a table, rows not corresponding to actual data can be added to the result of the sort.</span></span> <span data-ttu-id="e6034-125">このような各行には、すべてのテーブルのすべての行と同様に、固有のインスタンスキーがあります。</span><span class="sxs-lookup"><span data-stu-id="e6034-125">Each such row, like all rows in all tables, has its own unique instance key.</span></span> 
  
 <span data-ttu-id="e6034-126">**PR_INSTANCE_KEY**は、テーブルイベント通知でも使用されます。</span><span class="sxs-lookup"><span data-stu-id="e6034-126">**PR_INSTANCE_KEY** is also used in table event notifications.</span></span> <span data-ttu-id="e6034-127">**propindex**と[TABLE_NOTIFICATION](table_notification.md)構造体の**前**のメンバーは、 **PR_INSTANCE_KEY**の値を保持する[spropvalue](spropvalue.md)構造です。</span><span class="sxs-lookup"><span data-stu-id="e6034-127">The **propIndex** and **propPrior** members of the [TABLE_NOTIFICATION](table_notification.md) structure are [SPropValue](spropvalue.md) structures holding **PR_INSTANCE_KEY** values.</span></span> <span data-ttu-id="e6034-128">**propindex**メンバーは、追加または変更された行を示します。</span><span class="sxs-lookup"><span data-stu-id="e6034-128">The **propIndex** member indicates the row that was added or changed.</span></span> <span data-ttu-id="e6034-129">**propprior**メンバーは、追加または変更された行の前の行を示します (**PR_NULL**は、最初の行に対する変更を示します)。</span><span class="sxs-lookup"><span data-stu-id="e6034-129">The **propPrior** member indicates the row before the added or changed row (**PR_NULL** indicates a change to the first row).</span></span> 
  
<span data-ttu-id="e6034-130">この値は、表示テーブルの一部としてコピーされません。</span><span class="sxs-lookup"><span data-stu-id="e6034-130">This value is not copied as part of the display table.</span></span> 
  
 <span data-ttu-id="e6034-131">**PR_INSTANCE_KEY**は、 [MAPIUID](mapiuid.md)構造体です。</span><span class="sxs-lookup"><span data-stu-id="e6034-131">**PR_INSTANCE_KEY** is a [MAPIUID](mapiuid.md) structure.</span></span> <span data-ttu-id="e6034-132">すべてのインスタンスキーは、バイナリ値として直接比較できます。</span><span class="sxs-lookup"><span data-stu-id="e6034-132">All instance keys can be directly compared as binary values.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e6034-133">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e6034-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e6034-134">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e6034-134">Protocol specifications</span></span>

<span data-ttu-id="e6034-135">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e6034-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e6034-136">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e6034-136">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e6034-137">[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e6034-137">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e6034-138">ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e6034-138">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e6034-139">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="e6034-139">Header files</span></span>

<span data-ttu-id="e6034-140">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e6034-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="e6034-141">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e6034-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="e6034-142">Mapitags</span><span class="sxs-lookup"><span data-stu-id="e6034-142">Mapitags.h</span></span>
  
> <span data-ttu-id="e6034-143">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e6034-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e6034-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="e6034-144">See also</span></span>



[<span data-ttu-id="e6034-145">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e6034-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e6034-146">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e6034-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e6034-147">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e6034-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e6034-148">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e6034-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

