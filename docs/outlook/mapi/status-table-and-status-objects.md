---
title: Status Table オブジェクトと Status オブジェクト
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
# <a name="status-table-and-status-objects"></a><span data-ttu-id="51be7-103">Status Table オブジェクトと Status オブジェクト</span><span class="sxs-lookup"><span data-stu-id="51be7-103">Status Table and Status Objects</span></span>

  
  
<span data-ttu-id="51be7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51be7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51be7-105">MAPI は、MAPI サブシステム、MAPI スプーラー、アドレス帳、または特定のサービス プロバイダーの状態に関する情報を表に提供します。</span><span class="sxs-lookup"><span data-stu-id="51be7-105">MAPI provides a table with information about the status of the MAPI subsystem, MAPI spooler, address book, or a particular service provider.</span></span> <span data-ttu-id="51be7-106">このテーブルにアクセスするには [、IMAPISession::GetStatusTable を呼び出します](imapisession-getstatustable.md)。</span><span class="sxs-lookup"><span data-stu-id="51be7-106">You can access this table by calling [IMAPISession::GetStatusTable](imapisession-getstatustable.md).</span></span>
  
<span data-ttu-id="51be7-107">状態テーブルの各行は、MAPI またはサービス プロバイダーによって実装された状態オブジェクトを表します。</span><span class="sxs-lookup"><span data-stu-id="51be7-107">Each row in the status table represents a status object implemented by MAPI or a service provider.</span></span> <span data-ttu-id="51be7-108">status オブジェクトを使用して、プロバイダーの構成プロパティ シートを表示したり、プロバイダー のパスワードを変更したり、メッセージをアップロードまたはダウンロードしたり、特定のトランスポート プロバイダーと通信することができます。</span><span class="sxs-lookup"><span data-stu-id="51be7-108">You can use a status object to display a provider's configuration property sheet, to change a provider password, to upload or download messages, and to communicate with a particular transport provider.</span></span> 
  
<span data-ttu-id="51be7-109">状態オブジェクトにアクセスするには、次の 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="51be7-109">There are two ways to access a status object:</span></span>
  
- <span data-ttu-id="51be7-110">状態テーブルを使用する</span><span class="sxs-lookup"><span data-stu-id="51be7-110">Through the status table</span></span>
    
- <span data-ttu-id="51be7-111">ログオン オブジェクトの **OpenStatusEntry メソッドを使用** する</span><span class="sxs-lookup"><span data-stu-id="51be7-111">Through a logon object's **OpenStatusEntry** method</span></span> 
    
<span data-ttu-id="51be7-112">ログオン オブジェクトはクライアントでは使用できないので、状態オブジェクトにアクセスするには、状態テーブルを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="51be7-112">Because logon objects are unavailable to clients, you must use the status table to access status objects.</span></span> <span data-ttu-id="51be7-113">状態テーブルのアプローチは間接的であり、status オブジェクトを開く前にいくつかの呼び出しが必要であり **、IMAPIStatus** 実装へのポインターが返されます。</span><span class="sxs-lookup"><span data-stu-id="51be7-113">The status table approach is indirect, requiring a few calls before the status object is opened and a pointer to its **IMAPIStatus** implementation returned.</span></span> 
  
 <span data-ttu-id="51be7-114">**状態テーブルを使用して状態オブジェクトを開く方法**</span><span class="sxs-lookup"><span data-stu-id="51be7-114">**To use the status table to open a status object**</span></span>
  
1. <span data-ttu-id="51be7-115">**IMAPIStatus::GetStatusTable** を呼び出して [IMAPITable ポインターを取得](imapitableiunknown.md)します。</span><span class="sxs-lookup"><span data-stu-id="51be7-115">Call **IMAPIStatus::GetStatusTable** to retrieve an [IMAPITable](imapitableiunknown.md) pointer.</span></span> 
    
2. <span data-ttu-id="51be7-116">状態テーブルの [IMAPITable::SetColumns](imapitable-setcolumns.md)メソッドを呼び出して、列セットを **PR_ENTRYID** [(PidTagEntryId)、PR_RESOURCE_TYPE](pidtagentryid-canonical-property.md)[(PidTagResourceType)、](pidtagresourcetype-canonical-property.md)および **PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)に制限します。 </span><span class="sxs-lookup"><span data-stu-id="51be7-116">Call the status table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)), and **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="51be7-117">テーブル ビューを特定の状態オブジェクトに制限します。</span><span class="sxs-lookup"><span data-stu-id="51be7-117">Limit the table view to a particular status object.</span></span> <span data-ttu-id="51be7-118">MAPI の実装では、クライアントはプロパティの制限を使用して定義 **PR_RESOURCE_TYPE。**</span><span class="sxs-lookup"><span data-stu-id="51be7-118">For MAPI implementations, a client can define a property restriction using **PR_RESOURCE_TYPE**.</span></span> <span data-ttu-id="51be7-119">サービス プロバイダーの実装では、クライアントは **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay)](pidtagproviderdisplay-canonical-property.md)、プロバイダーの名前、または **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName)](pidtagproviderdllname-canonical-property.md)、プロバイダー DLL ファイルの名前を制限できます。</span><span class="sxs-lookup"><span data-stu-id="51be7-119">For service provider implementations, a client can restrict on **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)), the name of the provider, or on **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)), the name of the provider DLL file.</span></span>
    
4. <span data-ttu-id="51be7-120">[IMAPITable::Restrict を呼び出して](imapitable-restrict.md)制限を設定します。</span><span class="sxs-lookup"><span data-stu-id="51be7-120">Call [IMAPITable::Restrict](imapitable-restrict.md) to set the restriction.</span></span> 
    
5. <span data-ttu-id="51be7-121">[HrQueryAllRows](hrqueryallrows.md)を呼び出し[、SPropertyRestriction](spropertyrestriction.md)構造体を渡して、プロバイダーの状態を表す行を取得します。</span><span class="sxs-lookup"><span data-stu-id="51be7-121">Call [HrQueryAllRows](hrqueryallrows.md), passing in the [SPropertyRestriction](spropertyrestriction.md) structure, to retrieve the row that represents the status of the provider.</span></span> 
    
6. <span data-ttu-id="51be7-122">STATUS オブジェクトを開き **、IMAPIStatus** ポインターを取得するには、状態テーブル行からエントリ識別子を指定して [、IMAPISession::OpenEntry](imapisession-openentry.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="51be7-122">Call [IMAPISession::OpenEntry](imapisession-openentry.md), specifying the entry identifier from the status table row, to open the status object and retrieve an **IMAPIStatus** pointer.</span></span> 
    
<span data-ttu-id="51be7-123">プロパティ シートを表示するには、ターゲット プロバイダーの [status オブジェクトの IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="51be7-123">To display a property sheet, call the status object's [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method for the target provider.</span></span> <span data-ttu-id="51be7-124">**SettingsDialog は** 、プロバイダーの構成プロパティを変更して表示するプロパティ シートを表示し、場合によっては表示します。</span><span class="sxs-lookup"><span data-stu-id="51be7-124">**SettingsDialog** displays a property sheet for viewing and in some cases, changing the configuration properties of a provider.</span></span> 
  
<span data-ttu-id="51be7-125">トランスポート プロバイダーと通信するには、その状態オブジェクトの [IMAPIStatus::ValidateState メソッドを呼び出](imapistatus-validatestate.md) します。</span><span class="sxs-lookup"><span data-stu-id="51be7-125">To communicate with a transport provider, call its status object's [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="51be7-126">**ValidateState** では、トランスポート プロバイダーを再構成し、プロバイダーがユーザー インターフェイスを表示し、渡すフラグに応じて、リモート サーバーからメッセージ ヘッダーをダウンロードするセッションを制御できます。</span><span class="sxs-lookup"><span data-stu-id="51be7-126">**ValidateState** can reconfigure a transport provider, prevent the provider from displaying a user interface, and control a session that involves downloading message headers from a remote server, depending on the flags that you pass in.</span></span> <span data-ttu-id="51be7-127">たとえば、リモート ヘッダーのダウンロードを取り消す場合は、ABORT_XP_HEADER_OPERATION **ValidateState に渡します**。</span><span class="sxs-lookup"><span data-stu-id="51be7-127">For example, to cancel the downloading of remote headers, pass the ABORT_XP_HEADER_OPERATION flag to **ValidateState**.</span></span> <span data-ttu-id="51be7-128">リモート サーバーに接続または切断するには、リモート サーバー FORCE_XP_CONNECTまたはFORCE_XP_DISCONNECT。</span><span class="sxs-lookup"><span data-stu-id="51be7-128">To connect or disconnect from the remote server, pass FORCE_XP_CONNECT or FORCE_XP_DISCONNECT.</span></span> <span data-ttu-id="51be7-129">プロバイダーを再構成するには、次のCONFIG_CHANGED。</span><span class="sxs-lookup"><span data-stu-id="51be7-129">To reconfigure the provider, pass CONFIG_CHANGED.</span></span> 
  
<span data-ttu-id="51be7-130">オンデマンドでメッセージの送受信を実装するクライアントは、トランスポート プロバイダーまたは MAPI スプーラーの [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="51be7-130">Clients that implement sending or receiving of messages on demand call either a transport provider's or the MAPI spooler's [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method.</span></span> <span data-ttu-id="51be7-131">メソッドに 3 つのフラグを渡FLUSH_UPLOAD、FLUSH_DOWNLOAD、FLUSH_FORCE。</span><span class="sxs-lookup"><span data-stu-id="51be7-131">You can pass three flags into the method: FLUSH_UPLOAD, FLUSH_DOWNLOAD, and FLUSH_FORCE.</span></span> <span data-ttu-id="51be7-132">FLUSH_UPLOADは、プロバイダーまたは MAPI スプーラーに、FLUSH_DOWNLOAD がプロバイダーまたは MAPI スプーラーに受信メッセージを受信するように指示している間に、出力キューで待機しているメッセージを送信するように指示します。</span><span class="sxs-lookup"><span data-stu-id="51be7-132">FLUSH_UPLOAD instructs the provider or the MAPI spooler to send any messages waiting in the output queue while FLUSH_DOWNLOAD instructs the provider or the MAPI spooler to receive any incoming messages.</span></span> <span data-ttu-id="51be7-133">FLUSH_FORCEフラグを設定すると、タイミングに関係なく status オブジェクトがフラッシュを実行します。</span><span class="sxs-lookup"><span data-stu-id="51be7-133">FLUSH_FORCE can be set with either of the other flags to cause the status object to perform the flush regardless of the timing.</span></span> 
  
<span data-ttu-id="51be7-134">MAPI サブシステム、MAPI スプーラー、またはアドレス帳の状態オブジェクトで **SettingsDialog** または [ChangePassword](imapistatus-changepassword.md) を呼び出せない。</span><span class="sxs-lookup"><span data-stu-id="51be7-134">Do not expect to be able to call **SettingsDialog** or [ChangePassword](imapistatus-changepassword.md) on any of the MAPI subsystem, MAPI spooler, or address book status objects.</span></span> <span data-ttu-id="51be7-135">サブシステムとアドレス帳の状態オブジェクトはどちらも **ValidateState のみをサポートします**。MAPI スプーラー状態オブジェクトは **ValidateState に加えて FlushQueues** **をサポートします**。</span><span class="sxs-lookup"><span data-stu-id="51be7-135">Both the subsystem and address book status objects only support **ValidateState**; the MAPI spooler status object supports **FlushQueues** in addition to **ValidateState**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="51be7-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="51be7-136">See also</span></span>



[<span data-ttu-id="51be7-137">状態テーブル</span><span class="sxs-lookup"><span data-stu-id="51be7-137">Status Tables</span></span>](status-tables.md)
  
[<span data-ttu-id="51be7-138">MAPI 状態オブジェクト</span><span class="sxs-lookup"><span data-stu-id="51be7-138">MAPI Status Objects</span></span>](mapi-status-objects.md)

