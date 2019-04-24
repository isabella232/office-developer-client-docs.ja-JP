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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326223"
---
# <a name="opening-a-message-store"></a><span data-ttu-id="d254e-103">メッセージ ストアを開く</span><span class="sxs-lookup"><span data-stu-id="d254e-103">Opening a message store</span></span>

<span data-ttu-id="d254e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d254e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d254e-105">プロファイルに応じて、クライアントは一般的なセッション中に1つ以上のメッセージストアを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="d254e-105">Depending on the profile, a client will need to open one or more message stores during a typical session.</span></span> <span data-ttu-id="d254e-106">メッセージストアを開くことは、 [IMsgStore: imapiprop](imsgstoreimapiprop.md)実装へのポインターへのアクセスを得ることを意味します。</span><span class="sxs-lookup"><span data-stu-id="d254e-106">Opening a message store means gaining access to a pointer to its [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) implementation.</span></span> <span data-ttu-id="d254e-107">**IMsgStore**インターフェイスには、通知、フォルダー割り当ての作成、およびフォルダーとメッセージへのアクセスのためのメソッドが用意されています。</span><span class="sxs-lookup"><span data-stu-id="d254e-107">The **IMsgStore** interface provides methods for notification, making folder assignments, and accessing folders and messages.</span></span> 
  
<span data-ttu-id="d254e-108">クライアントは、ログオン時、およびプロファイルが変更されるときに、メッセージストアを開きます。</span><span class="sxs-lookup"><span data-stu-id="d254e-108">Clients open message stores at logon and when a profile is being modified.</span></span> <span data-ttu-id="d254e-109">クライアントで、アクティブなセッション中にユーザーがプロファイルにメッセージストアを追加できるようにする場合は、それらをすぐに開くか、または次のセッションまで無視できます。</span><span class="sxs-lookup"><span data-stu-id="d254e-109">If your client allows users to add message stores to the profile during an active session, you can either open them immediately or ignore them until the next session.</span></span> <span data-ttu-id="d254e-110">メッセージストアテーブルに通知を登録することによって、新しいメッセージストアの可用性に関する警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d254e-110">By registering for notifications on the message store table, you will be alerted to the availability of a new message store.</span></span>
  
<span data-ttu-id="d254e-111">メッセージストアを開くには、そのエントリ識別子を使用できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d254e-111">To open a message store, you must have its entry identifier available.</span></span> <span data-ttu-id="d254e-112">ほとんどのクライアントは、メッセージストアテーブルを使用して開くメッセージストアのエントリ識別子にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="d254e-112">Most clients access the entry identifiers for the message stores they wish to open through the message store table.</span></span> <span data-ttu-id="d254e-113">ただし、メッセージストアによっては、エントリ識別子の形式が文書化されているため、クライアントがメッセージストアテーブルをバイパスし、必要なエントリ識別子を作成できるようになります。</span><span class="sxs-lookup"><span data-stu-id="d254e-113">However, some message stores document the format of their entry identifiers, thereby enabling clients to bypass the message store table and construct the necessary entry identifier.</span></span> <span data-ttu-id="d254e-114">このエントリ識別子を[imapisession:: openmsgstore](imapisession-openmsgstore.md)に直接渡すことができます。また、MAPI は、メッセージサービスに関連付けずにプロバイダーのプロファイルセクションを自動的に作成します。</span><span class="sxs-lookup"><span data-stu-id="d254e-114">They can pass this entry identifier directly to [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) and MAPI automatically creates a profile section for the provider without associating it with any message service.</span></span> 
  
## <a name="retrieve-an-entry-identifier-from-the-message-store-table"></a><span data-ttu-id="d254e-115">メッセージストアテーブルからエントリ識別子を取得する</span><span class="sxs-lookup"><span data-stu-id="d254e-115">Retrieve an entry identifier from the message store table</span></span>
  
1. <span data-ttu-id="d254e-116">呼び出し[imapisession:: getmsgstorestable](imapisession-getmsgstorestable.md)メッセージストアテーブルを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="d254e-116">Call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to open the message store table.</span></span> 
    
2. <span data-ttu-id="d254e-117">**IMAPITable:: SetColumns**を呼び出して、テーブルを次の列を含む小さな列セットに制限します。</span><span class="sxs-lookup"><span data-stu-id="d254e-117">Call **IMAPITable::SetColumns** to limit the table to a small column set that includes the following columns:</span></span> 
    
   - <span data-ttu-id="d254e-118">**PR_PROVIDER_DISPLAY**または**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="d254e-118">**PR_PROVIDER_DISPLAY** or **PR_DISPLAY_NAME**</span></span>
   - <span data-ttu-id="d254e-119">**PR_ENTRYID**プロパティ</span><span class="sxs-lookup"><span data-stu-id="d254e-119">**PR_ENTRYID** properties</span></span> 
   - <span data-ttu-id="d254e-120">**PR_MDB_PROVIDER**</span><span class="sxs-lookup"><span data-stu-id="d254e-120">**PR_MDB_PROVIDER**</span></span>
   - <span data-ttu-id="d254e-121">**PR_RESOURCE_FLAGS**</span><span class="sxs-lookup"><span data-stu-id="d254e-121">**PR_RESOURCE_FLAGS**</span></span>
    
3. <span data-ttu-id="d254e-122">開くメッセージストアを表す行をフィルターで除外する制限を作成します。</span><span class="sxs-lookup"><span data-stu-id="d254e-122">Build a restriction to filter out the row that represents the message store to be opened.</span></span> <span data-ttu-id="d254e-123">既定のメッセージストアの検索の詳細については、「[既定のメッセージストアを開く](opening-the-default-message-store.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d254e-123">For more information about looking for the default message store, see [Opening the Default Message Store](opening-the-default-message-store.md).</span></span> <span data-ttu-id="d254e-124">名前でメッセージストアを検索するには、次のいずれかのプロパティ制限を適用します。</span><span class="sxs-lookup"><span data-stu-id="d254e-124">To look for a message store by name, apply any of the following property restrictions:</span></span>
    
   - <span data-ttu-id="d254e-125">この種類のメッセージストアの一般的な名前を**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) と照合します。</span><span class="sxs-lookup"><span data-stu-id="d254e-125">Match **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) with the general name for this type of message store.</span></span> <span data-ttu-id="d254e-126">たとえば、PR_PROVIDER_DISPLAY は "個人用フォルダー" に設定されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="d254e-126">For example, PR_PROVIDER_DISPLAY might be set to "Personal Folders".</span></span>
    
   - <span data-ttu-id="d254e-127">この種類のメッセージストアについて、 **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) を特定の**MAPIUID**に一致させます。</span><span class="sxs-lookup"><span data-stu-id="d254e-127">Match **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) with the specific **MAPIUID** for this type of message store.</span></span> 
    
   - <span data-ttu-id="d254e-128">この特定のメッセージストアの名前を**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) と照合します。</span><span class="sxs-lookup"><span data-stu-id="d254e-128">Match **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) with the name for this particular message store.</span></span> <span data-ttu-id="d254e-129">たとえば、 **PR_DISPLAY_NAME**は "私のメッセージは会計年度 2010" に設定されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="d254e-129">For example, **PR_DISPLAY_NAME** might be set to "My Messages for Fiscal Year 2010."</span></span> 
    
4. <span data-ttu-id="d254e-130">[hrqueryallrows](hrqueryallrows.md)を呼び出して、メッセージストアテーブルから適切な行を取得します。</span><span class="sxs-lookup"><span data-stu-id="d254e-130">Call [HrQueryAllRows](hrqueryallrows.md) to retrieve the appropriate row from the message store table.</span></span> <span data-ttu-id="d254e-131">_pprows_パラメーターによって指定された行セットの arow \*\*\*\* member メンバーのプロパティ値配列に、その行のエントリ識別子が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d254e-131">The entry identifier for the row will be included in the property value array for the **aRow** member of the row set pointed to by the  _pprows_ parameter.</span></span> 
    
5. <span data-ttu-id="d254e-132">[freeprows](freeprows.md)を呼び出して、 _pprows_が指す行セットを解放します。</span><span class="sxs-lookup"><span data-stu-id="d254e-132">Call [FreeProws](freeprows.md) to free the row set pointed to by  _pprows_.</span></span>
    
6. <span data-ttu-id="d254e-133">**IUnknown:: release**メソッドを呼び出して、メッセージストアテーブルを解放します。</span><span class="sxs-lookup"><span data-stu-id="d254e-133">Release the message store table by calling its **IUnknown::Release** method.</span></span> 
    
<span data-ttu-id="d254e-134">メッセージストアを開くためのカスタムエントリ識別子を作成した場合は、 [WrapStoreEntryID](wrapstoreentryid.md)関数を呼び出して標準のエントリ識別子に変換します。</span><span class="sxs-lookup"><span data-stu-id="d254e-134">If you have created a custom entry identifier for the message store to be opened, call the [WrapStoreEntryID](wrapstoreentryid.md) function to convert it to a standard entry identifier.</span></span> 
  
<span data-ttu-id="d254e-135">メッセージストアのエントリ識別子を取得したら、次のいずれかのメソッドを呼び出して開きます。</span><span class="sxs-lookup"><span data-stu-id="d254e-135">After you have a message store's entry identifier, call one of the following methods to open it:</span></span>
  
- [<span data-ttu-id="d254e-136">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="d254e-136">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
- [<span data-ttu-id="d254e-137">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="d254e-137">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
    
<span data-ttu-id="d254e-138">メッセージストアにさまざまな特別なオプションを指定する必要がある場合は、 **openmsgstore**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d254e-138">Call **OpenMsgStore** if you need to specify a variety of special options for the message store.</span></span> <span data-ttu-id="d254e-139">**openmsgstore**を使用すると、ダイアログボックスの表示を抑制したり、メッセージストアを一時的または非メッセージングストアとして指定したり、アクセスレベルを設定したり、エラーを遅延させたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="d254e-139">**OpenMsgStore** allows you to suppress the display of dialog boxes, identify the message store as temporary or as a nonmessaging store, set access levels, and to defer errors.</span></span> <span data-ttu-id="d254e-140">**openentry**では、アクセスレベルを設定したり、エラーを遅延させることができます。</span><span class="sxs-lookup"><span data-stu-id="d254e-140">**OpenEntry** allows you only to set access levels and defer errors.</span></span> 
  
<span data-ttu-id="d254e-141">MDB_NO_MAIL フラグを設定すると、メッセージストアがメッセージの送信または受信に使用されないことを MAPI に示します。</span><span class="sxs-lookup"><span data-stu-id="d254e-141">Setting the MDB_NO_MAIL flag indicates to MAPI that the message store will not be used for sending or receiving messages.</span></span> <span data-ttu-id="d254e-142">mapi は、このメッセージストアが存在することを mapi スプーラーに通知しません。</span><span class="sxs-lookup"><span data-stu-id="d254e-142">MAPI does not inform the MAPI spooler about the existence of this message store.</span></span> <span data-ttu-id="d254e-143">MDB_TEMPORARY フラグは、メッセージストアを一時的なものとして指定します。これは永続的な情報を格納するためには使用できません。</span><span class="sxs-lookup"><span data-stu-id="d254e-143">The MDB_TEMPORARY flag designates a message store as temporary, implying that it cannot be used to store permanent information.</span></span> <span data-ttu-id="d254e-144">一時メッセージストアは、メッセージストアテーブルには表示されません。</span><span class="sxs-lookup"><span data-stu-id="d254e-144">Temporary message stores do not appear in the message store table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d254e-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="d254e-145">See also</span></span>

- [<span data-ttu-id="d254e-146">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="d254e-146">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)

