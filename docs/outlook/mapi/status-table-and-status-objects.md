---
title: 状態テーブルと状態オブジェクト
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 203765c1-4b08-4032-a5bf-18f3e752a899
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3eb190069b43ea1960c3b6edf30a9e0b782d2c41
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425177"
---
# <a name="status-table-and-status-objects"></a><span data-ttu-id="528f4-103">状態テーブルと状態オブジェクト</span><span class="sxs-lookup"><span data-stu-id="528f4-103">Status Table and Status Objects</span></span>

  
  
<span data-ttu-id="528f4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="528f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="528f4-105">mapi は、mapi サブシステム、mapi スプーラー、アドレス帳、または特定のサービスプロバイダーの状態に関する情報を表として提供します。</span><span class="sxs-lookup"><span data-stu-id="528f4-105">MAPI provides a table with information about the status of the MAPI subsystem, MAPI spooler, address book, or a particular service provider.</span></span> <span data-ttu-id="528f4-106">このテーブルにアクセスするには、 [imapisession:: getstatustable](imapisession-getstatustable.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="528f4-106">You can access this table by calling [IMAPISession::GetStatusTable](imapisession-getstatustable.md).</span></span>
  
<span data-ttu-id="528f4-107">状態テーブルの各行は、MAPI またはサービスプロバイダーによって実装された状態オブジェクトを表します。</span><span class="sxs-lookup"><span data-stu-id="528f4-107">Each row in the status table represents a status object implemented by MAPI or a service provider.</span></span> <span data-ttu-id="528f4-108">status オブジェクトを使用して、プロバイダーの構成プロパティシートを表示したり、プロバイダーパスワードを変更したり、メッセージをアップロードまたはダウンロードしたり、特定のトランスポートプロバイダーと通信したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="528f4-108">You can use a status object to display a provider's configuration property sheet, to change a provider password, to upload or download messages, and to communicate with a particular transport provider.</span></span> 
  
<span data-ttu-id="528f4-109">status オブジェクトには、次の2つの方法でアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="528f4-109">There are two ways to access a status object:</span></span>
  
- <span data-ttu-id="528f4-110">状態テーブルを使用する</span><span class="sxs-lookup"><span data-stu-id="528f4-110">Through the status table</span></span>
    
- <span data-ttu-id="528f4-111">ログオンオブジェクトの**openstatusentry**メソッドを使用する</span><span class="sxs-lookup"><span data-stu-id="528f4-111">Through a logon object's **OpenStatusEntry** method</span></span> 
    
<span data-ttu-id="528f4-112">ログオンオブジェクトはクライアントで使用できないため、状態のオブジェクトにアクセスするには、状態テーブルを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="528f4-112">Because logon objects are unavailable to clients, you must use the status table to access status objects.</span></span> <span data-ttu-id="528f4-113">状態テーブルの方法は間接的で、status オブジェクトが開かれる前にいくつかの呼び出しを必要とし、 **imapistatus**実装へのポインターが返されます。</span><span class="sxs-lookup"><span data-stu-id="528f4-113">The status table approach is indirect, requiring a few calls before the status object is opened and a pointer to its **IMAPIStatus** implementation returned.</span></span> 
  
 <span data-ttu-id="528f4-114">**状態テーブルを使用して status オブジェクトを開くには**</span><span class="sxs-lookup"><span data-stu-id="528f4-114">**To use the status table to open a status object**</span></span>
  
1. <span data-ttu-id="528f4-115">Call **imapistatus:: getstatustable**が[IMAPITable](imapitableiunknown.md)ポインターを取得することができます。</span><span class="sxs-lookup"><span data-stu-id="528f4-115">Call **IMAPIStatus::GetStatusTable** to retrieve an [IMAPITable](imapitableiunknown.md) pointer.</span></span> 
    
2. <span data-ttu-id="528f4-116">状態テーブルの[IMAPITable:: SetColumns](imapitable-setcolumns.md)メソッドを呼び出して、列セットを**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))、 **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))、および**PR_DISPLAY_NAME** () に制限します ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="528f4-116">Call the status table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)), and **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="528f4-117">テーブルビューを特定のステータスオブジェクトに制限します。</span><span class="sxs-lookup"><span data-stu-id="528f4-117">Limit the table view to a particular status object.</span></span> <span data-ttu-id="528f4-118">MAPI 実装の場合、クライアントは**PR_RESOURCE_TYPE**を使用してプロパティ制限を定義できます。</span><span class="sxs-lookup"><span data-stu-id="528f4-118">For MAPI implementations, a client can define a property restriction using **PR_RESOURCE_TYPE**.</span></span> <span data-ttu-id="528f4-119">サービスプロバイダーの実装では、クライアントは**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))、プロバイダーの名前、または**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) のプロバイダー DLL の名前を制限できます。拡張子.</span><span class="sxs-lookup"><span data-stu-id="528f4-119">For service provider implementations, a client can restrict on **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)), the name of the provider, or on **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)), the name of the provider DLL file.</span></span>
    
4. <span data-ttu-id="528f4-120">[IMAPITable:: Restrict](imapitable-restrict.md)を呼び出して制限を設定します。</span><span class="sxs-lookup"><span data-stu-id="528f4-120">Call [IMAPITable::Restrict](imapitable-restrict.md) to set the restriction.</span></span> 
    
5. <span data-ttu-id="528f4-121">プロバイダーの状態を表す行を取得するには、 [hrqueryallrows](hrqueryallrows.md)を呼び出し、 [spropertyrestriction](spropertyrestriction.md)構造を渡します。</span><span class="sxs-lookup"><span data-stu-id="528f4-121">Call [HrQueryAllRows](hrqueryallrows.md), passing in the [SPropertyRestriction](spropertyrestriction.md) structure, to retrieve the row that represents the status of the provider.</span></span> 
    
6. <span data-ttu-id="528f4-122">open [imapisession:: openentry](imapisession-openentry.md)。状態テーブルの行からエントリ識別子を指定して、status オブジェクトを開いて**imapisession**ポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="528f4-122">Call [IMAPISession::OpenEntry](imapisession-openentry.md), specifying the entry identifier from the status table row, to open the status object and retrieve an **IMAPIStatus** pointer.</span></span> 
    
<span data-ttu-id="528f4-123">プロパティシートを表示するには、対象プロバイダーの status オブジェクトの[imapistatus:: settingsdialog](imapistatus-settingsdialog.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="528f4-123">To display a property sheet, call the status object's [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method for the target provider.</span></span> <span data-ttu-id="528f4-124">**settingsdialog**表示用のプロパティシートを表示します。場合によっては、プロバイダーの構成プロパティを変更します。</span><span class="sxs-lookup"><span data-stu-id="528f4-124">**SettingsDialog** displays a property sheet for viewing and in some cases, changing the configuration properties of a provider.</span></span> 
  
<span data-ttu-id="528f4-125">トランスポートプロバイダーと通信するには、状態オブジェクトの[imapistatus:: validatestate](imapistatus-validatestate.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="528f4-125">To communicate with a transport provider, call its status object's [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="528f4-126">**validatestate**を使用すると、トランスポートプロバイダーを再構成し、プロバイダーがユーザーインターフェイスを表示できないようにしたり、渡されたフラグに応じてリモートサーバーからのメッセージヘッダーのダウンロードを伴うセッションを制御したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="528f4-126">**ValidateState** can reconfigure a transport provider, prevent the provider from displaying a user interface, and control a session that involves downloading message headers from a remote server, depending on the flags that you pass in.</span></span> <span data-ttu-id="528f4-127">たとえば、リモートヘッダーのダウンロードを取り消すには、ABORT_XP_HEADER_OPERATION フラグを**validatestate**に渡します。</span><span class="sxs-lookup"><span data-stu-id="528f4-127">For example, to cancel the downloading of remote headers, pass the ABORT_XP_HEADER_OPERATION flag to **ValidateState**.</span></span> <span data-ttu-id="528f4-128">リモートサーバーとの接続または切断を行うには、FORCE_XP_CONNECT または FORCE_XP_DISCONNECT を渡します。</span><span class="sxs-lookup"><span data-stu-id="528f4-128">To connect or disconnect from the remote server, pass FORCE_XP_CONNECT or FORCE_XP_DISCONNECT.</span></span> <span data-ttu-id="528f4-129">プロバイダーを再構成するには、CONFIG_CHANGED を渡します。</span><span class="sxs-lookup"><span data-stu-id="528f4-129">To reconfigure the provider, pass CONFIG_CHANGED.</span></span> 
  
<span data-ttu-id="528f4-130">オンデマンドでメッセージの送信または受信を実装するクライアントは、トランスポートプロバイダーまたは MAPI スプーラーの[imapistatus:: flushqueues](imapistatus-flushqueues.md)メソッドのいずれかを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="528f4-130">Clients that implement sending or receiving of messages on demand call either a transport provider's or the MAPI spooler's [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method.</span></span> <span data-ttu-id="528f4-131">FLUSH_UPLOAD、FLUSH_DOWNLOAD、および FLUSH_FORCE の3つのフラグをメソッドに渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="528f4-131">You can pass three flags into the method: FLUSH_UPLOAD, FLUSH_DOWNLOAD, and FLUSH_FORCE.</span></span> <span data-ttu-id="528f4-132">FLUSH_UPLOAD は、プロバイダーまたは mapi スプーラーに対して、出力キューで待機しているメッセージを送信するように指示します。 FLUSH_DOWNLOAD は、受信メッセージを受信するようにプロバイダーまたは mapi スプーラーに指示します。</span><span class="sxs-lookup"><span data-stu-id="528f4-132">FLUSH_UPLOAD instructs the provider or the MAPI spooler to send any messages waiting in the output queue while FLUSH_DOWNLOAD instructs the provider or the MAPI spooler to receive any incoming messages.</span></span> <span data-ttu-id="528f4-133">FLUSH_FORCE は他のフラグのいずれかを使用して設定することができます。この場合、状態オブジェクトは、タイミングに関係なく、フラッシュを実行します。</span><span class="sxs-lookup"><span data-stu-id="528f4-133">FLUSH_FORCE can be set with either of the other flags to cause the status object to perform the flush regardless of the timing.</span></span> 
  
<span data-ttu-id="528f4-134">どの mapi サブシステム、mapi スプーラー、またはアドレス帳状態オブジェクトでも、 **settingsdialog**または[ChangePassword](imapistatus-changepassword.md)を呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="528f4-134">Do not expect to be able to call **SettingsDialog** or [ChangePassword](imapistatus-changepassword.md) on any of the MAPI subsystem, MAPI spooler, or address book status objects.</span></span> <span data-ttu-id="528f4-135">サブシステムとアドレス帳の状態オブジェクトの両方が、 **validatestate**のみをサポートしています。MAPI スプーラー status オブジェクトは、 **validatestate**に加えて**flushqueues**をサポートします。</span><span class="sxs-lookup"><span data-stu-id="528f4-135">Both the subsystem and address book status objects only support **ValidateState**; the MAPI spooler status object supports **FlushQueues** in addition to **ValidateState**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="528f4-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="528f4-136">See also</span></span>



[<span data-ttu-id="528f4-137">状態テーブル</span><span class="sxs-lookup"><span data-stu-id="528f4-137">Status Tables</span></span>](status-tables.md)
  
[<span data-ttu-id="528f4-138">MAPI 状態オブジェクト</span><span class="sxs-lookup"><span data-stu-id="528f4-138">MAPI Status Objects</span></span>](mapi-status-objects.md)

