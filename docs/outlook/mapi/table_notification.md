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
# <a name="table_notification"></a><span data-ttu-id="a4001-103">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="a4001-103">TABLE_NOTIFICATION</span></span>

<span data-ttu-id="a4001-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4001-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4001-105">変更やエラーなど、何らかの種類のイベントの影響を受けたテーブル内の行について説明します。</span><span class="sxs-lookup"><span data-stu-id="a4001-105">Describes a row in a table that has been affected by some type of event, such as a change or an error.</span></span> <span data-ttu-id="a4001-106">これにより、テーブル通知が生成されます。</span><span class="sxs-lookup"><span data-stu-id="a4001-106">This causes a table notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a4001-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a4001-107">Header file:</span></span>  <br/> |<span data-ttu-id="a4001-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a4001-108">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="a4001-109">Members</span><span class="sxs-lookup"><span data-stu-id="a4001-109">Members</span></span>

<span data-ttu-id="a4001-110">**ulTableEvent**</span><span class="sxs-lookup"><span data-stu-id="a4001-110">**ulTableEvent**</span></span>
  
> <span data-ttu-id="a4001-111">テーブル イベントの種類を表すフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="a4001-111">Bitmask of flags used to represent the table event type.</span></span> <span data-ttu-id="a4001-112">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a4001-112">The following flags can be set:</span></span>
    
<span data-ttu-id="a4001-113">TABLE_CHANGED</span><span class="sxs-lookup"><span data-stu-id="a4001-113">TABLE_CHANGED</span></span> 
  
> <span data-ttu-id="a4001-114">テーブルに関する情報が変更されたことを高レベルで示します。</span><span class="sxs-lookup"><span data-stu-id="a4001-114">Indicates at a high level that something about the table has changed.</span></span> <span data-ttu-id="a4001-115">テーブルの状態は、イベントの前の状態です。</span><span class="sxs-lookup"><span data-stu-id="a4001-115">The table's state is as it was before the event.</span></span> <span data-ttu-id="a4001-116">つまり **、すべてのPR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) プロパティ、ブックマーク、現在の配置、およびユーザー インターフェイスの選択は引き続き有効です。</span><span class="sxs-lookup"><span data-stu-id="a4001-116">This means that all **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) properties, bookmarks, current positioning, and user interface selections are still valid.</span></span> <span data-ttu-id="a4001-117">テーブルを再読み込みして、このイベントを処理します。</span><span class="sxs-lookup"><span data-stu-id="a4001-117">Handle this event by rereading the table.</span></span> <span data-ttu-id="a4001-118">リッチ テーブル通知を実装しないサービス プロバイダーは、特定の種類の変更TABLE_CHANGED詳細なイベントではなく、イベントを送信します。</span><span class="sxs-lookup"><span data-stu-id="a4001-118">Service providers that do not want to implement rich table notifications send TABLE_CHANGED events instead of more detailed events to indicate a particular type of change.</span></span> 
    
<span data-ttu-id="a4001-119">TABLE_ERROR</span><span class="sxs-lookup"><span data-stu-id="a4001-119">TABLE_ERROR</span></span> 
  
> <span data-ttu-id="a4001-120">通常、非同期操作の処理中にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a4001-120">An error has occurred, usually during the processing of an asynchronous operation.</span></span> <span data-ttu-id="a4001-121">次のメソッドの処理中にエラーが発生すると、このイベントが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a4001-121">Errors during the processing of the following methods can generate this event:</span></span> 
    
   - [<span data-ttu-id="a4001-122">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="a4001-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
   - [<span data-ttu-id="a4001-123">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="a4001-123">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
    
   - [<span data-ttu-id="a4001-124">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="a4001-124">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
    
   <span data-ttu-id="a4001-125">イベントを受信TABLE_ERROR、クライアントは表の内容の精度に依存できません。</span><span class="sxs-lookup"><span data-stu-id="a4001-125">After receiving a TABLE_ERROR event, a client cannot rely on the accuracy of the table contents.</span></span> <span data-ttu-id="a4001-126">また、他の変更に関する保留中の通知が失われる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a4001-126">Also, pending notifications about other changes might be lost.</span></span> <span data-ttu-id="a4001-127">[IMAPITable::GetLastError](imapitable-getlasterror.md)メソッドは、以前の時点で生成されたエラーに関する追加情報を提供しない場合があります。必ずしも最後のメソッド呼び出しから生成されたとは限りません。</span><span class="sxs-lookup"><span data-stu-id="a4001-127">The [IMAPITable::GetLastError](imapitable-getlasterror.md) method might not provide any additional information about the error because it was generated at some previous point, not necessarily from the last method call.</span></span> 
    
<span data-ttu-id="a4001-128">TABLE_RELOAD</span><span class="sxs-lookup"><span data-stu-id="a4001-128">TABLE_RELOAD</span></span> 
  
> <span data-ttu-id="a4001-129">テーブル内のデータを再読み込みする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a4001-129">The data in the table should be reloaded.</span></span> <span data-ttu-id="a4001-130">サービス プロバイダーは、TABLE_RELOAD基になるデータがデータベースに格納され、データベースが置き換えられた場合に、このデータを送信します。</span><span class="sxs-lookup"><span data-stu-id="a4001-130">Service providers send TABLE_RELOAD when, for example, the underlying data is stored in a database and the database is replaced.</span></span> <span data-ttu-id="a4001-131">テーブルに関する何も有効でないと仮定し、テーブルを再読み込みすることで、このイベントを処理します。</span><span class="sxs-lookup"><span data-stu-id="a4001-131">Handle this event by assuming that nothing about the table is still valid and by rereading the table.</span></span> <span data-ttu-id="a4001-132">ブックマーク、インスタンス キー、状態、および位置情報はすべて無効です。</span><span class="sxs-lookup"><span data-stu-id="a4001-132">All bookmarks, instance keys, status and positioning information are invalid.</span></span>
    
<span data-ttu-id="a4001-133">TABLE_RESTRICT_DONE</span><span class="sxs-lookup"><span data-stu-id="a4001-133">TABLE_RESTRICT_DONE</span></span> 
  
> <span data-ttu-id="a4001-134">**IMAPITable::Restrict** メソッド呼び出しで開始された制限操作が完了しました。</span><span class="sxs-lookup"><span data-stu-id="a4001-134">A restriction operation initiated with an **IMAPITable::Restrict** method call has completed.</span></span> 
    
<span data-ttu-id="a4001-135">TABLE_ROW_ADDED</span><span class="sxs-lookup"><span data-stu-id="a4001-135">TABLE_ROW_ADDED</span></span> 
  
> <span data-ttu-id="a4001-136">テーブルに新しい行が追加され、対応するオブジェクトが保存されました。</span><span class="sxs-lookup"><span data-stu-id="a4001-136">A new row has been added to the table and the corresponding object saved.</span></span> <span data-ttu-id="a4001-137">TABLE_ROW_ADDEDは [、IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドの呼び出し後に生成されます。</span><span class="sxs-lookup"><span data-stu-id="a4001-137">TABLE_ROW_ADDED events are generated after a call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
    
<span data-ttu-id="a4001-138">TABLE_ROW_DELETED</span><span class="sxs-lookup"><span data-stu-id="a4001-138">TABLE_ROW_DELETED</span></span> 
  
> <span data-ttu-id="a4001-139">テーブルから行が削除されました。</span><span class="sxs-lookup"><span data-stu-id="a4001-139">A row has been removed from the table.</span></span> <span data-ttu-id="a4001-140">**propPrior メンバーは** NULL に設定されます。</span><span class="sxs-lookup"><span data-stu-id="a4001-140">The **propPrior** member is set to NULL.</span></span> 
    
<span data-ttu-id="a4001-141">TABLE_ROW_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="a4001-141">TABLE_ROW_MODIFIED</span></span> 
  
> <span data-ttu-id="a4001-142">行が変更されました。</span><span class="sxs-lookup"><span data-stu-id="a4001-142">A row has been changed.</span></span> <span data-ttu-id="a4001-143">行 **メンバーには** 、その行の影響を受けるプロパティが含まれる。</span><span class="sxs-lookup"><span data-stu-id="a4001-143">The **row** member contains the affected properties for the row.</span></span> <span data-ttu-id="a4001-144">複数TABLE_ROW_MODIFIEDイベントは、テーブル ビューに表示される順序で送信されます。</span><span class="sxs-lookup"><span data-stu-id="a4001-144">Multiple TABLE_ROW_MODIFIED events are sent in the order that they appear in the table view.</span></span> 
    
  <span data-ttu-id="a4001-145">TABLE_ROW_MODIFIEDは **、IMAPIProp::SaveChanges** メソッドの呼び出しで、対応するオブジェクトに対する変更がコミットされた後に送信されます。</span><span class="sxs-lookup"><span data-stu-id="a4001-145">TABLE_ROW_MODIFIED events are sent after changes to the corresponding object have been committed with a call to the **IMAPIProp::SaveChanges** method.</span></span> <span data-ttu-id="a4001-146">変更された行がテーブルの最初の行である場合 **、propPrior** メンバーのプロパティ タグの値は PR_NULL ([PidTagNull) になります](pidtagnull-canonical-property.md)。 </span><span class="sxs-lookup"><span data-stu-id="a4001-146">If the modified row is now the first row in the table, the value of the property tag in the **propPrior** member is **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span></span>
    
<span data-ttu-id="a4001-147">TABLE_SETCOL_DONE</span><span class="sxs-lookup"><span data-stu-id="a4001-147">TABLE_SETCOL_DONE</span></span> 
  
> <span data-ttu-id="a4001-148">**IMAPITable::SetColumns** メソッド呼び出しで開始された列設定操作が完了しました。</span><span class="sxs-lookup"><span data-stu-id="a4001-148">A column setting operation initiated with an **IMAPITable::SetColumns** method call has completed.</span></span> 
    
<span data-ttu-id="a4001-149">TABLE_SORT_DONE</span><span class="sxs-lookup"><span data-stu-id="a4001-149">TABLE_SORT_DONE</span></span> 
  
> <span data-ttu-id="a4001-150">**IMAPITable::SortTable** メソッド呼び出しで開始されたテーブルの並べ替え操作が完了しました。</span><span class="sxs-lookup"><span data-stu-id="a4001-150">A table sorting operation initiated with an **IMAPITable::SortTable** method call has completed.</span></span> 
    
<span data-ttu-id="a4001-151">**hResult**</span><span class="sxs-lookup"><span data-stu-id="a4001-151">**hResult**</span></span>
  
> <span data-ttu-id="a4001-152">ulTableEvent メンバーがエラーに設定されている場合に発生したエラーの **HRESULT** TABLE_ERROR。</span><span class="sxs-lookup"><span data-stu-id="a4001-152">HRESULT value for the error that has occurred, if the **ulTableEvent** member is set to TABLE_ERROR.</span></span> 
    
<span data-ttu-id="a4001-153">**propIndex**</span><span class="sxs-lookup"><span data-stu-id="a4001-153">**propIndex**</span></span>
  
> <span data-ttu-id="a4001-154">[影響を受](spropvalue.md) ける **行の** PR_INSTANCE_KEYプロパティの SPropValue 構造体。</span><span class="sxs-lookup"><span data-stu-id="a4001-154">[SPropValue](spropvalue.md) structure for the **PR_INSTANCE_KEY** property of the affected row.</span></span> 
    
<span data-ttu-id="a4001-155">**propPrior**</span><span class="sxs-lookup"><span data-stu-id="a4001-155">**propPrior**</span></span>
  
> <span data-ttu-id="a4001-156">**影響を受** ける行の **前PR_INSTANCE_KEY** プロパティの SPropValue 構造体。</span><span class="sxs-lookup"><span data-stu-id="a4001-156">**SPropValue** structure for the **PR_INSTANCE_KEY** property of the row before the affected one.</span></span> <span data-ttu-id="a4001-157">影響を受ける行が表の最初の行である場合 **、propPrior** は 0 ではなく、PR_NULL **に設定** する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a4001-157">If the affected row is the first row in the table, **propPrior** must be set to **PR_NULL** and not zero.</span></span> <span data-ttu-id="a4001-158">ゼロは有効なプロパティ タグではありません。</span><span class="sxs-lookup"><span data-stu-id="a4001-158">Zero is not a valid property tag.</span></span> 
    
<span data-ttu-id="a4001-159">**row**</span><span class="sxs-lookup"><span data-stu-id="a4001-159">**row**</span></span>
  
> <span data-ttu-id="a4001-160">[影響を受](srow.md) ける行を記述する SRow 構造体。</span><span class="sxs-lookup"><span data-stu-id="a4001-160">[SRow](srow.md) structure describing the affected row.</span></span> <span data-ttu-id="a4001-161">この構造は、すべてのテーブル通知イベントに対して入力されます。</span><span class="sxs-lookup"><span data-stu-id="a4001-161">This structure is filled for all table notification events.</span></span> <span data-ttu-id="a4001-162">行データを渡していないテーブル通知イベントの場合 **、SRow** 構造体の **cValues** メンバーは 0 に設定され **、lpProps** メンバーは NULL に設定されます。</span><span class="sxs-lookup"><span data-stu-id="a4001-162">For table notification events that do not pass row data, the **cValues** member of the **SRow** structure is set to zero and the **lpProps** member is set to NULL.</span></span> <span data-ttu-id="a4001-163">この **SRow 構造体は** 読み取り専用のためです。クライアントが変更を行う場合は、そのコピーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a4001-163">Because this **SRow** structure is read-only; clients must make a copy of it if they want to make modifications.</span></span> <span data-ttu-id="a4001-164">[ScDupPropset 関数](scduppropset.md)を使用してコピーを作成できます。</span><span class="sxs-lookup"><span data-stu-id="a4001-164">The [ScDupPropset](scduppropset.md) function can be used to make the copy.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a4001-165">注釈</span><span class="sxs-lookup"><span data-stu-id="a4001-165">Remarks</span></span>

<span data-ttu-id="a4001-166">**TABLE \_ NOTIFICATION 構造体** は、NOTIFICATION 構造体の info メンバーに含まれる構造体の共用体のメンバーの [1](notification.md)つです。 </span><span class="sxs-lookup"><span data-stu-id="a4001-166">The **TABLE\_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="a4001-167">info **メンバー** には、構造体の **ulEventType** メンバーが _fnevTableModified_ に設定されている場合に TABLE NOTIFICATION 構造が含まれます。 **\_**</span><span class="sxs-lookup"><span data-stu-id="a4001-167">The **info** member includes a **TABLE\_NOTIFICATION** structure when the **ulEventType** member of the structure is set to  _fnevTableModified_.</span></span>
  
<span data-ttu-id="a4001-168">行メンバーの列の順序と種類は、通知が生成された時点で有効だった順序と種類を反映します。</span><span class="sxs-lookup"><span data-stu-id="a4001-168">The order and type of columns in the row member reflect the order and type that was in effect at the time that the notification was generated.</span></span> <span data-ttu-id="a4001-169">通知が生成された時点での順序と種類は、通知が配信された場合と必ずしも同じではありません。</span><span class="sxs-lookup"><span data-stu-id="a4001-169">The order and type at the time that the notification was generated is not necessarily the same as when the notification was delivered.</span></span> 
  
<span data-ttu-id="a4001-170">通知の詳細については、次の表で説明するトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a4001-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="a4001-171">**トピック**</span><span class="sxs-lookup"><span data-stu-id="a4001-171">**Topic**</span></span>|<span data-ttu-id="a4001-172">**説明**</span><span class="sxs-lookup"><span data-stu-id="a4001-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a4001-173">MAPI のイベント通知</span><span class="sxs-lookup"><span data-stu-id="a4001-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="a4001-174">通知イベントと通知イベントの一般的な概要。</span><span class="sxs-lookup"><span data-stu-id="a4001-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="a4001-175">通知の処理</span><span class="sxs-lookup"><span data-stu-id="a4001-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="a4001-176">クライアントが通知を処理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a4001-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="a4001-177">サポート イベント通知</span><span class="sxs-lookup"><span data-stu-id="a4001-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="a4001-178">サービス プロバイダーが **IMAPISupport** メソッドを使用して通知を生成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a4001-178">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
<span data-ttu-id="a4001-179">テーブル通知は非同期なので、クライアントは別の方法で追加について学習した後、追加された行の通知を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="a4001-179">Because table notifications are asynchronous, clients can receive notification of an added row after learning about the addition through another means.</span></span> <span data-ttu-id="a4001-180">**IMAPITable::Sort** **、IMAPITable::Restrict、または** **IMAPITable::SetColumns** メソッドでエラーが発生した場合、または基になるプロセスが新しい行や変更された行を含むテーブルを更新しようとすると、TABLE_ERROR イベントを受け取る可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a4001-180">It is possible to receive a TABLE_ERROR event when there is an error in an **IMAPITable::Sort**, **IMAPITable::Restrict**, or **IMAPITable::SetColumns** method or when an underlying process attempts to update a table with, for example, new or modified rows.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a4001-181">関連項目</span><span class="sxs-lookup"><span data-stu-id="a4001-181">See also</span></span>

- [<span data-ttu-id="a4001-182">�ʒm</span><span class="sxs-lookup"><span data-stu-id="a4001-182">NOTIFICATION</span></span>](notification.md) 
- [<span data-ttu-id="a4001-183">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="a4001-183">ScDupPropset</span></span>](scduppropset.md)
- [<span data-ttu-id="a4001-184">SRow</span><span class="sxs-lookup"><span data-stu-id="a4001-184">SRow</span></span>](srow.md)
- [<span data-ttu-id="a4001-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="a4001-185">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="a4001-186">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="a4001-186">MAPI Structures</span></span>](mapi-structures.md)

