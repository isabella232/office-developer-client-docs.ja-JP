---
title: MAPI へのログオン
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 05bafe43-a78a-4659-92f0-0b4fe444c64f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: cce43301ac73a5646e263b2ab92700e57804637d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419710"
---
# <a name="logging-on-to-mapi"></a><span data-ttu-id="0d028-103">MAPI へのログオン</span><span class="sxs-lookup"><span data-stu-id="0d028-103">Logging on to MAPI</span></span>
 
<span data-ttu-id="0d028-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d028-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d028-105">クライアント アプリケーションは、MAPILogonEx 関数を呼び出して **MAPI サブシステムにログオン** します。</span><span class="sxs-lookup"><span data-stu-id="0d028-105">Client applications log on to the MAPI subsystem by calling the **MAPILogonEx** function.</span></span> <span data-ttu-id="0d028-106">詳細については [、「MAPILogonEx」を参照してください](mapilogonex.md)。</span><span class="sxs-lookup"><span data-stu-id="0d028-106">For more information, see [MAPILogonEx](mapilogonex.md).</span></span> <span data-ttu-id="0d028-107">**MAPILogonEx** は、プロファイルの選択と、プロファイル内の各サービス プロバイダーの構成を検証します。</span><span class="sxs-lookup"><span data-stu-id="0d028-107">**MAPILogonEx** validates the profile selection and the configuration of each service provider in the profile.</span></span> <span data-ttu-id="0d028-108">構成が完了すると、MAPI はメッセージ ストア プロバイダーを開始する前にアドレス帳プロバイダーを開始します。</span><span class="sxs-lookup"><span data-stu-id="0d028-108">Once configured, MAPI starts the address book providers before starting the message store providers.</span></span> <span data-ttu-id="0d028-109">トランスポート プロバイダーは、サービスが最初に必要なときに開始されます。</span><span class="sxs-lookup"><span data-stu-id="0d028-109">Transport providers are started when their services are first required.</span></span> 
  
## <a name="choose-a-profile"></a><span data-ttu-id="0d028-110">プロファイルの選択</span><span class="sxs-lookup"><span data-stu-id="0d028-110">Choose a profile</span></span>
  
- <span data-ttu-id="0d028-111">_lpszProfileName_ パラメーター内のプロファイルの名前を表す文字列を **MAPILogonEx** に渡します。</span><span class="sxs-lookup"><span data-stu-id="0d028-111">Pass in a character string that represents the name of the profile in the  _lpszProfileName_ parameter to **MAPILogonEx**, or...</span></span>
    
- <span data-ttu-id="0d028-112">_lpszProfileName_ パラメーターに NULL を渡し、MAPI_LOGON_UIフラグを設定することで、プロファイルを指定できます。</span><span class="sxs-lookup"><span data-stu-id="0d028-112">Allow the user to specify the profile by passing NULL in the  _lpszProfileName_ parameter and setting the MAPI_LOGON_UI flag, or...</span></span> 

- <span data-ttu-id="0d028-113">_lpszProfileName_ パラメーターに NULL を渡し、既定のプロファイルフラグをMAPI_USE_DEFAULTします。</span><span class="sxs-lookup"><span data-stu-id="0d028-113">Select the default profile by passing NULL in the  _lpszProfileName_ parameter and setting the MAPI_USE_DEFAULT flag.</span></span> 
    
<span data-ttu-id="0d028-114">既定のプロファイル以外の特定のプロファイルが必要な場合は、その名前を独自の構成データベースに保存するか、特定の名前付け規則を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d028-114">If you require a specific profile other than the default profile, you must save its name in your own configuration database or use a specific naming convention.</span></span> <span data-ttu-id="0d028-115">MAPI では、プロファイル テーブルの名前と既定のフラグ以外のプロファイル属性は公開されません。既定のプロファイル フラグはメッセージング クライアントおよび関連する IPM アプリケーション用に予約されています。</span><span class="sxs-lookup"><span data-stu-id="0d028-115">MAPI does not expose any profile attributes other than the name and default flag in the profile table, and the default profile flag is reserved for messaging client and related IPM applications.</span></span>
  
<span data-ttu-id="0d028-116">**MAPILogonEx** に部分的なプロファイルまたはプロバイダー構成情報を提供するクライアントは、ダイアログ ボックスを表示できるようにして、ユーザーに追加データの入力を求める必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d028-116">Clients that supply partial profile or provider configuration information to **MAPILogonEx** must prompt the user for the additional data by allowing a dialog box to be displayed.</span></span> <span data-ttu-id="0d028-117">情報が不足し **、MAPILogonEx** がユーザーに入力を求めできない場合、ログオンは失敗します。</span><span class="sxs-lookup"><span data-stu-id="0d028-117">If information is missing and **MAPILogonEx** cannot prompt the user to supply it, the logon fails.</span></span> <span data-ttu-id="0d028-118">ユーザー入力を必要としないクライアントは、ダイアログ ボックスの表示を抑制できます。</span><span class="sxs-lookup"><span data-stu-id="0d028-118">Clients that do not need user input can suppress the dialog box display.</span></span> 
  
<span data-ttu-id="0d028-119">**MAPILogonEx がユーザー** インターフェイスを有効にするために使用するフラグは、相互に排他的です。設定できるのは 1 つのみです。</span><span class="sxs-lookup"><span data-stu-id="0d028-119">The flags that **MAPILogonEx** uses to enable a user interface are mutually exclusive; only one can be set.</span></span> <span data-ttu-id="0d028-120">これらのフラグを設定解除すると、ユーザー インターフェイスの表示が抑制され、必要な情報が見つからない場合 **に MAPILogonEx** が失敗します。</span><span class="sxs-lookup"><span data-stu-id="0d028-120">Leaving these flags unset suppresses the display of a user interface, causing **MAPILogonEx** to fail if necessary information is missing.</span></span> <span data-ttu-id="0d028-121">つまり、ユーザー インターフェイスを無効にし  _、lpszProfileName_ パラメーターに NULL を渡し、MAPI_USE_DEFAULT フラグを設定しない場合 **、MAPILogonEx** はプロファイル名を取得できないので失敗します。</span><span class="sxs-lookup"><span data-stu-id="0d028-121">That is, if you disable the user interface and pass NULL for the  _lpszProfileName_ parameter and do not set the MAPI_USE_DEFAULT flag, **MAPILogonEx** will fail because it cannot retrieve a profile name.</span></span> 
  
<span data-ttu-id="0d028-122">**MAPILogonEx** が確立するセッションには、個別のメッセージング セッション、共有メッセージング セッション、または非messaging セッションを指定できます。</span><span class="sxs-lookup"><span data-stu-id="0d028-122">The session that **MAPILogonEx** establishes can be an individual messaging session, a shared messaging session, or a nonmessaging session.</span></span> <span data-ttu-id="0d028-123">個々のメッセージング セッションは、クライアントと MAPI サブシステム間のプライベート接続であり **、MAPILogonEx** への呼び出しで MAPI_NEW_SESSION フラグを設定することで確立できます。</span><span class="sxs-lookup"><span data-stu-id="0d028-123">Individual messaging sessions are private connections between your client and the MAPI subsystem and can be established by setting the MAPI_NEW_SESSION flag in the call to **MAPILogonEx**.</span></span>
  
<span data-ttu-id="0d028-124">共有メッセージング セッションは、複数のメッセージング クライアントが使用できる接続です。</span><span class="sxs-lookup"><span data-stu-id="0d028-124">Shared messaging sessions are connections that multiple messaging clients can use.</span></span> <span data-ttu-id="0d028-125">共有セッションは、通常、クライアントが同じプロファイルを使用するために確立されます。</span><span class="sxs-lookup"><span data-stu-id="0d028-125">Shared sessions are typically established for clients use the same profile.</span></span> <span data-ttu-id="0d028-126">共有セッションとして新しいセッションを確立するには、MAPI_ALLOW_OTHERS設定します。</span><span class="sxs-lookup"><span data-stu-id="0d028-126">To establish a new session as a shared session, set the MAPI_ALLOW_OTHERS flag.</span></span> 
  
## <a name="use-an-existing-shared-session"></a><span data-ttu-id="0d028-127">既存の共有セッションを使用する</span><span class="sxs-lookup"><span data-stu-id="0d028-127">Use an existing shared session</span></span>
  
- <span data-ttu-id="0d028-128">このフラグを設定MAPI_NEW_SESSIONしない。</span><span class="sxs-lookup"><span data-stu-id="0d028-128">Do not set the MAPI_NEW_SESSION flag.</span></span>
    
- <span data-ttu-id="0d028-129">このフラグを設定MAPI_ALLOW_OTHERSしない。</span><span class="sxs-lookup"><span data-stu-id="0d028-129">Do not set the MAPI_ALLOW_OTHERS flag.</span></span>
    
- <span data-ttu-id="0d028-130">_lpszProfileName パラメーターに NULL を渡_ します。</span><span class="sxs-lookup"><span data-stu-id="0d028-130">Pass NULL for the  _lpszProfileName_ parameter.</span></span> 
    
- <span data-ttu-id="0d028-131">_lpszPassword パラメーターに NULL を渡_ します。</span><span class="sxs-lookup"><span data-stu-id="0d028-131">Pass NULL for the  _lpszPassword_ parameter.</span></span> 
    
<span data-ttu-id="0d028-132">非messaging セッションでは、クライアントは MAPI サブシステムにアクセスできますが、メッセージの送信または受信は許可されません。</span><span class="sxs-lookup"><span data-stu-id="0d028-132">Nonmessaging sessions allow clients to access the MAPI subsystem, but do not allow messages to be sent or received.</span></span> <span data-ttu-id="0d028-133">構成アプリケーションまたは管理アプリケーションは、非messaging セッションを確立する必要がある可能性があるクライアントの例です。</span><span class="sxs-lookup"><span data-stu-id="0d028-133">Configuration or administration applications are examples of clients that might need to establish nonmessaging sessions.</span></span> <span data-ttu-id="0d028-134">非messaging セッションを要求するには、次のフラグMAPI_NO_MAILします。</span><span class="sxs-lookup"><span data-stu-id="0d028-134">To request a nonmessaging session, set the MAPI_NO_MAIL flag.</span></span> <span data-ttu-id="0d028-135">このフラグを設定すると、MAPI スプーラーに通知せずにクライアントがログオンします。</span><span class="sxs-lookup"><span data-stu-id="0d028-135">Setting this flag logs your client on without informing the MAPI spooler.</span></span> <span data-ttu-id="0d028-136">このフラグを使用して MAPI にログオンするクライアントは、読み取り状態レポートを受け取る必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d028-136">Clients that log on to MAPI with this flag cannot expect to ever receive read status reports.</span></span>
  
<span data-ttu-id="0d028-137">次MAPI_NO_MAILフラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d028-137">The MAPI_NO_MAIL flag should only be set:</span></span>
  
- <span data-ttu-id="0d028-138">セッション中にクライアントがメッセージを送受信しない場合。</span><span class="sxs-lookup"><span data-stu-id="0d028-138">If your client will not send or receive messages during the session.</span></span>
    
- <span data-ttu-id="0d028-139">クライアントがプロファイルの内容を完全に制御し、Microsoft Exchange プロバイダーなどの緊密に結合されたメッセージ ストアとトランスポート プロバイダーを使用してメッセージを送信および受信する場合。</span><span class="sxs-lookup"><span data-stu-id="0d028-139">If your client has complete control over the contents of the profile and messages are sent and received using tightly coupled message store and transport providers, such as the Microsoft Exchange providers.</span></span>
    
<span data-ttu-id="0d028-140">メッセージング クライアントは、セッションを非メッシュクライアントと共有できます。</span><span class="sxs-lookup"><span data-stu-id="0d028-140">A messaging client can share a session with a nonmessaging client.</span></span> <span data-ttu-id="0d028-141">共有セッションの 1 つのメンバーの特性は、他のメンバーの特性の影響を受け取る必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d028-141">The characteristics of one member of a shared session are not affected by the characteristics of other members.</span></span> <span data-ttu-id="0d028-142">つまり、MAPI_NO_MAIL フラグと MAPI_ALLOW_OTHERS フラグセットを使用してログオンすると、セッションにログオンするメッセージング クライアントはクライアントの操作に影響を与え、その逆も影響を受け取らなくなります。</span><span class="sxs-lookup"><span data-stu-id="0d028-142">That is, if you log on with the MAPI_NO_MAIL and MAPI_ALLOW_OTHERS flags set, a messaging client logging on to your session has no affect on the operation of your client and vice versa.</span></span> <span data-ttu-id="0d028-143">メッセージング クライアントは引き続きメッセージを送受信できます。クライアントはメッセージを送受信しません。</span><span class="sxs-lookup"><span data-stu-id="0d028-143">The messaging client will still be able to send and receive messages and your client will not.</span></span>
  
<span data-ttu-id="0d028-144">**MAPILogonEx には** 、設定できるその他のフラグがいくつか定義されています。</span><span class="sxs-lookup"><span data-stu-id="0d028-144">**MAPILogonEx** defines a few other flags that you can set:</span></span> 
  
- <span data-ttu-id="0d028-145">MAPI_FORCE_DOWNLOAD MAPILogonEx が返される前に受信メッセージをダウンロード **する必要があります。**</span><span class="sxs-lookup"><span data-stu-id="0d028-145">MAPI_FORCE_DOWNLOAD indicates that incoming messages should be downloaded before **MAPILogonEx** returns.</span></span> <span data-ttu-id="0d028-146">このフラグを設定しない場合、メッセージは後でバックグラウンドでダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="0d028-146">Not setting this flag causes messages to be downloaded in the background at a later time.</span></span> 
    
- <span data-ttu-id="0d028-147">MAPI_SERVICE_UI_ALWAYS内のすべてのメッセージ サービスに構成ダイアログ ボックスが表示されるという要求があります。</span><span class="sxs-lookup"><span data-stu-id="0d028-147">MAPI_SERVICE_UI_ALWAYS requests that every message service in the profile display a configuration dialog box.</span></span>
    
- <span data-ttu-id="0d028-148">MAPI_NT_SERVICEクライアントがサービスとして実装Windowsします。</span><span class="sxs-lookup"><span data-stu-id="0d028-148">MAPI_NT_SERVICE indicates that your client is implemented as a Windows service.</span></span> <span data-ttu-id="0d028-149">クライアントがサービスの場合は、このフラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d028-149">This flag must be set if your client is a service.</span></span>
    
<span data-ttu-id="0d028-150">ログオンが成功すると **、MAPILogonEx** は MAPI セッションへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="0d028-150">With every successful logon, **MAPILogonEx** returns a pointer to a MAPI session.</span></span> <span data-ttu-id="0d028-151">このポインターを使用して **、IMAPISession インターフェイスのメソッドを呼び出** します。</span><span class="sxs-lookup"><span data-stu-id="0d028-151">You can use this pointer to call the methods of the **IMAPISession** interface.</span></span> <span data-ttu-id="0d028-152">詳細については [、「IMAPISession : IUnknown 」を参照してください](imapisessioniunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="0d028-152">For more information, see [IMAPISession : IUnknown](imapisessioniunknown.md).</span></span> <span data-ttu-id="0d028-153">セッション ポインターは、セッションの種類に関係なく、それらを受け取るクライアントに固有であり、タスク間では無効です。</span><span class="sxs-lookup"><span data-stu-id="0d028-153">Session pointers, regardless of the type of session, are unique to the clients that receive them and are not valid across tasks.</span></span>
  

