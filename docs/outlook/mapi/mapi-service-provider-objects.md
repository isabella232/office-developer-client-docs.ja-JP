---
title: MAPI サービス プロバイダー オブジェクト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f8ade454-2450-49e6-a76f-93801055a7e5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0976e986a33d8b96366a84527f227bd05ef7845e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432269"
---
# <a name="mapi-service-provider-objects"></a><span data-ttu-id="be049-103">MAPI サービス プロバイダー オブジェクト</span><span class="sxs-lookup"><span data-stu-id="be049-103">MAPI Service Provider Objects</span></span>

  
  
<span data-ttu-id="be049-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be049-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be049-105">サービス プロバイダーは、多くのオブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="be049-105">Service providers implement many objects.</span></span> <span data-ttu-id="be049-106">一部は主に MAPI で使用され、一部はクライアント アプリケーションで使用されます。</span><span class="sxs-lookup"><span data-stu-id="be049-106">Some are used primarily by MAPI and some are used by client applications.</span></span> <span data-ttu-id="be049-107">いくつかのオブジェクトは、すべての種類のサービス プロバイダーによって実装されます。残りは単一のプロバイダーの種類に固有です。</span><span class="sxs-lookup"><span data-stu-id="be049-107">A few objects are implemented by all types of service providers; the rest are specific to a single provider type.</span></span> <span data-ttu-id="be049-108">次の表では、すべてのサービス プロバイダー オブジェクトについて説明します。</span><span class="sxs-lookup"><span data-stu-id="be049-108">The following table describes all of the service provider objects.</span></span>
  
|<span data-ttu-id="be049-109">**サービス プロバイダー オブジェクト**</span><span class="sxs-lookup"><span data-stu-id="be049-109">**Service provider object**</span></span>|<span data-ttu-id="be049-110">**説明**</span><span class="sxs-lookup"><span data-stu-id="be049-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="be049-111">アドレス帳コンテナー</span><span class="sxs-lookup"><span data-stu-id="be049-111">Address book container</span></span>  <br/> |<span data-ttu-id="be049-112">アクティブ なプロファイル内の 1 つのアドレス帳プロバイダーの受信者情報を含む。アドレス帳プロバイダーは、1 つ以上のアドレス帳コンテナーを持つ場合があります。</span><span class="sxs-lookup"><span data-stu-id="be049-112">Contains recipient information for one address book provider in the active profile; address book providers can have one or more address book containers.</span></span>  <br/> |
|<span data-ttu-id="be049-113">添付ファイル</span><span class="sxs-lookup"><span data-stu-id="be049-113">Attachment</span></span>  <br/> |<span data-ttu-id="be049-114">メッセージに関連付けられる追加のデータ (ファイルや OLE オブジェクトなど) が含まれる。</span><span class="sxs-lookup"><span data-stu-id="be049-114">Contains additional data, such as a file or OLE object, to be associated with a message.</span></span>  <br/> |
|<span data-ttu-id="be049-115">コントロール</span><span class="sxs-lookup"><span data-stu-id="be049-115">Control</span></span>  <br/> |<span data-ttu-id="be049-116">ボタンを有効または無効にし、ボタンをクリックすると処理を開始します。</span><span class="sxs-lookup"><span data-stu-id="be049-116">Enables or disables a button and initiates processing when the button is clicked.</span></span>  <br/> |
|<span data-ttu-id="be049-117">配布リスト</span><span class="sxs-lookup"><span data-stu-id="be049-117">Distribution list</span></span>  <br/> |<span data-ttu-id="be049-118">個々のメッセージ受信者のグループ化について説明します。</span><span class="sxs-lookup"><span data-stu-id="be049-118">Describes a grouping of individual message recipients.</span></span>  <br/> |
|<span data-ttu-id="be049-119">Folder</span><span class="sxs-lookup"><span data-stu-id="be049-119">Folder</span></span>  <br/> |<span data-ttu-id="be049-120">メッセージと他のメッセージ コンテナーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="be049-120">Contains messages and other message containers.</span></span>  <br/> |
|<span data-ttu-id="be049-121">Logon</span><span class="sxs-lookup"><span data-stu-id="be049-121">Logon</span></span>  <br/> |<span data-ttu-id="be049-122">サービス プロバイダーのイベント通知とクライアント要求を処理します。</span><span class="sxs-lookup"><span data-stu-id="be049-122">Handles service provider event notification and client requests.</span></span>  <br/> |
|<span data-ttu-id="be049-123">メッセージング ユーザー</span><span class="sxs-lookup"><span data-stu-id="be049-123">Messaging user</span></span>  <br/> |<span data-ttu-id="be049-124">メッセージの個々の受信者について説明します。</span><span class="sxs-lookup"><span data-stu-id="be049-124">Describes an individual recipient of a message.</span></span>  <br/> |
|<span data-ttu-id="be049-125">メッセージ</span><span class="sxs-lookup"><span data-stu-id="be049-125">Message</span></span>  <br/> |<span data-ttu-id="be049-126">1 つ以上の受信者に送信できる情報が含まれる。</span><span class="sxs-lookup"><span data-stu-id="be049-126">Contains information that can be sent to one or more recipients.</span></span>  <br/> |
|<span data-ttu-id="be049-127">メッセージ ストア</span><span class="sxs-lookup"><span data-stu-id="be049-127">Message store</span></span>  <br/> |<span data-ttu-id="be049-128">メッセージの階層的に整理されたデータベースとして機能します。</span><span class="sxs-lookup"><span data-stu-id="be049-128">Acts as a hierarchically organized database of messages.</span></span>  <br/> |
|<span data-ttu-id="be049-129">プロバイダー</span><span class="sxs-lookup"><span data-stu-id="be049-129">Provider</span></span>  <br/> |<span data-ttu-id="be049-130">サービス プロバイダーの起動とシャットダウンを処理します。</span><span class="sxs-lookup"><span data-stu-id="be049-130">Handles service provider startup and shutdown.</span></span>  <br/> |
|<span data-ttu-id="be049-131">スプーラー フック</span><span class="sxs-lookup"><span data-stu-id="be049-131">Spooler hook</span></span>  <br/> |<span data-ttu-id="be049-132">受信メッセージと送信メッセージに対して特別な処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="be049-132">Performs special processing on inbound and outbound messages.</span></span>  <br/> |
|<span data-ttu-id="be049-133">状態</span><span class="sxs-lookup"><span data-stu-id="be049-133">Status</span></span>  <br/> |<span data-ttu-id="be049-134">サービス プロバイダーの状態へのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="be049-134">Provides access to the service provider's state.</span></span>  <br/> |
|<span data-ttu-id="be049-135">Table</span><span class="sxs-lookup"><span data-stu-id="be049-135">Table</span></span>  <br/> |<span data-ttu-id="be049-136">データベース テーブルと同様に、行および列形式のオブジェクト データの概要ビューへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="be049-136">Provides access to a summary view of object data in row and column format, similar to a database table.</span></span>  <br/> |
   
<span data-ttu-id="be049-137">すべてのサービス プロバイダーは、プロバイダー オブジェクトとログオン オブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="be049-137">All service providers implement a provider object and a logon object.</span></span> <span data-ttu-id="be049-138">プロバイダー オブジェクトは厳密に簿記用です。これらは、MAPI によって起動プロセスとシャットダウン プロセスを制御するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="be049-138">Provider objects are strictly for bookkeeping; they are used by MAPI to control the startup and shutdown processes.</span></span> <span data-ttu-id="be049-139">ログオン オブジェクトは、一部のクライアント要求を間接的に処理します。</span><span class="sxs-lookup"><span data-stu-id="be049-139">Logon objects service some client requests indirectly.</span></span> <span data-ttu-id="be049-140">たとえば、メッセージ ストア プロバイダーのログオン オブジェクトは、通知登録とメッセージ ストア オブジェクトを開く要求を処理します。</span><span class="sxs-lookup"><span data-stu-id="be049-140">For example, the message store provider's logon object handles notification registration and requests to open message store objects.</span></span> 
  
<span data-ttu-id="be049-141">プロバイダー オブジェクトとログオン オブジェクトは、実装を提供するサービス プロバイダーの種類に応じて異なるインターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="be049-141">Provider and logon objects implement a different interface depending on the type of service provider that supplies the implementation.</span></span> <span data-ttu-id="be049-142">メッセージ ストア プロバイダーは、プロバイダーおよびログオン オブジェクトに [IMSProvider : IUnknown](imsprovideriunknown.md) インターフェイスと [IMSLogon : IUnknown](imslogoniunknown.md) インターフェイスを実装し、アドレス帳プロバイダーは [IABProvider : IUnknown](iabprovideriunknown.md) インターフェイスと [IABLogon](iablogoniunknown.md) : IUnknown インターフェイスを実装し、トランスポート プロバイダーは [IXPProvider : IUnknown](ixpprovideriunknown.md) および [IXPLogon : IUnknown](ixplogoniunknown.md) インターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="be049-142">A message store provider implements the [IMSProvider : IUnknown](imsprovideriunknown.md) and [IMSLogon : IUnknown](imslogoniunknown.md) interfaces in its provider and logon objects, an address book provider implements the [IABProvider : IUnknown](iabprovideriunknown.md) and [IABLogon : IUnknown](iablogoniunknown.md) interfaces, and a transport provider implements the [IXPProvider : IUnknown](ixpprovideriunknown.md) and [IXPLogon : IUnknown](ixplogoniunknown.md) interfaces.</span></span> 
  
<span data-ttu-id="be049-143">メッセージ フック プロバイダーは、スプーラー フック オブジェクト、または受信メッセージと送信メッセージをフィルター処理するオブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="be049-143">Message hook providers implement spooler hook objects, or objects that filter inbound and outbound messages.</span></span>
  
<span data-ttu-id="be049-144">サービス プロバイダーは通常、少数のオブジェクトのみを使用します。</span><span class="sxs-lookup"><span data-stu-id="be049-144">Service providers typically use only a few objects.</span></span> <span data-ttu-id="be049-145">ほとんどの場合、MAPI が提供するサポート オブジェクトを使用して、クライアント要求の実装に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="be049-145">Most frequently, they use a support object that MAPI provides to help implement client requests.</span></span> <span data-ttu-id="be049-146">サポート オブジェクトは、使用しているプロバイダーの種類に合わせてカスタマイズされます。</span><span class="sxs-lookup"><span data-stu-id="be049-146">The support object is customized for the type of provider that is using it.</span></span> <span data-ttu-id="be049-147">すべてのサービス プロバイダーに対して、サポート オブジェクトには、イベント通知の処理、構成プロパティの表示、オブジェクトの開き方、エラー処理のためのメソッドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="be049-147">For all service providers, the support object includes methods for handling event notification, displaying configuration properties, opening objects, and error handling.</span></span> <span data-ttu-id="be049-148">残りのメソッドは、その使用に固有です。アドレス帳、メッセージ ストア、トランスポート プロバイダー、および構成のサポート用にカスタマイズされたバージョンがあります。</span><span class="sxs-lookup"><span data-stu-id="be049-148">The rest of the methods are specific to its use; there are customized versions for address book, message store, and transport providers, and for configuration support.</span></span> <span data-ttu-id="be049-149">たとえば、アドレス帳のサポート オブジェクトには、詳細とカスタム受信者のダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="be049-149">For example, the address book support object displays details and custom recipient dialog boxes.</span></span> <span data-ttu-id="be049-150">メッセージ ストアのサポート オブジェクトは、フォルダーとメッセージのコピー操作と移動操作をサポートします。</span><span class="sxs-lookup"><span data-stu-id="be049-150">The message store support object supports copy and move operations for folders and messages.</span></span> <span data-ttu-id="be049-151">トランスポート プロバイダーのサポート オブジェクトには、MAPI スプーラーとの対話を容易にするメソッドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="be049-151">The transport provider support object includes methods for facilitating interaction with the MAPI spooler.</span></span> 
  
<span data-ttu-id="be049-152">一部のサービス プロバイダーは、MAPI が実装するユーティリティ オブジェクトであるテーブル データおよびプロパティ データ オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="be049-152">Some service providers use table data and property data objects — utility objects that MAPI implements.</span></span> <span data-ttu-id="be049-153">テーブル データ オブジェクトを使用すると、サービス プロバイダーはテーブルの基になるデータを管理できます。</span><span class="sxs-lookup"><span data-stu-id="be049-153">Table data objects enable service providers to manage the underlying data of a table.</span></span> <span data-ttu-id="be049-154">プロパティ データ オブジェクトを使用すると、サービス プロバイダーはオブジェクトとプロパティへのアクセスを設定できます。</span><span class="sxs-lookup"><span data-stu-id="be049-154">Property data objects enable service providers to set object and property access.</span></span> 
  
<span data-ttu-id="be049-155">プロパティを転送するためのトランスポート ニュートラル カプセル化形式 (TNEF) をサポートするトランスポート プロバイダーは [、ITnef : IUnknown](itnefiunknown.md) インターフェイスをサポートするために MAPI が実装する TNEF オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="be049-155">Transport providers that support the Transport Neutral Encapsulation Format (TNEF) for transferring properties use a TNEF object that MAPI implements to support the [ITnef : IUnknown](itnefiunknown.md) interface.</span></span> <span data-ttu-id="be049-156">詳細については、「Developing [a TNEF-Enabled トランスポート プロバイダー」を参照してください](developing-a-tnef-enabled-transport-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="be049-156">For more information, see [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="be049-157">関連項目</span><span class="sxs-lookup"><span data-stu-id="be049-157">See also</span></span>



[<span data-ttu-id="be049-158">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="be049-158">ITnef : IUnknown</span></span>](itnefiunknown.md)
  
[<span data-ttu-id="be049-159">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="be049-159">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)
  
[<span data-ttu-id="be049-160">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="be049-160">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)
  
[<span data-ttu-id="be049-161">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="be049-161">IABProvider : IUnknown</span></span>](iabprovideriunknown.md)
  
[<span data-ttu-id="be049-162">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="be049-162">IABLogon : IUnknown</span></span>](iablogoniunknown.md)
  
[<span data-ttu-id="be049-163">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="be049-163">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)
  
[<span data-ttu-id="be049-164">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="be049-164">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)


[<span data-ttu-id="be049-165">トランスポート プロバイダーTNEF-Enabled開発する</span><span class="sxs-lookup"><span data-stu-id="be049-165">Developing a TNEF-Enabled Transport Provider</span></span>](developing-a-tnef-enabled-transport-provider.md)

