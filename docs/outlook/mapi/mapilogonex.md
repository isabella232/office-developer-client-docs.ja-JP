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
# <a name="mapilogonex"></a><span data-ttu-id="1af8c-103">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="1af8c-103">MAPILogonEx</span></span>

  
  
<span data-ttu-id="1af8c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1af8c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1af8c-105">クライアント アプリケーションをメッセージング システムとのセッションにログに記録します。</span><span class="sxs-lookup"><span data-stu-id="1af8c-105">Logs a client application on to a session with the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1af8c-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="1af8c-106">Header file:</span></span>  <br/> |<span data-ttu-id="1af8c-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="1af8c-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="1af8c-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="1af8c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1af8c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1af8c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1af8c-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="1af8c-110">Called by:</span></span>  <br/> |<span data-ttu-id="1af8c-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="1af8c-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPILogonEx(
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  FLAGS flFlags,
  LPMAPISESSION FAR * lppSession
);
```

## <a name="parameters"></a><span data-ttu-id="1af8c-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1af8c-112">Parameters</span></span>

 <span data-ttu-id="1af8c-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1af8c-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="1af8c-114">[in]ログオン ダイアログ ボックスがモーダルであるウィンドウを処理します。</span><span class="sxs-lookup"><span data-stu-id="1af8c-114">[in] Handle to the window to which the logon dialog box is modal.</span></span> <span data-ttu-id="1af8c-115">呼び出し中にダイアログ ボックスが表示されない場合  _、ulUIParam_ パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="1af8c-115">If no dialog box appears during the call, the  _ulUIParam_ parameter is ignored.</span></span> <span data-ttu-id="1af8c-116">このパラメーターには 0 を指定できます。</span><span class="sxs-lookup"><span data-stu-id="1af8c-116">This parameter can be zero.</span></span> 
    
 <span data-ttu-id="1af8c-117">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="1af8c-117">_lpszProfileName_</span></span>
  
> <span data-ttu-id="1af8c-118">[in]ユーザーがログオンするときに使用するプロファイルの名前を含む文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1af8c-118">[in] Pointer to a string that contains the name of the profile to use when the user logs on.</span></span> <span data-ttu-id="1af8c-119">この文字列は、64 文字に制限されています。</span><span class="sxs-lookup"><span data-stu-id="1af8c-119">This string is limited to 64 characters.</span></span>
    
 <span data-ttu-id="1af8c-120">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="1af8c-120">_lpszPassword_</span></span>
  
> <span data-ttu-id="1af8c-121">[in]プロファイルのパスワードを含む文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1af8c-121">[in] Pointer to a string that contains the password of the profile.</span></span> <span data-ttu-id="1af8c-122">_lpszPassword パラメーター_ は NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="1af8c-122">The  _lpszPassword_ parameter must be NULL.</span></span> 
    
 <span data-ttu-id="1af8c-123">_flFlags_</span><span class="sxs-lookup"><span data-stu-id="1af8c-123">_flFlags_</span></span>
  
> <span data-ttu-id="1af8c-124">[in]ログオンの実行方法を制御するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="1af8c-124">[in] Bitmask of flags used to control how logon is performed.</span></span> <span data-ttu-id="1af8c-125">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="1af8c-125">The following flags can be set:</span></span>
    
<span data-ttu-id="1af8c-126">MAPI_ALLOW_OTHERS</span><span class="sxs-lookup"><span data-stu-id="1af8c-126">MAPI_ALLOW_OTHERS</span></span> 
  
> <span data-ttu-id="1af8c-127">共有セッションを返す必要があります。これにより、後のクライアントはユーザー資格情報を提供せずにセッションを取得できます。</span><span class="sxs-lookup"><span data-stu-id="1af8c-127">The shared session should be returned, which allows later clients to obtain the session without providing any user credentials.</span></span> 
    
<span data-ttu-id="1af8c-128">MAPI_BG_SESSION</span><span class="sxs-lookup"><span data-stu-id="1af8c-128">MAPI_BG_SESSION</span></span>
  
> <span data-ttu-id="1af8c-129">セッションにログオンし、バックグラウンドで任意の操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="1af8c-129">Log on to a session and run any operations in the background.</span></span> <span data-ttu-id="1af8c-130">一般に、クライアントがフォアグラウンド スレッドに対して控えめな方法でバックグラウンド スレッドまたは別のプロセスで処理を行う場合は、MAPI_BG_SESSION フラグを使用して呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="1af8c-130">In general, if a client intends to do processing on a background thread or in a separate process in a manner that is unobtrusive to the foreground thread, it should call with the MAPI_BG_SESSION flag.</span></span> <span data-ttu-id="1af8c-131">インデックス エンジンや、バックグラウンドタイプアクセス用の個人用フォルダー ファイル (PST) を開くなどのクライアント アプリケーションは、ユーザーが使用する場所の例MAPI_BG_SESSION。MAPILogonEx。</span><span class="sxs-lookup"><span data-stu-id="1af8c-131">A client application such as an indexing engine or opening a Personal Folders File (PST) for background type access are some examples of where to use MAPI_BG_SESSION.MAPILogonEx.</span></span>
    
<span data-ttu-id="1af8c-132">MAPI_EXPLICIT_PROFILE</span><span class="sxs-lookup"><span data-stu-id="1af8c-132">MAPI_EXPLICIT_PROFILE</span></span> 
  
> <span data-ttu-id="1af8c-133">既定のプロファイルを使用し、ユーザーがプロファイルを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1af8c-133">The default profile should not be used and the user should be required to supply a profile.</span></span> 
    
<span data-ttu-id="1af8c-134">MAPI_EXTENDED</span><span class="sxs-lookup"><span data-stu-id="1af8c-134">MAPI_EXTENDED</span></span> 
  
> <span data-ttu-id="1af8c-135">拡張機能を使用してログオンします。</span><span class="sxs-lookup"><span data-stu-id="1af8c-135">Log on with extended capabilities.</span></span> <span data-ttu-id="1af8c-136">このフラグは常に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1af8c-136">This flag should always be set.</span></span>
    
<span data-ttu-id="1af8c-137">MAPI_FORCE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="1af8c-137">MAPI_FORCE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="1af8c-138">戻る前に、すべてのユーザーのメッセージをダウンロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1af8c-138">An attempt should be made to download all of the user's messages before returning.</span></span> <span data-ttu-id="1af8c-139">このフラグMAPI_FORCE_DOWNLOAD設定されていない場合、MAPILogonEx の呼び出しが返された後、メッセージをバックグラウンドでダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="1af8c-139">If the MAPI_FORCE_DOWNLOAD flag is not set, messages can be downloaded in the background after the call to MAPILogonEx returns.</span></span> 
    
<span data-ttu-id="1af8c-140">MAPI_LOGON_UI</span><span class="sxs-lookup"><span data-stu-id="1af8c-140">MAPI_LOGON_UI</span></span> 
  
> <span data-ttu-id="1af8c-141">必要に応じて、ログオン情報の入力を求めるダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1af8c-141">A dialog box should be displayed to prompt the user for logon information if required.</span></span> <span data-ttu-id="1af8c-142">MAPI_LOGON_UIフラグが設定されていない場合、呼び出し元のクライアントはログオン ダイアログ ボックスを表示し、ユーザーがログオンしていない場合はエラー値を返します。</span><span class="sxs-lookup"><span data-stu-id="1af8c-142">When the MAPI_LOGON_UI flag is not set, the calling client does not display a logon dialog box and returns an error value if the user is not logged on.</span></span>
    
<span data-ttu-id="1af8c-143">MAPI_NEW_SESSION</span><span class="sxs-lookup"><span data-stu-id="1af8c-143">MAPI_NEW_SESSION</span></span> 
  
> <span data-ttu-id="1af8c-144">共有セッションを取得する代わりに、新しい MAPI セッションを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1af8c-144">An attempt should be made to create a new MAPI session instead of acquiring the shared session.</span></span> <span data-ttu-id="1af8c-145">このフラグMAPI_NEW_SESSION設定されていない場合  _、lpszprofileName_ パラメーターが NULL でなくても、MAPILogonEx は既存の共有セッションを使用します。</span><span class="sxs-lookup"><span data-stu-id="1af8c-145">If the MAPI_NEW_SESSION flag is not set, MAPILogonEx uses an existing shared session even if the  _lpszprofileName_ parameter is not NULL.</span></span> 
    
<span data-ttu-id="1af8c-146">MAPI_NO_MAIL</span><span class="sxs-lookup"><span data-stu-id="1af8c-146">MAPI_NO_MAIL</span></span> 
  
> <span data-ttu-id="1af8c-147">MAPI は、セッションの存在を MAPI スプーラーに通知する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1af8c-147">MAPI should not inform the MAPI spooler of the session's existence.</span></span> <span data-ttu-id="1af8c-148">その結果、緊密に結合されたストアとトランスポートのペアを除き、セッションでメッセージを送信または受信できません。</span><span class="sxs-lookup"><span data-stu-id="1af8c-148">The result is that no messages can be sent or received in the session except through a tightly coupled store and transport pair.</span></span> <span data-ttu-id="1af8c-149">呼び出し元のクライアントは、エージェントとして機能している場合、構成作業を行う必要がある場合、またはクライアントが使用可能なメッセージ ストアを参照している場合に、このフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="1af8c-149">A calling client sets this flag if it is acting as an agent, if configuration work must be done, or if the client is browsing the available message stores.</span></span> 
    
<span data-ttu-id="1af8c-150">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="1af8c-150">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="1af8c-151">呼び出し元は、Windowsサービスとして実行されています。</span><span class="sxs-lookup"><span data-stu-id="1af8c-151">The caller is running as a Windows service.</span></span> <span data-ttu-id="1af8c-152">サービスとして実行されていない呼び出し元Windowsこのフラグを設定する必要があります。サービスとして実行されている呼び出し元は、このフラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1af8c-152">Callers that are not running as a Windows service should not set this flag; callers that are running as a service must set this flag.</span></span> 
    
<span data-ttu-id="1af8c-153">MAPI_SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="1af8c-153">MAPI_SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="1af8c-154">MAPILogonEx は、プロファイル内の各メッセージ サービスの構成ダイアログ ボックスを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1af8c-154">MAPILogonEx should display a configuration dialog box for each message service in the profile.</span></span> <span data-ttu-id="1af8c-155">このダイアログ ボックスは、プロファイルが選択された後、メッセージ サービスがログオンする前に表示されます。</span><span class="sxs-lookup"><span data-stu-id="1af8c-155">The dialog boxes are displayed after the profile has been chosen but before any message service is logged on.</span></span> <span data-ttu-id="1af8c-156">ログオンの MAPI 共通ダイアログ ボックスには、同じ操作を要求するチェック ボックスも含まれる。</span><span class="sxs-lookup"><span data-stu-id="1af8c-156">The MAPI common dialog box for logon also contains a check box that requests the same operation.</span></span> 
    
<span data-ttu-id="1af8c-157">MAPI_TIMEOUT_SHORT</span><span class="sxs-lookup"><span data-stu-id="1af8c-157">MAPI_TIMEOUT_SHORT</span></span> 
  
> <span data-ttu-id="1af8c-158">数秒間以上ブロックされた場合、ログオンは失敗する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1af8c-158">The logon should fail if blocked for more than a few seconds.</span></span> 
    
<span data-ttu-id="1af8c-159">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1af8c-159">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1af8c-160">渡された文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="1af8c-160">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="1af8c-161">このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="1af8c-161">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="1af8c-162">MAPI_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="1af8c-162">MAPI_USE_DEFAULT</span></span> 
  
> <span data-ttu-id="1af8c-163">メッセージング サブシステムは、lpszProfileName パラメーターの既定のプロファイルのプロファイル名  _を置き換える必要_ があります。</span><span class="sxs-lookup"><span data-stu-id="1af8c-163">The messaging subsystem should substitute the profile name of the default profile for the  _lpszProfileName_ parameter.</span></span> <span data-ttu-id="1af8c-164">_lpszProfileName_ が NULL または空の場合を指定しない限り、MAPI_EXPLICIT_PROFILEフラグは無視されます。</span><span class="sxs-lookup"><span data-stu-id="1af8c-164">The MAPI_EXPLICIT_PROFILE flag is ignored unless  _lpszProfileName_ is NULL or empty.</span></span> 
    
 <span data-ttu-id="1af8c-165">_lppSession_</span><span class="sxs-lookup"><span data-stu-id="1af8c-165">_lppSession_</span></span>
  
> <span data-ttu-id="1af8c-166">[out]MAPI セッション インターフェイスへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="1af8c-166">[out] Pointer to a pointer to the MAPI session interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1af8c-167">戻り値</span><span class="sxs-lookup"><span data-stu-id="1af8c-167">Return value</span></span>

<span data-ttu-id="1af8c-168">S_OK</span><span class="sxs-lookup"><span data-stu-id="1af8c-168">S_OK</span></span> 
  
> <span data-ttu-id="1af8c-169">ログオンが成功しました。</span><span class="sxs-lookup"><span data-stu-id="1af8c-169">The logon succeeded.</span></span>
    
<span data-ttu-id="1af8c-170">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="1af8c-170">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="1af8c-171">MAPILogonEx に対する 1 つ以上のパラメーターが無効であるか、既に開いているセッションが多すぎたため、ログオンが失敗しました。</span><span class="sxs-lookup"><span data-stu-id="1af8c-171">The logon was unsuccessful, either because one or more of the parameters to MAPILogonEx were invalid or because there were too many sessions open already.</span></span>
    
<span data-ttu-id="1af8c-172">MAPI_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="1af8c-172">MAPI_E_TIMEOUT</span></span> 
  
> <span data-ttu-id="1af8c-173">MAPI は、ミューテックスを介してすべてのログオンをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="1af8c-173">MAPI serializes all logons through a mutex.</span></span> <span data-ttu-id="1af8c-174">この値は、MAPI_TIMEOUT_SHORTフラグが設定され、別のスレッドがミューテックスを保持している場合に返されます。</span><span class="sxs-lookup"><span data-stu-id="1af8c-174">This is returned if the MAPI_TIMEOUT_SHORT flag was set and another thread held the mutex.</span></span> 
    
<span data-ttu-id="1af8c-175">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="1af8c-175">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="1af8c-176">通常、ユーザーはダイアログ ボックスの [キャンセル] ボタンをクリック **して操作を** キャンセルしました。</span><span class="sxs-lookup"><span data-stu-id="1af8c-176">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1af8c-177">注釈</span><span class="sxs-lookup"><span data-stu-id="1af8c-177">Remarks</span></span>

<span data-ttu-id="1af8c-178">MAPI クライアント アプリケーションは MAPILogonEx 関数を呼び出して、メッセージング システムとのセッションにログオンします。</span><span class="sxs-lookup"><span data-stu-id="1af8c-178">MAPI client applications call the MAPILogonEx function to log on to a session with the messaging system.</span></span> <span data-ttu-id="1af8c-179">MAPI 呼び出しで渡され、MAPI 呼び出しとの間で返される文字列はすべて null で終了し、呼び出し元のクライアントまたはプロバイダーのオペレーティング システムの現在の文字セットまたはコード ページで指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1af8c-179">All strings that are passed in and returned to and from MAPI calls are null-terminated and must be specified in the current character set or code page of the calling client or provider's operating system.</span></span>
  
<span data-ttu-id="1af8c-180">_lpszProfileName_ パラメーターは、MAPI_ALLOW_OTHERS フラグが設定された MapiLogonEx と呼ばれる既存の以前のセッションがある場合、およびフラグ MAPI_NEW_SESSION が設定されていない場合は無視されます。</span><span class="sxs-lookup"><span data-stu-id="1af8c-180">The  _lpszProfileName_ parameter is ignored if there is an existing previous session that called MapiLogonEx with the MAPI_ALLOW_OTHERS flag set and if the flag MAPI_NEW_SESSION is not set.</span></span> <span data-ttu-id="1af8c-181">_lpszProfileName_ パラメーターが NULL または空の文字列をポイントし _、flFlags_ パラメーターに MAPI_LOGON_UI フラグが含まれる場合、MAPILogonEx 関数は、プロファイル名の空のフィールドを持つログオン ダイアログ ボックスを生成します。</span><span class="sxs-lookup"><span data-stu-id="1af8c-181">If the  _lpszProfileName_ parameter is NULL or points to an empty string, and the  _flFlags_ parameter includes the MAPI_LOGON_UI flag, the MAPILogonEx function generates a logon dialog box that has an empty field for the profile name.</span></span> 
  
<span data-ttu-id="1af8c-182">特定のプロファイルにログオンする場合、クライアントはプロファイル名に加MAPI_NEW_SESSION MAPILogonEx にメッセージ フラグを渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="1af8c-182">When logging on to a specific profile, a client should pass the MAPI_NEW_SESSION flag into MAPILogonEx in addition to the profile name.</span></span> <span data-ttu-id="1af8c-183">それ以外の場合、別のクライアントが MAPI_ALLOW_OTHERS でログオンして共有セッションを確立した場合、クライアントは要求されたプロファイルではなく共有セッションにログオンします。</span><span class="sxs-lookup"><span data-stu-id="1af8c-183">Otherwise, if another client has established a shared session by logging on with MAPI_ALLOW_OTHERS, the client will be logged on to the shared session instead of to the profile requested.</span></span> 
  
<span data-ttu-id="1af8c-184">この MAPI_EXPLICIT_PROFILEフラグを指定しても  _、lpszProfileName_ が NULL または空の場合、既定のプロファイル名は使用されません(MAPI_USE_DEFAULT フラグも存在しない限り)。</span><span class="sxs-lookup"><span data-stu-id="1af8c-184">The MAPI_EXPLICIT_PROFILE flag does not cause the default profile name to be used when  _lpszProfileName_ is NULL or empty unless the MAPI_USE_DEFAULT flag is also present.</span></span> 
  
<span data-ttu-id="1af8c-185">このMAPI_NO_MAILには、MAPI スプーラーを使用しない場合に次のような効果があります。</span><span class="sxs-lookup"><span data-stu-id="1af8c-185">The MAPI_NO_MAIL flag has several effects that cause the following when not using the MAPI spooler:</span></span>
  
- <span data-ttu-id="1af8c-186">このセッション中に MAPI スプーラーによってメッセージを送信または配信できません。</span><span class="sxs-lookup"><span data-stu-id="1af8c-186">No messages can be sent or delivered by the MAPI spooler during this session.</span></span> <span data-ttu-id="1af8c-187">緊密に結合されたストアプロバイダーとトランスポート プロバイダーだけがメッセージを送受信できます。</span><span class="sxs-lookup"><span data-stu-id="1af8c-187">Only tightly coupled store and transport providers can send and deliver messages.</span></span> 
    
- <span data-ttu-id="1af8c-188">サーバー ベースのストアは、メッセージを送信または配信する場合があります。</span><span class="sxs-lookup"><span data-stu-id="1af8c-188">Server based stores might still send or deliver messages.</span></span> 
    
- <span data-ttu-id="1af8c-189">サーバー ベースのストアによって送信または配信されたメッセージは、フック プロバイダーによって処理されません。</span><span class="sxs-lookup"><span data-stu-id="1af8c-189">Messages sent or delivered by server based stores are not processed by any hook providers.</span></span> 
    
- <span data-ttu-id="1af8c-190">トランスポートのメッセージごとのオプションと受信者ごとのオプションは使用できません。</span><span class="sxs-lookup"><span data-stu-id="1af8c-190">Per-message and per-recipient options for transports are not available.</span></span> 
    
- <span data-ttu-id="1af8c-191">状態テーブルにはトランスポート プロバイダーのエントリは含めず、状態オブジェクトに依存するトランスポート機能 (構成など) は使用できません。</span><span class="sxs-lookup"><span data-stu-id="1af8c-191">The status table does not contain entries for transport providers, and any transport functionality dependent on status objects (such as configuration) is not available.</span></span> 
    
- <span data-ttu-id="1af8c-192">状態テーブルのメッセージ スプーラー行には、次の値STATUS_FAILUREされます。</span><span class="sxs-lookup"><span data-stu-id="1af8c-192">The message spooler row in the status table contains the STATUS_FAILURE value.</span></span> 
    
- <span data-ttu-id="1af8c-193">ピギーバックされたログオンは許可されますが、これらのログオンでは、前回のログオンで状態オブジェクトの更新プログラムが受信されません。</span><span class="sxs-lookup"><span data-stu-id="1af8c-193">Piggybacked logons are allowed, but those logons do not cause the previous logon to receive status object updates.</span></span> 
    
<span data-ttu-id="1af8c-194">サービスは常に、このフラグを使用MAPI_NO_MAILする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1af8c-194">A service should always log on using the MAPI_NO_MAIL flag.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1af8c-195">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="1af8c-195">MFCMAPI reference</span></span>

<span data-ttu-id="1af8c-196">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1af8c-196">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1af8c-197">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="1af8c-197">**File**</span></span>|<span data-ttu-id="1af8c-198">**関数**</span><span class="sxs-lookup"><span data-stu-id="1af8c-198">**Function**</span></span>|<span data-ttu-id="1af8c-199">**コメント**</span><span class="sxs-lookup"><span data-stu-id="1af8c-199">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1af8c-200">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="1af8c-200">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="1af8c-201">CMapiObjects::MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="1af8c-201">CMapiObjects::MAPILogonEx</span></span>  <br/> |<span data-ttu-id="1af8c-202">MFCMAPI は MAPILogonEx メソッドを使用して MAPI にログオンします。</span><span class="sxs-lookup"><span data-stu-id="1af8c-202">MFCMAPI uses the MAPILogonEx method to log on to MAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1af8c-203">関連項目</span><span class="sxs-lookup"><span data-stu-id="1af8c-203">See also</span></span>



[<span data-ttu-id="1af8c-204">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="1af8c-204">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="1af8c-205">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="1af8c-205">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)


<span data-ttu-id="1af8c-206">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="1af8c-206">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

