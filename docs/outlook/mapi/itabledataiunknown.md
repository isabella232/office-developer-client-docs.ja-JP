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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3992bea899239ee5975505dec366490d6bbe1698
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430596"
---
# <a name="itabledata--iunknown"></a><span data-ttu-id="11ba4-103">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="11ba4-103">ITableData : IUnknown</span></span>

  
  
<span data-ttu-id="11ba4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11ba4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11ba4-105">テーブルを操作するユーティリティ メソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="11ba4-105">Provides utility methods for working with tables.</span></span> <span data-ttu-id="11ba4-106">MAPI には、サービス プロバイダーがテーブルのメンテナンスを実行するのに役立つ **、ITableData** を実装するテーブル データ オブジェクトまたはオブジェクトが提供されています。</span><span class="sxs-lookup"><span data-stu-id="11ba4-106">MAPI provides table data objects or objects that implement **ITableData** to help service providers perform table maintenance.</span></span> <span data-ttu-id="11ba4-107">テーブル データ オブジェクトを取得するために、サービス プロバイダーは [CreateTable 関数を呼び出](createtable.md) します。</span><span class="sxs-lookup"><span data-stu-id="11ba4-107">To obtain a table data object, service providers call the [CreateTable](createtable.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="11ba4-108">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="11ba4-108">Header file:</span></span>  <br/> |<span data-ttu-id="11ba4-109">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="11ba4-109">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="11ba4-110">次のユーザーによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="11ba4-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="11ba4-111">テーブル データ オブジェクト</span><span class="sxs-lookup"><span data-stu-id="11ba4-111">Table data objects</span></span>  <br/> |
|<span data-ttu-id="11ba4-112">実装元:</span><span class="sxs-lookup"><span data-stu-id="11ba4-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="11ba4-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="11ba4-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="11ba4-114">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="11ba4-114">Called by:</span></span>  <br/> |<span data-ttu-id="11ba4-115">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="11ba4-115">Service providers</span></span>  <br/> |
|<span data-ttu-id="11ba4-116">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="11ba4-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="11ba4-117">IID_IMAPITableData</span><span class="sxs-lookup"><span data-stu-id="11ba4-117">IID_IMAPITableData</span></span>  <br/> |
|<span data-ttu-id="11ba4-118">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="11ba4-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="11ba4-119">LPTABLEDATA</span><span class="sxs-lookup"><span data-stu-id="11ba4-119">LPTABLEDATA</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="11ba4-120">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="11ba4-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="11ba4-121">HrGetView</span><span class="sxs-lookup"><span data-stu-id="11ba4-121">HrGetView</span></span>](itabledata-hrgetview.md) <br/> |<span data-ttu-id="11ba4-122">IMAPITable 実装へのポインターを返すテーブル [ビューを作成](imapitableiunknown.md) します。</span><span class="sxs-lookup"><span data-stu-id="11ba4-122">Creates a table view, returning a pointer to an [IMAPITable](imapitableiunknown.md) implementation.</span></span>  <br/> |
|[<span data-ttu-id="11ba4-123">HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="11ba4-123">HrModifyRow</span></span>](itabledata-hrmodifyrow.md) <br/> |<span data-ttu-id="11ba4-124">新しいテーブル行を挿入し、既存の行を置き換える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="11ba4-124">Inserts a new table row, possibly replacing an existing row.</span></span>  <br/> |
|[<span data-ttu-id="11ba4-125">HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="11ba4-125">HrDeleteRow</span></span>](itabledata-hrdeleterow.md) <br/> |<span data-ttu-id="11ba4-126">テーブル行を削除します。</span><span class="sxs-lookup"><span data-stu-id="11ba4-126">Deletes a table row.</span></span>  <br/> |
|[<span data-ttu-id="11ba4-127">HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="11ba4-127">HrQueryRow</span></span>](itabledata-hrqueryrow.md) <br/> |<span data-ttu-id="11ba4-128">テーブル行を取得します。</span><span class="sxs-lookup"><span data-stu-id="11ba4-128">Retrieves a table row.</span></span>  <br/> |
|[<span data-ttu-id="11ba4-129">HrEnumRow</span><span class="sxs-lookup"><span data-stu-id="11ba4-129">HrEnumRow</span></span>](itabledata-hrenumrow.md) <br/> |<span data-ttu-id="11ba4-130">テーブル内の位置に基づいて行を取得します。</span><span class="sxs-lookup"><span data-stu-id="11ba4-130">Retrieves a row based on its position in the table.</span></span>  <br/> |
|[<span data-ttu-id="11ba4-131">HrNotify</span><span class="sxs-lookup"><span data-stu-id="11ba4-131">HrNotify</span></span>](itabledata-hrnotify.md) <br/> |<span data-ttu-id="11ba4-132">テーブル行の通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="11ba4-132">Sends a notification for a table row.</span></span>  <br/> |
|[<span data-ttu-id="11ba4-133">HrInsertRow</span><span class="sxs-lookup"><span data-stu-id="11ba4-133">HrInsertRow</span></span>](itabledata-hrinsertrow.md) <br/> |<span data-ttu-id="11ba4-134">テーブル行を挿入します。</span><span class="sxs-lookup"><span data-stu-id="11ba4-134">Inserts a table row.</span></span>  <br/> |
|[<span data-ttu-id="11ba4-135">HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="11ba4-135">HrModifyRows</span></span>](itabledata-hrmodifyrows.md) <br/> |<span data-ttu-id="11ba4-136">複数のテーブル行を挿入し、既存の行を置き換える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="11ba4-136">Inserts multiple table rows, possibly replacing existing rows.</span></span>  <br/> |
|[<span data-ttu-id="11ba4-137">HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="11ba4-137">HrDeleteRows</span></span>](itabledata-hrdeleterows.md) <br/> |<span data-ttu-id="11ba4-138">複数のテーブル行を削除します。</span><span class="sxs-lookup"><span data-stu-id="11ba4-138">Deletes multiple table rows.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="11ba4-139">注釈</span><span class="sxs-lookup"><span data-stu-id="11ba4-139">Remarks</span></span>

<span data-ttu-id="11ba4-140">**ITableData** の MAPI 実装は、すべてのデータと関連する制限をメモリに保持することでテーブルと動作し、非常に大きなテーブルでの使用には適しなされません。</span><span class="sxs-lookup"><span data-stu-id="11ba4-140">The MAPI implementation of **ITableData** works with tables by holding all of the data and any associated restrictions in memory, making it unsuitable for use with very large tables.</span></span> <span data-ttu-id="11ba4-141">大きな制限や、分類などの複雑な操作はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="11ba4-141">Large restrictions and complex operations such as categorization are not supported.</span></span> 
  
<span data-ttu-id="11ba4-142">テーブル データ オブジェクトは、各行に一意の値を持つプロパティであるインデックス列を使用して行を識別します。</span><span class="sxs-lookup"><span data-stu-id="11ba4-142">Table data objects identify rows by using an index column, a property that is guaranteed to have a unique value for each row.</span></span> <span data-ttu-id="11ba4-143">ほとんどのサービス プロバイダーは **、PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) プロパティをインデックス列として使用します。</span><span class="sxs-lookup"><span data-stu-id="11ba4-143">Most service providers use the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property as the index column.</span></span> <span data-ttu-id="11ba4-144">複数の値を持つプロパティをインデックス列として使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="11ba4-144">Properties that have multiple values cannot be used as an index column.</span></span>
  
<span data-ttu-id="11ba4-145">テーブル データ オブジェクトは、変更または削除の影響を受ける行の数に関係なく、1 つの通知を生成します。</span><span class="sxs-lookup"><span data-stu-id="11ba4-145">Table data objects generate a single notification regardless of the number of rows affected by a change or deletion.</span></span> <span data-ttu-id="11ba4-146">操作のターゲット行が存在しない場合は、行が追加されます。</span><span class="sxs-lookup"><span data-stu-id="11ba4-146">If a target row in an operation does not exist, a row is added.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="11ba4-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="11ba4-147">See also</span></span>



[<span data-ttu-id="11ba4-148">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="11ba4-148">MAPI Interfaces</span></span>](mapi-interfaces.md)

