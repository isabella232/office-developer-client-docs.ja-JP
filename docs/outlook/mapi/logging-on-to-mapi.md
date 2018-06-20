---
title: MAPI にログオンします。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 05bafe43-a78a-4659-92f0-0b4fe444c64f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1ae3c47964ff238f57e98e0005a966008192f7c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801296"
---
# <a name="logging-on-to-mapi"></a><span data-ttu-id="2dd2e-103">MAPI にログオンします。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-103">Logging on to MAPI</span></span>
 
<span data-ttu-id="2dd2e-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2dd2e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2dd2e-105">**MAPILogonEx**関数を呼び出すことによって、MAPI サブシステムには、クライアント アプリケーションがログオンするとします。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-105">Client applications log on to the MAPI subsystem by calling the **MAPILogonEx** function.</span></span> <span data-ttu-id="2dd2e-106">詳細については、 [MAPILogonEx](mapilogonex.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-106">For more information, see [MAPILogonEx](mapilogonex.md).</span></span> <span data-ttu-id="2dd2e-107">**MAPILogonEx**では、プロファイルの選択と、プロファイル内の各サービス プロバイダーの構成を検証します。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-107">**MAPILogonEx** validates the profile selection and the configuration of each service provider in the profile.</span></span> <span data-ttu-id="2dd2e-108">構成にすると、MAPI は、メッセージ ストア プロバイダーを開始する前に、アドレス帳プロバイダーを起動します。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-108">Once configured, MAPI starts the address book providers before starting the message store providers.</span></span> <span data-ttu-id="2dd2e-109">トランスポート プロバイダーは、そのサービスは、まず、必要なときに開始されます。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-109">Transport providers are started when their services are first required.</span></span> 
  
## <a name="choose-a-profile"></a><span data-ttu-id="2dd2e-110">プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-110">Choose a profile</span></span>
  
- <span data-ttu-id="2dd2e-111">**MAPILogonEx**、 _lpszProfileName_パラメーターにプロファイルの名前を表す文字列を渡すか、.</span><span class="sxs-lookup"><span data-stu-id="2dd2e-111">Pass in a character string that represents the name of the profile in the  _lpszProfileName_ parameter to **MAPILogonEx**, or...</span></span>
    
- <span data-ttu-id="2dd2e-112">プロファイルを指定するには、 _lpszProfileName_パラメーターに NULL を渡すと、MAPI_LOGON_UI フラグを設定するユーザーを許可するか、.</span><span class="sxs-lookup"><span data-stu-id="2dd2e-112">Allow the user to specify the profile by passing NULL in the  _lpszProfileName_ parameter and setting the MAPI_LOGON_UI flag, or...</span></span> 

- <span data-ttu-id="2dd2e-113">既定のプロファイルを選択するには、 _lpszProfileName_パラメーターに NULL を渡すと、MAPI_USE_DEFAULT フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-113">Select the default profile by passing NULL in the  _lpszProfileName_ parameter and setting the MAPI_USE_DEFAULT flag.</span></span> 
    
<span data-ttu-id="2dd2e-114">デフォルトのプロファイル以外の特定のプロファイルを必要とする場合の構成データベースの名前を保存するか、特定の命名規則を使用してください。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-114">If you require a specific profile other than the default profile, you must save its name in your own configuration database or use a specific naming convention.</span></span> <span data-ttu-id="2dd2e-115">MAPI は、プロファイル テーブルの名前と既定のフラグ以外のすべてのプロファイル属性を公開していないと、メッセージング クライアントおよび関連する IPM アプリケーションの既定のプロファイル フラグが予約されています。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-115">MAPI does not expose any profile attributes other than the name and default flag in the profile table, and the default profile flag is reserved for messaging client and related IPM applications.</span></span>
  
<span data-ttu-id="2dd2e-116">部分的なプロファイル] または [ **MAPILogonEx**プロバイダーの構成情報を提供するクライアントでは、表示されるダイアログ ボックスを許可することでユーザーに追加のデータを求める必要があります。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-116">Clients that supply partial profile or provider configuration information to **MAPILogonEx** must prompt the user for the additional data by allowing a dialog box to be displayed.</span></span> <span data-ttu-id="2dd2e-117">情報が不足しているユーザーにそれを入力することはできません**MAPILogonEx**の入力を求める場合は、ログオンが失敗します。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-117">If information is missing and **MAPILogonEx** cannot prompt the user to supply it, the logon fails.</span></span> <span data-ttu-id="2dd2e-118">しない必要があるユーザーの入力を実行するクライアントでは、ダイアログ ボックスの表示を抑制できます。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-118">Clients that do not need user input can suppress the dialog box display.</span></span> 
  
<span data-ttu-id="2dd2e-119">**MAPILogonEx**を使用してユーザー インターフェイスを有効にするためのフラグは相互に排他的です。1 つだけを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-119">The flags that **MAPILogonEx** uses to enable a user interface are mutually exclusive; only one can be set.</span></span> <span data-ttu-id="2dd2e-120">これらのフラグを設定しないまま、必要な情報が存在しない場合にエラーが発生する**MAPILogonEx**の原因で、ユーザー インターフェイスの表示を抑制します。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-120">Leaving these flags unset suppresses the display of a user interface, causing **MAPILogonEx** to fail if necessary information is missing.</span></span> <span data-ttu-id="2dd2e-121">つまり、 _lpszProfileName_パラメーターに NULL を渡すと、MAPI_USE_DEFAULT フラグを設定しないし、ユーザー ・ インタ フェースを無効にする場合、は、 **MAPILogonEx**はプロファイル名を取得できないために失敗します。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-121">That is, if you disable the user interface and pass NULL for the  _lpszProfileName_ parameter and do not set the MAPI_USE_DEFAULT flag, **MAPILogonEx** will fail because it cannot retrieve a profile name.</span></span> 
  
<span data-ttu-id="2dd2e-122">**MAPILogonEx**が確立したセッションには、個別のメッセージング セッション、メッセージの共有セッション、またはメッセージング セッションができます。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-122">The session that **MAPILogonEx** establishes can be an individual messaging session, a shared messaging session, or a nonmessaging session.</span></span> <span data-ttu-id="2dd2e-123">個々 のメッセージング セッション、クライアントと、MAPI サブシステムのプライベート接続は、 **MAPILogonEx**の呼び出しで、MAPI_NEW_SESSION フラグを設定することによって確立することができます。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-123">Individual messaging sessions are private connections between your client and the MAPI subsystem and can be established by setting the MAPI_NEW_SESSION flag in the call to **MAPILogonEx**.</span></span>
  
<span data-ttu-id="2dd2e-124">メッセージング セッションの共有は、複数のメッセージング クライアントを使用している接続です。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-124">Shared messaging sessions are connections that multiple messaging clients can use.</span></span> <span data-ttu-id="2dd2e-125">同じプロファイルを使用するクライアントの通常の共有セッションを確立します。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-125">Shared sessions are typically established for clients use the same profile.</span></span> <span data-ttu-id="2dd2e-126">共有セッションに新しいセッションを確立するために MAPI_ALLOW_OTHERS フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-126">To establish a new session as a shared session, set the MAPI_ALLOW_OTHERS flag.</span></span> 
  
## <a name="use-an-existing-shared-session"></a><span data-ttu-id="2dd2e-127">既存の共有セッションを使用します。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-127">Use an existing shared session</span></span>
  
- <span data-ttu-id="2dd2e-128">MAPI_NEW_SESSION フラグを設定しません。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-128">Do not set the MAPI_NEW_SESSION flag.</span></span>
    
- <span data-ttu-id="2dd2e-129">MAPI_ALLOW_OTHERS フラグを設定しません。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-129">Do not set the MAPI_ALLOW_OTHERS flag.</span></span>
    
- <span data-ttu-id="2dd2e-130">_LpszProfileName_パラメーターに NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-130">Pass NULL for the  _lpszProfileName_ parameter.</span></span> 
    
- <span data-ttu-id="2dd2e-131">_LpszPassword_パラメーターに NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-131">Pass NULL for the  _lpszPassword_ parameter.</span></span> 
    
<span data-ttu-id="2dd2e-132">メッセージング セッションでは、MAPI のサブシステムにアクセスするクライアントを許可するが、メッセージの送信または受信を許可しません。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-132">Nonmessaging sessions allow clients to access the MAPI subsystem, but do not allow messages to be sent or received.</span></span> <span data-ttu-id="2dd2e-133">構成または管理アプリケーションでは、メッセージング セッションを確立する必要があるクライアントの例を示します。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-133">Configuration or administration applications are examples of clients that might need to establish nonmessaging sessions.</span></span> <span data-ttu-id="2dd2e-134">メッセージング セッションを要求するには、MAPI_NO_MAIL フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-134">To request a nonmessaging session, set the MAPI_NO_MAIL flag.</span></span> <span data-ttu-id="2dd2e-135">このフラグを設定、MAPI スプーラーに通知せず、クライアントを記録します。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-135">Setting this flag logs your client on without informing the MAPI spooler.</span></span> <span data-ttu-id="2dd2e-136">このフラグを使用して MAPI にログオンするクライアントは、読み取りの進捗レポートを受け取ることはありませんすることはできません。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-136">Clients that log on to MAPI with this flag cannot expect to ever receive read status reports.</span></span>
  
<span data-ttu-id="2dd2e-137">MAPI_NO_MAIL フラグを設定する必要がありますのみ。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-137">The MAPI_NO_MAIL flag should only be set:</span></span>
  
- <span data-ttu-id="2dd2e-138">場合は、クライアントは、送信またはセッション中にメッセージを受信ができません。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-138">If your client will not send or receive messages during the session.</span></span>
    
- <span data-ttu-id="2dd2e-139">場合は、クライアントには、プロファイルの内容を完全に制御し、メッセージの送信し受信は密結合を使用してメッセージ ストアと、トランスポート プロバイダーは、Microsoft Exchange プロバイダー。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-139">If your client has complete control over the contents of the profile and messages are sent and received using tightly coupled message store and transport providers, such as the Microsoft Exchange providers.</span></span>
    
<span data-ttu-id="2dd2e-140">メッセージング クライアントは、メッセージング クライアントを使用してセッションを共有できます。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-140">A messaging client can share a session with a nonmessaging client.</span></span> <span data-ttu-id="2dd2e-141">共有セッションの 1 つのメンバーの特性は、他のメンバーの特性の影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-141">The characteristics of one member of a shared session are not affected by the characteristics of other members.</span></span> <span data-ttu-id="2dd2e-142">MAPI_NO_MAIL と MAPI_ALLOW_OTHERS のフラグのセットを使用してログオンする場合、セッションにログオンしているメッセージング クライアントには影響しません、クライアント、およびその逆の操作です。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-142">That is, if you log on with the MAPI_NO_MAIL and MAPI_ALLOW_OTHERS flags set, a messaging client logging on to your session has no affect on the operation of your client and vice versa.</span></span> <span data-ttu-id="2dd2e-143">メッセージング クライアントは、メッセージの送受信を行うことができ、クライアントには表示されません。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-143">The messaging client will still be able to send and receive messages and your client will not.</span></span>
  
<span data-ttu-id="2dd2e-144">**MAPILogonEx**に設定できるその他のいくつかのフラグが定義されています。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-144">**MAPILogonEx** defines a few other flags that you can set:</span></span> 
  
- <span data-ttu-id="2dd2e-145">MAPI_FORCE_DOWNLOAD は、 **MAPILogonEx**が返される前に受信したメッセージをダウンロードする必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-145">MAPI_FORCE_DOWNLOAD indicates that incoming messages should be downloaded before **MAPILogonEx** returns.</span></span> <span data-ttu-id="2dd2e-146">このフラグを設定しない場合、メッセージは後でバック グラウンドでダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-146">Not setting this flag causes messages to be downloaded in the background at a later time.</span></span> 
    
- <span data-ttu-id="2dd2e-147">MAPI_SERVICE_UI_ALWAYS は、プロファイル内のすべてのメッセージ サービスが、[構成] ダイアログ ボックスを表示することを要求します。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-147">MAPI_SERVICE_UI_ALWAYS requests that every message service in the profile display a configuration dialog box.</span></span>
    
- <span data-ttu-id="2dd2e-148">MAPI_NT_SERVICE では、クライアントが Windows サービスとして実装されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-148">MAPI_NT_SERVICE indicates that your client is implemented as a Windows service.</span></span> <span data-ttu-id="2dd2e-149">クライアントがサービスである場合、このフラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-149">This flag must be set if your client is a service.</span></span>
    
<span data-ttu-id="2dd2e-150">成功したログオンのたびには、 **MAPILogonEx**は、MAPI セッションへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-150">With every successful logon, **MAPILogonEx** returns a pointer to a MAPI session.</span></span> <span data-ttu-id="2dd2e-151">**IMAPISession**インターフェイスのメソッドを呼び出すには、このポインターを使用できます。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-151">You can use this pointer to call the methods of the **IMAPISession** interface.</span></span> <span data-ttu-id="2dd2e-152">詳細についてを参照してください[IMAPISession: IUnknown](imapisessioniunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-152">For more information, see [IMAPISession : IUnknown](imapisessioniunknown.md).</span></span> <span data-ttu-id="2dd2e-153">セッションの種類に関係なく、セッションのポインターは、そのメッセージを受信し、有効ではないタスク全体にわたってクライアントに固有です。</span><span class="sxs-lookup"><span data-stu-id="2dd2e-153">Session pointers, regardless of the type of session, are unique to the clients that receive them and are not valid across tasks.</span></span>
  

