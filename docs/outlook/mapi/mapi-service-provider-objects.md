---
title: MAPI サービスプロバイダオブジェクト
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
# <a name="mapi-service-provider-objects"></a><span data-ttu-id="cbb53-103">MAPI サービスプロバイダオブジェクト</span><span class="sxs-lookup"><span data-stu-id="cbb53-103">MAPI Service Provider Objects</span></span>

  
  
<span data-ttu-id="cbb53-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cbb53-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cbb53-105">サービスプロバイダーは、多くのオブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="cbb53-105">Service providers implement many objects.</span></span> <span data-ttu-id="cbb53-106">一部は、主に MAPI で使用され、一部はクライアントアプリケーションによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="cbb53-106">Some are used primarily by MAPI and some are used by client applications.</span></span> <span data-ttu-id="cbb53-107">一部のオブジェクトは、すべての種類のサービスプロバイダーで実装されています。rest は、単一のプロバイダーの種類に固有のものです。</span><span class="sxs-lookup"><span data-stu-id="cbb53-107">A few objects are implemented by all types of service providers; the rest are specific to a single provider type.</span></span> <span data-ttu-id="cbb53-108">次の表では、すべてのサービスプロバイダオブジェクトについて説明します。</span><span class="sxs-lookup"><span data-stu-id="cbb53-108">The following table describes all of the service provider objects.</span></span>
  
|<span data-ttu-id="cbb53-109">**サービスプロバイダオブジェクト**</span><span class="sxs-lookup"><span data-stu-id="cbb53-109">**Service provider object**</span></span>|<span data-ttu-id="cbb53-110">**説明**</span><span class="sxs-lookup"><span data-stu-id="cbb53-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cbb53-111">アドレス帳コンテナー</span><span class="sxs-lookup"><span data-stu-id="cbb53-111">Address book container</span></span>  <br/> |<span data-ttu-id="cbb53-112">アクティブなプロファイル内の1つのアドレス帳プロバイダーの受信者の情報が含まれています。アドレス帳プロバイダーには、1つ以上のアドレス帳コンテナーを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="cbb53-112">Contains recipient information for one address book provider in the active profile; address book providers can have one or more address book containers.</span></span>  <br/> |
|<span data-ttu-id="cbb53-113">添付ファイル</span><span class="sxs-lookup"><span data-stu-id="cbb53-113">Attachment</span></span>  <br/> |<span data-ttu-id="cbb53-114">メッセージに関連付けられるファイルまたは OLE オブジェクトなどの追加データが含まれています。</span><span class="sxs-lookup"><span data-stu-id="cbb53-114">Contains additional data, such as a file or OLE object, to be associated with a message.</span></span>  <br/> |
|<span data-ttu-id="cbb53-115">コントロール</span><span class="sxs-lookup"><span data-stu-id="cbb53-115">Control</span></span>  <br/> |<span data-ttu-id="cbb53-116">ボタンを有効または無効にし、ボタンがクリックされたときの処理を開始します。</span><span class="sxs-lookup"><span data-stu-id="cbb53-116">Enables or disables a button and initiates processing when the button is clicked.</span></span>  <br/> |
|<span data-ttu-id="cbb53-117">配布リスト</span><span class="sxs-lookup"><span data-stu-id="cbb53-117">Distribution list</span></span>  <br/> |<span data-ttu-id="cbb53-118">個々のメッセージの受信者のグループについて説明します。</span><span class="sxs-lookup"><span data-stu-id="cbb53-118">Describes a grouping of individual message recipients.</span></span>  <br/> |
|<span data-ttu-id="cbb53-119">フォルダー</span><span class="sxs-lookup"><span data-stu-id="cbb53-119">Folder</span></span>  <br/> |<span data-ttu-id="cbb53-120">メッセージおよびその他のメッセージコンテナーが保存されています。</span><span class="sxs-lookup"><span data-stu-id="cbb53-120">Contains messages and other message containers.</span></span>  <br/> |
|<span data-ttu-id="cbb53-121">Logon</span><span class="sxs-lookup"><span data-stu-id="cbb53-121">Logon</span></span>  <br/> |<span data-ttu-id="cbb53-122">サービスプロバイダーのイベント通知とクライアント要求を処理します。</span><span class="sxs-lookup"><span data-stu-id="cbb53-122">Handles service provider event notification and client requests.</span></span>  <br/> |
|<span data-ttu-id="cbb53-123">メッセージングユーザー</span><span class="sxs-lookup"><span data-stu-id="cbb53-123">Messaging user</span></span>  <br/> |<span data-ttu-id="cbb53-124">メッセージの個々の受信者を表します。</span><span class="sxs-lookup"><span data-stu-id="cbb53-124">Describes an individual recipient of a message.</span></span>  <br/> |
|<span data-ttu-id="cbb53-125">Message</span><span class="sxs-lookup"><span data-stu-id="cbb53-125">Message</span></span>  <br/> |<span data-ttu-id="cbb53-126">1人または複数の受信者に送信できる情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cbb53-126">Contains information that can be sent to one or more recipients.</span></span>  <br/> |
|<span data-ttu-id="cbb53-127">メッセージストア</span><span class="sxs-lookup"><span data-stu-id="cbb53-127">Message store</span></span>  <br/> |<span data-ttu-id="cbb53-128">階層構造のメッセージのデータベースとして機能します。</span><span class="sxs-lookup"><span data-stu-id="cbb53-128">Acts as a hierarchically organized database of messages.</span></span>  <br/> |
|<span data-ttu-id="cbb53-129">プロバイダー</span><span class="sxs-lookup"><span data-stu-id="cbb53-129">Provider</span></span>  <br/> |<span data-ttu-id="cbb53-130">サービスプロバイダーの起動およびシャットダウンを処理します。</span><span class="sxs-lookup"><span data-stu-id="cbb53-130">Handles service provider startup and shutdown.</span></span>  <br/> |
|<span data-ttu-id="cbb53-131">スプーラーフック</span><span class="sxs-lookup"><span data-stu-id="cbb53-131">Spooler hook</span></span>  <br/> |<span data-ttu-id="cbb53-132">受信メッセージと送信メッセージに対して特別な処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="cbb53-132">Performs special processing on inbound and outbound messages.</span></span>  <br/> |
|<span data-ttu-id="cbb53-133">状態</span><span class="sxs-lookup"><span data-stu-id="cbb53-133">Status</span></span>  <br/> |<span data-ttu-id="cbb53-134">サービスプロバイダーの状態へのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="cbb53-134">Provides access to the service provider's state.</span></span>  <br/> |
|<span data-ttu-id="cbb53-135">Table</span><span class="sxs-lookup"><span data-stu-id="cbb53-135">Table</span></span>  <br/> |<span data-ttu-id="cbb53-136">データベーステーブルと同様に、行と列の形式でのオブジェクトデータの概要ビューへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="cbb53-136">Provides access to a summary view of object data in row and column format, similar to a database table.</span></span>  <br/> |
   
<span data-ttu-id="cbb53-137">すべてのサービスプロバイダーは、プロバイダーオブジェクトとログオンオブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="cbb53-137">All service providers implement a provider object and a logon object.</span></span> <span data-ttu-id="cbb53-138">プロバイダーオブジェクトは、ブックの場合にのみ使用できます。これらは MAPI によって使用され、スタートアップおよびシャットダウンプロセスを制御します。</span><span class="sxs-lookup"><span data-stu-id="cbb53-138">Provider objects are strictly for bookkeeping; they are used by MAPI to control the startup and shutdown processes.</span></span> <span data-ttu-id="cbb53-139">ログオンオブジェクトサービス一部のクライアント要求を間接的に行います。</span><span class="sxs-lookup"><span data-stu-id="cbb53-139">Logon objects service some client requests indirectly.</span></span> <span data-ttu-id="cbb53-140">たとえば、メッセージストアプロバイダーのログオンオブジェクトは、通知の登録と、メッセージストアオブジェクトを開くための要求を処理します。</span><span class="sxs-lookup"><span data-stu-id="cbb53-140">For example, the message store provider's logon object handles notification registration and requests to open message store objects.</span></span> 
  
<span data-ttu-id="cbb53-141">プロバイダーおよびログオンオブジェクトは、実装を提供するサービスプロバイダーの種類に応じて、異なるインターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="cbb53-141">Provider and logon objects implement a different interface depending on the type of service provider that supplies the implementation.</span></span> <span data-ttu-id="cbb53-142">メッセージストアプロバイダーは、プロバイダーおよびログオンオブジェクトに[IMSProvider: iunknown](imsprovideriunknown.md)インターフェイスと[IMSLogon: iunknown](imslogoniunknown.md)インターフェイスを実装します。アドレス帳プロバイダーは[IABProvider: iunknown](iabprovideriunknown.md)および[IABLogon:](iablogoniunknown.md) iunknown を実装します。インターフェイス、トランスポートプロバイダーは[ixpprovider: iunknown](ixpprovideriunknown.md)インターフェイスと[IXPLogon: iunknown](ixplogoniunknown.md)インターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="cbb53-142">A message store provider implements the [IMSProvider : IUnknown](imsprovideriunknown.md) and [IMSLogon : IUnknown](imslogoniunknown.md) interfaces in its provider and logon objects, an address book provider implements the [IABProvider : IUnknown](iabprovideriunknown.md) and [IABLogon : IUnknown](iablogoniunknown.md) interfaces, and a transport provider implements the [IXPProvider : IUnknown](ixpprovideriunknown.md) and [IXPLogon : IUnknown](ixplogoniunknown.md) interfaces.</span></span> 
  
<span data-ttu-id="cbb53-143">メッセージフックプロバイダーは、スプーラーフックオブジェクト、または受信メッセージと送信メッセージをフィルター処理するオブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="cbb53-143">Message hook providers implement spooler hook objects, or objects that filter inbound and outbound messages.</span></span>
  
<span data-ttu-id="cbb53-144">通常、サービスプロバイダーは少数のオブジェクトのみを使用します。</span><span class="sxs-lookup"><span data-stu-id="cbb53-144">Service providers typically use only a few objects.</span></span> <span data-ttu-id="cbb53-145">多くの場合、クライアント要求を実装するために、MAPI が提供するサポートオブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="cbb53-145">Most frequently, they use a support object that MAPI provides to help implement client requests.</span></span> <span data-ttu-id="cbb53-146">support オブジェクトは、そのオブジェクトを使用しているプロバイダーの種類に合わせてカスタマイズされています。</span><span class="sxs-lookup"><span data-stu-id="cbb53-146">The support object is customized for the type of provider that is using it.</span></span> <span data-ttu-id="cbb53-147">すべてのサービスプロバイダーについて、support オブジェクトには、イベント通知の処理、構成プロパティの表示、オブジェクトの開始、およびエラー処理のメソッドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="cbb53-147">For all service providers, the support object includes methods for handling event notification, displaying configuration properties, opening objects, and error handling.</span></span> <span data-ttu-id="cbb53-148">その他のメソッドは、その使い方に固有のものです。アドレス帳、メッセージストア、およびトランスポートプロバイダーのカスタマイズされたバージョン、および構成のサポートがあります。</span><span class="sxs-lookup"><span data-stu-id="cbb53-148">The rest of the methods are specific to its use; there are customized versions for address book, message store, and transport providers, and for configuration support.</span></span> <span data-ttu-id="cbb53-149">たとえば、アドレス帳のサポートオブジェクトには、詳細とカスタム受信者のダイアログボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="cbb53-149">For example, the address book support object displays details and custom recipient dialog boxes.</span></span> <span data-ttu-id="cbb53-150">メッセージストアサポートオブジェクトは、フォルダーとメッセージのコピー操作と移動操作をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="cbb53-150">The message store support object supports copy and move operations for folders and messages.</span></span> <span data-ttu-id="cbb53-151">トランスポートプロバイダーのサポートオブジェクトには、MAPI スプーラーとの対話を容易にするためのメソッドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="cbb53-151">The transport provider support object includes methods for facilitating interaction with the MAPI spooler.</span></span> 
  
<span data-ttu-id="cbb53-152">一部のサービスプロバイダーは、テーブルデータおよびプロパティデータオブジェクトを使用します。このユーティリティオブジェクトは、MAPI で実装されます。</span><span class="sxs-lookup"><span data-stu-id="cbb53-152">Some service providers use table data and property data objects — utility objects that MAPI implements.</span></span> <span data-ttu-id="cbb53-153">テーブルデータオブジェクトを使用すると、サービスプロバイダーは、テーブルの基になるデータを管理できます。</span><span class="sxs-lookup"><span data-stu-id="cbb53-153">Table data objects enable service providers to manage the underlying data of a table.</span></span> <span data-ttu-id="cbb53-154">プロパティデータオブジェクトを使用すると、サービスプロバイダーは、オブジェクトおよびプロパティへのアクセスを設定できます。</span><span class="sxs-lookup"><span data-stu-id="cbb53-154">Property data objects enable service providers to set object and property access.</span></span> 
  
<span data-ttu-id="cbb53-155">プロパティを転送するためのトランスポートニュートラルカプセル化形式 (tnef) をサポートするトランスポートプロバイダーは、 [ITnef: IUnknown](itnefiunknown.md)インターフェイスをサポートするために MAPI に実装されている TNEF オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="cbb53-155">Transport providers that support the Transport Neutral Encapsulation Format (TNEF) for transferring properties use a TNEF object that MAPI implements to support the [ITnef : IUnknown](itnefiunknown.md) interface.</span></span> <span data-ttu-id="cbb53-156">詳細については、「 [TNEF 対応のトランスポートプロバイダーを開発する](developing-a-tnef-enabled-transport-provider.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cbb53-156">For more information, see [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cbb53-157">関連項目</span><span class="sxs-lookup"><span data-stu-id="cbb53-157">See also</span></span>



[<span data-ttu-id="cbb53-158">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cbb53-158">ITnef : IUnknown</span></span>](itnefiunknown.md)
  
[<span data-ttu-id="cbb53-159">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cbb53-159">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)
  
[<span data-ttu-id="cbb53-160">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cbb53-160">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)
  
[<span data-ttu-id="cbb53-161">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cbb53-161">IABProvider : IUnknown</span></span>](iabprovideriunknown.md)
  
[<span data-ttu-id="cbb53-162">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cbb53-162">IABLogon : IUnknown</span></span>](iablogoniunknown.md)
  
[<span data-ttu-id="cbb53-163">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cbb53-163">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)
  
[<span data-ttu-id="cbb53-164">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cbb53-164">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)


[<span data-ttu-id="cbb53-165">TNEF 対応のトランスポートプロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="cbb53-165">Developing a TNEF-Enabled Transport Provider</span></span>](developing-a-tnef-enabled-transport-provider.md)

