---
title: MAPILogonEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPILogonEx
api_type:
- HeaderDef
ms.assetid: 98091e5b-1abd-4814-9c7a-583b420ee11d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9f2ec8f0ec00f7314982e9b112415f69901c358c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424120"
---
# <a name="mapilogonex"></a><span data-ttu-id="0ce81-103">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="0ce81-103">MAPILogonEx</span></span>

  
  
<span data-ttu-id="0ce81-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ce81-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ce81-105">クライアントアプリケーションをメッセージングシステムとのセッションに記録します。</span><span class="sxs-lookup"><span data-stu-id="0ce81-105">Logs a client application on to a session with the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0ce81-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0ce81-106">Header file:</span></span>  <br/> |<span data-ttu-id="0ce81-107">mapix</span><span class="sxs-lookup"><span data-stu-id="0ce81-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="0ce81-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="0ce81-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0ce81-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0ce81-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0ce81-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="0ce81-110">Called by:</span></span>  <br/> |<span data-ttu-id="0ce81-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="0ce81-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPILogonEx(
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  FLAGS flFlags,
  LPMAPISESSION FAR * lppSession
);
```

## <a name="parameters"></a><span data-ttu-id="0ce81-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0ce81-112">Parameters</span></span>

 <span data-ttu-id="0ce81-113">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="0ce81-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="0ce81-114">順番ログオンダイアログボックスがモーダルであるウィンドウを処理します。</span><span class="sxs-lookup"><span data-stu-id="0ce81-114">[in] Handle to the window to which the logon dialog box is modal.</span></span> <span data-ttu-id="0ce81-115">呼び出し中にダイアログボックスが表示されない場合、 _uluiparam_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="0ce81-115">If no dialog box appears during the call, the  _ulUIParam_ parameter is ignored.</span></span> <span data-ttu-id="0ce81-116">このパラメーターには0を指定できます。</span><span class="sxs-lookup"><span data-stu-id="0ce81-116">This parameter can be zero.</span></span> 
    
 <span data-ttu-id="0ce81-117">_lpszprofilename_</span><span class="sxs-lookup"><span data-stu-id="0ce81-117">_lpszProfileName_</span></span>
  
> <span data-ttu-id="0ce81-118">順番ユーザーがログオンするときに使用するプロファイルの名前を含む文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0ce81-118">[in] Pointer to a string that contains the name of the profile to use when the user logs on.</span></span> <span data-ttu-id="0ce81-119">この文字列は、64 文字に制限されています。</span><span class="sxs-lookup"><span data-stu-id="0ce81-119">This string is limited to 64 characters.</span></span>
    
 <span data-ttu-id="0ce81-120">_lpszpassword_</span><span class="sxs-lookup"><span data-stu-id="0ce81-120">_lpszPassword_</span></span>
  
> <span data-ttu-id="0ce81-121">順番プロファイルのパスワードを含む文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0ce81-121">[in] Pointer to a string that contains the password of the profile.</span></span> <span data-ttu-id="0ce81-122">_lpszpassword_パラメーターは NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ce81-122">The  _lpszPassword_ parameter must be NULL.</span></span> 
    
 <span data-ttu-id="0ce81-123">_flflags_</span><span class="sxs-lookup"><span data-stu-id="0ce81-123">_flFlags_</span></span>
  
> <span data-ttu-id="0ce81-124">順番ログオンの実行方法を制御するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="0ce81-124">[in] Bitmask of flags used to control how logon is performed.</span></span> <span data-ttu-id="0ce81-125">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="0ce81-125">The following flags can be set:</span></span>
    
<span data-ttu-id="0ce81-126">MAPI_ALLOW_OTHERS</span><span class="sxs-lookup"><span data-stu-id="0ce81-126">MAPI_ALLOW_OTHERS</span></span> 
  
> <span data-ttu-id="0ce81-127">共有セッションが返されます。これにより、後のクライアントがユーザーの資格情報を指定せずにセッションを取得できるようになります。</span><span class="sxs-lookup"><span data-stu-id="0ce81-127">The shared session should be returned, which allows later clients to obtain the session without providing any user credentials.</span></span> 
    
<span data-ttu-id="0ce81-128">MAPI_BG_SESSION</span><span class="sxs-lookup"><span data-stu-id="0ce81-128">MAPI_BG_SESSION</span></span>
  
> <span data-ttu-id="0ce81-129">セッションにログオンし、バックグラウンドで任意の操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="0ce81-129">Log on to a session and run any operations in the background.</span></span> <span data-ttu-id="0ce81-130">一般に、クライアントがバックグラウンドスレッドで処理を行う場合や、フォアグラウンドスレッドに対して安全でない方法で処理を行う場合は、MAPI_BG_SESSION フラグを指定して呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0ce81-130">In general, if a client intends to do processing on a background thread or in a separate process in a manner that is unobtrusive to the foreground thread, it should call with the MAPI_BG_SESSION flag.</span></span> <span data-ttu-id="0ce81-131">MAPI_BG_SESSION を使用する場所の例として、インデックスエンジンなどのクライアントアプリケーションや、バックグラウンドの種類のアクセスのための個人用フォルダーファイル (PST) を開くことがあります。MAPILogonEx。</span><span class="sxs-lookup"><span data-stu-id="0ce81-131">A client application such as an indexing engine or opening a Personal Folders File (PST) for background type access are some examples of where to use MAPI_BG_SESSION.MAPILogonEx.</span></span>
    
<span data-ttu-id="0ce81-132">MAPI_EXPLICIT_PROFILE</span><span class="sxs-lookup"><span data-stu-id="0ce81-132">MAPI_EXPLICIT_PROFILE</span></span> 
  
> <span data-ttu-id="0ce81-133">既定のプロファイルを使用しないで、ユーザーがプロファイルを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ce81-133">The default profile should not be used and the user should be required to supply a profile.</span></span> 
    
<span data-ttu-id="0ce81-134">MAPI_EXTENDED</span><span class="sxs-lookup"><span data-stu-id="0ce81-134">MAPI_EXTENDED</span></span> 
  
> <span data-ttu-id="0ce81-135">拡張機能を使用してログオンします。</span><span class="sxs-lookup"><span data-stu-id="0ce81-135">Log on with extended capabilities.</span></span> <span data-ttu-id="0ce81-136">このフラグは常に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ce81-136">This flag should always be set.</span></span>
    
<span data-ttu-id="0ce81-137">MAPI_FORCE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="0ce81-137">MAPI_FORCE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="0ce81-138">戻る前に、すべてのユーザーのメッセージをダウンロードするように試行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ce81-138">An attempt should be made to download all of the user's messages before returning.</span></span> <span data-ttu-id="0ce81-139">MAPI_FORCE_DOWNLOAD フラグが設定されていない場合、MAPILogonEx の呼び出し後に、メッセージをバックグラウンドでダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="0ce81-139">If the MAPI_FORCE_DOWNLOAD flag is not set, messages can be downloaded in the background after the call to MAPILogonEx returns.</span></span> 
    
<span data-ttu-id="0ce81-140">MAPI_LOGON_UI</span><span class="sxs-lookup"><span data-stu-id="0ce81-140">MAPI_LOGON_UI</span></span> 
  
> <span data-ttu-id="0ce81-141">必要に応じて、ユーザーにログオン情報の入力を求めるダイアログボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0ce81-141">A dialog box should be displayed to prompt the user for logon information if required.</span></span> <span data-ttu-id="0ce81-142">MAPI_LOGON_UI フラグが設定されていない場合、呼び出し元クライアントはログオンダイアログボックスを表示せず、ユーザーがログオンしていない場合はエラー値を返します。</span><span class="sxs-lookup"><span data-stu-id="0ce81-142">When the MAPI_LOGON_UI flag is not set, the calling client does not display a logon dialog box and returns an error value if the user is not logged on.</span></span>
    
<span data-ttu-id="0ce81-143">MAPI_NEW_SESSION</span><span class="sxs-lookup"><span data-stu-id="0ce81-143">MAPI_NEW_SESSION</span></span> 
  
> <span data-ttu-id="0ce81-144">共有セッションを取得するのではなく、新しい MAPI セッションを作成しようとしています。</span><span class="sxs-lookup"><span data-stu-id="0ce81-144">An attempt should be made to create a new MAPI session instead of acquiring the shared session.</span></span> <span data-ttu-id="0ce81-145">MAPI_NEW_SESSION フラグが設定されていない場合、MAPILogonEx は、 _lpszprofilename_パラメーターが NULL でない場合でも、既存の共有セッションを使用します。</span><span class="sxs-lookup"><span data-stu-id="0ce81-145">If the MAPI_NEW_SESSION flag is not set, MAPILogonEx uses an existing shared session even if the  _lpszprofileName_ parameter is not NULL.</span></span> 
    
<span data-ttu-id="0ce81-146">MAPI_NO_MAIL</span><span class="sxs-lookup"><span data-stu-id="0ce81-146">MAPI_NO_MAIL</span></span> 
  
> <span data-ttu-id="0ce81-147">mapi では、セッションの存在が mapi スプーラーに通知されません。</span><span class="sxs-lookup"><span data-stu-id="0ce81-147">MAPI should not inform the MAPI spooler of the session's existence.</span></span> <span data-ttu-id="0ce81-148">その結果、密結合ストアとトランスポートペアを使用した場合を除き、セッションでメッセージを送受信できなくなります。</span><span class="sxs-lookup"><span data-stu-id="0ce81-148">The result is that no messages can be sent or received in the session except through a tightly coupled store and transport pair.</span></span> <span data-ttu-id="0ce81-149">呼び出し元クライアントがエージェントとして機能している場合、構成作業を実行する必要がある場合、または使用可能なメッセージストアをクライアントが参照している場合は、このフラグが設定されます。</span><span class="sxs-lookup"><span data-stu-id="0ce81-149">A calling client sets this flag if it is acting as an agent, if configuration work must be done, or if the client is browsing the available message stores.</span></span> 
    
<span data-ttu-id="0ce81-150">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="0ce81-150">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="0ce81-151">発信者が Windows サービスとして実行されている。</span><span class="sxs-lookup"><span data-stu-id="0ce81-151">The caller is running as a Windows service.</span></span> <span data-ttu-id="0ce81-152">Windows サービスとして実行されていない発信者は、このフラグを設定してはなりません。サービスとして実行されている発信者は、このフラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ce81-152">Callers that are not running as a Windows service should not set this flag; callers that are running as a service must set this flag.</span></span> 
    
<span data-ttu-id="0ce81-153">MAPI_SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="0ce81-153">MAPI_SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="0ce81-154">MAPILogonEx は、プロファイル内の各メッセージサービスについて、構成ダイアログボックスを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ce81-154">MAPILogonEx should display a configuration dialog box for each message service in the profile.</span></span> <span data-ttu-id="0ce81-155">このダイアログボックスは、プロファイルが選択された後、メッセージサービスがログオンする前に表示されます。</span><span class="sxs-lookup"><span data-stu-id="0ce81-155">The dialog boxes are displayed after the profile has been chosen but before any message service is logged on.</span></span> <span data-ttu-id="0ce81-156">ログオン用の MAPI コモンダイアログボックスにも、同じ操作を要求するチェックボックスがあります。</span><span class="sxs-lookup"><span data-stu-id="0ce81-156">The MAPI common dialog box for logon also contains a check box that requests the same operation.</span></span> 
    
<span data-ttu-id="0ce81-157">MAPI_TIMEOUT_SHORT</span><span class="sxs-lookup"><span data-stu-id="0ce81-157">MAPI_TIMEOUT_SHORT</span></span> 
  
> <span data-ttu-id="0ce81-158">数秒以上ブロックされた場合、ログオンは失敗します。</span><span class="sxs-lookup"><span data-stu-id="0ce81-158">The logon should fail if blocked for more than a few seconds.</span></span> 
    
<span data-ttu-id="0ce81-159">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0ce81-159">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="0ce81-160">渡された文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="0ce81-160">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="0ce81-161">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="0ce81-161">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="0ce81-162">MAPI_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="0ce81-162">MAPI_USE_DEFAULT</span></span> 
  
> <span data-ttu-id="0ce81-163">メッセージングサブシステムは、 _lpszprofilename_パラメーターの既定のプロファイルのプロファイル名を置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ce81-163">The messaging subsystem should substitute the profile name of the default profile for the  _lpszProfileName_ parameter.</span></span> <span data-ttu-id="0ce81-164">_lpszprofilename_が NULL または空の場合を除き、MAPI_EXPLICIT_PROFILE フラグは無視されます。</span><span class="sxs-lookup"><span data-stu-id="0ce81-164">The MAPI_EXPLICIT_PROFILE flag is ignored unless  _lpszProfileName_ is NULL or empty.</span></span> 
    
 <span data-ttu-id="0ce81-165">_lppsession_</span><span class="sxs-lookup"><span data-stu-id="0ce81-165">_lppSession_</span></span>
  
> <span data-ttu-id="0ce81-166">読み上げMAPI セッションインターフェイスへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="0ce81-166">[out] Pointer to a pointer to the MAPI session interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0ce81-167">戻り値</span><span class="sxs-lookup"><span data-stu-id="0ce81-167">Return value</span></span>

<span data-ttu-id="0ce81-168">S_OK</span><span class="sxs-lookup"><span data-stu-id="0ce81-168">S_OK</span></span> 
  
> <span data-ttu-id="0ce81-169">ログオンに成功しました。</span><span class="sxs-lookup"><span data-stu-id="0ce81-169">The logon succeeded.</span></span>
    
<span data-ttu-id="0ce81-170">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="0ce81-170">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="0ce81-171">MAPILogonEx への1つ以上のパラメーターが無効であったか、既に開いているセッションが多すぎるため、ログオンに失敗しました。</span><span class="sxs-lookup"><span data-stu-id="0ce81-171">The logon was unsuccessful, either because one or more of the parameters to MAPILogonEx were invalid or because there were too many sessions open already.</span></span>
    
<span data-ttu-id="0ce81-172">MAPI_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="0ce81-172">MAPI_E_TIMEOUT</span></span> 
  
> <span data-ttu-id="0ce81-173">MAPI は、ミューテックスを介してすべてのログオンをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="0ce81-173">MAPI serializes all logons through a mutex.</span></span> <span data-ttu-id="0ce81-174">これは、MAPI_TIMEOUT_SHORT フラグが設定されていて、別のスレッドがミューテックスを保持した場合に返されます。</span><span class="sxs-lookup"><span data-stu-id="0ce81-174">This is returned if the MAPI_TIMEOUT_SHORT flag was set and another thread held the mutex.</span></span> 
    
<span data-ttu-id="0ce81-175">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="0ce81-175">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="0ce81-176">ユーザーが操作をキャンセルしました。通常は、ダイアログボックスの **[キャンセル**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0ce81-176">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0ce81-177">注釈</span><span class="sxs-lookup"><span data-stu-id="0ce81-177">Remarks</span></span>

<span data-ttu-id="0ce81-178">MAPI クライアントアプリケーションは、MAPILogonEx 関数を呼び出して、メッセージングシステムとのセッションにログオンします。</span><span class="sxs-lookup"><span data-stu-id="0ce81-178">MAPI client applications call the MAPILogonEx function to log on to a session with the messaging system.</span></span> <span data-ttu-id="0ce81-179">MAPI 呼び出しとの間で送受信されるすべての文字列は、null で終了し、呼び出し元クライアントまたはプロバイダーのオペレーティングシステムの現在の文字セットまたはコードページで指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ce81-179">All strings that are passed in and returned to and from MAPI calls are null-terminated and must be specified in the current character set or code page of the calling client or provider's operating system.</span></span>
  
<span data-ttu-id="0ce81-180">MAPI_ALLOW_OTHERS フラグを設定して MapiLogonEx を呼び出し、フラグ MAPI_NEW_SESSION が設定されていない場合は、既に前のセッションが存在する場合、 _lpszprofilename_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="0ce81-180">The  _lpszProfileName_ parameter is ignored if there is an existing previous session that called MapiLogonEx with the MAPI_ALLOW_OTHERS flag set and if the flag MAPI_NEW_SESSION is not set.</span></span> <span data-ttu-id="0ce81-181">_lpszprofilename_パラメーターが NULL の場合、または空の文字列をポイントしていて、 _flflags_パラメーターに MAPI_LOGON_UI フラグが含まれている場合、MAPILogonEx 関数はプロファイル名に空のフィールドを持つログオンダイアログボックスを生成します。</span><span class="sxs-lookup"><span data-stu-id="0ce81-181">If the  _lpszProfileName_ parameter is NULL or points to an empty string, and the  _flFlags_ parameter includes the MAPI_LOGON_UI flag, the MAPILogonEx function generates a logon dialog box that has an empty field for the profile name.</span></span> 
  
<span data-ttu-id="0ce81-182">特定のプロファイルにログオンする場合、クライアントはプロファイル名に加えて MAPI_NEW_SESSION フラグを MAPILogonEx に渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ce81-182">When logging on to a specific profile, a client should pass the MAPI_NEW_SESSION flag into MAPILogonEx in addition to the profile name.</span></span> <span data-ttu-id="0ce81-183">または、別のクライアントが MAPI_ALLOW_OTHERS を使用してログオンして共有セッションを確立した場合、クライアントは要求されたプロファイルではなく、共有セッションにログオンします。</span><span class="sxs-lookup"><span data-stu-id="0ce81-183">Otherwise, if another client has established a shared session by logging on with MAPI_ALLOW_OTHERS, the client will be logged on to the shared session instead of to the profile requested.</span></span> 
  
<span data-ttu-id="0ce81-184">MAPI_EXPLICIT_PROFILE フラグは、MAPI_USE_DEFAULT フラグも存在しない限り、 _lpszprofilename_が NULL または空の場合は、既定のプロファイル名を使用しません。</span><span class="sxs-lookup"><span data-stu-id="0ce81-184">The MAPI_EXPLICIT_PROFILE flag does not cause the default profile name to be used when  _lpszProfileName_ is NULL or empty unless the MAPI_USE_DEFAULT flag is also present.</span></span> 
  
<span data-ttu-id="0ce81-185">MAPI_NO_MAIL フラグには、MAPI スプーラーを使用しない場合に、次のようないくつかの影響があります。</span><span class="sxs-lookup"><span data-stu-id="0ce81-185">The MAPI_NO_MAIL flag has several effects that cause the following when not using the MAPI spooler:</span></span>
  
- <span data-ttu-id="0ce81-186">このセッション中に MAPI スプーラーでメッセージを送信または配信することはできません。</span><span class="sxs-lookup"><span data-stu-id="0ce81-186">No messages can be sent or delivered by the MAPI spooler during this session.</span></span> <span data-ttu-id="0ce81-187">密結合ストアとトランスポートプロバイダーのみが、メッセージの送受信を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="0ce81-187">Only tightly coupled store and transport providers can send and deliver messages.</span></span> 
    
- <span data-ttu-id="0ce81-188">サーバーベースのストアは依然としてメッセージを送信または配信する場合があります。</span><span class="sxs-lookup"><span data-stu-id="0ce81-188">Server based stores might still send or deliver messages.</span></span> 
    
- <span data-ttu-id="0ce81-189">サーバーベースのストアによって送信または配信されたメッセージは、フックプロバイダーによって処理されません。</span><span class="sxs-lookup"><span data-stu-id="0ce81-189">Messages sent or delivered by server based stores are not processed by any hook providers.</span></span> 
    
- <span data-ttu-id="0ce81-190">トランスポートのメッセージ単位および受信者ごとのオプションは使用できません。</span><span class="sxs-lookup"><span data-stu-id="0ce81-190">Per-message and per-recipient options for transports are not available.</span></span> 
    
- <span data-ttu-id="0ce81-191">状態テーブルには、トランスポートプロバイダーのエントリは含まれていません。状態オブジェクトに依存するトランスポート機能 (構成など) は使用できません。</span><span class="sxs-lookup"><span data-stu-id="0ce81-191">The status table does not contain entries for transport providers, and any transport functionality dependent on status objects (such as configuration) is not available.</span></span> 
    
- <span data-ttu-id="0ce81-192">状態テーブルのメッセージスプーラー行には、STATUS_FAILURE の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0ce81-192">The message spooler row in the status table contains the STATUS_FAILURE value.</span></span> 
    
- <span data-ttu-id="0ce81-193">上乗せログオンは許可されますが、これらのログオンによって、以前のログオンがステータスオブジェクトの更新を受信することはありません。</span><span class="sxs-lookup"><span data-stu-id="0ce81-193">Piggybacked logons are allowed, but those logons do not cause the previous logon to receive status object updates.</span></span> 
    
<span data-ttu-id="0ce81-194">サービスは常に MAPI_NO_MAIL フラグを使用してログオンする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ce81-194">A service should always log on using the MAPI_NO_MAIL flag.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0ce81-195">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="0ce81-195">MFCMAPI reference</span></span>

<span data-ttu-id="0ce81-196">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0ce81-196">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0ce81-197">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="0ce81-197">**File**</span></span>|<span data-ttu-id="0ce81-198">**関数**</span><span class="sxs-lookup"><span data-stu-id="0ce81-198">**Function**</span></span>|<span data-ttu-id="0ce81-199">**コメント**</span><span class="sxs-lookup"><span data-stu-id="0ce81-199">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0ce81-200">MAPIObjects</span><span class="sxs-lookup"><span data-stu-id="0ce81-200">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="0ce81-201">cmapiobjects:: MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="0ce81-201">CMapiObjects::MAPILogonEx</span></span>  <br/> |<span data-ttu-id="0ce81-202">mfcmapi は、MAPILogonEx メソッドを使用して MAPI にログオンします。</span><span class="sxs-lookup"><span data-stu-id="0ce81-202">MFCMAPI uses the MAPILogonEx method to log on to MAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0ce81-203">関連項目</span><span class="sxs-lookup"><span data-stu-id="0ce81-203">See also</span></span>



[<span data-ttu-id="0ce81-204">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="0ce81-204">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="0ce81-205">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="0ce81-205">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)


<span data-ttu-id="0ce81-206">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="0ce81-206">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

