---
title: itabledata IUnknown
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3992bea899239ee5975505dec366490d6bbe1698
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430596"
---
# <a name="itabledata--iunknown"></a><span data-ttu-id="7caf9-103">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7caf9-103">ITableData : IUnknown</span></span>

  
  
<span data-ttu-id="7caf9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7caf9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7caf9-105">テーブルを処理するためのユーティリティメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="7caf9-105">Provides utility methods for working with tables.</span></span> <span data-ttu-id="7caf9-106">MAPI は、サービスプロバイダーがテーブルのメンテナンスを実行するのに役立つ、 **itabledata**を実装するテーブルデータオブジェクトまたはオブジェクトを提供します。</span><span class="sxs-lookup"><span data-stu-id="7caf9-106">MAPI provides table data objects or objects that implement **ITableData** to help service providers perform table maintenance.</span></span> <span data-ttu-id="7caf9-107">テーブルデータオブジェクトを取得するために、サービスプロバイダーは[CreateTable](createtable.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7caf9-107">To obtain a table data object, service providers call the [CreateTable](createtable.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7caf9-108">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="7caf9-108">Header file:</span></span>  <br/> |<span data-ttu-id="7caf9-109">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="7caf9-109">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7caf9-110">公開者:</span><span class="sxs-lookup"><span data-stu-id="7caf9-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="7caf9-111">テーブルデータオブジェクト</span><span class="sxs-lookup"><span data-stu-id="7caf9-111">Table data objects</span></span>  <br/> |
|<span data-ttu-id="7caf9-112">実装元:</span><span class="sxs-lookup"><span data-stu-id="7caf9-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="7caf9-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="7caf9-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="7caf9-114">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="7caf9-114">Called by:</span></span>  <br/> |<span data-ttu-id="7caf9-115">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="7caf9-115">Service providers</span></span>  <br/> |
|<span data-ttu-id="7caf9-116">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="7caf9-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="7caf9-117">IID_IMAPITableData</span><span class="sxs-lookup"><span data-stu-id="7caf9-117">IID_IMAPITableData</span></span>  <br/> |
|<span data-ttu-id="7caf9-118">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="7caf9-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="7caf9-119">LPTABLEDATA</span><span class="sxs-lookup"><span data-stu-id="7caf9-119">LPTABLEDATA</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="7caf9-120">v の順序</span><span class="sxs-lookup"><span data-stu-id="7caf9-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="7caf9-121">hrgetview</span><span class="sxs-lookup"><span data-stu-id="7caf9-121">HrGetView</span></span>](itabledata-hrgetview.md) <br/> |<span data-ttu-id="7caf9-122">[IMAPITable](imapitableiunknown.md)実装へのポインターを返すテーブルビューを作成します。</span><span class="sxs-lookup"><span data-stu-id="7caf9-122">Creates a table view, returning a pointer to an [IMAPITable](imapitableiunknown.md) implementation.</span></span>  <br/> |
|[<span data-ttu-id="7caf9-123">hrmodifyrow</span><span class="sxs-lookup"><span data-stu-id="7caf9-123">HrModifyRow</span></span>](itabledata-hrmodifyrow.md) <br/> |<span data-ttu-id="7caf9-124">既存の行を置き換える可能性がある新しいテーブル行を挿入します。</span><span class="sxs-lookup"><span data-stu-id="7caf9-124">Inserts a new table row, possibly replacing an existing row.</span></span>  <br/> |
|[<span data-ttu-id="7caf9-125">HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="7caf9-125">HrDeleteRow</span></span>](itabledata-hrdeleterow.md) <br/> |<span data-ttu-id="7caf9-126">表の行を削除します。</span><span class="sxs-lookup"><span data-stu-id="7caf9-126">Deletes a table row.</span></span>  <br/> |
|[<span data-ttu-id="7caf9-127">hrqueryrow</span><span class="sxs-lookup"><span data-stu-id="7caf9-127">HrQueryRow</span></span>](itabledata-hrqueryrow.md) <br/> |<span data-ttu-id="7caf9-128">表の行を取得します。</span><span class="sxs-lookup"><span data-stu-id="7caf9-128">Retrieves a table row.</span></span>  <br/> |
|[<span data-ttu-id="7caf9-129">HrEnumRow</span><span class="sxs-lookup"><span data-stu-id="7caf9-129">HrEnumRow</span></span>](itabledata-hrenumrow.md) <br/> |<span data-ttu-id="7caf9-130">テーブル内の位置に基づいて行を取得します。</span><span class="sxs-lookup"><span data-stu-id="7caf9-130">Retrieves a row based on its position in the table.</span></span>  <br/> |
|[<span data-ttu-id="7caf9-131">hrnotify</span><span class="sxs-lookup"><span data-stu-id="7caf9-131">HrNotify</span></span>](itabledata-hrnotify.md) <br/> |<span data-ttu-id="7caf9-132">表の行の通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="7caf9-132">Sends a notification for a table row.</span></span>  <br/> |
|[<span data-ttu-id="7caf9-133">HrInsertRow</span><span class="sxs-lookup"><span data-stu-id="7caf9-133">HrInsertRow</span></span>](itabledata-hrinsertrow.md) <br/> |<span data-ttu-id="7caf9-134">表の行を挿入します。</span><span class="sxs-lookup"><span data-stu-id="7caf9-134">Inserts a table row.</span></span>  <br/> |
|[<span data-ttu-id="7caf9-135">hrmodifyrows</span><span class="sxs-lookup"><span data-stu-id="7caf9-135">HrModifyRows</span></span>](itabledata-hrmodifyrows.md) <br/> |<span data-ttu-id="7caf9-136">複数のテーブル行を挿入します。既存の行を置換する場合もあります。</span><span class="sxs-lookup"><span data-stu-id="7caf9-136">Inserts multiple table rows, possibly replacing existing rows.</span></span>  <br/> |
|[<span data-ttu-id="7caf9-137">HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="7caf9-137">HrDeleteRows</span></span>](itabledata-hrdeleterows.md) <br/> |<span data-ttu-id="7caf9-138">複数の表の行を削除します。</span><span class="sxs-lookup"><span data-stu-id="7caf9-138">Deletes multiple table rows.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7caf9-139">注釈</span><span class="sxs-lookup"><span data-stu-id="7caf9-139">Remarks</span></span>

<span data-ttu-id="7caf9-140">**itabledata**の MAPI 実装は、すべてのデータと、関連するすべての制限をメモリに保持することによってテーブルで機能し、非常に大きなテーブルで使用するのに適していません。</span><span class="sxs-lookup"><span data-stu-id="7caf9-140">The MAPI implementation of **ITableData** works with tables by holding all of the data and any associated restrictions in memory, making it unsuitable for use with very large tables.</span></span> <span data-ttu-id="7caf9-141">大規模な制限や分類などの複雑な操作はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="7caf9-141">Large restrictions and complex operations such as categorization are not supported.</span></span> 
  
<span data-ttu-id="7caf9-142">テーブルデータオブジェクトは、インデックス列を使用して行を識別します。プロパティは、各行に一意の値があることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="7caf9-142">Table data objects identify rows by using an index column, a property that is guaranteed to have a unique value for each row.</span></span> <span data-ttu-id="7caf9-143">ほとんどのサービスプロバイダーは、インデックス列として**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="7caf9-143">Most service providers use the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property as the index column.</span></span> <span data-ttu-id="7caf9-144">複数の値を持つプロパティをインデックス列として使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="7caf9-144">Properties that have multiple values cannot be used as an index column.</span></span>
  
<span data-ttu-id="7caf9-145">テーブルデータオブジェクトは、変更または削除によって影響を受ける行の数に関係なく、1つの通知を生成します。</span><span class="sxs-lookup"><span data-stu-id="7caf9-145">Table data objects generate a single notification regardless of the number of rows affected by a change or deletion.</span></span> <span data-ttu-id="7caf9-146">操作の対象となる行が存在しない場合は、行が追加されます。</span><span class="sxs-lookup"><span data-stu-id="7caf9-146">If a target row in an operation does not exist, a row is added.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7caf9-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="7caf9-147">See also</span></span>



[<span data-ttu-id="7caf9-148">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="7caf9-148">MAPI Interfaces</span></span>](mapi-interfaces.md)

