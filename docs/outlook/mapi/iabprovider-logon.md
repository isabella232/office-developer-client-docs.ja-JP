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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 59c6d4a05c91511ad8c481fd4ddbe42396442190
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348784"
---
# <a name="iabproviderlogon"></a><span data-ttu-id="1be81-103">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="1be81-103">IABProvider::Logon</span></span>

  
  
<span data-ttu-id="1be81-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1be81-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1be81-105">アクティブなセッションへの接続を確立します。</span><span class="sxs-lookup"><span data-stu-id="1be81-105">Establishes a connection to an active session.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="1be81-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1be81-106">Parameters</span></span>

 <span data-ttu-id="1be81-107">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="1be81-107">_lpMAPISup_</span></span>
  
> <span data-ttu-id="1be81-108">順番アドレス帳プロバイダーのサポートオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="1be81-108">[in] A pointer to the address book provider's support object.</span></span>
    
 <span data-ttu-id="1be81-109">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="1be81-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="1be81-110">順番**ログオン**方法が表示されるログオンダイアログボックスの親ウィンドウへのハンドル (許可されている場合)。</span><span class="sxs-lookup"><span data-stu-id="1be81-110">[in] A handle to the parent window for the logon dialog box that the **Logon** method displays, if permitted.</span></span> <span data-ttu-id="1be81-111">_uluiparam_パラメーターには、前の[MAPILogonEx](mapilogonex.md)関数の呼び出しで MAPI に渡された名前のパラメーターの値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1be81-111">The  _ulUIParam_ parameter contains the value of the parameter of the same name passed to MAPI in the previous call to the [MAPILogonEx](mapilogonex.md) function.</span></span> 
    
 <span data-ttu-id="1be81-112">_lpszprofilename_</span><span class="sxs-lookup"><span data-stu-id="1be81-112">_lpszProfileName_</span></span>
  
> <span data-ttu-id="1be81-113">順番セッションプロファイルの名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1be81-113">[in] A pointer to the name of the session profile.</span></span>
    
 <span data-ttu-id="1be81-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1be81-114">_ulFlags_</span></span>
  
> <span data-ttu-id="1be81-115">順番ログオンの実行方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="1be81-115">[in] A bitmask of flags that controls how the logon is performed.</span></span> <span data-ttu-id="1be81-116">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="1be81-116">The following flags can be set:</span></span>
    
<span data-ttu-id="1be81-117">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="1be81-117">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="1be81-118">プロバイダーは、ログオン時にダイアログボックスを表示しないようにします。</span><span class="sxs-lookup"><span data-stu-id="1be81-118">The provider should not display a dialog box during logon.</span></span> <span data-ttu-id="1be81-119">このフラグが設定されていない場合、プロバイダーはユーザーに構成情報が不足していることを確認するダイアログボックスを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="1be81-119">If this flag is not set, the provider can display a dialog box to prompt the user for missing configuration information.</span></span>
    
<span data-ttu-id="1be81-120">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="1be81-120">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="1be81-121">ログオン処理が完了する前に、**ログオン**が正常に返されるようにします。</span><span class="sxs-lookup"><span data-stu-id="1be81-121">Enables **Logon** to return successfully, possibly before the logon process is finished.</span></span> 
    
<span data-ttu-id="1be81-122">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1be81-122">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1be81-123">すべての文字列は Unicode 形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="1be81-123">All strings should be in Unicode format.</span></span> <span data-ttu-id="1be81-124">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="1be81-124">If the MAPI_UNICODE flag is not set, the strings should be in ANSI format.</span></span>
    
 <span data-ttu-id="1be81-125">_lアウト cbsecurity_</span><span class="sxs-lookup"><span data-stu-id="1be81-125">_lpulcbSecurity_</span></span>
  
> <span data-ttu-id="1be81-126">[入力]_lppbsecurity_パラメーターによって示されるセキュリティ資格情報構造のサイズ (バイト単位) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1be81-126">[in, out] A pointer to the size, in bytes, of the security credentials structure pointed to by the  _lppbSecurity_ parameter.</span></span> <span data-ttu-id="1be81-127">入力の場合、値は0以外の値である必要があります。出力では、この値は0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="1be81-127">On input, the value must be nonzero; on output, the value must be zero.</span></span> <span data-ttu-id="1be81-128">どちらの場合も、ポインターが有効である必要があります。</span><span class="sxs-lookup"><span data-stu-id="1be81-128">In both cases, the pointers must be valid.</span></span> 
    
 <span data-ttu-id="1be81-129">_lppbsecurity_</span><span class="sxs-lookup"><span data-stu-id="1be81-129">_lppbSecurity_</span></span>
  
> <span data-ttu-id="1be81-130">[入力]セキュリティ資格情報へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="1be81-130">[in, out] A pointer to a pointer to security credentials.</span></span> <span data-ttu-id="1be81-131">入力の場合、値は0以外の値である必要があります。出力では、この値は0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="1be81-131">On input, the value must be nonzero; on output, the value must be zero.</span></span> <span data-ttu-id="1be81-132">どちらの場合も、ポインターが有効である必要があります。</span><span class="sxs-lookup"><span data-stu-id="1be81-132">In both cases the pointer must be valid.</span></span>
    
 <span data-ttu-id="1be81-133">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="1be81-133">_lppMAPIError_</span></span>
  
> <span data-ttu-id="1be81-134">読み上げ[MAPIERROR](mapierror.md)構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="1be81-134">[out] A pointer to a pointer to a [MAPIERROR](mapierror.md) structure.</span></span> <span data-ttu-id="1be81-135">返す**MAPIERROR**構造体がない場合は、 _lppMAPIError_パラメーターを NULL に設定できます。</span><span class="sxs-lookup"><span data-stu-id="1be81-135">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
 <span data-ttu-id="1be81-136">_lppablogon_</span><span class="sxs-lookup"><span data-stu-id="1be81-136">_lppABLogon_</span></span>
  
> <span data-ttu-id="1be81-137">読み上げプロバイダーのログオンオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="1be81-137">[out] A pointer to a pointer to the provider's logon object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1be81-138">戻り値</span><span class="sxs-lookup"><span data-stu-id="1be81-138">Return value</span></span>

<span data-ttu-id="1be81-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="1be81-139">S_OK</span></span> 
  
> <span data-ttu-id="1be81-140">アクティブなセッションへの接続が正常に確立されました。</span><span class="sxs-lookup"><span data-stu-id="1be81-140">A connection to an active session was successfully established.</span></span>
    
<span data-ttu-id="1be81-141">MAPI_E_FAILONEPROVIDER</span><span class="sxs-lookup"><span data-stu-id="1be81-141">MAPI_E_FAILONEPROVIDER</span></span> 
  
> <span data-ttu-id="1be81-142">プロバイダーはログオンできませんが、MAPI は、プロバイダーが属しているメッセージサービスの他のプロバイダーに引き続きログオンできます。</span><span class="sxs-lookup"><span data-stu-id="1be81-142">The provider cannot log on, but MAPI can continue to log on the other providers in the message service to which the provider belongs.</span></span> 
    
<span data-ttu-id="1be81-143">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="1be81-143">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="1be81-144">プロバイダーに、ログオンを完了するための十分な情報がありません。</span><span class="sxs-lookup"><span data-stu-id="1be81-144">The provider has insufficient information to complete the logon.</span></span> <span data-ttu-id="1be81-145">MAPI は、プロバイダーのメッセージサービスのエントリ関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1be81-145">MAPI calls the provider's message service entry function.</span></span>
    
<span data-ttu-id="1be81-146">MAPI_E_UNKNOWN_CPID</span><span class="sxs-lookup"><span data-stu-id="1be81-146">MAPI_E_UNKNOWN_CPID</span></span> 
  
> <span data-ttu-id="1be81-147">サーバーは、クライアントのコードページをサポートするように構成されていません。</span><span class="sxs-lookup"><span data-stu-id="1be81-147">The server is not configured to support the client's code page.</span></span>
    
<span data-ttu-id="1be81-148">MAPI_E_UNKNOWN_LCID</span><span class="sxs-lookup"><span data-stu-id="1be81-148">MAPI_E_UNKNOWN_LCID</span></span> 
  
> <span data-ttu-id="1be81-149">サーバーは、クライアントのロケール情報をサポートするように構成されていません。</span><span class="sxs-lookup"><span data-stu-id="1be81-149">The server is not configured to support the client's locale information.</span></span>
    
<span data-ttu-id="1be81-150">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="1be81-150">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="1be81-151">ユーザーが操作をキャンセルしました。通常は、ログオンダイアログボックスの **[キャンセル**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="1be81-151">The user canceled the operation, typically by clicking the **Cancel** button in the logon dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1be81-152">解説</span><span class="sxs-lookup"><span data-stu-id="1be81-152">Remarks</span></span>

<span data-ttu-id="1be81-153">クライアントが[imapisession:: OpenAddressBook](imapisession-openaddressbook.md)メソッドを呼び出すと、セッションプロファイル内の各アドレス帳プロバイダーとの接続が確立されます。</span><span class="sxs-lookup"><span data-stu-id="1be81-153">Connections are established with each address book provider in the session profile when a client calls the [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) method.</span></span> <span data-ttu-id="1be81-154">**OpenAddressBook**は、各プロバイダーの**ログオン**方法を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1be81-154">**OpenAddressBook** then calls each provider's **Logon** method.</span></span> 
  
<span data-ttu-id="1be81-155">_lpszprofilename_パラメーターで指定されているプロファイル名が、 _ulflags_パラメーターの MAPI_UNICODE フラグのプレゼンスまたは欠落によって示されるユーザーのクライアントの文字セットに表示されます。</span><span class="sxs-lookup"><span data-stu-id="1be81-155">The profile name pointed to by the  _lpszProfileName_ parameter is displayed in the character set of the user's client as indicated by the presence or absence of the MAPI_UNICODE flag in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1be81-156">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="1be81-156">Notes to implementers</span></span>

<span data-ttu-id="1be81-157">**ログオン**方法の実装で、 [imapisupport:: setprovideruid](imapisupport-setprovideruid.md)メソッドを呼び出して、一意の識別子または[MAPIUID](mapiuid.md)構造体を登録します。</span><span class="sxs-lookup"><span data-stu-id="1be81-157">In your implementation of the **Logon** method, call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register a unique identifier, or [MAPIUID](mapiuid.md) structure.</span></span> <span data-ttu-id="1be81-158">各オブジェクトには、この**MAPIUID**を含むエントリ識別子があります。</span><span class="sxs-lookup"><span data-stu-id="1be81-158">Each of your objects will have an entry identifier that includes this **MAPIUID**.</span></span> <span data-ttu-id="1be81-159">MAPI では、 **MAPIUID**を使用してオブジェクトをプロバイダーに一致させます。</span><span class="sxs-lookup"><span data-stu-id="1be81-159">MAPI uses the **MAPIUID** to match an object with its provider.</span></span> <span data-ttu-id="1be81-160">たとえば、クライアントが[imapisession:: openentry](imapisession-openentry.md)メソッドを呼び出してメッセージングユーザーを開くと、 **openentry**は、渡されたエントリ識別子の**MAPIUID**部分を調べ、それと一致する**MAPIUID**を使用して登録したアドレス帳プロバイダー。</span><span class="sxs-lookup"><span data-stu-id="1be81-160">For example, when a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open a messaging user, **OpenEntry** examines the **MAPIUID** portion of the entry identifier that was passed in and matches it with a **MAPIUID** registered by an address book provider.</span></span> 
  
<span data-ttu-id="1be81-161">クライアントがプロバイダーに複数回ログオンしている場合は、ログオンごとに異なる**MAPIUID**を登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1be81-161">If a client logs on to your provider more than once, you may want to register a different **MAPIUID** for each logon.</span></span> <span data-ttu-id="1be81-162">一意の**MAPIUID**構造を登録すると、MAPI が適切なプロバイダーインスタンスに要求を正しくルーティングできるようになります。</span><span class="sxs-lookup"><span data-stu-id="1be81-162">Registering unique **MAPIUID** structures enables MAPI to correctly route requests to the appropriate provider instance.</span></span> <span data-ttu-id="1be81-163">ただし、すべてのログオンオブジェクトで1つの**MAPIUID**を共有する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="1be81-163">However, you may want to have every logon object share one **MAPIUID**.</span></span> <span data-ttu-id="1be81-164">この場合は、MAPI に依存するのではなく、自分でルーティングを処理できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="1be81-164">In this case, you must be able to handle the routing yourself instead of relying on MAPI.</span></span> <span data-ttu-id="1be81-165">**MAPIUID**の作成方法の詳細については、「[サービスプロバイダーの一意識別子の登録](registering-service-provider-unique-identifiers.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1be81-165">For more information about how to create a **MAPIUID**, see [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).</span></span>
  
<span data-ttu-id="1be81-166">MAPI が_lpMAPISup_パラメーターで**ログオン**方法に渡すサポートオブジェクトは、 [imapisupport: IUnknown](imapisupportiunknown.md)インターフェイスに含まれる多くのメソッドへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="1be81-166">The support object that MAPI passes to your **Logon** method in the  _lpMAPISup_ parameter provides access to many of the methods included in the [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> <span data-ttu-id="1be81-167">MAPI は、プロバイダーの種類に合わせてカスタマイズされたサポートオブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="1be81-167">MAPI creates a support object that is customized to your type of provider.</span></span> <span data-ttu-id="1be81-168">たとえば、接続を確立するときに、基になるメッセージングシステムまたはディレクトリサービスにログオンする必要がある場合は、 [imapisupport:: openapiaddressmethod](imapisupport-openprofilesection.md)を呼び出して、この特定のログオンセッションのセキュリティ資格情報を取得することができます。</span><span class="sxs-lookup"><span data-stu-id="1be81-168">For example, if you need to log on to an underlying messaging system or directory service when you establish your connection, you can call the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to retrieve security credentials for this particular logon session.</span></span> 
  
<span data-ttu-id="1be81-169">正常に**ログオン**できた場合は、サポートオブジェクトの[IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx)メソッドを呼び出して、参照カウントをインクリメントするようにしてください。</span><span class="sxs-lookup"><span data-stu-id="1be81-169">If **Logon** is successful, be sure that you call the support object's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method to increment its reference count.</span></span> <span data-ttu-id="1be81-170">これにより、プロバイダーは、セッションの残りの部分に対して support オブジェクトポインターを保持できます。</span><span class="sxs-lookup"><span data-stu-id="1be81-170">This enables your provider to hold onto the support object pointer for the rest of the session.</span></span> <span data-ttu-id="1be81-171">この**AddRef**メソッドを呼び出さない場合、MAPI はプロバイダーをアンロードします。</span><span class="sxs-lookup"><span data-stu-id="1be81-171">If you do not call this **AddRef** method, MAPI will unload your provider.</span></span> 
  
<span data-ttu-id="1be81-172">エラーダイアログボックス、ログオン画面、またはその他のユーザーインターフェイスで、 _lpszprofilename_パラメーターに渡されたプロファイル名を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="1be81-172">You can include the profile name passed in the  _lpszProfileName_ parameter in error dialog boxes, logon screens, or other user interfaces.</span></span> <span data-ttu-id="1be81-173">プロファイル名を使用するには、割り当てた記憶域にプロファイル名をコピーします。</span><span class="sxs-lookup"><span data-stu-id="1be81-173">To use the profile name, copy it to storage that you have allocated.</span></span> 
  
<span data-ttu-id="1be81-174">ログオンオブジェクトを作成し、 _lppablogon_パラメーターでそのオブジェクトへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="1be81-174">Create a logon object and return a pointer to it in the  _lppABLogon_ parameter.</span></span> <span data-ttu-id="1be81-175">MAPI は、このログオンオブジェクトを使用して、 [IABLogon](iablogoniunknown.md)の実装内のメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1be81-175">MAPI uses this logon object to make calls to the methods in your [IABLogon](iablogoniunknown.md) implementation.</span></span> 
  
<span data-ttu-id="1be81-176">ログオン時にパスワードが必要な場合は、AB_NO_DIALOG フラグが設定されていない場合にのみ、ログオンダイアログボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="1be81-176">If you require a password during logon, display a logon dialog box only if the AB_NO_DIALOG flag is not set.</span></span> <span data-ttu-id="1be81-177">ユーザーがログオンプロセスをキャンセルした場合 (通常は、ダイアログボックスの **[キャンセル**] ボタンをクリックすることによって、**ログオン**から MAPI_E_USER_CANCEL を返します。</span><span class="sxs-lookup"><span data-stu-id="1be81-177">If the user cancels the logon process, typically by clicking the **Cancel** button in the dialog box, return MAPI_E_USER_CANCEL from **Logon**.</span></span>
  
<span data-ttu-id="1be81-178">通常、アドレス帳プロバイダーがログオンできない場合、mapi はエラーが発生しているプロバイダーが属しているメッセージサービスを無効にします。つまり、mapi は、セッションの残りの部分では、そのサービスに属している他のすべてのプロバイダーの接続を確立しようとしません。時間.</span><span class="sxs-lookup"><span data-stu-id="1be81-178">Typically, when an address book provider cannot log on, MAPI disables the message service to which the failing provider belongs—that is, MAPI will not try to establish connections for any of the other providers that belong to the service for the rest of the session's lifetime.</span></span> <span data-ttu-id="1be81-179">ただし、プロバイダーが接続を確立できず、サービス全体を無効にしない場合は、MAPI_E_FAILONEPROVIDER または MAPI_E_UNCONFIGURED のいずれかを返します。</span><span class="sxs-lookup"><span data-stu-id="1be81-179">However, if your provider cannot establish a connection and you want not to disable the entire service, return either MAPI_E_FAILONEPROVIDER or MAPI_E_UNCONFIGURED.</span></span> <span data-ttu-id="1be81-180">MAPI は、プロバイダーが属しているメッセージサービスを無効にしません。</span><span class="sxs-lookup"><span data-stu-id="1be81-180">MAPI will not disable the message service to which the provider belongs.</span></span> 
  
<span data-ttu-id="1be81-181">メッセージサービス内の他のプロバイダーが接続を確立できないほど深刻でないエラーが発生した場合は、MAPI_E_FAILONEPROVIDER を返します。</span><span class="sxs-lookup"><span data-stu-id="1be81-181">Return MAPI_E_FAILONEPROVIDER if an error occurs that is not serious enough to prevent the other providers in the message service from establishing connections.</span></span> <span data-ttu-id="1be81-182">必要な構成情報がプロファイルに欠落していて、ユーザーに入力を求めるダイアログボックスを表示できない場合は、MAPI_E_UNCONFIGURED を返します。</span><span class="sxs-lookup"><span data-stu-id="1be81-182">Return MAPI_E_UNCONFIGURED if the necessary configuration information is missing from the profile and you cannot display a dialog box to prompt the user.</span></span> <span data-ttu-id="1be81-183">MAPI は、MSG_SERVICE_CONFIGURE を_ulcontext_パラメーターとして設定し、プロバイダーのメッセージサービスエントリポイント関数を呼び出して応答することによって、プログラムまたはプロパティシートを使用してサービスを自ら構成する機会を提供します。</span><span class="sxs-lookup"><span data-stu-id="1be81-183">MAPI will respond by calling your provider's message service entry point function with MSG_SERVICE_CONFIGURE set as the  _ulContext_ parameter to give the service a chance to configure itself, either programmatically or using a property sheet.</span></span> <span data-ttu-id="1be81-184">メッセージサービスエントリポイント関数が終了すると、MAPI はログオンを再試行します。</span><span class="sxs-lookup"><span data-stu-id="1be81-184">When the message service entry point function has finished, MAPI retries the logon.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1be81-185">関連項目</span><span class="sxs-lookup"><span data-stu-id="1be81-185">See also</span></span>



[<span data-ttu-id="1be81-186">IABLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="1be81-186">IABLogon::Logoff</span></span>](iablogon-logoff.md)
  
[<span data-ttu-id="1be81-187">IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="1be81-187">IABLogon::OpenEntry</span></span>](iablogon-openentry.md)
  
[<span data-ttu-id="1be81-188">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="1be81-188">IMAPISupport::OpenProfileSection</span></span>](imapisupport-openprofilesection.md)
  
[<span data-ttu-id="1be81-189">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="1be81-189">IMAPISupport::SetProviderUID</span></span>](imapisupport-setprovideruid.md)
  
[<span data-ttu-id="1be81-190">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="1be81-190">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="1be81-191">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1be81-191">IABProvider : IUnknown</span></span>](iabprovideriunknown.md)

