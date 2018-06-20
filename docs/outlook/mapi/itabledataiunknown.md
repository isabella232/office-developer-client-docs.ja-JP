---
title: ITableData IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData
api_type:
- COM
ms.assetid: ac7ae09f-ce19-45cf-8963-fad5bba75452
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 968768fe75286b93bf12e349a4845fdfaa1923e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801232"
---
# <a name="itabledata--iunknown"></a><span data-ttu-id="6711a-103">ITableData: IUnknown</span><span class="sxs-lookup"><span data-stu-id="6711a-103">ITableData : IUnknown</span></span>

  
  
<span data-ttu-id="6711a-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6711a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6711a-105">テーブルを操作するためのユーティリティ メソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="6711a-105">Provides utility methods for working with tables.</span></span> <span data-ttu-id="6711a-106">MAPI には、データ オブジェクトのテーブルまたはテーブルのメンテナンスを実行するサービス プロバイダーのために**ITableData**を実装するオブジェクトが用意されています。</span><span class="sxs-lookup"><span data-stu-id="6711a-106">MAPI provides table data objects or objects that implement **ITableData** to help service providers perform table maintenance.</span></span> <span data-ttu-id="6711a-107">テーブルのデータ オブジェクトを取得するには、サービス プロバイダーは、 [CreateTable](createtable.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6711a-107">To obtain a table data object, service providers call the [CreateTable](createtable.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6711a-108">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="6711a-108">Header file:</span></span>  <br/> |<span data-ttu-id="6711a-109">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="6711a-109">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="6711a-110">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="6711a-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="6711a-111">テーブルのデータ オブジェクト</span><span class="sxs-lookup"><span data-stu-id="6711a-111">Table data objects</span></span>  <br/> |
|<span data-ttu-id="6711a-112">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="6711a-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="6711a-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="6711a-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="6711a-114">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6711a-114">Called by:</span></span>  <br/> |<span data-ttu-id="6711a-115">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="6711a-115">Service providers</span></span>  <br/> |
|<span data-ttu-id="6711a-116">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="6711a-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="6711a-117">IID_IMAPITableData</span><span class="sxs-lookup"><span data-stu-id="6711a-117">IID_IMAPITableData</span></span>  <br/> |
|<span data-ttu-id="6711a-118">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="6711a-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="6711a-119">LPTABLEDATA</span><span class="sxs-lookup"><span data-stu-id="6711a-119">LPTABLEDATA</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="6711a-120">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="6711a-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="6711a-121">HrGetView</span><span class="sxs-lookup"><span data-stu-id="6711a-121">HrGetView</span></span>](itabledata-hrgetview.md) <br/> |<span data-ttu-id="6711a-122">[IMAPITable](imapitableiunknown.md)実装へのポインターを返す表形式ビューを作成します。</span><span class="sxs-lookup"><span data-stu-id="6711a-122">Creates a table view, returning a pointer to an [IMAPITable](imapitableiunknown.md) implementation.</span></span>  <br/> |
|[<span data-ttu-id="6711a-123">HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="6711a-123">HrModifyRow</span></span>](itabledata-hrmodifyrow.md) <br/> |<span data-ttu-id="6711a-124">既存の行が上書きされる、テーブルの新しい行を挿入します。</span><span class="sxs-lookup"><span data-stu-id="6711a-124">Inserts a new table row, possibly replacing an existing row.</span></span>  <br/> |
|[<span data-ttu-id="6711a-125">HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="6711a-125">HrDeleteRow</span></span>](itabledata-hrdeleterow.md) <br/> |<span data-ttu-id="6711a-126">テーブルの行を削除します。</span><span class="sxs-lookup"><span data-stu-id="6711a-126">Deletes a table row.</span></span>  <br/> |
|[<span data-ttu-id="6711a-127">HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="6711a-127">HrQueryRow</span></span>](itabledata-hrqueryrow.md) <br/> |<span data-ttu-id="6711a-128">テーブルの行を取得します。</span><span class="sxs-lookup"><span data-stu-id="6711a-128">Retrieves a table row.</span></span>  <br/> |
|[<span data-ttu-id="6711a-129">HrEnumRow</span><span class="sxs-lookup"><span data-stu-id="6711a-129">HrEnumRow</span></span>](itabledata-hrenumrow.md) <br/> |<span data-ttu-id="6711a-130">テーブル内の位置に基づいて行を取得します。</span><span class="sxs-lookup"><span data-stu-id="6711a-130">Retrieves a row based on its position in the table.</span></span>  <br/> |
|[<span data-ttu-id="6711a-131">HrNotify</span><span class="sxs-lookup"><span data-stu-id="6711a-131">HrNotify</span></span>](itabledata-hrnotify.md) <br/> |<span data-ttu-id="6711a-132">テーブルの行の通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="6711a-132">Sends a notification for a table row.</span></span>  <br/> |
|[<span data-ttu-id="6711a-133">HrInsertRow</span><span class="sxs-lookup"><span data-stu-id="6711a-133">HrInsertRow</span></span>](itabledata-hrinsertrow.md) <br/> |<span data-ttu-id="6711a-134">テーブルの行を挿入します。</span><span class="sxs-lookup"><span data-stu-id="6711a-134">Inserts a table row.</span></span>  <br/> |
|[<span data-ttu-id="6711a-135">HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="6711a-135">HrModifyRows</span></span>](itabledata-hrmodifyrows.md) <br/> |<span data-ttu-id="6711a-136">既存の行が上書きされる、複数のテーブル行を挿入します。</span><span class="sxs-lookup"><span data-stu-id="6711a-136">Inserts multiple table rows, possibly replacing existing rows.</span></span>  <br/> |
|[<span data-ttu-id="6711a-137">HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="6711a-137">HrDeleteRows</span></span>](itabledata-hrdeleterows.md) <br/> |<span data-ttu-id="6711a-138">複数のテーブル行を削除します。</span><span class="sxs-lookup"><span data-stu-id="6711a-138">Deletes multiple table rows.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6711a-139">備考</span><span class="sxs-lookup"><span data-stu-id="6711a-139">Remarks</span></span>

<span data-ttu-id="6711a-140">**ITableData**の MAPI 実装では、非常に大きなテーブルでの使用に適していませんので、メモリ内のすべてのデータと関連付けられている制限を押しながら、テーブルと連携します。</span><span class="sxs-lookup"><span data-stu-id="6711a-140">The MAPI implementation of **ITableData** works with tables by holding all of the data and any associated restrictions in memory, making it unsuitable for use with very large tables.</span></span> <span data-ttu-id="6711a-141">大規模な制限や分類などの複雑な操作はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6711a-141">Large restrictions and complex operations such as categorization are not supported.</span></span> 
  
<span data-ttu-id="6711a-142">テーブルのデータ オブジェクトは、インデックス列、行ごとに一意の値を持つことが保証されているプロパティを使用して行を識別します。</span><span class="sxs-lookup"><span data-stu-id="6711a-142">Table data objects identify rows by using an index column, a property that is guaranteed to have a unique value for each row.</span></span> <span data-ttu-id="6711a-143">ほとんどのサービス プロバイダーは、インデックス列として**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="6711a-143">Most service providers use the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property as the index column.</span></span> <span data-ttu-id="6711a-144">複数値を持つプロパティは、インデックス列として使用できません。</span><span class="sxs-lookup"><span data-stu-id="6711a-144">Properties that have multiple values cannot be used as an index column.</span></span>
  
<span data-ttu-id="6711a-145">テーブルのデータ オブジェクトは、変更や削除によって影響を受ける行の数に関係なく 1 つの通知を生成します。</span><span class="sxs-lookup"><span data-stu-id="6711a-145">Table data objects generate a single notification regardless of the number of rows affected by a change or deletion.</span></span> <span data-ttu-id="6711a-146">操作の対象の行が存在しない場合は、行が追加されます。</span><span class="sxs-lookup"><span data-stu-id="6711a-146">If a target row in an operation does not exist, a row is added.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6711a-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="6711a-147">See also</span></span>



[<span data-ttu-id="6711a-148">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="6711a-148">MAPI Interfaces</span></span>](mapi-interfaces.md)

