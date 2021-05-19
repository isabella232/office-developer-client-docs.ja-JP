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
# <a name="iabproviderlogon"></a><span data-ttu-id="0c317-103">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="0c317-103">IABProvider::Logon</span></span>

  
  
<span data-ttu-id="0c317-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c317-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c317-105">アクティブ なセッションへの接続を確立します。</span><span class="sxs-lookup"><span data-stu-id="0c317-105">Establishes a connection to an active session.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="0c317-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0c317-106">Parameters</span></span>

 <span data-ttu-id="0c317-107">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="0c317-107">_lpMAPISup_</span></span>
  
> <span data-ttu-id="0c317-108">[in]アドレス帳プロバイダーのサポート オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="0c317-108">[in] A pointer to the address book provider's support object.</span></span>
    
 <span data-ttu-id="0c317-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="0c317-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="0c317-110">[in]ログオン メソッドが表示されるログオン ダイアログ ボックスの親ウィンドウへのハンドル (許可されている場合)。</span><span class="sxs-lookup"><span data-stu-id="0c317-110">[in] A handle to the parent window for the logon dialog box that the **Logon** method displays, if permitted.</span></span> <span data-ttu-id="0c317-111">_ulUIParam_ パラメーターには [、MAPILogonEx](mapilogonex.md)関数の前の呼び出しで MAPI に渡された同じ名前のパラメーターの値が含まれる。</span><span class="sxs-lookup"><span data-stu-id="0c317-111">The  _ulUIParam_ parameter contains the value of the parameter of the same name passed to MAPI in the previous call to the [MAPILogonEx](mapilogonex.md) function.</span></span> 
    
 <span data-ttu-id="0c317-112">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="0c317-112">_lpszProfileName_</span></span>
  
> <span data-ttu-id="0c317-113">[in]セッション プロファイルの名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0c317-113">[in] A pointer to the name of the session profile.</span></span>
    
 <span data-ttu-id="0c317-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0c317-114">_ulFlags_</span></span>
  
> <span data-ttu-id="0c317-115">[in]ログオンの実行方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="0c317-115">[in] A bitmask of flags that controls how the logon is performed.</span></span> <span data-ttu-id="0c317-116">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="0c317-116">The following flags can be set:</span></span>
    
<span data-ttu-id="0c317-117">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="0c317-117">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="0c317-118">ログオン時に、プロバイダーがダイアログ ボックスを表示しなける必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c317-118">The provider should not display a dialog box during logon.</span></span> <span data-ttu-id="0c317-119">このフラグが設定されていない場合、プロバイダーはダイアログ ボックスを表示して、不足している構成情報をユーザーに求めるメッセージを表示できます。</span><span class="sxs-lookup"><span data-stu-id="0c317-119">If this flag is not set, the provider can display a dialog box to prompt the user for missing configuration information.</span></span>
    
<span data-ttu-id="0c317-120">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="0c317-120">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="0c317-121">ログオン **プロセスが** 完了する前に、ログオンが正常に返される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0c317-121">Enables **Logon** to return successfully, possibly before the logon process is finished.</span></span> 
    
<span data-ttu-id="0c317-122">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0c317-122">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="0c317-123">すべての文字列は Unicode 形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c317-123">All strings should be in Unicode format.</span></span> <span data-ttu-id="0c317-124">このフラグMAPI_UNICODE設定しない場合、文字列は ANSI 形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c317-124">If the MAPI_UNICODE flag is not set, the strings should be in ANSI format.</span></span>
    
 <span data-ttu-id="0c317-125">_lpulcbSecurity_</span><span class="sxs-lookup"><span data-stu-id="0c317-125">_lpulcbSecurity_</span></span>
  
> <span data-ttu-id="0c317-126">[in, out]  _lppbSecurity_ パラメーターが指すセキュリティ資格情報構造のサイズ (バイト単位) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0c317-126">[in, out] A pointer to the size, in bytes, of the security credentials structure pointed to by the  _lppbSecurity_ parameter.</span></span> <span data-ttu-id="0c317-127">入力では、値は 0 以外である必要があります。出力の場合、値は 0 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c317-127">On input, the value must be nonzero; on output, the value must be zero.</span></span> <span data-ttu-id="0c317-128">どちらの場合も、ポインターは有効である必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c317-128">In both cases, the pointers must be valid.</span></span> 
    
 <span data-ttu-id="0c317-129">_lppbSecurity_</span><span class="sxs-lookup"><span data-stu-id="0c317-129">_lppbSecurity_</span></span>
  
> <span data-ttu-id="0c317-130">[in, out]セキュリティ資格情報へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0c317-130">[in, out] A pointer to a pointer to security credentials.</span></span> <span data-ttu-id="0c317-131">入力では、値は 0 以外である必要があります。出力の場合、値は 0 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c317-131">On input, the value must be nonzero; on output, the value must be zero.</span></span> <span data-ttu-id="0c317-132">どちらの場合も、ポインターは有効である必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c317-132">In both cases the pointer must be valid.</span></span>
    
 <span data-ttu-id="0c317-133">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="0c317-133">_lppMAPIError_</span></span>
  
> <span data-ttu-id="0c317-134">[out]MAPIERROR 構造体へのポインターを [指す](mapierror.md) ポインター。</span><span class="sxs-lookup"><span data-stu-id="0c317-134">[out] A pointer to a pointer to a [MAPIERROR](mapierror.md) structure.</span></span> <span data-ttu-id="0c317-135">_戻す MAPIERROR 構造体がない場合、lppMAPIError_ パラメーターを **NULL に** 設定できます。</span><span class="sxs-lookup"><span data-stu-id="0c317-135">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
 <span data-ttu-id="0c317-136">_lppABLogon_</span><span class="sxs-lookup"><span data-stu-id="0c317-136">_lppABLogon_</span></span>
  
> <span data-ttu-id="0c317-137">[out]プロバイダーのログオン オブジェクトへのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="0c317-137">[out] A pointer to a pointer to the provider's logon object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0c317-138">戻り値</span><span class="sxs-lookup"><span data-stu-id="0c317-138">Return value</span></span>

<span data-ttu-id="0c317-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="0c317-139">S_OK</span></span> 
  
> <span data-ttu-id="0c317-140">アクティブ なセッションへの接続が正常に確立されました。</span><span class="sxs-lookup"><span data-stu-id="0c317-140">A connection to an active session was successfully established.</span></span>
    
<span data-ttu-id="0c317-141">MAPI_E_FAILONEPROVIDER</span><span class="sxs-lookup"><span data-stu-id="0c317-141">MAPI_E_FAILONEPROVIDER</span></span> 
  
> <span data-ttu-id="0c317-142">プロバイダーはログオンできませんが、MAPI は、プロバイダーが属するメッセージ サービス内の他のプロバイダーに引き続きログオンできます。</span><span class="sxs-lookup"><span data-stu-id="0c317-142">The provider cannot log on, but MAPI can continue to log on the other providers in the message service to which the provider belongs.</span></span> 
    
<span data-ttu-id="0c317-143">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="0c317-143">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="0c317-144">プロバイダーにログオンを完了する情報が不足しています。</span><span class="sxs-lookup"><span data-stu-id="0c317-144">The provider has insufficient information to complete the logon.</span></span> <span data-ttu-id="0c317-145">MAPI は、プロバイダーのメッセージ サービス エントリ関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0c317-145">MAPI calls the provider's message service entry function.</span></span>
    
<span data-ttu-id="0c317-146">MAPI_E_UNKNOWN_CPID</span><span class="sxs-lookup"><span data-stu-id="0c317-146">MAPI_E_UNKNOWN_CPID</span></span> 
  
> <span data-ttu-id="0c317-147">サーバーは、クライアントのコード ページをサポートするように構成されていません。</span><span class="sxs-lookup"><span data-stu-id="0c317-147">The server is not configured to support the client's code page.</span></span>
    
<span data-ttu-id="0c317-148">MAPI_E_UNKNOWN_LCID</span><span class="sxs-lookup"><span data-stu-id="0c317-148">MAPI_E_UNKNOWN_LCID</span></span> 
  
> <span data-ttu-id="0c317-149">サーバーは、クライアントのロケール情報をサポートするように構成されていません。</span><span class="sxs-lookup"><span data-stu-id="0c317-149">The server is not configured to support the client's locale information.</span></span>
    
<span data-ttu-id="0c317-150">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="0c317-150">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="0c317-151">通常、ユーザーはログオン ダイアログ ボックスの [ **キャンセル** ] ボタンをクリックして操作をキャンセルしました。</span><span class="sxs-lookup"><span data-stu-id="0c317-151">The user canceled the operation, typically by clicking the **Cancel** button in the logon dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0c317-152">注釈</span><span class="sxs-lookup"><span data-stu-id="0c317-152">Remarks</span></span>

<span data-ttu-id="0c317-153">クライアントが [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) メソッドを呼び出す場合、セッション プロファイル内の各アドレス帳プロバイダーとの接続が確立されます。</span><span class="sxs-lookup"><span data-stu-id="0c317-153">Connections are established with each address book provider in the session profile when a client calls the [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) method.</span></span> <span data-ttu-id="0c317-154">**OpenAddressBook は、** 各プロバイダーの Logon メソッドを **呼び出** します。</span><span class="sxs-lookup"><span data-stu-id="0c317-154">**OpenAddressBook** then calls each provider's **Logon** method.</span></span> 
  
<span data-ttu-id="0c317-155">_lpszProfileName_ パラメーターが示すプロファイル名は _、ulFlags_ パラメーターの MAPI_UNICODE フラグの有無によって示される、ユーザーのクライアントの文字セットに表示されます。</span><span class="sxs-lookup"><span data-stu-id="0c317-155">The profile name pointed to by the  _lpszProfileName_ parameter is displayed in the character set of the user's client as indicated by the presence or absence of the MAPI_UNICODE flag in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0c317-156">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="0c317-156">Notes to implementers</span></span>

<span data-ttu-id="0c317-157">Logon メソッドの実装 **では**[、IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)メソッドを呼び出して、一意の識別子 [(MAPIUID](mapiuid.md)構造) を登録します。</span><span class="sxs-lookup"><span data-stu-id="0c317-157">In your implementation of the **Logon** method, call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register a unique identifier, or [MAPIUID](mapiuid.md) structure.</span></span> <span data-ttu-id="0c317-158">各オブジェクトには、この MAPIUID を含むエントリ **識別子が含まれます**。</span><span class="sxs-lookup"><span data-stu-id="0c317-158">Each of your objects will have an entry identifier that includes this **MAPIUID**.</span></span> <span data-ttu-id="0c317-159">MAPI は **MAPIUID を使用** して、オブジェクトをプロバイダーと一致します。</span><span class="sxs-lookup"><span data-stu-id="0c317-159">MAPI uses the **MAPIUID** to match an object with its provider.</span></span> <span data-ttu-id="0c317-160">たとえば、クライアントが [IMAPISession::OpenEntry](imapisession-openentry.md) メソッドを呼び出してメッセージング ユーザーを開く場合 **、OpenEntry** は、渡されたエントリ識別子の **MAPIUID** 部分を調べ、アドレス帳プロバイダーによって登録された **MAPIUID** と一致します。</span><span class="sxs-lookup"><span data-stu-id="0c317-160">For example, when a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open a messaging user, **OpenEntry** examines the **MAPIUID** portion of the entry identifier that was passed in and matches it with a **MAPIUID** registered by an address book provider.</span></span> 
  
<span data-ttu-id="0c317-161">クライアントがプロバイダーに複数ログオンする場合は、ログオンごとに異なる **MAPIUID** を登録できます。</span><span class="sxs-lookup"><span data-stu-id="0c317-161">If a client logs on to your provider more than once, you may want to register a different **MAPIUID** for each logon.</span></span> <span data-ttu-id="0c317-162">一意の **MAPIUID 構造体を登録** すると、MAPI は適切なプロバイダー インスタンスに要求を正しくルーティングできます。</span><span class="sxs-lookup"><span data-stu-id="0c317-162">Registering unique **MAPIUID** structures enables MAPI to correctly route requests to the appropriate provider instance.</span></span> <span data-ttu-id="0c317-163">ただし、すべてのログオン オブジェクトで 1 つの **MAPIUID を共有できます**。</span><span class="sxs-lookup"><span data-stu-id="0c317-163">However, you may want to have every logon object share one **MAPIUID**.</span></span> <span data-ttu-id="0c317-164">この場合、MAPI に依存するのではなく、自分でルーティングを処理できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c317-164">In this case, you must be able to handle the routing yourself instead of relying on MAPI.</span></span> <span data-ttu-id="0c317-165">**MAPIUID** を作成する方法の詳細については、「Registering Service [Provider Unique IDENTIFIERs」を参照してください](registering-service-provider-unique-identifiers.md)。</span><span class="sxs-lookup"><span data-stu-id="0c317-165">For more information about how to create a **MAPIUID**, see [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).</span></span>
  
<span data-ttu-id="0c317-166">MAPI が _lpMAPISup_ パラメーターの **Logon** メソッドに渡すサポート オブジェクトは [、IMAPISupport : IUnknown](imapisupportiunknown.md)インターフェイスに含まれる多くのメソッドにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="0c317-166">The support object that MAPI passes to your **Logon** method in the  _lpMAPISup_ parameter provides access to many of the methods included in the [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> <span data-ttu-id="0c317-167">MAPI は、プロバイダーの種類に合わせてカスタマイズされたサポート オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="0c317-167">MAPI creates a support object that is customized to your type of provider.</span></span> <span data-ttu-id="0c317-168">たとえば、接続を確立するときに基になるメッセージング システムまたはディレクトリ サービスにログオンする必要がある場合は [、IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) メソッドを呼び出して、この特定のログオン セッションのセキュリティ資格情報を取得できます。</span><span class="sxs-lookup"><span data-stu-id="0c317-168">For example, if you need to log on to an underlying messaging system or directory service when you establish your connection, you can call the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to retrieve security credentials for this particular logon session.</span></span> 
  
<span data-ttu-id="0c317-169">Logon **が** 成功した場合は、サポート オブジェクトの [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) メソッドを呼び出して参照カウントを増やしてください。</span><span class="sxs-lookup"><span data-stu-id="0c317-169">If **Logon** is successful, be sure that you call the support object's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method to increment its reference count.</span></span> <span data-ttu-id="0c317-170">これにより、プロバイダーは、セッションの残りの部分のサポート オブジェクト ポインターを保持できます。</span><span class="sxs-lookup"><span data-stu-id="0c317-170">This enables your provider to hold onto the support object pointer for the rest of the session.</span></span> <span data-ttu-id="0c317-171">この AddRef メソッドを呼 **び出していない** 場合、MAPI はプロバイダーをアンロードします。</span><span class="sxs-lookup"><span data-stu-id="0c317-171">If you do not call this **AddRef** method, MAPI will unload your provider.</span></span> 
  
<span data-ttu-id="0c317-172">_lpszProfileName_ パラメーターで渡されたプロファイル名は、エラー ダイアログ ボックス、ログオン画面、または他のユーザー インターフェイスに含めできます。</span><span class="sxs-lookup"><span data-stu-id="0c317-172">You can include the profile name passed in the  _lpszProfileName_ parameter in error dialog boxes, logon screens, or other user interfaces.</span></span> <span data-ttu-id="0c317-173">プロファイル名を使用するには、割り当て済みストレージにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0c317-173">To use the profile name, copy it to storage that you have allocated.</span></span> 
  
<span data-ttu-id="0c317-174">ログオン オブジェクトを作成し  _、lppABLogon_ パラメーターにポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="0c317-174">Create a logon object and return a pointer to it in the  _lppABLogon_ parameter.</span></span> <span data-ttu-id="0c317-175">MAPI では、このログオン オブジェクトを使用して [、IABLogon 実装内のメソッドを呼び出](iablogoniunknown.md) します。</span><span class="sxs-lookup"><span data-stu-id="0c317-175">MAPI uses this logon object to make calls to the methods in your [IABLogon](iablogoniunknown.md) implementation.</span></span> 
  
<span data-ttu-id="0c317-176">ログオン時にパスワードが必要な場合は、ログオン フラグが設定されていないAB_NO_DIALOGダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="0c317-176">If you require a password during logon, display a logon dialog box only if the AB_NO_DIALOG flag is not set.</span></span> <span data-ttu-id="0c317-177">ユーザーがログオン プロセスを取り消す場合は、通常、ダイアログ ボックスの [キャンセル] ボタンをクリックして、[ログオン] からMAPI_E_USER_CANCEL返 **します**。</span><span class="sxs-lookup"><span data-stu-id="0c317-177">If the user cancels the logon process, typically by clicking the **Cancel** button in the dialog box, return MAPI_E_USER_CANCEL from **Logon**.</span></span>
  
<span data-ttu-id="0c317-178">通常、アドレス帳プロバイダーがログオンできない場合、MAPI は、障害が発生したプロバイダーが属するメッセージ サービス (つまり、MAPI はセッションの残りの期間、サービスに属する他のプロバイダーの接続を確立しようとしません) を無効にします。</span><span class="sxs-lookup"><span data-stu-id="0c317-178">Typically, when an address book provider cannot log on, MAPI disables the message service to which the failing provider belongs—that is, MAPI will not try to establish connections for any of the other providers that belong to the service for the rest of the session's lifetime.</span></span> <span data-ttu-id="0c317-179">ただし、プロバイダーが接続を確立できない場合に、サービス全体を無効にしない場合は、サービス全体をMAPI_E_FAILONEPROVIDERまたはMAPI_E_UNCONFIGURED。</span><span class="sxs-lookup"><span data-stu-id="0c317-179">However, if your provider cannot establish a connection and you want not to disable the entire service, return either MAPI_E_FAILONEPROVIDER or MAPI_E_UNCONFIGURED.</span></span> <span data-ttu-id="0c317-180">MAPI では、プロバイダーが属するメッセージ サービスは無効にされません。</span><span class="sxs-lookup"><span data-stu-id="0c317-180">MAPI will not disable the message service to which the provider belongs.</span></span> 
  
<span data-ttu-id="0c317-181">メッセージ MAPI_E_FAILONEPROVIDERの他のプロバイダーが接続を確立できないほど重大ではないエラーが発生した場合は、このエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="0c317-181">Return MAPI_E_FAILONEPROVIDER if an error occurs that is not serious enough to prevent the other providers in the message service from establishing connections.</span></span> <span data-ttu-id="0c317-182">必要MAPI_E_UNCONFIGUREDプロファイルに必要な構成情報が見つからない場合に、ユーザーにメッセージを表示するダイアログ ボックスを表示できない場合は、このダイアログ ボックスを返します。</span><span class="sxs-lookup"><span data-stu-id="0c317-182">Return MAPI_E_UNCONFIGURED if the necessary configuration information is missing from the profile and you cannot display a dialog box to prompt the user.</span></span> <span data-ttu-id="0c317-183">MAPI は、MSG_SERVICE_CONFIGURE を  _ulContext_ パラメーターとして設定したプロバイダーのメッセージ サービス エントリ ポイント関数を呼び出して、プログラムによって、またはプロパティ シートを使用してサービスを構成する機会を与えます。</span><span class="sxs-lookup"><span data-stu-id="0c317-183">MAPI will respond by calling your provider's message service entry point function with MSG_SERVICE_CONFIGURE set as the  _ulContext_ parameter to give the service a chance to configure itself, either programmatically or using a property sheet.</span></span> <span data-ttu-id="0c317-184">メッセージ サービスエントリ ポイント関数が終了すると、MAPI はログオンを再試行します。</span><span class="sxs-lookup"><span data-stu-id="0c317-184">When the message service entry point function has finished, MAPI retries the logon.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0c317-185">関連項目</span><span class="sxs-lookup"><span data-stu-id="0c317-185">See also</span></span>



[<span data-ttu-id="0c317-186">IABLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="0c317-186">IABLogon::Logoff</span></span>](iablogon-logoff.md)
  
[<span data-ttu-id="0c317-187">IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="0c317-187">IABLogon::OpenEntry</span></span>](iablogon-openentry.md)
  
[<span data-ttu-id="0c317-188">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="0c317-188">IMAPISupport::OpenProfileSection</span></span>](imapisupport-openprofilesection.md)
  
[<span data-ttu-id="0c317-189">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="0c317-189">IMAPISupport::SetProviderUID</span></span>](imapisupport-setprovideruid.md)
  
[<span data-ttu-id="0c317-190">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="0c317-190">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="0c317-191">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0c317-191">IABProvider : IUnknown</span></span>](iabprovideriunknown.md)

