---
title: MAPI サービス プロバイダー オブジェクト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f8ade454-2450-49e6-a76f-93801055a7e5
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 505b27b469a4ab197b41058ea5b933608818f0d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801444"
---
# <a name="mapi-service-provider-objects"></a><span data-ttu-id="56a9d-103">MAPI サービス プロバイダー オブジェクト</span><span class="sxs-lookup"><span data-stu-id="56a9d-103">MAPI Service Provider Objects</span></span>

  
  
<span data-ttu-id="56a9d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="56a9d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="56a9d-105">サービス プロバイダーは、多くのオブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="56a9d-105">Service providers implement many objects.</span></span> <span data-ttu-id="56a9d-106">MAPI によって主に使用される、いくつかと、クライアント アプリケーションによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="56a9d-106">Some are used primarily by MAPI and some are used by client applications.</span></span> <span data-ttu-id="56a9d-107">サービス ・ プロバイダーのすべての種類によって、いくつかのオブジェクトの実装します。残りの部分は、1 つのプロバイダーの種類に固有です。</span><span class="sxs-lookup"><span data-stu-id="56a9d-107">A few objects are implemented by all types of service providers; the rest are specific to a single provider type.</span></span> <span data-ttu-id="56a9d-108">次の表では、すべてのサービス プロバイダー オブジェクトについて説明します。</span><span class="sxs-lookup"><span data-stu-id="56a9d-108">The following table describes all of the service provider objects.</span></span>
  
|<span data-ttu-id="56a9d-109">**サービス プロバイダー オブジェクト**</span><span class="sxs-lookup"><span data-stu-id="56a9d-109">**Service provider object**</span></span>|<span data-ttu-id="56a9d-110">**説明**</span><span class="sxs-lookup"><span data-stu-id="56a9d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="56a9d-111">アドレス帳コンテナー</span><span class="sxs-lookup"><span data-stu-id="56a9d-111">Address book container</span></span>  <br/> |<span data-ttu-id="56a9d-112">アクティブなプロファイルに 1 つのアドレス帳プロバイダーに受信者の情報が含まれていますアドレス帳プロバイダーは、1 つまたは複数のアドレス帳コンテナーを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="56a9d-112">Contains recipient information for one address book provider in the active profile; address book providers can have one or more address book containers.</span></span>  <br/> |
|<span data-ttu-id="56a9d-113">Attachment</span><span class="sxs-lookup"><span data-stu-id="56a9d-113">Attachment</span></span>  <br/> |<span data-ttu-id="56a9d-114">ファイルまたはメッセージに関連する、OLE オブジェクトなどの追加データが含まれています。</span><span class="sxs-lookup"><span data-stu-id="56a9d-114">Contains additional data, such as a file or OLE object, to be associated with a message.</span></span>  <br/> |
|<span data-ttu-id="56a9d-115">コントロール</span><span class="sxs-lookup"><span data-stu-id="56a9d-115">Control</span></span>  <br/> |<span data-ttu-id="56a9d-116">またはボタンを無効にでき、ボタンがクリックされたときの処理を開始します。</span><span class="sxs-lookup"><span data-stu-id="56a9d-116">Enables or disables a button and initiates processing when the button is clicked.</span></span>  <br/> |
|<span data-ttu-id="56a9d-117">配布リスト</span><span class="sxs-lookup"><span data-stu-id="56a9d-117">Distribution list</span></span>  <br/> |<span data-ttu-id="56a9d-118">個々 のメッセージの受信者のグループ化をについて説明します。</span><span class="sxs-lookup"><span data-stu-id="56a9d-118">Describes a grouping of individual message recipients.</span></span>  <br/> |
|<span data-ttu-id="56a9d-119">Folder</span><span class="sxs-lookup"><span data-stu-id="56a9d-119">Folder</span></span>  <br/> |<span data-ttu-id="56a9d-120">メッセージおよびその他のメッセージのコンテナーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="56a9d-120">Contains messages and other message containers.</span></span>  <br/> |
|<span data-ttu-id="56a9d-121">ログオン</span><span class="sxs-lookup"><span data-stu-id="56a9d-121">Logon</span></span>  <br/> |<span data-ttu-id="56a9d-122">ハンドルは、プロバイダーのイベントの通知とクライアントの要求をサービスします。</span><span class="sxs-lookup"><span data-stu-id="56a9d-122">Handles service provider event notification and client requests.</span></span>  <br/> |
|<span data-ttu-id="56a9d-123">メッセージング ユーザー</span><span class="sxs-lookup"><span data-stu-id="56a9d-123">Messaging user</span></span>  <br/> |<span data-ttu-id="56a9d-124">メッセージの各受信者をについて説明します。</span><span class="sxs-lookup"><span data-stu-id="56a9d-124">Describes an individual recipient of a message.</span></span>  <br/> |
|<span data-ttu-id="56a9d-125">Message</span><span class="sxs-lookup"><span data-stu-id="56a9d-125">Message</span></span>  <br/> |<span data-ttu-id="56a9d-126">1 つまたは複数の受信者に送信できる情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="56a9d-126">Contains information that can be sent to one or more recipients.</span></span>  <br/> |
|<span data-ttu-id="56a9d-127">メッセージ ・ ストア</span><span class="sxs-lookup"><span data-stu-id="56a9d-127">Message store</span></span>  <br/> |<span data-ttu-id="56a9d-128">メッセージの階層構造のデータベースとして機能します。</span><span class="sxs-lookup"><span data-stu-id="56a9d-128">Acts as a hierarchically organized database of messages.</span></span>  <br/> |
|<span data-ttu-id="56a9d-129">プロバイダー</span><span class="sxs-lookup"><span data-stu-id="56a9d-129">Provider</span></span>  <br/> |<span data-ttu-id="56a9d-130">ハンドルはサービス プロバイダーの起動とシャット ダウンします。</span><span class="sxs-lookup"><span data-stu-id="56a9d-130">Handles service provider startup and shutdown.</span></span>  <br/> |
|<span data-ttu-id="56a9d-131">スプーラーのフック</span><span class="sxs-lookup"><span data-stu-id="56a9d-131">Spooler hook</span></span>  <br/> |<span data-ttu-id="56a9d-132">受信および送信メッセージに対して特別な処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="56a9d-132">Performs special processing on inbound and outbound messages.</span></span>  <br/> |
|<span data-ttu-id="56a9d-133">Status</span><span class="sxs-lookup"><span data-stu-id="56a9d-133">Status</span></span>  <br/> |<span data-ttu-id="56a9d-134">サービス プロバイダーの状態へのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="56a9d-134">Provides access to the service provider's state.</span></span>  <br/> |
|<span data-ttu-id="56a9d-135">テーブル</span><span class="sxs-lookup"><span data-stu-id="56a9d-135">Table</span></span>  <br/> |<span data-ttu-id="56a9d-136">行と列の形式でデータベース テーブルのようなオブジェクトのデータの概要ビューへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="56a9d-136">Provides access to a summary view of object data in row and column format, similar to a database table.</span></span>  <br/> |
   
<span data-ttu-id="56a9d-137">すべてのサービス プロバイダーは、プロバイダーのオブジェクトとログオン オブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="56a9d-137">All service providers implement a provider object and a logon object.</span></span> <span data-ttu-id="56a9d-138">プロバイダー オブジェクトは厳密に管理します。スタートアップおよびシャット ダウンの処理を制御するのには MAPI によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="56a9d-138">Provider objects are strictly for bookkeeping; they are used by MAPI to control the startup and shutdown processes.</span></span> <span data-ttu-id="56a9d-139">ログオン オブジェクト サービスを提供しないクライアント要求をいくつか直接。</span><span class="sxs-lookup"><span data-stu-id="56a9d-139">Logon objects service some client requests indirectly.</span></span> <span data-ttu-id="56a9d-140">たとえば、メッセージは、プロバイダーのログオン オブジェクト ハンドル通知の登録とメッセージ ストアのオブジェクトを開く要求を格納します。</span><span class="sxs-lookup"><span data-stu-id="56a9d-140">For example, the message store provider's logon object handles notification registration and requests to open message store objects.</span></span> 
  
<span data-ttu-id="56a9d-141">プロバイダーおよびログオン オブジェクトでは、実装を提供するサービス プロバイダーの種類によって異なるインターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="56a9d-141">Provider and logon objects implement a different interface depending on the type of service provider that supplies the implementation.</span></span> <span data-ttu-id="56a9d-142">メッセージ ストア プロバイダーを実装して、 [IMSProvider: IUnknown](imsprovideriunknown.md)と[IMSLogon: IUnknown](imslogoniunknown.md)インターフェイスは、プロバイダーおよびログオン オブジェクトは、アドレスがプロバイダーの実装を予約、 [IABProvider: IUnknown](iabprovideriunknown.md)と[IABLogon: IUnknown](iablogoniunknown.md)インターフェイス、およびトランスポート プロバイダーを実装して、 [IXPProvider: IUnknown](ixpprovideriunknown.md)と[IXPLogon: IUnknown](ixplogoniunknown.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="56a9d-142">A message store provider implements the [IMSProvider : IUnknown](imsprovideriunknown.md) and [IMSLogon : IUnknown](imslogoniunknown.md) interfaces in its provider and logon objects, an address book provider implements the [IABProvider : IUnknown](iabprovideriunknown.md) and [IABLogon : IUnknown](iablogoniunknown.md) interfaces, and a transport provider implements the [IXPProvider : IUnknown](ixpprovideriunknown.md) and [IXPLogon : IUnknown](ixplogoniunknown.md) interfaces.</span></span> 
  
<span data-ttu-id="56a9d-143">メッセージ フック プロバイダーでは、スプーラーのフックのオブジェクト、または受信メッセージと送信メッセージにフィルターを適用するオブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="56a9d-143">Message hook providers implement spooler hook objects, or objects that filter inbound and outbound messages.</span></span>
  
<span data-ttu-id="56a9d-144">サービス プロバイダーは、通常、いくつかのオブジェクトのみを使用します。</span><span class="sxs-lookup"><span data-stu-id="56a9d-144">Service providers typically use only a few objects.</span></span> <span data-ttu-id="56a9d-145">最も頻繁に、MAPI は、クライアントの要求を助けるために提供するサポート オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="56a9d-145">Most frequently, they use a support object that MAPI provides to help implement client requests.</span></span> <span data-ttu-id="56a9d-146">サポート オブジェクトは、それを使用するプロバイダーの種類をカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="56a9d-146">The support object is customized for the type of provider that is using it.</span></span> <span data-ttu-id="56a9d-147">すべてのサービス プロバイダーのサポート オブジェクトには、イベント通知の処理、構成のプロパティ、オブジェクトのオープン、およびエラー処理を表示するためのメソッドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="56a9d-147">For all service providers, the support object includes methods for handling event notification, displaying configuration properties, opening objects, and error handling.</span></span> <span data-ttu-id="56a9d-148">メソッドの残りの部分は特定の使用です。アドレス帳、メッセージ ストア、およびトランスポート プロバイダー、および構成をサポートするためのカスタマイズされたバージョンがあります。</span><span class="sxs-lookup"><span data-stu-id="56a9d-148">The rest of the methods are specific to its use; there are customized versions for address book, message store, and transport providers, and for configuration support.</span></span> <span data-ttu-id="56a9d-149">たとえば、アドレス帳のサポート オブジェクトには、詳細およびカスタム受信者ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="56a9d-149">For example, the address book support object displays details and custom recipient dialog boxes.</span></span> <span data-ttu-id="56a9d-150">メッセージ ・ ストアでは、オブジェクトのサポートのコピーをサポートし、フォルダーとメッセージの操作を移動します。</span><span class="sxs-lookup"><span data-stu-id="56a9d-150">The message store support object supports copy and move operations for folders and messages.</span></span> <span data-ttu-id="56a9d-151">トランスポート プロバイダーのサポートのオブジェクトには、MAPI スプーラーとの対話を促進するためのメソッドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="56a9d-151">The transport provider support object includes methods for facilitating interaction with the MAPI spooler.</span></span> 
  
<span data-ttu-id="56a9d-152">サービス プロバイダーによっては、テーブルのデータとプロパティのデータ オブジェクトを使用して、MAPI が実装しているユーティリティ オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="56a9d-152">Some service providers use table data and property data objects — utility objects that MAPI implements.</span></span> <span data-ttu-id="56a9d-153">テーブルのデータ オブジェクトは、基になるテーブルのデータを管理するサービス プロバイダーを有効にします。</span><span class="sxs-lookup"><span data-stu-id="56a9d-153">Table data objects enable service providers to manage the underlying data of a table.</span></span> <span data-ttu-id="56a9d-154">データ オブジェクトのプロパティは、オブジェクトとプロパティのアクセスを設定するのにはサービス ・ プロバイダーを有効にします。</span><span class="sxs-lookup"><span data-stu-id="56a9d-154">Property data objects enable service providers to set object and property access.</span></span> 
  
<span data-ttu-id="56a9d-155">プロパティを転送するためにトランスポート ニュートラル カプセル化形式 (TNEF) をサポートするトランスポート プロバイダーは、MAPI をサポートするために実装する TNEF オブジェクトを使用して、 [ITnef: IUnknown](itnefiunknown.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="56a9d-155">Transport providers that support the Transport Neutral Encapsulation Format (TNEF) for transferring properties use a TNEF object that MAPI implements to support the [ITnef : IUnknown](itnefiunknown.md) interface.</span></span> <span data-ttu-id="56a9d-156">詳細については、 [TNEF-Enabled トランスポート プロバイダーの開発](developing-a-tnef-enabled-transport-provider.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="56a9d-156">For more information, see [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="56a9d-157">関連項目</span><span class="sxs-lookup"><span data-stu-id="56a9d-157">See also</span></span>



[<span data-ttu-id="56a9d-158">ITnef: IUnknown</span><span class="sxs-lookup"><span data-stu-id="56a9d-158">ITnef : IUnknown</span></span>](itnefiunknown.md)
  
[<span data-ttu-id="56a9d-159">IMSProvider: IUnknown</span><span class="sxs-lookup"><span data-stu-id="56a9d-159">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)
  
[<span data-ttu-id="56a9d-160">IMSLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="56a9d-160">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)
  
[<span data-ttu-id="56a9d-161">IABProvider: IUnknown</span><span class="sxs-lookup"><span data-stu-id="56a9d-161">IABProvider : IUnknown</span></span>](iabprovideriunknown.md)
  
[<span data-ttu-id="56a9d-162">IABLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="56a9d-162">IABLogon : IUnknown</span></span>](iablogoniunknown.md)
  
[<span data-ttu-id="56a9d-163">IXPProvider: IUnknown</span><span class="sxs-lookup"><span data-stu-id="56a9d-163">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)
  
[<span data-ttu-id="56a9d-164">IXPLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="56a9d-164">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)


[<span data-ttu-id="56a9d-165">TNEF を有効にしたトランスポート プロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="56a9d-165">Developing a TNEF-Enabled Transport Provider</span></span>](developing-a-tnef-enabled-transport-provider.md)

