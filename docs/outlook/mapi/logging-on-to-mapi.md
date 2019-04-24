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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307778"
---
# <a name="logging-on-to-mapi"></a><span data-ttu-id="532fa-103">MAPI へのログオン</span><span class="sxs-lookup"><span data-stu-id="532fa-103">Logging on to MAPI</span></span>
 
<span data-ttu-id="532fa-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="532fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="532fa-105">クライアントアプリケーションは、 **MAPILogonEx**関数を呼び出して MAPI サブシステムにログオンします。</span><span class="sxs-lookup"><span data-stu-id="532fa-105">Client applications log on to the MAPI subsystem by calling the **MAPILogonEx** function.</span></span> <span data-ttu-id="532fa-106">詳細については、「 [MAPILogonEx](mapilogonex.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="532fa-106">For more information, see [MAPILogonEx](mapilogonex.md).</span></span> <span data-ttu-id="532fa-107">**MAPILogonEx**は、プロファイルの選択と、プロファイル内の各サービスプロバイダーの構成を検証します。</span><span class="sxs-lookup"><span data-stu-id="532fa-107">**MAPILogonEx** validates the profile selection and the configuration of each service provider in the profile.</span></span> <span data-ttu-id="532fa-108">構成が完了すると、MAPI はメッセージストアプロバイダーを開始する前にアドレス帳プロバイダーを開始します。</span><span class="sxs-lookup"><span data-stu-id="532fa-108">Once configured, MAPI starts the address book providers before starting the message store providers.</span></span> <span data-ttu-id="532fa-109">サービスが最初に必要になると、トランスポートプロバイダーが開始されます。</span><span class="sxs-lookup"><span data-stu-id="532fa-109">Transport providers are started when their services are first required.</span></span> 
  
## <a name="choose-a-profile"></a><span data-ttu-id="532fa-110">プロファイルを選択する</span><span class="sxs-lookup"><span data-stu-id="532fa-110">Choose a profile</span></span>
  
- <span data-ttu-id="532fa-111">**MAPILogonEx**への_lpszprofilename_パラメーターのプロファイルの名前を表す文字列を渡します。または、...</span><span class="sxs-lookup"><span data-stu-id="532fa-111">Pass in a character string that represents the name of the profile in the  _lpszProfileName_ parameter to **MAPILogonEx**, or...</span></span>
    
- <span data-ttu-id="532fa-112">ユーザーが_lpszprofilename_パラメーターで NULL を渡し、MAPI_LOGON_UI フラグを設定することにより、プロファイルを指定できるようにします。</span><span class="sxs-lookup"><span data-stu-id="532fa-112">Allow the user to specify the profile by passing NULL in the  _lpszProfileName_ parameter and setting the MAPI_LOGON_UI flag, or...</span></span> 

- <span data-ttu-id="532fa-113">_lpszprofilename_パラメーターに NULL を渡し、MAPI_USE_DEFAULT フラグを設定することによって、既定のプロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="532fa-113">Select the default profile by passing NULL in the  _lpszProfileName_ parameter and setting the MAPI_USE_DEFAULT flag.</span></span> 
    
<span data-ttu-id="532fa-114">既定のプロファイル以外の特定のプロファイルが必要な場合は、その名前を独自の構成データベースに保存するか、特定の名前付け規則を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="532fa-114">If you require a specific profile other than the default profile, you must save its name in your own configuration database or use a specific naming convention.</span></span> <span data-ttu-id="532fa-115">MAPI は、プロファイルテーブルの名前と既定のフラグ以外のプロファイル属性を公開しません。また、既定のプロファイルフラグは、メッセージングクライアントおよび関連する IPM アプリケーション用に予約されています。</span><span class="sxs-lookup"><span data-stu-id="532fa-115">MAPI does not expose any profile attributes other than the name and default flag in the profile table, and the default profile flag is reserved for messaging client and related IPM applications.</span></span>
  
<span data-ttu-id="532fa-116">部分的なプロファイルまたはプロバイダーの構成情報を**MAPILogonEx**に提供するクライアントは、ダイアログボックスを表示できるようにすることで、追加のデータをユーザーに確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="532fa-116">Clients that supply partial profile or provider configuration information to **MAPILogonEx** must prompt the user for the additional data by allowing a dialog box to be displayed.</span></span> <span data-ttu-id="532fa-117">情報が不足していて、 **MAPILogonEx**がユーザーに入力を求められない場合、ログオンは失敗します。</span><span class="sxs-lookup"><span data-stu-id="532fa-117">If information is missing and **MAPILogonEx** cannot prompt the user to supply it, the logon fails.</span></span> <span data-ttu-id="532fa-118">ユーザー入力を必要としないクライアントでは、ダイアログボックスの表示が抑制されます。</span><span class="sxs-lookup"><span data-stu-id="532fa-118">Clients that do not need user input can suppress the dialog box display.</span></span> 
  
<span data-ttu-id="532fa-119">**MAPILogonEx**がユーザーインターフェイスを有効にするために使用するフラグは相互に排他的です。設定できるのは1つだけです。</span><span class="sxs-lookup"><span data-stu-id="532fa-119">The flags that **MAPILogonEx** uses to enable a user interface are mutually exclusive; only one can be set.</span></span> <span data-ttu-id="532fa-120">これらのフラグを設定しないままにすると、ユーザーインターフェイスの表示が抑制され、必要な情報が見つからない場合は**MAPILogonEx**が失敗します。</span><span class="sxs-lookup"><span data-stu-id="532fa-120">Leaving these flags unset suppresses the display of a user interface, causing **MAPILogonEx** to fail if necessary information is missing.</span></span> <span data-ttu-id="532fa-121">つまり、ユーザーインターフェイスを無効にし、 _lpszprofilename_パラメーターに NULL を渡すと、MAPI_USE_DEFAULT フラグを設定しないと、 **MAPILogonEx**はプロファイル名を取得できないため、失敗します。</span><span class="sxs-lookup"><span data-stu-id="532fa-121">That is, if you disable the user interface and pass NULL for the  _lpszProfileName_ parameter and do not set the MAPI_USE_DEFAULT flag, **MAPILogonEx** will fail because it cannot retrieve a profile name.</span></span> 
  
<span data-ttu-id="532fa-122">**MAPILogonEx**が確立するセッションは、個別のメッセージングセッション、共有されたメッセージングセッション、または非メッセージングセッションの場合があります。</span><span class="sxs-lookup"><span data-stu-id="532fa-122">The session that **MAPILogonEx** establishes can be an individual messaging session, a shared messaging session, or a nonmessaging session.</span></span> <span data-ttu-id="532fa-123">個々のメッセージングセッションは、クライアントと MAPI サブシステム間のプライベート接続であり、 **MAPILogonEx**への呼び出しで MAPI_NEW_SESSION フラグを設定することによって確立できます。</span><span class="sxs-lookup"><span data-stu-id="532fa-123">Individual messaging sessions are private connections between your client and the MAPI subsystem and can be established by setting the MAPI_NEW_SESSION flag in the call to **MAPILogonEx**.</span></span>
  
<span data-ttu-id="532fa-124">共有メッセージングセッションは、複数のメッセージングクライアントが使用できる接続です。</span><span class="sxs-lookup"><span data-stu-id="532fa-124">Shared messaging sessions are connections that multiple messaging clients can use.</span></span> <span data-ttu-id="532fa-125">通常、共有セッションはクライアントが同じプロファイルを使用するように設定されます。</span><span class="sxs-lookup"><span data-stu-id="532fa-125">Shared sessions are typically established for clients use the same profile.</span></span> <span data-ttu-id="532fa-126">共有セッションとして新しいセッションを確立するには、MAPI_ALLOW_OTHERS フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="532fa-126">To establish a new session as a shared session, set the MAPI_ALLOW_OTHERS flag.</span></span> 
  
## <a name="use-an-existing-shared-session"></a><span data-ttu-id="532fa-127">既存の共有セッションを使用する</span><span class="sxs-lookup"><span data-stu-id="532fa-127">Use an existing shared session</span></span>
  
- <span data-ttu-id="532fa-128">MAPI_NEW_SESSION フラグは設定しません。</span><span class="sxs-lookup"><span data-stu-id="532fa-128">Do not set the MAPI_NEW_SESSION flag.</span></span>
    
- <span data-ttu-id="532fa-129">MAPI_ALLOW_OTHERS フラグは設定しません。</span><span class="sxs-lookup"><span data-stu-id="532fa-129">Do not set the MAPI_ALLOW_OTHERS flag.</span></span>
    
- <span data-ttu-id="532fa-130">_lpszprofilename_パラメーターに NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="532fa-130">Pass NULL for the  _lpszProfileName_ parameter.</span></span> 
    
- <span data-ttu-id="532fa-131">_lpszpassword_パラメーターに NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="532fa-131">Pass NULL for the  _lpszPassword_ parameter.</span></span> 
    
<span data-ttu-id="532fa-132">非メッセージングセッションでは、クライアントは MAPI サブシステムにアクセスできますが、メッセージの送受信は許可されません。</span><span class="sxs-lookup"><span data-stu-id="532fa-132">Nonmessaging sessions allow clients to access the MAPI subsystem, but do not allow messages to be sent or received.</span></span> <span data-ttu-id="532fa-133">メッセージング以外のセッションを確立する必要があるクライアントの例として、構成または管理アプリケーションが挙げられます。</span><span class="sxs-lookup"><span data-stu-id="532fa-133">Configuration or administration applications are examples of clients that might need to establish nonmessaging sessions.</span></span> <span data-ttu-id="532fa-134">非メッセージングセッションを要求するには、MAPI_NO_MAIL フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="532fa-134">To request a nonmessaging session, set the MAPI_NO_MAIL flag.</span></span> <span data-ttu-id="532fa-135">このフラグを設定すると、MAPI スプーラーに通知されることなくクライアントがログに記録されます。</span><span class="sxs-lookup"><span data-stu-id="532fa-135">Setting this flag logs your client on without informing the MAPI spooler.</span></span> <span data-ttu-id="532fa-136">このフラグを使用して MAPI にログオンするクライアントは、閲覧状態レポートを受信することを期待できません。</span><span class="sxs-lookup"><span data-stu-id="532fa-136">Clients that log on to MAPI with this flag cannot expect to ever receive read status reports.</span></span>
  
<span data-ttu-id="532fa-137">MAPI_NO_MAIL フラグは、次のように設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="532fa-137">The MAPI_NO_MAIL flag should only be set:</span></span>
  
- <span data-ttu-id="532fa-138">クライアントがセッション中にメッセージを送信または受信しない場合。</span><span class="sxs-lookup"><span data-stu-id="532fa-138">If your client will not send or receive messages during the session.</span></span>
    
- <span data-ttu-id="532fa-139">クライアントがプロファイルの内容を完全に制御しており、Microsoft Exchange プロバイダーなどの密結合メッセージストアとトランスポートプロバイダーを使用してメッセージが送受信された場合。</span><span class="sxs-lookup"><span data-stu-id="532fa-139">If your client has complete control over the contents of the profile and messages are sent and received using tightly coupled message store and transport providers, such as the Microsoft Exchange providers.</span></span>
    
<span data-ttu-id="532fa-140">メッセージングクライアントは、非メッセージングクライアントとのセッションを共有できます。</span><span class="sxs-lookup"><span data-stu-id="532fa-140">A messaging client can share a session with a nonmessaging client.</span></span> <span data-ttu-id="532fa-141">共有セッションの1つのメンバーの特性は、他のメンバーの特性の影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="532fa-141">The characteristics of one member of a shared session are not affected by the characteristics of other members.</span></span> <span data-ttu-id="532fa-142">つまり、MAPI_NO_MAIL および MAPI_ALLOW_OTHERS フラグを設定してログオンした場合、セッションにログオンしたメッセージングクライアントはクライアントの操作に影響を与えず、その逆も同様です。</span><span class="sxs-lookup"><span data-stu-id="532fa-142">That is, if you log on with the MAPI_NO_MAIL and MAPI_ALLOW_OTHERS flags set, a messaging client logging on to your session has no affect on the operation of your client and vice versa.</span></span> <span data-ttu-id="532fa-143">メッセージングクライアントは依然としてメッセージの送受信を行うことができますが、クライアントは受信できません。</span><span class="sxs-lookup"><span data-stu-id="532fa-143">The messaging client will still be able to send and receive messages and your client will not.</span></span>
  
<span data-ttu-id="532fa-144">**MAPILogonEx**では、設定できる他のいくつかのフラグが定義されています。</span><span class="sxs-lookup"><span data-stu-id="532fa-144">**MAPILogonEx** defines a few other flags that you can set:</span></span> 
  
- <span data-ttu-id="532fa-145">MAPI_FORCE_DOWNLOAD は、 **MAPILogonEx**が戻る前に、受信メッセージをダウンロードする必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="532fa-145">MAPI_FORCE_DOWNLOAD indicates that incoming messages should be downloaded before **MAPILogonEx** returns.</span></span> <span data-ttu-id="532fa-146">このフラグを設定しないと、後でバックグラウンドでメッセージがダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="532fa-146">Not setting this flag causes messages to be downloaded in the background at a later time.</span></span> 
    
- <span data-ttu-id="532fa-147">MAPI_SERVICE_UI_ALWAYS は、プロファイル内のすべてのメッセージサービスに構成ダイアログボックスを表示するよう要求します。</span><span class="sxs-lookup"><span data-stu-id="532fa-147">MAPI_SERVICE_UI_ALWAYS requests that every message service in the profile display a configuration dialog box.</span></span>
    
- <span data-ttu-id="532fa-148">MAPI_NT_SERVICE は、クライアントが Windows サービスとして実装されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="532fa-148">MAPI_NT_SERVICE indicates that your client is implemented as a Windows service.</span></span> <span data-ttu-id="532fa-149">クライアントがサービスの場合は、このフラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="532fa-149">This flag must be set if your client is a service.</span></span>
    
<span data-ttu-id="532fa-150">正常にログオンするたびに、 **MAPILogonEx**は MAPI セッションへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="532fa-150">With every successful logon, **MAPILogonEx** returns a pointer to a MAPI session.</span></span> <span data-ttu-id="532fa-151">このポインターを使用して、 **imapisession**インターフェイスのメソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="532fa-151">You can use this pointer to call the methods of the **IMAPISession** interface.</span></span> <span data-ttu-id="532fa-152">詳細については、「 [imapisession: IUnknown](imapisessioniunknown.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="532fa-152">For more information, see [IMAPISession : IUnknown](imapisessioniunknown.md).</span></span> <span data-ttu-id="532fa-153">セッションポインターは、セッションの種類に関係なく、それらを受信するクライアントに固有のものであり、タスク間では有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="532fa-153">Session pointers, regardless of the type of session, are unique to the clients that receive them and are not valid across tasks.</span></span>
  

