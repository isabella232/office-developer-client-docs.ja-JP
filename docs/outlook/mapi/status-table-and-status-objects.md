---
title: 状態テーブルとオブジェクトの状態
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 203765c1-4b08-4032-a5bf-18f3e752a899
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 774aaea0365066981b9d6426a2579160f6578844
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804008"
---
# <a name="status-table-and-status-objects"></a><span data-ttu-id="eb01b-103">状態テーブルとオブジェクトの状態</span><span class="sxs-lookup"><span data-stu-id="eb01b-103">Status Table and Status Objects</span></span>

  
  
<span data-ttu-id="eb01b-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eb01b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="eb01b-105">MAPI は MAPI のサブシステム、MAPI スプーラー、アドレス帳、または特定のサービス プロバイダーのステータスに関する情報を持つテーブルを提供します。</span><span class="sxs-lookup"><span data-stu-id="eb01b-105">MAPI provides a table with information about the status of the MAPI subsystem, MAPI spooler, address book, or a particular service provider.</span></span> <span data-ttu-id="eb01b-106">[IMAPISession::GetStatusTable](imapisession-getstatustable.md)を呼び出すことによってこのテーブルにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="eb01b-106">You can access this table by calling [IMAPISession::GetStatusTable](imapisession-getstatustable.md).</span></span>
  
<span data-ttu-id="eb01b-107">状態テーブル内の各行は、MAPI またはサービス プロバイダーによって実装される状態オブジェクトを表します。</span><span class="sxs-lookup"><span data-stu-id="eb01b-107">Each row in the status table represents a status object implemented by MAPI or a service provider.</span></span> <span data-ttu-id="eb01b-108">アップロードまたはメッセージをダウンロードしてのに、特定のトランスポート プロバイダーと通信するのにプロバイダーのパスワードを変更するのには、プロバイダーの設定] プロパティ シートを表示するのには、状態オブジェクトを使用できます。</span><span class="sxs-lookup"><span data-stu-id="eb01b-108">You can use a status object to display a provider's configuration property sheet, to change a provider password, to upload or download messages, and to communicate with a particular transport provider.</span></span> 
  
<span data-ttu-id="eb01b-109">状態オブジェクトにアクセスするための 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="eb01b-109">There are two ways to access a status object:</span></span>
  
- <span data-ttu-id="eb01b-110">状態テーブルを</span><span class="sxs-lookup"><span data-stu-id="eb01b-110">Through the status table</span></span>
    
- <span data-ttu-id="eb01b-111">ログオン オブジェクトの**OpenStatusEntry**メソッドを使用</span><span class="sxs-lookup"><span data-stu-id="eb01b-111">Through a logon object's **OpenStatusEntry** method</span></span> 
    
<span data-ttu-id="eb01b-112">ログオン オブジェクトがクライアントに使用可能なため、状態オブジェクトにアクセスするのにはステータス ・ テーブルを使わなければなりません。</span><span class="sxs-lookup"><span data-stu-id="eb01b-112">Because logon objects are unavailable to clients, you must use the status table to access status objects.</span></span> <span data-ttu-id="eb01b-113">状態テーブルのアプローチは、いくつかの呼び出しを必要とする状態オブジェクトが開かれ、その**IMAPIStatus**実装へのポインターが返される前に、直接ではありません。</span><span class="sxs-lookup"><span data-stu-id="eb01b-113">The status table approach is indirect, requiring a few calls before the status object is opened and a pointer to its **IMAPIStatus** implementation returned.</span></span> 
  
 <span data-ttu-id="eb01b-114">**開くには、状態オブジェクトの状態テーブルを使用するには**</span><span class="sxs-lookup"><span data-stu-id="eb01b-114">**To use the status table to open a status object**</span></span>
  
1. <span data-ttu-id="eb01b-115">[IMAPITable](imapitableiunknown.md)ポインターを取得するために**IMAPIStatus::GetStatusTable**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="eb01b-115">Call **IMAPIStatus::GetStatusTable** to retrieve an [IMAPITable](imapitableiunknown.md) pointer.</span></span> 
    
2. <span data-ttu-id="eb01b-116">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))、 **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) および**PR_DISPLAY_NAME** ([に設定する列を制限するのには、状態テーブルの[IMAPITable::SetColumns](imapitable-setcolumns.md)メソッドを呼び出すPidTagDisplayName](pidtagdisplayname-canonical-property.md))。</span><span class="sxs-lookup"><span data-stu-id="eb01b-116">Call the status table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)), and **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="eb01b-117">特定のステータスのオブジェクトをテーブルのビューを制限します。</span><span class="sxs-lookup"><span data-stu-id="eb01b-117">Limit the table view to a particular status object.</span></span> <span data-ttu-id="eb01b-118">MAPI 実装では、クライアントは**PR_RESOURCE_TYPE**を使用してプロパティの制限を定義できます。</span><span class="sxs-lookup"><span data-stu-id="eb01b-118">For MAPI implementations, a client can define a property restriction using **PR_RESOURCE_TYPE**.</span></span> <span data-ttu-id="eb01b-119">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))、プロバイダーの名前や**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) は、プロバイダーの DLL の名前サービス プロバイダー実装では、クライアントを制限することができます。ファイルです。</span><span class="sxs-lookup"><span data-stu-id="eb01b-119">For service provider implementations, a client can restrict on **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)), the name of the provider, or on **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)), the name of the provider DLL file.</span></span>
    
4. <span data-ttu-id="eb01b-120">制限を設定するのには[IMAPITable::Restrict](imapitable-restrict.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="eb01b-120">Call [IMAPITable::Restrict](imapitable-restrict.md) to set the restriction.</span></span> 
    
5. <span data-ttu-id="eb01b-121">[HrQueryAllRows](hrqueryallrows.md)、 [SPropertyRestriction](spropertyrestriction.md)構造体を渡すことを呼び出し、プロバイダーの状態を表す行を取得します。</span><span class="sxs-lookup"><span data-stu-id="eb01b-121">Call [HrQueryAllRows](hrqueryallrows.md), passing in the [SPropertyRestriction](spropertyrestriction.md) structure, to retrieve the row that represents the status of the provider.</span></span> 
    
6. <span data-ttu-id="eb01b-122">[IMAPISession::OpenEntry](imapisession-openentry.md)、状態テーブルの行からのエントリ id を指定する状態オブジェクトを開き、 **IMAPIStatus**ポインターを取得するを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="eb01b-122">Call [IMAPISession::OpenEntry](imapisession-openentry.md), specifying the entry identifier from the status table row, to open the status object and retrieve an **IMAPIStatus** pointer.</span></span> 
    
<span data-ttu-id="eb01b-123">プロパティ シートを表示するには、対象のプロバイダーの状態のオブジェクトの[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="eb01b-123">To display a property sheet, call the status object's [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method for the target provider.</span></span> <span data-ttu-id="eb01b-124">**SettingsDialog**では、プロバイダーの構成のプロパティを変更する表示のため、場合によっては、プロパティ シートを表示します。</span><span class="sxs-lookup"><span data-stu-id="eb01b-124">**SettingsDialog** displays a property sheet for viewing and in some cases, changing the configuration properties of a provider.</span></span> 
  
<span data-ttu-id="eb01b-125">トランスポート プロバイダーとの通信をするには、その状態のオブジェクトの[IMAPIStatus::ValidateState](imapistatus-validatestate.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="eb01b-125">To communicate with a transport provider, call its status object's [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="eb01b-126">**ValidateState**は、トランスポート プロバイダーを再構成品を獲得し、プロバイダーが、ユーザー インターフェイスを表示しないようにするに渡されるフラグの設定により、リモート サーバーからのメッセージ ヘッダーのダウンロードに関連するセッションを制御できます。</span><span class="sxs-lookup"><span data-stu-id="eb01b-126">**ValidateState** can reconfigure a transport provider, prevent the provider from displaying a user interface, and control a session that involves downloading message headers from a remote server, depending on the flags that you pass in.</span></span> <span data-ttu-id="eb01b-127">たとえば、リモート ヘッダーのダウンロードをキャンセルするには、 **ValidateState**に ABORT_XP_HEADER_OPERATION フラグを渡します。</span><span class="sxs-lookup"><span data-stu-id="eb01b-127">For example, to cancel the downloading of remote headers, pass the ABORT_XP_HEADER_OPERATION flag to **ValidateState**.</span></span> <span data-ttu-id="eb01b-128">リモート サーバーから切断、または接続するには、FORCE_XP_CONNECT または FORCE_XP_DISCONNECT を渡します。</span><span class="sxs-lookup"><span data-stu-id="eb01b-128">To connect or disconnect from the remote server, pass FORCE_XP_CONNECT or FORCE_XP_DISCONNECT.</span></span> <span data-ttu-id="eb01b-129">プロバイダーを再設定するには、CONFIG_CHANGED を渡します。</span><span class="sxs-lookup"><span data-stu-id="eb01b-129">To reconfigure the provider, pass CONFIG_CHANGED.</span></span> 
  
<span data-ttu-id="eb01b-130">要求時にメッセージの送信または受信を実装するクライアントは、トランスポート プロバイダーのまたは MAPI スプーラーのいずれかの[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="eb01b-130">Clients that implement sending or receiving of messages on demand call either a transport provider's or the MAPI spooler's [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method.</span></span> <span data-ttu-id="eb01b-131">メソッドに 3 つのフラグを渡すことができます: FLUSH_UPLOAD、FLUSH_DOWNLOAD、および FLUSH_FORCE。</span><span class="sxs-lookup"><span data-stu-id="eb01b-131">You can pass three flags into the method: FLUSH_UPLOAD, FLUSH_DOWNLOAD, and FLUSH_FORCE.</span></span> <span data-ttu-id="eb01b-132">FLUSH_UPLOAD は、着信メッセージを受信するプロバイダーまたは FLUSH_DOWNLOAD プロバイダーを指示するときに、出力キューで待機しているすべてのメッセージを送信するのには、MAPI スプーラーを無効、または MAPI スプーラーに指示します。</span><span class="sxs-lookup"><span data-stu-id="eb01b-132">FLUSH_UPLOAD instructs the provider or the MAPI spooler to send any messages waiting in the output queue while FLUSH_DOWNLOAD instructs the provider or the MAPI spooler to receive any incoming messages.</span></span> <span data-ttu-id="eb01b-133">FLUSH_FORCE は、タイミングに関係なく、フラッシュを実行する状態オブジェクトが発生する他のフラグのいずれかを設定できます。</span><span class="sxs-lookup"><span data-stu-id="eb01b-133">FLUSH_FORCE can be set with either of the other flags to cause the status object to perform the flush regardless of the timing.</span></span> 
  
<span data-ttu-id="eb01b-134">呼び出せるように**SettingsDialog**または[パスワードの変更](imapistatus-changepassword.md)を、MAPI サブシステム、MAPI スプーラーを無効、またはアドレスのいずれかの書籍の状態のオブジェクトにされないようにします。</span><span class="sxs-lookup"><span data-stu-id="eb01b-134">Do not expect to be able to call **SettingsDialog** or [ChangePassword](imapistatus-changepassword.md) on any of the MAPI subsystem, MAPI spooler, or address book status objects.</span></span> <span data-ttu-id="eb01b-135">のみ、サブシステムとアドレス帳のステータスのオブジェクトがサポートしている**ValidateState**です。MAPI スプーラーの状態オブジェクトは、 **ValidateState**だけでなく、 **FlushQueues**をサポートします。</span><span class="sxs-lookup"><span data-stu-id="eb01b-135">Both the subsystem and address book status objects only support **ValidateState**; the MAPI spooler status object supports **FlushQueues** in addition to **ValidateState**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="eb01b-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="eb01b-136">See also</span></span>



[<span data-ttu-id="eb01b-137">ステータス ・ テーブル</span><span class="sxs-lookup"><span data-stu-id="eb01b-137">Status Tables</span></span>](status-tables.md)
  
[<span data-ttu-id="eb01b-138">MAPI オブジェクトのステータス</span><span class="sxs-lookup"><span data-stu-id="eb01b-138">MAPI Status Objects</span></span>](mapi-status-objects.md)

