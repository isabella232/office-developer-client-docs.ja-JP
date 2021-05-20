---
title: メッセージ ストアを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 43b23fd7-999a-42c0-8f4d-47f5de266bdb
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 665c14b285db166e4f2a421d46e57f23e2f7ad52
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432374"
---
# <a name="opening-a-message-store"></a><span data-ttu-id="0e010-103">メッセージ ストアを開く</span><span class="sxs-lookup"><span data-stu-id="0e010-103">Opening a message store</span></span>

<span data-ttu-id="0e010-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e010-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e010-105">プロファイルによっては、クライアントは一般的なセッション中に 1 つ以上のメッセージ ストアを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e010-105">Depending on the profile, a client will need to open one or more message stores during a typical session.</span></span> <span data-ttu-id="0e010-106">メッセージ ストアを開くとは、 [その IMsgStore : IMAPIProp](imsgstoreimapiprop.md) 実装へのポインターへのアクセスを得るという意味です。</span><span class="sxs-lookup"><span data-stu-id="0e010-106">Opening a message store means gaining access to a pointer to its [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) implementation.</span></span> <span data-ttu-id="0e010-107">**IMsgStore インターフェイスには**、通知、フォルダーの割り当て、フォルダーとメッセージへのアクセスのためのメソッドが提供されます。</span><span class="sxs-lookup"><span data-stu-id="0e010-107">The **IMsgStore** interface provides methods for notification, making folder assignments, and accessing folders and messages.</span></span> 
  
<span data-ttu-id="0e010-108">クライアントは、ログオン時とプロファイルの変更時にメッセージ ストアを開きます。</span><span class="sxs-lookup"><span data-stu-id="0e010-108">Clients open message stores at logon and when a profile is being modified.</span></span> <span data-ttu-id="0e010-109">クライアントがアクティブ セッション中にユーザーがプロファイルにメッセージ ストアを追加することを許可している場合は、すぐに開くか、次のセッションまで無視できます。</span><span class="sxs-lookup"><span data-stu-id="0e010-109">If your client allows users to add message stores to the profile during an active session, you can either open them immediately or ignore them until the next session.</span></span> <span data-ttu-id="0e010-110">メッセージ ストア テーブルに通知を登録すると、新しいメッセージ ストアの可用性が通知されます。</span><span class="sxs-lookup"><span data-stu-id="0e010-110">By registering for notifications on the message store table, you will be alerted to the availability of a new message store.</span></span>
  
<span data-ttu-id="0e010-111">メッセージ ストアを開くには、そのエントリ識別子を使用できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e010-111">To open a message store, you must have its entry identifier available.</span></span> <span data-ttu-id="0e010-112">ほとんどのクライアントは、メッセージ ストア テーブルから開くメッセージ ストアのエントリ識別子にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="0e010-112">Most clients access the entry identifiers for the message stores they wish to open through the message store table.</span></span> <span data-ttu-id="0e010-113">ただし、一部のメッセージ ストアでは、エントリ識別子の形式を文書化するため、クライアントはメッセージ ストア テーブルをバイパスして、必要なエントリ識別子を構築できます。</span><span class="sxs-lookup"><span data-stu-id="0e010-113">However, some message stores document the format of their entry identifiers, thereby enabling clients to bypass the message store table and construct the necessary entry identifier.</span></span> <span data-ttu-id="0e010-114">このエントリ識別子を [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) に直接渡し、MAPI はメッセージ サービスに関連付けずにプロバイダーのプロファイル セクションを自動的に作成します。</span><span class="sxs-lookup"><span data-stu-id="0e010-114">They can pass this entry identifier directly to [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) and MAPI automatically creates a profile section for the provider without associating it with any message service.</span></span> 
  
## <a name="retrieve-an-entry-identifier-from-the-message-store-table"></a><span data-ttu-id="0e010-115">メッセージ ストア テーブルからエントリ識別子を取得する</span><span class="sxs-lookup"><span data-stu-id="0e010-115">Retrieve an entry identifier from the message store table</span></span>
  
1. <span data-ttu-id="0e010-116">[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)を呼び出して、メッセージ ストア テーブルを開きます。</span><span class="sxs-lookup"><span data-stu-id="0e010-116">Call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to open the message store table.</span></span> 
    
2. <span data-ttu-id="0e010-117">**IMAPITable::SetColumns** を呼び出して、テーブルを次の列を含む小さな列セットに制限します。</span><span class="sxs-lookup"><span data-stu-id="0e010-117">Call **IMAPITable::SetColumns** to limit the table to a small column set that includes the following columns:</span></span> 
    
   - <span data-ttu-id="0e010-118">**PR_PROVIDER_DISPLAY** または **PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="0e010-118">**PR_PROVIDER_DISPLAY** or **PR_DISPLAY_NAME**</span></span>
   - <span data-ttu-id="0e010-119">**PR_ENTRYID** プロパティ</span><span class="sxs-lookup"><span data-stu-id="0e010-119">**PR_ENTRYID** properties</span></span> 
   - <span data-ttu-id="0e010-120">**PR_MDB_PROVIDER**</span><span class="sxs-lookup"><span data-stu-id="0e010-120">**PR_MDB_PROVIDER**</span></span>
   - <span data-ttu-id="0e010-121">**PR_RESOURCE_FLAGS**</span><span class="sxs-lookup"><span data-stu-id="0e010-121">**PR_RESOURCE_FLAGS**</span></span>
    
3. <span data-ttu-id="0e010-122">開くメッセージ ストアを表す行をフィルター処理する制限を作成します。</span><span class="sxs-lookup"><span data-stu-id="0e010-122">Build a restriction to filter out the row that represents the message store to be opened.</span></span> <span data-ttu-id="0e010-123">既定のメッセージ ストアを探す方法の詳細については、「既定のメッセージ ストアを開 [く」を参照してください](opening-the-default-message-store.md)。</span><span class="sxs-lookup"><span data-stu-id="0e010-123">For more information about looking for the default message store, see [Opening the Default Message Store](opening-the-default-message-store.md).</span></span> <span data-ttu-id="0e010-124">名前でメッセージ ストアを検索するには、次のプロパティ制限を適用します。</span><span class="sxs-lookup"><span data-stu-id="0e010-124">To look for a message store by name, apply any of the following property restrictions:</span></span>
    
   - <span data-ttu-id="0e010-125">この **PR_PROVIDER_DISPLAY** [(PidTagProviderDisplay)](pidtagproviderdisplay-canonical-property.md)とこの種類のメッセージ ストアの一般的な名前を一致します。</span><span class="sxs-lookup"><span data-stu-id="0e010-125">Match **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) with the general name for this type of message store.</span></span> <span data-ttu-id="0e010-126">たとえば、ユーザー PR_PROVIDER_DISPLAY "個人用フォルダー" に設定できます。</span><span class="sxs-lookup"><span data-stu-id="0e010-126">For example, PR_PROVIDER_DISPLAY might be set to "Personal Folders".</span></span>
    
   - <span data-ttu-id="0e010-127">この **PR_MDB_PROVIDER** の **MAPIUID** と一致するメッセージ ストア ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) を指定します。</span><span class="sxs-lookup"><span data-stu-id="0e010-127">Match **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) with the specific **MAPIUID** for this type of message store.</span></span> 
    
   - <span data-ttu-id="0e010-128">この **PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)とこの特定のメッセージ ストアの名前を一致します。</span><span class="sxs-lookup"><span data-stu-id="0e010-128">Match **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) with the name for this particular message store.</span></span> <span data-ttu-id="0e010-129">たとえば、PR_DISPLAY_NAME"2010 会計年度のマイ メッセージ" に設定できます。 </span><span class="sxs-lookup"><span data-stu-id="0e010-129">For example, **PR_DISPLAY_NAME** might be set to "My Messages for Fiscal Year 2010."</span></span> 
    
4. <span data-ttu-id="0e010-130">[HrQueryAllRows を呼び出](hrqueryallrows.md)して、メッセージ ストア テーブルから適切な行を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e010-130">Call [HrQueryAllRows](hrqueryallrows.md) to retrieve the appropriate row from the message store table.</span></span> <span data-ttu-id="0e010-131">行のエントリ識別子は _、pprows_ パラメーターが指す行セットの **aRow** メンバーのプロパティ値配列に含まれます。</span><span class="sxs-lookup"><span data-stu-id="0e010-131">The entry identifier for the row will be included in the property value array for the **aRow** member of the row set pointed to by the  _pprows_ parameter.</span></span> 
    
5. <span data-ttu-id="0e010-132">[FreeProws を呼び出](freeprows.md)して、pprows が指す行セット _を解放します_。</span><span class="sxs-lookup"><span data-stu-id="0e010-132">Call [FreeProws](freeprows.md) to free the row set pointed to by  _pprows_.</span></span>
    
6. <span data-ttu-id="0e010-133">メッセージ ストア テーブルを解放するには、 **その IUnknown::Release メソッドを呼び出** します。</span><span class="sxs-lookup"><span data-stu-id="0e010-133">Release the message store table by calling its **IUnknown::Release** method.</span></span> 
    
<span data-ttu-id="0e010-134">開くメッセージ ストアのカスタム エントリ識別子を作成した場合は [、WrapStoreEntryID](wrapstoreentryid.md) 関数を呼び出して、標準エントリ識別子に変換します。</span><span class="sxs-lookup"><span data-stu-id="0e010-134">If you have created a custom entry identifier for the message store to be opened, call the [WrapStoreEntryID](wrapstoreentryid.md) function to convert it to a standard entry identifier.</span></span> 
  
<span data-ttu-id="0e010-135">メッセージ ストアのエントリ識別子を取得した後、次のいずれかのメソッドを呼び出して開きます。</span><span class="sxs-lookup"><span data-stu-id="0e010-135">After you have a message store's entry identifier, call one of the following methods to open it:</span></span>
  
- [<span data-ttu-id="0e010-136">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="0e010-136">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
- [<span data-ttu-id="0e010-137">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="0e010-137">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
    
<span data-ttu-id="0e010-138">メッセージ ストアのさまざまな特別なオプションを指定する必要がある場合は **、OpenMsgStore** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0e010-138">Call **OpenMsgStore** if you need to specify a variety of special options for the message store.</span></span> <span data-ttu-id="0e010-139">**OpenMsgStore** を使用すると、ダイアログ ボックスの表示を抑制し、メッセージ ストアを一時的なストアまたは非メッシュ ストアとして識別し、アクセス レベルを設定し、エラーを延期できます。</span><span class="sxs-lookup"><span data-stu-id="0e010-139">**OpenMsgStore** allows you to suppress the display of dialog boxes, identify the message store as temporary or as a nonmessaging store, set access levels, and to defer errors.</span></span> <span data-ttu-id="0e010-140">**OpenEntry では** 、アクセス レベルの設定とエラーの延期のみを行います。</span><span class="sxs-lookup"><span data-stu-id="0e010-140">**OpenEntry** allows you only to set access levels and defer errors.</span></span> 
  
<span data-ttu-id="0e010-141">メッセージ のMDB_NO_MAIL設定すると、メッセージ ストアはメッセージの送受信に使用されません。</span><span class="sxs-lookup"><span data-stu-id="0e010-141">Setting the MDB_NO_MAIL flag indicates to MAPI that the message store will not be used for sending or receiving messages.</span></span> <span data-ttu-id="0e010-142">MAPI では、このメッセージ ストアの存在について MAPI スプーラーには通知されません。</span><span class="sxs-lookup"><span data-stu-id="0e010-142">MAPI does not inform the MAPI spooler about the existence of this message store.</span></span> <span data-ttu-id="0e010-143">このMDB_TEMPORARYは、メッセージ ストアを一時的なものとして指定します。これは、永続的な情報を格納するために使用できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="0e010-143">The MDB_TEMPORARY flag designates a message store as temporary, implying that it cannot be used to store permanent information.</span></span> <span data-ttu-id="0e010-144">一時メッセージ ストアは、メッセージ ストア テーブルには表示されません。</span><span class="sxs-lookup"><span data-stu-id="0e010-144">Temporary message stores do not appear in the message store table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0e010-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="0e010-145">See also</span></span>

- [<span data-ttu-id="0e010-146">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="0e010-146">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)

