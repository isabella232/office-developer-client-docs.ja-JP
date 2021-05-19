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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c237149c305a80012d1f06ea4373b892d25daec1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358512"
---
# <a name="pidtaginstancekey-canonical-property"></a><span data-ttu-id="f8bf7-103">PidTagInstanceKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f8bf7-103">PidTagInstanceKey Canonical Property</span></span>

  
  
<span data-ttu-id="f8bf7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8bf7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8bf7-105">テーブル内の行を一意に識別する値を含む。</span><span class="sxs-lookup"><span data-stu-id="f8bf7-105">Contains a value that uniquely identifies a row in a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f8bf7-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f8bf7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f8bf7-107">PR_INSTANCE_KEY</span><span class="sxs-lookup"><span data-stu-id="f8bf7-107">PR_INSTANCE_KEY</span></span>  <br/> |
|<span data-ttu-id="f8bf7-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f8bf7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f8bf7-109">0x0FF6</span><span class="sxs-lookup"><span data-stu-id="f8bf7-109">0x0FF6</span></span>  <br/> |
|<span data-ttu-id="f8bf7-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f8bf7-110">Data type:</span></span>  <br/> |<span data-ttu-id="f8bf7-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f8bf7-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f8bf7-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="f8bf7-112">Area:</span></span>  <br/> |<span data-ttu-id="f8bf7-113">Table</span><span class="sxs-lookup"><span data-stu-id="f8bf7-113">Table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f8bf7-114">注釈</span><span class="sxs-lookup"><span data-stu-id="f8bf7-114">Remarks</span></span>

<span data-ttu-id="f8bf7-115">このプロパティは、テーブル ビュー内の行を一意に識別するバイナリ値です。</span><span class="sxs-lookup"><span data-stu-id="f8bf7-115">This property is a binary value that uniquely identifies a row in a table view.</span></span> <span data-ttu-id="f8bf7-116">ほとんどのテーブルでは必須の列です。</span><span class="sxs-lookup"><span data-stu-id="f8bf7-116">It is a required column in most tables.</span></span> <span data-ttu-id="f8bf7-117">行が 2 つのビューに含まれている場合は、2 つの異なるインスタンス キーがあります。</span><span class="sxs-lookup"><span data-stu-id="f8bf7-117">If a row is included in two views, there are two different instance keys.</span></span> <span data-ttu-id="f8bf7-118">行のインスタンス キーは、テーブルを開くごとに異なる場合がありますが、テーブルが開いている間は一定のままです。</span><span class="sxs-lookup"><span data-stu-id="f8bf7-118">The instance key of a row may differ each time the table is opened, but remains constant while the table is open.</span></span> <span data-ttu-id="f8bf7-119">テーブルの実行中に追加された行は、以前に使用されたインスタンス キーを再利用しないでください。</span><span class="sxs-lookup"><span data-stu-id="f8bf7-119">Rows added while a table is in use do not reuse an instance key that was previously used.</span></span> 
  
<span data-ttu-id="f8bf7-120">拡張のすべての **行PR_ENTRYID** 関連付けるには、PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティまたは **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="f8bf7-120">Use the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) or **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) properties to correlate all the rows of an expansion.</span></span> <span data-ttu-id="f8bf7-121">拡張 **PR_INSTANCE_KEY** 特定のインスタンスを検索するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="f8bf7-121">Use **PR_INSTANCE_KEY** to locate a particular instance within the expansion.</span></span> 
  
<span data-ttu-id="f8bf7-122">テーブル内で複数値プロパティを展開すると、拡張の各インスタンス (つまり、そのプロパティの値ごとに) に対して行が作成されます。</span><span class="sxs-lookup"><span data-stu-id="f8bf7-122">When a multivalued property is expanded in a table, a row is created for each instance of the expansion, that is, for each value of that property.</span></span> <span data-ttu-id="f8bf7-123">各行には PR_INSTANCE_KEY プロパティの一意の値が設定され **、他のすべての** 列は展開中も元の値を保持します。</span><span class="sxs-lookup"><span data-stu-id="f8bf7-123">Each row has a unique value for the **PR_INSTANCE_KEY** property, while all the other columns retain their original values throughout the expansion.</span></span> 
  
<span data-ttu-id="f8bf7-124">テーブルの分類された並べ替えでは、実際のデータに対応しない行を並べ替えの結果に追加できます。</span><span class="sxs-lookup"><span data-stu-id="f8bf7-124">In a categorized sort of a table, rows not corresponding to actual data can be added to the result of the sort.</span></span> <span data-ttu-id="f8bf7-125">このような各行は、すべてのテーブルのすべての行と同様に、独自の一意のインスタンス キーを持っています。</span><span class="sxs-lookup"><span data-stu-id="f8bf7-125">Each such row, like all rows in all tables, has its own unique instance key.</span></span> 
  
 <span data-ttu-id="f8bf7-126">**PR_INSTANCE_KEY** は、テーブル イベント通知でも使用されます。</span><span class="sxs-lookup"><span data-stu-id="f8bf7-126">**PR_INSTANCE_KEY** is also used in table event notifications.</span></span> <span data-ttu-id="f8bf7-127">プロパティ **構造体の propIndex** および **propPrior** メンバーは、TABLE_NOTIFICATION値を保持する [SPropValue](spropvalue.md) **PR_INSTANCE_KEY** です。 [](table_notification.md)</span><span class="sxs-lookup"><span data-stu-id="f8bf7-127">The **propIndex** and **propPrior** members of the [TABLE_NOTIFICATION](table_notification.md) structure are [SPropValue](spropvalue.md) structures holding **PR_INSTANCE_KEY** values.</span></span> <span data-ttu-id="f8bf7-128">**propIndex メンバー** は、追加または変更された行を示します。</span><span class="sxs-lookup"><span data-stu-id="f8bf7-128">The **propIndex** member indicates the row that was added or changed.</span></span> <span data-ttu-id="f8bf7-129">**propPrior メンバーは**、追加または変更された行の前の **行を示** します (PR_NULL行への変更を示します)。</span><span class="sxs-lookup"><span data-stu-id="f8bf7-129">The **propPrior** member indicates the row before the added or changed row (**PR_NULL** indicates a change to the first row).</span></span> 
  
<span data-ttu-id="f8bf7-130">この値は、表示テーブルの一部としてコピーされません。</span><span class="sxs-lookup"><span data-stu-id="f8bf7-130">This value is not copied as part of the display table.</span></span> 
  
 <span data-ttu-id="f8bf7-131">**PR_INSTANCE_KEY** [MAPIUID](mapiuid.md) 構造体です。</span><span class="sxs-lookup"><span data-stu-id="f8bf7-131">**PR_INSTANCE_KEY** is a [MAPIUID](mapiuid.md) structure.</span></span> <span data-ttu-id="f8bf7-132">すべてのインスタンス キーをバイナリ値として直接比較できます。</span><span class="sxs-lookup"><span data-stu-id="f8bf7-132">All instance keys can be directly compared as binary values.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f8bf7-133">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f8bf7-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f8bf7-134">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f8bf7-134">Protocol specifications</span></span>

<span data-ttu-id="f8bf7-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f8bf7-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f8bf7-136">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="f8bf7-136">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f8bf7-137">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f8bf7-137">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f8bf7-138">ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="f8bf7-138">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f8bf7-139">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f8bf7-139">Header files</span></span>

<span data-ttu-id="f8bf7-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f8bf7-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="f8bf7-141">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f8bf7-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="f8bf7-142">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f8bf7-142">Mapitags.h</span></span>
  
> <span data-ttu-id="f8bf7-143">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="f8bf7-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f8bf7-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="f8bf7-144">See also</span></span>



[<span data-ttu-id="f8bf7-145">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="f8bf7-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f8bf7-146">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f8bf7-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f8bf7-147">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="f8bf7-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f8bf7-148">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="f8bf7-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

