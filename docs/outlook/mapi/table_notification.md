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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6c35220529fb88b470c563a0b004bfcf7e63ef76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415958"
---
# <a name="tablenotification"></a><span data-ttu-id="61933-103">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="61933-103">TABLE_NOTIFICATION</span></span>

<span data-ttu-id="61933-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61933-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61933-105">変更やエラーなど、何らかの種類のイベントの影響を受けたテーブル内の行について説明します。</span><span class="sxs-lookup"><span data-stu-id="61933-105">Describes a row in a table that has been affected by some type of event, such as a change or an error.</span></span> <span data-ttu-id="61933-106">これにより、テーブル通知が生成されます。</span><span class="sxs-lookup"><span data-stu-id="61933-106">This causes a table notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="61933-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="61933-107">Header file:</span></span>  <br/> |<span data-ttu-id="61933-108">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="61933-108">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="61933-109">メンバー</span><span class="sxs-lookup"><span data-stu-id="61933-109">Members</span></span>

<span data-ttu-id="61933-110">**ultableevent**</span><span class="sxs-lookup"><span data-stu-id="61933-110">**ulTableEvent**</span></span>
  
> <span data-ttu-id="61933-111">テーブルイベントの種類を表すために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="61933-111">Bitmask of flags used to represent the table event type.</span></span> <span data-ttu-id="61933-112">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="61933-112">The following flags can be set:</span></span>
    
<span data-ttu-id="61933-113">TABLE_CHANGED</span><span class="sxs-lookup"><span data-stu-id="61933-113">TABLE_CHANGED</span></span> 
  
> <span data-ttu-id="61933-114">テーブルに関する何らかの変更が、高レベルであることを示します。</span><span class="sxs-lookup"><span data-stu-id="61933-114">Indicates at a high level that something about the table has changed.</span></span> <span data-ttu-id="61933-115">テーブルの状態はイベントの前と同じです。</span><span class="sxs-lookup"><span data-stu-id="61933-115">The table's state is as it was before the event.</span></span> <span data-ttu-id="61933-116">これは、すべての**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) プロパティ、ブックマーク、現在の配置、およびユーザーインターフェイスの選択が有効なままであることを意味します。</span><span class="sxs-lookup"><span data-stu-id="61933-116">This means that all **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) properties, bookmarks, current positioning, and user interface selections are still valid.</span></span> <span data-ttu-id="61933-117">このイベントを処理するには、テーブルを再度読み込みます。</span><span class="sxs-lookup"><span data-stu-id="61933-117">Handle this event by rereading the table.</span></span> <span data-ttu-id="61933-118">リッチテーブル通知を実装しないサービスプロバイダーは、より詳細なイベントの代わりに TABLE_CHANGED イベントを送信して、特定の種類の変更を示します。</span><span class="sxs-lookup"><span data-stu-id="61933-118">Service providers that do not want to implement rich table notifications send TABLE_CHANGED events instead of more detailed events to indicate a particular type of change.</span></span> 
    
<span data-ttu-id="61933-119">TABLE_ERROR</span><span class="sxs-lookup"><span data-stu-id="61933-119">TABLE_ERROR</span></span> 
  
> <span data-ttu-id="61933-120">エラーが発生しました。通常は、非同期操作の処理中です。</span><span class="sxs-lookup"><span data-stu-id="61933-120">An error has occurred, usually during the processing of an asynchronous operation.</span></span> <span data-ttu-id="61933-121">次のメソッドの処理中にエラーが発生すると、このイベントが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="61933-121">Errors during the processing of the following methods can generate this event:</span></span> 
    
   - [<span data-ttu-id="61933-122">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="61933-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
   - [<span data-ttu-id="61933-123">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="61933-123">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
    
   - [<span data-ttu-id="61933-124">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="61933-124">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
    
   <span data-ttu-id="61933-125">TABLE_ERROR イベントを受け取った後、クライアントはテーブルの内容の正確性を信頼できません。</span><span class="sxs-lookup"><span data-stu-id="61933-125">After receiving a TABLE_ERROR event, a client cannot rely on the accuracy of the table contents.</span></span> <span data-ttu-id="61933-126">また、他の変更に関する保留中の通知が失われる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="61933-126">Also, pending notifications about other changes might be lost.</span></span> <span data-ttu-id="61933-127">[IMAPITable:: GetLastError](imapitable-getlasterror.md)メソッドは、前の時点で生成されたものではなく、最後のメソッドの呼び出しからは、エラーに関する追加情報を提供していない場合があります。</span><span class="sxs-lookup"><span data-stu-id="61933-127">The [IMAPITable::GetLastError](imapitable-getlasterror.md) method might not provide any additional information about the error because it was generated at some previous point, not necessarily from the last method call.</span></span> 
    
<span data-ttu-id="61933-128">TABLE_RELOAD</span><span class="sxs-lookup"><span data-stu-id="61933-128">TABLE_RELOAD</span></span> 
  
> <span data-ttu-id="61933-129">テーブル内のデータを再度読み込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="61933-129">The data in the table should be reloaded.</span></span> <span data-ttu-id="61933-130">サービスプロバイダーは、たとえば、基になるデータがデータベースに格納され、データベースが置換されるときに、TABLE_RELOAD を送信します。</span><span class="sxs-lookup"><span data-stu-id="61933-130">Service providers send TABLE_RELOAD when, for example, the underlying data is stored in a database and the database is replaced.</span></span> <span data-ttu-id="61933-131">このイベントを処理するのは、テーブルに関する情報がまだ有効でないことを前提にして、テーブルを再度読み込みます。</span><span class="sxs-lookup"><span data-stu-id="61933-131">Handle this event by assuming that nothing about the table is still valid and by rereading the table.</span></span> <span data-ttu-id="61933-132">すべてのブックマーク、インスタンスキー、状態、および配置情報が無効です。</span><span class="sxs-lookup"><span data-stu-id="61933-132">All bookmarks, instance keys, status and positioning information are invalid.</span></span>
    
<span data-ttu-id="61933-133">TABLE_RESTRICT_DONE</span><span class="sxs-lookup"><span data-stu-id="61933-133">TABLE_RESTRICT_DONE</span></span> 
  
> <span data-ttu-id="61933-134">**IMAPITable:: Restrict**メソッド呼び出しで開始された制限の操作が完了しました。</span><span class="sxs-lookup"><span data-stu-id="61933-134">A restriction operation initiated with an **IMAPITable::Restrict** method call has completed.</span></span> 
    
<span data-ttu-id="61933-135">TABLE_ROW_ADDED</span><span class="sxs-lookup"><span data-stu-id="61933-135">TABLE_ROW_ADDED</span></span> 
  
> <span data-ttu-id="61933-136">テーブルに新しい行が追加され、対応するオブジェクトが保存されます。</span><span class="sxs-lookup"><span data-stu-id="61933-136">A new row has been added to the table and the corresponding object saved.</span></span> <span data-ttu-id="61933-137">TABLE_ROW_ADDED イベントは、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出した後に生成されます。</span><span class="sxs-lookup"><span data-stu-id="61933-137">TABLE_ROW_ADDED events are generated after a call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
    
<span data-ttu-id="61933-138">TABLE_ROW_DELETED</span><span class="sxs-lookup"><span data-stu-id="61933-138">TABLE_ROW_DELETED</span></span> 
  
> <span data-ttu-id="61933-139">行がテーブルから削除されました。</span><span class="sxs-lookup"><span data-stu-id="61933-139">A row has been removed from the table.</span></span> <span data-ttu-id="61933-140">**propprior**メンバーは NULL に設定されています。</span><span class="sxs-lookup"><span data-stu-id="61933-140">The **propPrior** member is set to NULL.</span></span> 
    
<span data-ttu-id="61933-141">TABLE_ROW_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="61933-141">TABLE_ROW_MODIFIED</span></span> 
  
> <span data-ttu-id="61933-142">行が変更されました。</span><span class="sxs-lookup"><span data-stu-id="61933-142">A row has been changed.</span></span> <span data-ttu-id="61933-143">行\*\*\*\* メンバーには、行の影響を受けるプロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="61933-143">The **row** member contains the affected properties for the row.</span></span> <span data-ttu-id="61933-144">複数の TABLE_ROW_MODIFIED イベントは、テーブルビューに表示される順序で送信されます。</span><span class="sxs-lookup"><span data-stu-id="61933-144">Multiple TABLE_ROW_MODIFIED events are sent in the order that they appear in the table view.</span></span> 
    
  <span data-ttu-id="61933-145">TABLE_ROW_MODIFIED イベントは、対応するオブジェクトへの変更が、 **imapiprop:: SaveChanges**メソッドへの呼び出しを使用してコミットされた後に送信されます。</span><span class="sxs-lookup"><span data-stu-id="61933-145">TABLE_ROW_MODIFIED events are sent after changes to the corresponding object have been committed with a call to the **IMAPIProp::SaveChanges** method.</span></span> <span data-ttu-id="61933-146">変更された行がテーブルの最初の行になった場合、その**前**のメンバーのプロパティタグの値は**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) になります。</span><span class="sxs-lookup"><span data-stu-id="61933-146">If the modified row is now the first row in the table, the value of the property tag in the **propPrior** member is **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span></span>
    
<span data-ttu-id="61933-147">TABLE_SETCOL_DONE</span><span class="sxs-lookup"><span data-stu-id="61933-147">TABLE_SETCOL_DONE</span></span> 
  
> <span data-ttu-id="61933-148">**IMAPITable:: SetColumns**メソッド呼び出しで開始された列設定操作が完了しました。</span><span class="sxs-lookup"><span data-stu-id="61933-148">A column setting operation initiated with an **IMAPITable::SetColumns** method call has completed.</span></span> 
    
<span data-ttu-id="61933-149">TABLE_SORT_DONE</span><span class="sxs-lookup"><span data-stu-id="61933-149">TABLE_SORT_DONE</span></span> 
  
> <span data-ttu-id="61933-150">**IMAPITable:: sorttable**メソッド呼び出しで開始されたテーブルの並べ替え操作が完了しました。</span><span class="sxs-lookup"><span data-stu-id="61933-150">A table sorting operation initiated with an **IMAPITable::SortTable** method call has completed.</span></span> 
    
<span data-ttu-id="61933-151">**hResult**</span><span class="sxs-lookup"><span data-stu-id="61933-151">**hResult**</span></span>
  
> <span data-ttu-id="61933-152">**ultableevent**メンバーが TABLE_ERROR に設定されている場合に、発生したエラーの HRESULT 値。</span><span class="sxs-lookup"><span data-stu-id="61933-152">HRESULT value for the error that has occurred, if the **ulTableEvent** member is set to TABLE_ERROR.</span></span> 
    
<span data-ttu-id="61933-153">**propindex**</span><span class="sxs-lookup"><span data-stu-id="61933-153">**propIndex**</span></span>
  
> <span data-ttu-id="61933-154">影響を受ける行の**PR_INSTANCE_KEY**プロパティの[spropvalue](spropvalue.md)構造。</span><span class="sxs-lookup"><span data-stu-id="61933-154">[SPropValue](spropvalue.md) structure for the **PR_INSTANCE_KEY** property of the affected row.</span></span> 
    
<span data-ttu-id="61933-155">**propprior**</span><span class="sxs-lookup"><span data-stu-id="61933-155">**propPrior**</span></span>
  
> <span data-ttu-id="61933-156">影響を受ける前の行の**PR_INSTANCE_KEY**プロパティの**spropvalue**構造。</span><span class="sxs-lookup"><span data-stu-id="61933-156">**SPropValue** structure for the **PR_INSTANCE_KEY** property of the row before the affected one.</span></span> <span data-ttu-id="61933-157">影響を受ける行がテーブルの最初の行である\*\*\*\* 場合は、 **PR_NULL**を0以外の値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="61933-157">If the affected row is the first row in the table, **propPrior** must be set to **PR_NULL** and not zero.</span></span> <span data-ttu-id="61933-158">0は、有効なプロパティタグではありません。</span><span class="sxs-lookup"><span data-stu-id="61933-158">Zero is not a valid property tag.</span></span> 
    
<span data-ttu-id="61933-159">**row**</span><span class="sxs-lookup"><span data-stu-id="61933-159">**row**</span></span>
  
> <span data-ttu-id="61933-160">影響を受ける行を説明する[srow](srow.md)構造。</span><span class="sxs-lookup"><span data-stu-id="61933-160">[SRow](srow.md) structure describing the affected row.</span></span> <span data-ttu-id="61933-161">この構造体は、すべてのテーブル通知イベントに対して入力されます。</span><span class="sxs-lookup"><span data-stu-id="61933-161">This structure is filled for all table notification events.</span></span> <span data-ttu-id="61933-162">行データを渡さないテーブル通知イベントの場合、 **srow**構造の**cvalues**メンバーは0に設定され、 **lpprops**メンバーは NULL に設定されます。</span><span class="sxs-lookup"><span data-stu-id="61933-162">For table notification events that do not pass row data, the **cValues** member of the **SRow** structure is set to zero and the **lpProps** member is set to NULL.</span></span> <span data-ttu-id="61933-163">この**srow**構造は読み取り専用であるためです。クライアントは、変更を行う場合は、そのコピーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="61933-163">Because this **SRow** structure is read-only; clients must make a copy of it if they want to make modifications.</span></span> <span data-ttu-id="61933-164">[ScDupPropset](scduppropset.md)関数を使用してコピーを作成できます。</span><span class="sxs-lookup"><span data-stu-id="61933-164">The [ScDupPropset](scduppropset.md) function can be used to make the copy.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="61933-165">注釈</span><span class="sxs-lookup"><span data-stu-id="61933-165">Remarks</span></span>

<span data-ttu-id="61933-166">**表\_通知**構造は、[通知](notification.md)構造の**info**メンバに含まれている構造体の和集合のメンバーのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="61933-166">The **TABLE\_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="61933-167">構造体の**uleventtype**メンバーが_fnevTableModified_に設定されている場合、 **info**メンバーには**テーブル\_通知**構造が含まれています。</span><span class="sxs-lookup"><span data-stu-id="61933-167">The **info** member includes a **TABLE\_NOTIFICATION** structure when the **ulEventType** member of the structure is set to  _fnevTableModified_.</span></span>
  
<span data-ttu-id="61933-168">行メンバーの列の順序と種類は、通知が生成されたときに有効だった順序と種類を反映しています。</span><span class="sxs-lookup"><span data-stu-id="61933-168">The order and type of columns in the row member reflect the order and type that was in effect at the time that the notification was generated.</span></span> <span data-ttu-id="61933-169">通知が生成されたときの順序と種類は、通知が配信されたときと必ずしも同じではありません。</span><span class="sxs-lookup"><span data-stu-id="61933-169">The order and type at the time that the notification was generated is not necessarily the same as when the notification was delivered.</span></span> 
  
<span data-ttu-id="61933-170">通知の詳細については、次の表で説明するトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="61933-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="61933-171">**トピック**</span><span class="sxs-lookup"><span data-stu-id="61933-171">**Topic**</span></span>|<span data-ttu-id="61933-172">**説明**</span><span class="sxs-lookup"><span data-stu-id="61933-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="61933-173">MAPI のイベント通知</span><span class="sxs-lookup"><span data-stu-id="61933-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="61933-174">通知イベントと通知イベントの一般的な概要。</span><span class="sxs-lookup"><span data-stu-id="61933-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="61933-175">通知の処理</span><span class="sxs-lookup"><span data-stu-id="61933-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="61933-176">クライアントが通知を処理する方法についての説明。</span><span class="sxs-lookup"><span data-stu-id="61933-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="61933-177">イベント通知のサポート</span><span class="sxs-lookup"><span data-stu-id="61933-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="61933-178">サービスプロバイダーが**imapisupport**メソッドを使用して通知を生成する方法についての説明。</span><span class="sxs-lookup"><span data-stu-id="61933-178">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
<span data-ttu-id="61933-179">テーブル通知は非同期であるため、クライアントは別の方法で追加について学習した後に、追加された行の通知を受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="61933-179">Because table notifications are asynchronous, clients can receive notification of an added row after learning about the addition through another means.</span></span> <span data-ttu-id="61933-180">TABLE_ERROR イベントは、 **IMAPITable:: Sort**、 **IMAPITable:: Restrict**、または**IMAPITable:: SetColumns**メソッドでエラーが発生した場合、または基になるプロセスがテーブルを更新しようとした場合 (たとえば、new または変更された行</span><span class="sxs-lookup"><span data-stu-id="61933-180">It is possible to receive a TABLE_ERROR event when there is an error in an **IMAPITable::Sort**, **IMAPITable::Restrict**, or **IMAPITable::SetColumns** method or when an underlying process attempts to update a table with, for example, new or modified rows.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="61933-181">関連項目</span><span class="sxs-lookup"><span data-stu-id="61933-181">See also</span></span>

- [<span data-ttu-id="61933-182">�ʒm</span><span class="sxs-lookup"><span data-stu-id="61933-182">NOTIFICATION</span></span>](notification.md) 
- [<span data-ttu-id="61933-183">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="61933-183">ScDupPropset</span></span>](scduppropset.md)
- [<span data-ttu-id="61933-184">SRow</span><span class="sxs-lookup"><span data-stu-id="61933-184">SRow</span></span>](srow.md)
- [<span data-ttu-id="61933-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="61933-185">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="61933-186">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="61933-186">MAPI Structures</span></span>](mapi-structures.md)

