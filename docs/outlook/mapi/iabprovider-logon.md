---
title: IABProviderLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABProvider.Logon
api_type:
- COM
ms.assetid: f9468715-1674-4d14-81c8-2f24dbaa0453
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 21a6907f7511779d7e8ec6825ac68d109d2f48eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800360"
---
# <a name="iabproviderlogon"></a><span data-ttu-id="5834d-103">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="5834d-103">IABProvider::Logon</span></span>

  
  
<span data-ttu-id="5834d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5834d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5834d-105">アクティブなセッションへの接続を確立します。</span><span class="sxs-lookup"><span data-stu-id="5834d-105">Establishes a connection to an active session.</span></span>
  
```cpp
HRESULT Logon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG ulFlags,
  ULONG FAR * lpulcbSecurity,
  LPBYTE FAR * lppbSecurity,
  LPMAPIERROR FAR * lppMAPIError,
  LPABLOGON FAR * lppABLogon
);
```

## <a name="parameters"></a><span data-ttu-id="5834d-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="5834d-106">Parameters</span></span>

 <span data-ttu-id="5834d-107">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="5834d-107">_lpMAPISup_</span></span>
  
> <span data-ttu-id="5834d-108">[in]アドレス帳プロバイダーのサポートのオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5834d-108">[in] A pointer to the address book provider's support object.</span></span>
    
 <span data-ttu-id="5834d-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="5834d-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="5834d-110">[in]許可されている場合、**ログオン**方法を表示する [ログオン] ダイアログ ボックスの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="5834d-110">[in] A handle to the parent window for the logon dialog box that the **Logon** method displays, if permitted.</span></span> <span data-ttu-id="5834d-111">_UlUIParam_パラメーターには、MAPI [MAPILogonEx](mapilogonex.md)関数には、以前の呼び出しで渡された同じ名前のパラメーターの値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5834d-111">The  _ulUIParam_ parameter contains the value of the parameter of the same name passed to MAPI in the previous call to the [MAPILogonEx](mapilogonex.md) function.</span></span> 
    
 <span data-ttu-id="5834d-112">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="5834d-112">_lpszProfileName_</span></span>
  
> <span data-ttu-id="5834d-113">[in]セッション ・ プロファイルの名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5834d-113">[in] A pointer to the name of the session profile.</span></span>
    
 <span data-ttu-id="5834d-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5834d-114">_ulFlags_</span></span>
  
> <span data-ttu-id="5834d-115">[in]ログオンを実行する方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="5834d-115">[in] A bitmask of flags that controls how the logon is performed.</span></span> <span data-ttu-id="5834d-116">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="5834d-116">The following flags can be set:</span></span>
    
<span data-ttu-id="5834d-117">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="5834d-117">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="5834d-118">プロバイダーは、ログオン時にダイアログ ボックスを表示しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="5834d-118">The provider should not display a dialog box during logon.</span></span> <span data-ttu-id="5834d-119">このフラグが設定されていない場合、プロバイダーは、構成情報が不足しているユーザーの入力を求めるダイアログ ボックスを表示できます。</span><span class="sxs-lookup"><span data-stu-id="5834d-119">If this flag is not set, the provider can display a dialog box to prompt the user for missing configuration information.</span></span>
    
<span data-ttu-id="5834d-120">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="5834d-120">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="5834d-121">正常に完了可能性がありますログオン プロセスを完了する前に**ログオン**を有効にします。</span><span class="sxs-lookup"><span data-stu-id="5834d-121">Enables **Logon** to return successfully, possibly before the logon process is finished.</span></span> 
    
<span data-ttu-id="5834d-122">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5834d-122">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="5834d-123">すべての文字列は、Unicode 形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="5834d-123">All strings should be in Unicode format.</span></span> <span data-ttu-id="5834d-124">MAPI_UNICODE フラグが設定されていない場合、ANSI 形式の文字列を引き起こすことがあります。</span><span class="sxs-lookup"><span data-stu-id="5834d-124">If the MAPI_UNICODE flag is not set, the strings should be in ANSI format.</span></span>
    
 <span data-ttu-id="5834d-125">_lpulcbSecurity_</span><span class="sxs-lookup"><span data-stu-id="5834d-125">_lpulcbSecurity_</span></span>
  
> <span data-ttu-id="5834d-126">[で [チェック アウト]_LppbSecurity_パラメーターで指定されたセキュリティ資格情報の構造体のバイト単位のサイズへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5834d-126">[in, out] A pointer to the size, in bytes, of the security credentials structure pointed to by the  _lppbSecurity_ parameter.</span></span> <span data-ttu-id="5834d-127">入力では、値を 0 以外にする必要があります。出力では、値は 0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5834d-127">On input, the value must be nonzero; on output, the value must be zero.</span></span> <span data-ttu-id="5834d-128">どちらの場合も、ポインターが有効でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="5834d-128">In both cases, the pointers must be valid.</span></span> 
    
 <span data-ttu-id="5834d-129">_lppbSecurity_</span><span class="sxs-lookup"><span data-stu-id="5834d-129">_lppbSecurity_</span></span>
  
> <span data-ttu-id="5834d-130">[で [チェック アウト]セキュリティの資格情報へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5834d-130">[in, out] A pointer to a pointer to security credentials.</span></span> <span data-ttu-id="5834d-131">入力では、値を 0 以外にする必要があります。出力では、値は 0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5834d-131">On input, the value must be nonzero; on output, the value must be zero.</span></span> <span data-ttu-id="5834d-132">どちらの場合も、ポインターが有効でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="5834d-132">In both cases the pointer must be valid.</span></span>
    
 <span data-ttu-id="5834d-133">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="5834d-133">_lppMAPIError_</span></span>
  
> <span data-ttu-id="5834d-134">[out][MAPIERROR](mapierror.md)構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5834d-134">[out] A pointer to a pointer to a [MAPIERROR](mapierror.md) structure.</span></span> <span data-ttu-id="5834d-135">取得する**MAPIERROR**構造体がない場合、 _lppMAPIError_パラメーターを NULL に設定できます。</span><span class="sxs-lookup"><span data-stu-id="5834d-135">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
 <span data-ttu-id="5834d-136">_lppABLogon_</span><span class="sxs-lookup"><span data-stu-id="5834d-136">_lppABLogon_</span></span>
  
> <span data-ttu-id="5834d-137">[out]プロバイダーのログオン オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5834d-137">[out] A pointer to a pointer to the provider's logon object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5834d-138">�߂�l</span><span class="sxs-lookup"><span data-stu-id="5834d-138">Return value</span></span>

<span data-ttu-id="5834d-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="5834d-139">S_OK</span></span> 
  
> <span data-ttu-id="5834d-140">アクティブなセッションへの接続が正常に確立しました。</span><span class="sxs-lookup"><span data-stu-id="5834d-140">A connection to an active session was successfully established.</span></span>
    
<span data-ttu-id="5834d-141">MAPI_E_FAILONEPROVIDER</span><span class="sxs-lookup"><span data-stu-id="5834d-141">MAPI_E_FAILONEPROVIDER</span></span> 
  
> <span data-ttu-id="5834d-142">プロバイダーがログオンできないが、MAPI は、メッセージ サービス プロバイダーが所属するその他のプロバイダーにログインを続行できます。</span><span class="sxs-lookup"><span data-stu-id="5834d-142">The provider cannot log on, but MAPI can continue to log on the other providers in the message service to which the provider belongs.</span></span> 
    
<span data-ttu-id="5834d-143">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="5834d-143">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="5834d-144">プロバイダーには、ログオンを完了する十分な情報があります。</span><span class="sxs-lookup"><span data-stu-id="5834d-144">The provider has insufficient information to complete the logon.</span></span> <span data-ttu-id="5834d-145">MAPI は、プロバイダーのメッセージ サービスのエントリ関数が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5834d-145">MAPI calls the provider's message service entry function.</span></span>
    
<span data-ttu-id="5834d-146">MAPI_E_UNKNOWN_CPID</span><span class="sxs-lookup"><span data-stu-id="5834d-146">MAPI_E_UNKNOWN_CPID</span></span> 
  
> <span data-ttu-id="5834d-147">サーバーは、クライアントのコード ページをサポートするために構成されていません。</span><span class="sxs-lookup"><span data-stu-id="5834d-147">The server is not configured to support the client's code page.</span></span>
    
<span data-ttu-id="5834d-148">MAPI_E_UNKNOWN_LCID</span><span class="sxs-lookup"><span data-stu-id="5834d-148">MAPI_E_UNKNOWN_LCID</span></span> 
  
> <span data-ttu-id="5834d-149">サーバーは、クライアントのロケール情報をサポートするために構成されていません。</span><span class="sxs-lookup"><span data-stu-id="5834d-149">The server is not configured to support the client's locale information.</span></span>
    
<span data-ttu-id="5834d-150">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="5834d-150">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="5834d-151">ユーザー操作がキャンセルされました、通常、[ログオン] ダイアログ ボックスで [**キャンセル**] ボタンをクリックするとします。</span><span class="sxs-lookup"><span data-stu-id="5834d-151">The user canceled the operation, typically by clicking the **Cancel** button in the logon dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5834d-152">備考</span><span class="sxs-lookup"><span data-stu-id="5834d-152">Remarks</span></span>

<span data-ttu-id="5834d-153">各アドレス帳プロバイダーには、クライアントが、 [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md)メソッドを呼び出すと、セッション ・ プロファイルで接続を確立します。</span><span class="sxs-lookup"><span data-stu-id="5834d-153">Connections are established with each address book provider in the session profile when a client calls the [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) method.</span></span> <span data-ttu-id="5834d-154">**OpenAddressBook**は、各プロバイダーの**ログオン**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5834d-154">**OpenAddressBook** then calls each provider's **Logon** method.</span></span> 
  
<span data-ttu-id="5834d-155">_UlFlags_パラメーターの MAPI_UNICODE フラグの有無によって示されているように、ユーザーのクライアントの文字セットでは、 _lpszProfileName_パラメーターで指定されたプロファイル名が表示されます。</span><span class="sxs-lookup"><span data-stu-id="5834d-155">The profile name pointed to by the  _lpszProfileName_ parameter is displayed in the character set of the user's client as indicated by the presence or absence of the MAPI_UNICODE flag in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5834d-156">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="5834d-156">Notes to implementers</span></span>

<span data-ttu-id="5834d-157">**ログオン**メソッドの実装では、一意の識別子、または[MAPIUID](mapiuid.md)の構造体を登録するのには[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5834d-157">In your implementation of the **Logon** method, call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register a unique identifier, or [MAPIUID](mapiuid.md) structure.</span></span> <span data-ttu-id="5834d-158">この**MAPIUID**を含むエントリの識別子をオブジェクトのがあります。</span><span class="sxs-lookup"><span data-stu-id="5834d-158">Each of your objects will have an entry identifier that includes this **MAPIUID**.</span></span> <span data-ttu-id="5834d-159">MAPI では、そのプロバイダーを使用してオブジェクトを一致するように**MAPIUID**を使用します。</span><span class="sxs-lookup"><span data-stu-id="5834d-159">MAPI uses the **MAPIUID** to match an object with its provider.</span></span> <span data-ttu-id="5834d-160">たとえば、クライアントは、メッセージングのユーザーを開くには、 [IMAPISession::OpenEntry](imapisession-openentry.md)メソッドを呼び出すと、 **OpenEntry**を調べ、 **MAPIUID**の部分で渡されたしで登録されている**MAPIUID**の内容と一致するエントリの識別子をアドレス帳プロバイダー。</span><span class="sxs-lookup"><span data-stu-id="5834d-160">For example, when a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open a messaging user, **OpenEntry** examines the **MAPIUID** portion of the entry identifier that was passed in and matches it with a **MAPIUID** registered by an address book provider.</span></span> 
  
<span data-ttu-id="5834d-161">クライアント ログオンした場合、プロバイダーを複数回、ログオンのたびに別の**MAPIUID**を登録することがあります。</span><span class="sxs-lookup"><span data-stu-id="5834d-161">If a client logs on to your provider more than once, you may want to register a different **MAPIUID** for each logon.</span></span> <span data-ttu-id="5834d-162">独自の**MAPIUID**構造体を登録するには、適切なプロバイダーのインスタンスに要求を正しくルーティングするための MAPI が有効にします。</span><span class="sxs-lookup"><span data-stu-id="5834d-162">Registering unique **MAPIUID** structures enables MAPI to correctly route requests to the appropriate provider instance.</span></span> <span data-ttu-id="5834d-163">ただし、1 つの**MAPIUID**を共有するすべてのログオン オブジェクトが存在する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5834d-163">However, you may want to have every logon object share one **MAPIUID**.</span></span> <span data-ttu-id="5834d-164">この例では、する必要があります、ルーティングを処理するために MAPI を使用する代わりに自分でします。</span><span class="sxs-lookup"><span data-stu-id="5834d-164">In this case, you must be able to handle the routing yourself instead of relying on MAPI.</span></span> <span data-ttu-id="5834d-165">の**MAPIUID**を作成する方法の詳細については、[登録するサービス プロバイダー固有の識別子](registering-service-provider-unique-identifiers.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5834d-165">For more information about how to create a **MAPIUID**, see [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).</span></span>
  
<span data-ttu-id="5834d-166">MAPI が_lpMAPISup_パラメーターで、**ログオン**のメソッドに渡されるサポート オブジェクトに含まれているメソッドの多くへのアクセスを提供する、 [IMAPISupport: IUnknown](imapisupportiunknown.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="5834d-166">The support object that MAPI passes to your **Logon** method in the  _lpMAPISup_ parameter provides access to many of the methods included in the [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> <span data-ttu-id="5834d-167">MAPI では、プロバイダーの種類に合わせてカスタマイズされたサポート オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="5834d-167">MAPI creates a support object that is customized to your type of provider.</span></span> <span data-ttu-id="5834d-168">などの接続を確立すると、基になるメッセージング システムやディレクトリ サービスへのログオンが必要な場合は、この特定のログオン セッションのセキュリティ資格情報を取得するために[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="5834d-168">For example, if you need to log on to an underlying messaging system or directory service when you establish your connection, you can call the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to retrieve security credentials for this particular logon session.</span></span> 
  
<span data-ttu-id="5834d-169">**ログオン**が成功した場合、参照カウントをインクリメントするサポート オブジェクトの[IUnknown::AddRef](http://msdn.microsoft.com/ja-jp/library/ms691379%28VS.85%29.aspx)メソッドを呼び出すことを確認します。</span><span class="sxs-lookup"><span data-stu-id="5834d-169">If **Logon** is successful, be sure that you call the support object's [IUnknown::AddRef](http://msdn.microsoft.com/ja-jp/library/ms691379%28VS.85%29.aspx) method to increment its reference count.</span></span> <span data-ttu-id="5834d-170">これは、セッションの残りの部分のサポート オブジェクトへのポインターを保持するのには、プロバイダーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="5834d-170">This enables your provider to hold onto the support object pointer for the rest of the session.</span></span> <span data-ttu-id="5834d-171">この**AddRef**メソッドを呼び出していないと、MAPI は、プロバイダーをアンロードします。</span><span class="sxs-lookup"><span data-stu-id="5834d-171">If you do not call this **AddRef** method, MAPI will unload your provider.</span></span> 
  
<span data-ttu-id="5834d-172">エラー] ダイアログ ボックス、ログオン画面、または他のユーザー インターフェイス内の_lpszProfileName_パラメーターで渡されたプロファイルの名前を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="5834d-172">You can include the profile name passed in the  _lpszProfileName_ parameter in error dialog boxes, logon screens, or other user interfaces.</span></span> <span data-ttu-id="5834d-173">プロファイル名を使用するに割り当てた記憶域にコピーします。</span><span class="sxs-lookup"><span data-stu-id="5834d-173">To use the profile name, copy it to storage that you have allocated.</span></span> 
  
<span data-ttu-id="5834d-174">ログオン オブジェクトを作成し、 _lppABLogon_パラメーターで、それへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="5834d-174">Create a logon object and return a pointer to it in the  _lppABLogon_ parameter.</span></span> <span data-ttu-id="5834d-175">MAPI では、このログオン オブジェクトを使用して、 [IABLogon](iablogoniunknown.md)実装では、メソッドへの呼び出しを加えます。</span><span class="sxs-lookup"><span data-stu-id="5834d-175">MAPI uses this logon object to make calls to the methods in your [IABLogon](iablogoniunknown.md) implementation.</span></span> 
  
<span data-ttu-id="5834d-176">ログオン時にパスワードを必要とする場合は、AB_NO_DIALOG フラグが設定されていない場合にのみ、[ログオン] ダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="5834d-176">If you require a password during logon, display a logon dialog box only if the AB_NO_DIALOG flag is not set.</span></span> <span data-ttu-id="5834d-177">ユーザーは、ログオン プロセスをキャンセルした場合通常、ダイアログ ボックスで [**キャンセル**] ボタンをクリックすると、MAPI_E_USER_CANCEL から返す**ログオン**します。</span><span class="sxs-lookup"><span data-stu-id="5834d-177">If the user cancels the logon process, typically by clicking the **Cancel** button in the dialog box, return MAPI_E_USER_CANCEL from **Logon**.</span></span>
  
<span data-ttu-id="5834d-178">通常、アドレス帳プロバイダーはログオンできません、MAPI が無効になります、メッセージ サービスが障害のあるプロバイダーが所属する、つまり、MAPI しようとしてのいずれかのセッションの残りの部分のサービスに属している他のプロバイダーの接続を確立有効期間です。</span><span class="sxs-lookup"><span data-stu-id="5834d-178">Typically, when an address book provider cannot log on, MAPI disables the message service to which the failing provider belongs—that is, MAPI will not try to establish connections for any of the other providers that belong to the service for the rest of the session's lifetime.</span></span> <span data-ttu-id="5834d-179">ただし、プロバイダーは接続を確立できませんし、全体のサービスを無効にしない場合は、MAPI_E_FAILONEPROVIDER または MAPI_E_UNCONFIGURED のいずれかを返します。</span><span class="sxs-lookup"><span data-stu-id="5834d-179">However, if your provider cannot establish a connection and you want not to disable the entire service, return either MAPI_E_FAILONEPROVIDER or MAPI_E_UNCONFIGURED.</span></span> <span data-ttu-id="5834d-180">MAPI には、プロバイダーが所属するメッセージ サービスは無効にされます。</span><span class="sxs-lookup"><span data-stu-id="5834d-180">MAPI will not disable the message service to which the provider belongs.</span></span> 
  
<span data-ttu-id="5834d-181">MAPI_E_FAILONEPROVIDER エラーが発生する場合の戻り値は、メッセージ サービスで他のプロバイダーが接続を確立することを防止するほど深刻ではありません。</span><span class="sxs-lookup"><span data-stu-id="5834d-181">Return MAPI_E_FAILONEPROVIDER if an error occurs that is not serious enough to prevent the other providers in the message service from establishing connections.</span></span> <span data-ttu-id="5834d-182">プロファイルから必要な構成情報が見つからない場合、戻り値の MAPI_E_UNCONFIGURED は、ユーザー入力を求めるダイアログ ボックスを表示できません。</span><span class="sxs-lookup"><span data-stu-id="5834d-182">Return MAPI_E_UNCONFIGURED if the necessary configuration information is missing from the profile and you cannot display a dialog box to prompt the user.</span></span> <span data-ttu-id="5834d-183">MAPI は、MSG_SERVICE_CONFIGURE セットを使用して、プロバイダーのメッセージ サービス エントリ ポイント関数を設定する機会自体、か、プログラムを使用してサービスを提供する_ulContext_パラメーターとして呼び出しまたはプロパティ シートを使用して応答します。</span><span class="sxs-lookup"><span data-stu-id="5834d-183">MAPI will respond by calling your provider's message service entry point function with MSG_SERVICE_CONFIGURE set as the  _ulContext_ parameter to give the service a chance to configure itself, either programmatically or using a property sheet.</span></span> <span data-ttu-id="5834d-184">メッセージ サービスのエントリ ポイント関数が完了、MAPI ログオンを再試行します。</span><span class="sxs-lookup"><span data-stu-id="5834d-184">When the message service entry point function has finished, MAPI retries the logon.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5834d-185">関連項目</span><span class="sxs-lookup"><span data-stu-id="5834d-185">See also</span></span>



[<span data-ttu-id="5834d-186">IABLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="5834d-186">IABLogon::Logoff</span></span>](iablogon-logoff.md)
  
[<span data-ttu-id="5834d-187">IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="5834d-187">IABLogon::OpenEntry</span></span>](iablogon-openentry.md)
  
[<span data-ttu-id="5834d-188">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="5834d-188">IMAPISupport::OpenProfileSection</span></span>](imapisupport-openprofilesection.md)
  
[<span data-ttu-id="5834d-189">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="5834d-189">IMAPISupport::SetProviderUID</span></span>](imapisupport-setprovideruid.md)
  
[<span data-ttu-id="5834d-190">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="5834d-190">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="5834d-191">IABProvider: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5834d-191">IABProvider : IUnknown</span></span>](iabprovideriunknown.md)

