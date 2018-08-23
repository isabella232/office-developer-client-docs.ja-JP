---
title: TABLE_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.TABLE_NOTIFICATION
api_type:
- COM
ms.assetid: 48e478c4-6e9a-40ab-a7bb-e6219b743b08
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7f32145e0947411c48e1e6c3a941c9913a08709c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565845"
---
# <a name="tablenotification"></a><span data-ttu-id="3ecde-103">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="3ecde-103">TABLE_NOTIFICATION</span></span>

<span data-ttu-id="3ecde-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ecde-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ecde-105">何らかの変更やエラーなどのイベントによって影響のあるテーブル内の行について説明します。</span><span class="sxs-lookup"><span data-stu-id="3ecde-105">Describes a row in a table that has been affected by some type of event, such as a change or an error.</span></span> <span data-ttu-id="3ecde-106">テーブル通知が生成されますが発生します。</span><span class="sxs-lookup"><span data-stu-id="3ecde-106">This causes a table notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3ecde-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="3ecde-107">Header file:</span></span>  <br/> |<span data-ttu-id="3ecde-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3ecde-108">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _TABLE_NOTIFICATION
{
  ULONG ulTableEvent;
  HRESULT hResult;
  SPropValue propIndex;
  SPropValue propPrior;
  SRow row;
} TABLE_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="3ecde-109">Members</span><span class="sxs-lookup"><span data-stu-id="3ecde-109">Members</span></span>

<span data-ttu-id="3ecde-110">**ulTableEvent**</span><span class="sxs-lookup"><span data-stu-id="3ecde-110">**ulTableEvent**</span></span>
  
> <span data-ttu-id="3ecde-111">テーブルのイベント タイプを表すために使用するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="3ecde-111">Bitmask of flags used to represent the table event type.</span></span> <span data-ttu-id="3ecde-112">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="3ecde-112">The following flags can be set:</span></span>
    
<span data-ttu-id="3ecde-113">TABLE_CHANGED</span><span class="sxs-lookup"><span data-stu-id="3ecde-113">TABLE_CHANGED</span></span> 
  
> <span data-ttu-id="3ecde-114">高いレベルの表について何かが変更されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="3ecde-114">Indicates at a high level that something about the table has changed.</span></span> <span data-ttu-id="3ecde-115">テーブルの状態は、イベントの前にします。</span><span class="sxs-lookup"><span data-stu-id="3ecde-115">The table's state is as it was before the event.</span></span> <span data-ttu-id="3ecde-116">これは、すべて**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) のプロパティ、ブックマーク、現在の位置、およびユーザー インターフェイスの選択は、まだ有効であることを意味します。</span><span class="sxs-lookup"><span data-stu-id="3ecde-116">This means that all **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) properties, bookmarks, current positioning, and user interface selections are still valid.</span></span> <span data-ttu-id="3ecde-117">このイベントを処理するには、テーブルを再読み取り.</span><span class="sxs-lookup"><span data-stu-id="3ecde-117">Handle this event by rereading the table.</span></span> <span data-ttu-id="3ecde-118">豊富なテーブルの通知を実装する必要のないサービス ・ プロバイダーは、特定の種類の変更を示すために詳細なイベントの代わりに TABLE_CHANGED イベントを送信します。</span><span class="sxs-lookup"><span data-stu-id="3ecde-118">Service providers that do not want to implement rich table notifications send TABLE_CHANGED events instead of more detailed events to indicate a particular type of change.</span></span> 
    
<span data-ttu-id="3ecde-119">TABLE_ERROR</span><span class="sxs-lookup"><span data-stu-id="3ecde-119">TABLE_ERROR</span></span> 
  
> <span data-ttu-id="3ecde-120">通常、非同期操作の処理中に、エラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="3ecde-120">An error has occurred, usually during the processing of an asynchronous operation.</span></span> <span data-ttu-id="3ecde-121">次のメソッドの処理中にエラーは、このイベントを生成できます。</span><span class="sxs-lookup"><span data-stu-id="3ecde-121">Errors during the processing of the following methods can generate this event:</span></span> 
    
   - [<span data-ttu-id="3ecde-122">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="3ecde-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
   - [<span data-ttu-id="3ecde-123">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="3ecde-123">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
    
   - [<span data-ttu-id="3ecde-124">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="3ecde-124">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
    
   <span data-ttu-id="3ecde-125">TABLE_ERROR イベントを受け取ると、クライアントは、テーブルの内容の正確さに依存できません。</span><span class="sxs-lookup"><span data-stu-id="3ecde-125">After receiving a TABLE_ERROR event, a client cannot rely on the accuracy of the table contents.</span></span> <span data-ttu-id="3ecde-126">また、保留中の他の変更についての通知は失われます。</span><span class="sxs-lookup"><span data-stu-id="3ecde-126">Also, pending notifications about other changes might be lost.</span></span> <span data-ttu-id="3ecde-127">最後のメソッド呼び出しからは、以前の時点で作成されたために、 [IMAPITable::GetLastError](imapitable-getlasterror.md)メソッドは、エラーに関する追加情報を提供しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="3ecde-127">The [IMAPITable::GetLastError](imapitable-getlasterror.md) method might not provide any additional information about the error because it was generated at some previous point, not necessarily from the last method call.</span></span> 
    
<span data-ttu-id="3ecde-128">TABLE_RELOAD</span><span class="sxs-lookup"><span data-stu-id="3ecde-128">TABLE_RELOAD</span></span> 
  
> <span data-ttu-id="3ecde-129">テーブル内のデータを再読み込みする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ecde-129">The data in the table should be reloaded.</span></span> <span data-ttu-id="3ecde-130">サービス ・ プロバイダーは TABLE_RELOAD を送信すると、たとえば、データベースの基になるデータが格納されているデータベースを交換してください。</span><span class="sxs-lookup"><span data-stu-id="3ecde-130">Service providers send TABLE_RELOAD when, for example, the underlying data is stored in a database and the database is replaced.</span></span> <span data-ttu-id="3ecde-131">何も表がまだ有効であることと仮定すると、テーブルを再読み取りがこのイベントを処理します。</span><span class="sxs-lookup"><span data-stu-id="3ecde-131">Handle this event by assuming that nothing about the table is still valid and by rereading the table.</span></span> <span data-ttu-id="3ecde-132">すべてのブックマーク、インスタンスのキー、状態、および位置情報が有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="3ecde-132">All bookmarks, instance keys, status and positioning information are invalid.</span></span>
    
<span data-ttu-id="3ecde-133">TABLE_RESTRICT_DONE</span><span class="sxs-lookup"><span data-stu-id="3ecde-133">TABLE_RESTRICT_DONE</span></span> 
  
> <span data-ttu-id="3ecde-134">制限操作が、 **IMAPITable::Restrict**メソッドの呼び出しで開始したが完了しました。</span><span class="sxs-lookup"><span data-stu-id="3ecde-134">A restriction operation initiated with an **IMAPITable::Restrict** method call has completed.</span></span> 
    
<span data-ttu-id="3ecde-135">TABLE_ROW_ADDED</span><span class="sxs-lookup"><span data-stu-id="3ecde-135">TABLE_ROW_ADDED</span></span> 
  
> <span data-ttu-id="3ecde-136">テーブルと、対応するオブジェクトを保存する新しい行が追加されました。</span><span class="sxs-lookup"><span data-stu-id="3ecde-136">A new row has been added to the table and the corresponding object saved.</span></span> <span data-ttu-id="3ecde-137">[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出した後は、TABLE_ROW_ADDED イベントが生成されます。</span><span class="sxs-lookup"><span data-stu-id="3ecde-137">TABLE_ROW_ADDED events are generated after a call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
    
<span data-ttu-id="3ecde-138">TABLE_ROW_DELETED</span><span class="sxs-lookup"><span data-stu-id="3ecde-138">TABLE_ROW_DELETED</span></span> 
  
> <span data-ttu-id="3ecde-139">テーブルから行が削除されました。</span><span class="sxs-lookup"><span data-stu-id="3ecde-139">A row has been removed from the table.</span></span> <span data-ttu-id="3ecde-140">**PropPrior**メンバーは、NULL に設定されています。</span><span class="sxs-lookup"><span data-stu-id="3ecde-140">The **propPrior** member is set to NULL.</span></span> 
    
<span data-ttu-id="3ecde-141">TABLE_ROW_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="3ecde-141">TABLE_ROW_MODIFIED</span></span> 
  
> <span data-ttu-id="3ecde-142">行が変更されました。</span><span class="sxs-lookup"><span data-stu-id="3ecde-142">A row has been changed.</span></span> <span data-ttu-id="3ecde-143">**行**メンバーには、行の影響を受けるプロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="3ecde-143">The **row** member contains the affected properties for the row.</span></span> <span data-ttu-id="3ecde-144">複数の TABLE_ROW_MODIFIED イベントは、テーブル ビューに表示される順序で送信されます。</span><span class="sxs-lookup"><span data-stu-id="3ecde-144">Multiple TABLE_ROW_MODIFIED events are sent in the order that they appear in the table view.</span></span> 
    
  <span data-ttu-id="3ecde-145">TABLE_ROW_MODIFIED イベントは、対応するオブジェクトへの変更が、 **IMAPIProp::SaveChanges**メソッドを呼び出して、コミットされた後に送信されます。</span><span class="sxs-lookup"><span data-stu-id="3ecde-145">TABLE_ROW_MODIFIED events are sent after changes to the corresponding object have been committed with a call to the **IMAPIProp::SaveChanges** method.</span></span> <span data-ttu-id="3ecde-146">ここで変更した行がテーブルの最初の行の場合は、 **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) は、 **propPrior**メンバーのプロパティ タグの値です。</span><span class="sxs-lookup"><span data-stu-id="3ecde-146">If the modified row is now the first row in the table, the value of the property tag in the **propPrior** member is **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span></span>
    
<span data-ttu-id="3ecde-147">TABLE_SETCOL_DONE</span><span class="sxs-lookup"><span data-stu-id="3ecde-147">TABLE_SETCOL_DONE</span></span> 
  
> <span data-ttu-id="3ecde-148">**IMAPITable::SetColumns**のメソッドの呼び出しを使用して開始列の設定操作が完了しました。</span><span class="sxs-lookup"><span data-stu-id="3ecde-148">A column setting operation initiated with an **IMAPITable::SetColumns** method call has completed.</span></span> 
    
<span data-ttu-id="3ecde-149">TABLE_SORT_DONE</span><span class="sxs-lookup"><span data-stu-id="3ecde-149">TABLE_SORT_DONE</span></span> 
  
> <span data-ttu-id="3ecde-150">テーブルの並べ替えの操作は、 **IMAPITable::SortTable**メソッドの呼び出しで開始したが完了しました。</span><span class="sxs-lookup"><span data-stu-id="3ecde-150">A table sorting operation initiated with an **IMAPITable::SortTable** method call has completed.</span></span> 
    
<span data-ttu-id="3ecde-151">**hResult**</span><span class="sxs-lookup"><span data-stu-id="3ecde-151">**hResult**</span></span>
  
> <span data-ttu-id="3ecde-152">**UlTableEvent**メンバーは、TABLE_ERROR に設定されている場合、発生したエラーの HRESULT 値です。</span><span class="sxs-lookup"><span data-stu-id="3ecde-152">HRESULT value for the error that has occurred, if the **ulTableEvent** member is set to TABLE_ERROR.</span></span> 
    
<span data-ttu-id="3ecde-153">**propIndex**</span><span class="sxs-lookup"><span data-stu-id="3ecde-153">**propIndex**</span></span>
  
> <span data-ttu-id="3ecde-154">影響を受ける行の**PR_INSTANCE_KEY**プロパティの値の[SPropValue](spropvalue.md)構造体です。</span><span class="sxs-lookup"><span data-stu-id="3ecde-154">[SPropValue](spropvalue.md) structure for the **PR_INSTANCE_KEY** property of the affected row.</span></span> 
    
<span data-ttu-id="3ecde-155">**propPrior**</span><span class="sxs-lookup"><span data-stu-id="3ecde-155">**propPrior**</span></span>
  
> <span data-ttu-id="3ecde-156">影響を受ける 1 つ前に、の行の**PR_INSTANCE_KEY**プロパティの**SPropValue**構造体です。</span><span class="sxs-lookup"><span data-stu-id="3ecde-156">**SPropValue** structure for the **PR_INSTANCE_KEY** property of the row before the affected one.</span></span> <span data-ttu-id="3ecde-157">影響を受ける行がテーブルの最初の行の場合は、 **PR_NULL**を 0 ではありません**propPrior**を設定しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="3ecde-157">If the affected row is the first row in the table, **propPrior** must be set to **PR_NULL** and not zero.</span></span> <span data-ttu-id="3ecde-158">0 は有効なプロパティのタグではありません。</span><span class="sxs-lookup"><span data-stu-id="3ecde-158">Zero is not a valid property tag.</span></span> 
    
<span data-ttu-id="3ecde-159">**row**</span><span class="sxs-lookup"><span data-stu-id="3ecde-159">**row**</span></span>
  
> <span data-ttu-id="3ecde-160">[SRow](srow.md)の構造が影響を受ける行を記述します。</span><span class="sxs-lookup"><span data-stu-id="3ecde-160">[SRow](srow.md) structure describing the affected row.</span></span> <span data-ttu-id="3ecde-161">この構造体は、テーブルのすべての通知イベントに入力されます。</span><span class="sxs-lookup"><span data-stu-id="3ecde-161">This structure is filled for all table notification events.</span></span> <span data-ttu-id="3ecde-162">テーブル通知、イベントの行データを渡さない、**あう**、 **SRow**構造体のメンバーを 0 に設定し、 **lpProps**メンバーは NULL に設定します。</span><span class="sxs-lookup"><span data-stu-id="3ecde-162">For table notification events that do not pass row data, the **cValues** member of the **SRow** structure is set to zero and the **lpProps** member is set to NULL.</span></span> <span data-ttu-id="3ecde-163">この**SRow**の構造が読み取り専用であるためクライアントは、変更を加える必要がある場合のコピーを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ecde-163">Because this **SRow** structure is read-only; clients must make a copy of it if they want to make modifications.</span></span> <span data-ttu-id="3ecde-164">コピーを作成するのには、 [ScDupPropset](scduppropset.md)関数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="3ecde-164">The [ScDupPropset](scduppropset.md) function can be used to make the copy.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3ecde-165">注釈</span><span class="sxs-lookup"><span data-stu-id="3ecde-165">Remarks</span></span>

<span data-ttu-id="3ecde-166">**テーブル\_通知**構造体は、[通知](notification.md)の構造体のメンバー**情報**に含まれる構造体の共用体のメンバーの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="3ecde-166">The **TABLE\_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="3ecde-167">**情報**メンバーが含まれています、**テーブル\_通知**、 **ulEventType**構造体のメンバーが_fnevTableModified_に設定されている場合を構造化します。</span><span class="sxs-lookup"><span data-stu-id="3ecde-167">The **info** member includes a **TABLE\_NOTIFICATION** structure when the **ulEventType** member of the structure is set to  _fnevTableModified_.</span></span>
  
<span data-ttu-id="3ecde-168">行メンバーの列の型と順序は、順序と、通知が生成された時点で有効であったタイプを反映します。</span><span class="sxs-lookup"><span data-stu-id="3ecde-168">The order and type of columns in the row member reflect the order and type that was in effect at the time that the notification was generated.</span></span> <span data-ttu-id="3ecde-169">順序と種類の通知が生成された時点では必ずしもと同じ通知が配布されたときです。</span><span class="sxs-lookup"><span data-stu-id="3ecde-169">The order and type at the time that the notification was generated is not necessarily the same as when the notification was delivered.</span></span> 
  
<span data-ttu-id="3ecde-170">通知の詳細については、次の表に記載されているトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3ecde-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="3ecde-171">**トピック**</span><span class="sxs-lookup"><span data-stu-id="3ecde-171">**Topic**</span></span>|<span data-ttu-id="3ecde-172">**説明**</span><span class="sxs-lookup"><span data-stu-id="3ecde-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3ecde-173">MAPI のイベント通知</span><span class="sxs-lookup"><span data-stu-id="3ecde-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="3ecde-174">通知と通知のイベントの概要です。</span><span class="sxs-lookup"><span data-stu-id="3ecde-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="3ecde-175">通知の処理</span><span class="sxs-lookup"><span data-stu-id="3ecde-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="3ecde-176">クライアントが通知を処理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3ecde-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="3ecde-177">イベント通知のサポート</span><span class="sxs-lookup"><span data-stu-id="3ecde-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="3ecde-178">サービス プロバイダーが、 **IMAPISupport**メソッドを使用して、通知を生成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3ecde-178">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
<span data-ttu-id="3ecde-179">テーブルの通知は非同期であるために、クライアントは別の方法で追加について学習した後、追加された行の通知を受信できます。</span><span class="sxs-lookup"><span data-stu-id="3ecde-179">Because table notifications are asynchronous, clients can receive notification of an added row after learning about the addition through another means.</span></span> <span data-ttu-id="3ecde-180">**IMAPITable::Sort**、 **IMAPITable::Restrict**、または**IMAPITable::SetColumns**メソッドでエラーが表示されるか、プロセスで、テーブルを更新しようとした、基になるときは、TABLE_ERROR イベントを受信することはまたは行を変更します。</span><span class="sxs-lookup"><span data-stu-id="3ecde-180">It is possible to receive a TABLE_ERROR event when there is an error in an **IMAPITable::Sort**, **IMAPITable::Restrict**, or **IMAPITable::SetColumns** method or when an underlying process attempts to update a table with, for example, new or modified rows.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3ecde-181">関連項目</span><span class="sxs-lookup"><span data-stu-id="3ecde-181">See also</span></span>

- [<span data-ttu-id="3ecde-182">�ʒm</span><span class="sxs-lookup"><span data-stu-id="3ecde-182">NOTIFICATION</span></span>](notification.md) 
- [<span data-ttu-id="3ecde-183">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="3ecde-183">ScDupPropset</span></span>](scduppropset.md)
- [<span data-ttu-id="3ecde-184">SRow</span><span class="sxs-lookup"><span data-stu-id="3ecde-184">SRow</span></span>](srow.md)
- [<span data-ttu-id="3ecde-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="3ecde-185">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="3ecde-186">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="3ecde-186">MAPI Structures</span></span>](mapi-structures.md)

