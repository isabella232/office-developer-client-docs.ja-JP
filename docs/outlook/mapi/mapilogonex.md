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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 08782fe616fe260388cff8982dfbb09951453a00
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801493"
---
# <a name="mapilogonex"></a><span data-ttu-id="ffead-103">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="ffead-103">MAPILogonEx</span></span>

  
  
<span data-ttu-id="ffead-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ffead-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ffead-105">メッセージング システムとのセッションに、クライアント アプリケーションを記録します。</span><span class="sxs-lookup"><span data-stu-id="ffead-105">Logs a client application on to a session with the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ffead-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ffead-106">Header file:</span></span>  <br/> |<span data-ttu-id="ffead-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="ffead-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="ffead-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="ffead-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ffead-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ffead-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ffead-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ffead-110">Called by:</span></span>  <br/> |<span data-ttu-id="ffead-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="ffead-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPILogonEx(
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  FLAGS flFlags,
  LPMAPISESSION FAR * lppSession
);
```

## <a name="parameters"></a><span data-ttu-id="ffead-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="ffead-112">Parameters</span></span>

 <span data-ttu-id="ffead-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="ffead-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="ffead-114">[in][ログオン] ダイアログ ボックスはモーダル ウィンドウへのハンドルします。</span><span class="sxs-lookup"><span data-stu-id="ffead-114">[in] Handle to the window to which the logon dialog box is modal.</span></span> <span data-ttu-id="ffead-115">呼び出し時にダイアログ ボックスが表示されない場合は、 _ulUIParam_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="ffead-115">If no dialog box appears during the call, the  _ulUIParam_ parameter is ignored.</span></span> <span data-ttu-id="ffead-116">このパラメーターは、0 にすることができます。</span><span class="sxs-lookup"><span data-stu-id="ffead-116">This parameter can be zero.</span></span> 
    
 <span data-ttu-id="ffead-117">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="ffead-117">_lpszProfileName_</span></span>
  
> <span data-ttu-id="ffead-118">[in]ユーザーがログオンしたときに使用するプロファイルの名前を含む文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ffead-118">[in] Pointer to a string that contains the name of the profile to use when the user logs on.</span></span> <span data-ttu-id="ffead-119">この文字列は、64 文字に制限されています。</span><span class="sxs-lookup"><span data-stu-id="ffead-119">This string is limited to 64 characters.</span></span>
    
 <span data-ttu-id="ffead-120">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="ffead-120">_lpszPassword_</span></span>
  
> <span data-ttu-id="ffead-121">[in]プロファイルのパスワードを含む文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ffead-121">[in] Pointer to a string that contains the password of the profile.</span></span> <span data-ttu-id="ffead-122">_LpszPassword_パラメーターは、NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffead-122">The  _lpszPassword_ parameter must be NULL.</span></span> 
    
 <span data-ttu-id="ffead-123">_flFlags_</span><span class="sxs-lookup"><span data-stu-id="ffead-123">_flFlags_</span></span>
  
> <span data-ttu-id="ffead-124">[in]ログオンを実行する方法を制御するためのフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="ffead-124">[in] Bitmask of flags used to control how logon is performed.</span></span> <span data-ttu-id="ffead-125">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="ffead-125">The following flags can be set:</span></span>
    
<span data-ttu-id="ffead-126">MAPI_ALLOW_OTHERS</span><span class="sxs-lookup"><span data-stu-id="ffead-126">MAPI_ALLOW_OTHERS</span></span> 
  
> <span data-ttu-id="ffead-127">以降のクライアントのユーザーの資格情報を提供することがなくセッションを取得することができますが、共有セッションが返されます。</span><span class="sxs-lookup"><span data-stu-id="ffead-127">The shared session should be returned, which allows later clients to obtain the session without providing any user credentials.</span></span> 
    
<span data-ttu-id="ffead-128">MAPI_BG_SESSION</span><span class="sxs-lookup"><span data-stu-id="ffead-128">MAPI_BG_SESSION</span></span>
  
> <span data-ttu-id="ffead-129">セッションにログオンし、バック グラウンドですべての操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="ffead-129">Log on to a session and run any operations in the background.</span></span> <span data-ttu-id="ffead-130">一般に、クライアントがバック グラウンド スレッドかフォア グラウンド スレッドに目障りではない方法で別のプロセスでの処理を実行しようとすると場合は、MAPI_BG_SESSION フラグを指定して呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffead-130">In general, if a client intends to do processing on a background thread or in a separate process in a manner that is unobtrusive to the foreground thread, it should call with the MAPI_BG_SESSION flag.</span></span> <span data-ttu-id="ffead-131">インデックス エンジンまたはバック グラウンドのアクセス権の種類の個人用フォルダー ファイル (PST) を開くなどのクライアント アプリケーションは、MAPI_BG_SESSION を使用する場所の例を示します。MAPILogonEx。</span><span class="sxs-lookup"><span data-stu-id="ffead-131">A client application such as an indexing engine or opening a Personal Folders File (PST) for background type access are some examples of where to use MAPI_BG_SESSION.MAPILogonEx.</span></span>
    
<span data-ttu-id="ffead-132">MAPI_EXPLICIT_PROFILE</span><span class="sxs-lookup"><span data-stu-id="ffead-132">MAPI_EXPLICIT_PROFILE</span></span> 
  
> <span data-ttu-id="ffead-133">既定のプロファイルを使用しない必要があり、ユーザーはプロファイルを指定する要求する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffead-133">The default profile should not be used and the user should be required to supply a profile.</span></span> 
    
<span data-ttu-id="ffead-134">MAPI_EXTENDED</span><span class="sxs-lookup"><span data-stu-id="ffead-134">MAPI_EXTENDED</span></span> 
  
> <span data-ttu-id="ffead-135">拡張機能を使用してログオンします。</span><span class="sxs-lookup"><span data-stu-id="ffead-135">Log on with extended capabilities.</span></span> <span data-ttu-id="ffead-136">このフラグを設定することが常にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffead-136">This flag should always be set.</span></span>
    
<span data-ttu-id="ffead-137">MAPI_FORCE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="ffead-137">MAPI_FORCE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="ffead-138">返す前にすべてのユーザーのメッセージをダウンロードするのには試行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffead-138">An attempt should be made to download all of the user's messages before returning.</span></span> <span data-ttu-id="ffead-139">MAPI_FORCE_DOWNLOAD フラグが設定されていない場合、MAPILogonEx への呼び出しが返された後のメッセージはバック グラウンドでダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="ffead-139">If the MAPI_FORCE_DOWNLOAD flag is not set, messages can be downloaded in the background after the call to MAPILogonEx returns.</span></span> 
    
<span data-ttu-id="ffead-140">MAPI_LOGON_UI</span><span class="sxs-lookup"><span data-stu-id="ffead-140">MAPI_LOGON_UI</span></span> 
  
> <span data-ttu-id="ffead-141">ダイアログ ボックスは、ログオン情報を求めるメッセージが必要な場合に表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffead-141">A dialog box should be displayed to prompt the user for logon information if required.</span></span> <span data-ttu-id="ffead-142">MAPI_LOGON_UI フラグが設定されていないと呼び出し元のクライアント ログオンのダイアログ ボックスは表示されません、ユーザーがログオンしていない場合、エラー値を返します。</span><span class="sxs-lookup"><span data-stu-id="ffead-142">When the MAPI_LOGON_UI flag is not set, the calling client does not display a logon dialog box and returns an error value if the user is not logged on.</span></span>
    
<span data-ttu-id="ffead-143">MAPI_NEW_SESSION</span><span class="sxs-lookup"><span data-stu-id="ffead-143">MAPI_NEW_SESSION</span></span> 
  
> <span data-ttu-id="ffead-144">共有セッションを取得するのではなく新しい MAPI セッションを作成する試行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffead-144">An attempt should be made to create a new MAPI session instead of acquiring the shared session.</span></span> <span data-ttu-id="ffead-145">MAPI_NEW_SESSION フラグが設定されていない場合、MAPILogonEx は、 _lpszprofileName_パラメーターが NULL でない場合でも、既存の共有セッションを使用します。</span><span class="sxs-lookup"><span data-stu-id="ffead-145">If the MAPI_NEW_SESSION flag is not set, MAPILogonEx uses an existing shared session even if the  _lpszprofileName_ parameter is not NULL.</span></span> 
    
<span data-ttu-id="ffead-146">MAPI_NO_MAIL</span><span class="sxs-lookup"><span data-stu-id="ffead-146">MAPI_NO_MAIL</span></span> 
  
> <span data-ttu-id="ffead-147">MAPI は MAPI スプーラー セッションの存在を通知する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffead-147">MAPI should not inform the MAPI spooler of the session's existence.</span></span> <span data-ttu-id="ffead-148">メッセージの送信も密結合を保存 [トランスポートのペア以外のセッションで受信したことになります。</span><span class="sxs-lookup"><span data-stu-id="ffead-148">The result is that no messages can be sent or received in the session except through a tightly coupled store and transport pair.</span></span> <span data-ttu-id="ffead-149">呼び出し側のクライアントは、構成作業を行う必要がある場合、エージェントとして動作しています。 クライアントが使用可能なメッセージ ストアを参照する場合、またはこのフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="ffead-149">A calling client sets this flag if it is acting as an agent, if configuration work must be done, or if the client is browsing the available message stores.</span></span> 
    
<span data-ttu-id="ffead-150">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="ffead-150">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="ffead-151">呼び出し元は、Windows サービスとして実行しています。</span><span class="sxs-lookup"><span data-stu-id="ffead-151">The caller is running as a Windows service.</span></span> <span data-ttu-id="ffead-152">Windows サービスではこのフラグが設定されていない必要がありますように実行されていない呼び出し元サービスとして実行されている呼び出し元は、このフラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffead-152">Callers that are not running as a Windows service should not set this flag; callers that are running as a service must set this flag.</span></span> 
    
<span data-ttu-id="ffead-153">MAPI_SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="ffead-153">MAPI_SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="ffead-154">MAPILogonEx は、プロファイル内の各メッセージ サービスの構成] ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ffead-154">MAPILogonEx should display a configuration dialog box for each message service in the profile.</span></span> <span data-ttu-id="ffead-155">プロファイルが選択されていますが、任意のメッセージの前にサービスがログオンした後、ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ffead-155">The dialog boxes are displayed after the profile has been chosen but before any message service is logged on.</span></span> <span data-ttu-id="ffead-156">ログオンの MAPI のコモン ダイアログ ボックスには、同じ操作を要求する] チェック ボックスも含まれています。</span><span class="sxs-lookup"><span data-stu-id="ffead-156">The MAPI common dialog box for logon also contains a check box that requests the same operation.</span></span> 
    
<span data-ttu-id="ffead-157">MAPI_TIMEOUT_SHORT</span><span class="sxs-lookup"><span data-stu-id="ffead-157">MAPI_TIMEOUT_SHORT</span></span> 
  
> <span data-ttu-id="ffead-158">数秒以上ブロックされている場合、ログオンが失敗する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffead-158">The logon should fail if blocked for more than a few seconds.</span></span> 
    
<span data-ttu-id="ffead-159">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ffead-159">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ffead-160">渡された文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="ffead-160">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="ffead-161">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="ffead-161">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="ffead-162">MAPI_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ffead-162">MAPI_USE_DEFAULT</span></span> 
  
> <span data-ttu-id="ffead-163">メッセージング サブシステムでは、 _lpszProfileName_パラメーターの既定のプロファイルのプロファイル名を置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffead-163">The messaging subsystem should substitute the profile name of the default profile for the  _lpszProfileName_ parameter.</span></span> <span data-ttu-id="ffead-164">_LpszProfileName_が NULL または空でない場合、MAPI_EXPLICIT_PROFILE フラグは無視されます。</span><span class="sxs-lookup"><span data-stu-id="ffead-164">The MAPI_EXPLICIT_PROFILE flag is ignored unless  _lpszProfileName_ is NULL or empty.</span></span> 
    
 <span data-ttu-id="ffead-165">_lppSession_</span><span class="sxs-lookup"><span data-stu-id="ffead-165">_lppSession_</span></span>
  
> <span data-ttu-id="ffead-166">[out]MAPI セッションのインターフェイスへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ffead-166">[out] Pointer to a pointer to the MAPI session interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ffead-167">�߂�l</span><span class="sxs-lookup"><span data-stu-id="ffead-167">Return value</span></span>

<span data-ttu-id="ffead-168">S_OK</span><span class="sxs-lookup"><span data-stu-id="ffead-168">S_OK</span></span> 
  
> <span data-ttu-id="ffead-169">ログオンに成功しました。</span><span class="sxs-lookup"><span data-stu-id="ffead-169">The logon succeeded.</span></span>
    
<span data-ttu-id="ffead-170">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="ffead-170">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="ffead-171">MAPILogonEx パラメーターの 1 つ以上無効であったためか、または存在しているセッションが多すぎます既にために、ログオンは成功すると、でした。</span><span class="sxs-lookup"><span data-stu-id="ffead-171">The logon was unsuccessful, either because one or more of the parameters to MAPILogonEx were invalid or because there were too many sessions open already.</span></span>
    
<span data-ttu-id="ffead-172">MAPI_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="ffead-172">MAPI_E_TIMEOUT</span></span> 
  
> <span data-ttu-id="ffead-173">MAPI では、すべてのログオン ミュー テックスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="ffead-173">MAPI serializes all logons through a mutex.</span></span> <span data-ttu-id="ffead-174">MAPI_TIMEOUT_SHORT フラグが設定された別のスレッドには、相互排他ロックが保持されている場合、この関数が返されます。</span><span class="sxs-lookup"><span data-stu-id="ffead-174">This is returned if the MAPI_TIMEOUT_SHORT flag was set and another thread held the mutex.</span></span> 
    
<span data-ttu-id="ffead-175">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="ffead-175">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="ffead-176">ユーザー操作がキャンセルされました、通常ダイアログ ボックスで [**キャンセル**] ボタンをクリックするとします。</span><span class="sxs-lookup"><span data-stu-id="ffead-176">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ffead-177">備考</span><span class="sxs-lookup"><span data-stu-id="ffead-177">Remarks</span></span>

<span data-ttu-id="ffead-178">MAPI クライアント アプリケーションでは、メッセージング システムとのセッションにログオンする MAPILogonEx 関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ffead-178">MAPI client applications call the MAPILogonEx function to log on to a session with the messaging system.</span></span> <span data-ttu-id="ffead-179">渡されして、MAPI の呼び出しから返されるすべての文字列は null で終わるが現在の文字セットで指定する必要がありますや、コードの呼び出し元のクライアントやプロバイダーのオペレーティング システムのページ。</span><span class="sxs-lookup"><span data-stu-id="ffead-179">All strings that are passed in and returned to and from MAPI calls are null-terminated and must be specified in the current character set or code page of the calling client or provider's operating system.</span></span>
  
<span data-ttu-id="ffead-180">フラグ MAPI_NEW_SESSION が設定されていない場合、MAPI_ALLOW_OTHERS フラグを設定して [MapiLogonEx と呼ばれる既存の以前のセッションがある場合、 _lpszProfileName_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="ffead-180">The  _lpszProfileName_ parameter is ignored if there is an existing previous session that called MapiLogonEx with the MAPI_ALLOW_OTHERS flag set and if the flag MAPI_NEW_SESSION is not set.</span></span> <span data-ttu-id="ffead-181">_LpszProfileName_パラメーターが NULL または空の文字列、および_flFlags_パラメーターへのポインターには、MAPI_LOGON_UI フラグが含まれています、MAPILogonEx 関数は、プロファイル名を空のフィールドを持つログオン] ダイアログ ボックスを生成します。</span><span class="sxs-lookup"><span data-stu-id="ffead-181">If the  _lpszProfileName_ parameter is NULL or points to an empty string, and the  _flFlags_ parameter includes the MAPI_LOGON_UI flag, the MAPILogonEx function generates a logon dialog box that has an empty field for the profile name.</span></span> 
  
<span data-ttu-id="ffead-182">特定のプロファイルにログオンしていると、クライアントする必要がありますフラグを渡す MAPI_NEW_SESSION MAPILogonEx にプロファイル名だけでなく。</span><span class="sxs-lookup"><span data-stu-id="ffead-182">When logging on to a specific profile, a client should pass the MAPI_NEW_SESSION flag into MAPILogonEx in addition to the profile name.</span></span> <span data-ttu-id="ffead-183">それ以外の場合場合、別のクライアントは、MAPI_ALLOW_OTHERS にログオンし、共有セッションを確立しましたが、クライアントがログオンするプロファイルを要求するのではなく共有セッションに。</span><span class="sxs-lookup"><span data-stu-id="ffead-183">Otherwise, if another client has established a shared session by logging on with MAPI_ALLOW_OTHERS, the client will be logged on to the shared session instead of to the profile requested.</span></span> 
  
<span data-ttu-id="ffead-184">MAPI_EXPLICIT_PROFILE フラグ_lpszProfileName_が NULL の場合に使用する既定のプロファイル名が発生したりしない空の場合を除き、MAPI_USE_DEFAULT のフラグもあります。</span><span class="sxs-lookup"><span data-stu-id="ffead-184">The MAPI_EXPLICIT_PROFILE flag does not cause the default profile name to be used when  _lpszProfileName_ is NULL or empty unless the MAPI_USE_DEFAULT flag is also present.</span></span> 
  
<span data-ttu-id="ffead-185">MAPI_NO_MAIL フラグには、MAPI スプーラーを使用するいないと、次が発生するいくつかの効果があります。</span><span class="sxs-lookup"><span data-stu-id="ffead-185">The MAPI_NO_MAIL flag has several effects that cause the following when not using the MAPI spooler:</span></span>
  
- <span data-ttu-id="ffead-186">メッセージの送信もこのセッション中に、MAPI スプーラーによって配信されることができます。</span><span class="sxs-lookup"><span data-stu-id="ffead-186">No messages can be sent or delivered by the MAPI spooler during this session.</span></span> <span data-ttu-id="ffead-187">唯一の密結合ストアおよびトランスポート プロバイダーは、送信し、メッセージを配信できます。</span><span class="sxs-lookup"><span data-stu-id="ffead-187">Only tightly coupled store and transport providers can send and deliver messages.</span></span> 
    
- <span data-ttu-id="ffead-188">サーバー ベース ストアの送信またはメッセージの配信可能性がありますもします。</span><span class="sxs-lookup"><span data-stu-id="ffead-188">Server based stores might still send or deliver messages.</span></span> 
    
- <span data-ttu-id="ffead-189">フック プロバイダーによって送信またはサーバー ベースのストアに配信されるメッセージは処理されません。</span><span class="sxs-lookup"><span data-stu-id="ffead-189">Messages sent or delivered by server based stores are not processed by any hook providers.</span></span> 
    
- <span data-ttu-id="ffead-190">メッセージと受信者ごとのトランスポート オプションはご利用いただけません。</span><span class="sxs-lookup"><span data-stu-id="ffead-190">Per-message and per-recipient options for transports are not available.</span></span> 
    
- <span data-ttu-id="ffead-191">ステータス テーブルに、トランスポート プロバイダーのエントリが含まれていないと、(構成) などのオブジェクトの状態に依存する任意のトランスポート機能を利用できません。</span><span class="sxs-lookup"><span data-stu-id="ffead-191">The status table does not contain entries for transport providers, and any transport functionality dependent on status objects (such as configuration) is not available.</span></span> 
    
- <span data-ttu-id="ffead-192">メッセージ スプーラー テーブル内の行ステータスにはには、STATUS_FAILURE の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ffead-192">The message spooler row in the status table contains the STATUS_FAILURE value.</span></span> 
    
- <span data-ttu-id="ffead-193">上乗せのログオンが許可されるが、これらのログオン状態のオブジェクトの更新を受信する前のログオンは発生しません。</span><span class="sxs-lookup"><span data-stu-id="ffead-193">Piggybacked logons are allowed, but those logons do not cause the previous logon to receive status object updates.</span></span> 
    
<span data-ttu-id="ffead-194">サービスは、MAPI_NO_MAIL フラグを使用してをログオンする必要があります常にします。</span><span class="sxs-lookup"><span data-stu-id="ffead-194">A service should always log on using the MAPI_NO_MAIL flag.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ffead-195">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="ffead-195">MFCMAPI reference</span></span>

<span data-ttu-id="ffead-196">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="ffead-196">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ffead-197">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="ffead-197">**File**</span></span>|<span data-ttu-id="ffead-198">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="ffead-198">**Function**</span></span>|<span data-ttu-id="ffead-199">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="ffead-199">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ffead-200">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="ffead-200">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="ffead-201">CMapiObjects::MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="ffead-201">CMapiObjects::MAPILogonEx</span></span>  <br/> |<span data-ttu-id="ffead-202">MFCMAPI では、MAPILogonEx メソッドを使用して、MAPI にログオンします。</span><span class="sxs-lookup"><span data-stu-id="ffead-202">MFCMAPI uses the MAPILogonEx method to log on to MAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ffead-203">関連項目</span><span class="sxs-lookup"><span data-stu-id="ffead-203">See also</span></span>



[<span data-ttu-id="ffead-204">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="ffead-204">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="ffead-205">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="ffead-205">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)


<span data-ttu-id="ffead-206">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="ffead-206">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

