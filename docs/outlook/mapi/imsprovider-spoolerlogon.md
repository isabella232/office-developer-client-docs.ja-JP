---
title: IMSProviderSpoolerLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.SpoolerLogon
api_type:
- COM
ms.assetid: 79d5af23-efad-4013-a330-56babfb2bb0f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 56c025713b0cc2b41a4bf4463f48f8d7c3d2124b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586418"
---
# <a name="imsproviderspoolerlogon"></a><span data-ttu-id="c506f-103">IMSProvider::SpoolerLogon</span><span class="sxs-lookup"><span data-stu-id="c506f-103">IMSProvider::SpoolerLogon</span></span>

  
  
<span data-ttu-id="c506f-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c506f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c506f-105">メッセージ ストアに、MAPI スプーラーをログに記録します。</span><span class="sxs-lookup"><span data-stu-id="c506f-105">Logs the MAPI spooler on to a message store.</span></span>
  
```cpp
HRESULT SpoolerLogon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  LPCIID lpInterface,
  ULONG cbSpoolSecurity,
  LPBYTE lpbSpoolSecurity,
  LPMAPIERROR FAR * lppMAPIError,
  LPMSLOGON FAR * lppMSLogon,
  LPMDB FAR * lppMDB     
);
```

## <a name="parameters"></a><span data-ttu-id="c506f-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c506f-106">Parameters</span></span>

 <span data-ttu-id="c506f-107">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="c506f-107">_lpMAPISup_</span></span>
  
> <span data-ttu-id="c506f-108">[in]MAPI へのポインターは、メッセージ ・ ストアのオブジェクトをサポートします。</span><span class="sxs-lookup"><span data-stu-id="c506f-108">[in] A pointer to the MAPI support object for the message store.</span></span>
    
 <span data-ttu-id="c506f-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c506f-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="c506f-110">[in]ダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドルを表示します。</span><span class="sxs-lookup"><span data-stu-id="c506f-110">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> 
    
 <span data-ttu-id="c506f-111">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="c506f-111">_lpszProfileName_</span></span>
  
> <span data-ttu-id="c506f-112">[in]MAPI スプーラーのログオンに使用されているプロファイルの名前を含む文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c506f-112">[in] A pointer to a string that contains the name of the profile being used for the MAPI spooler logon.</span></span> <span data-ttu-id="c506f-113">この文字列のダイアログ ボックスに表示される、ログ ファイルに書き出されます。 または単に無視されます。</span><span class="sxs-lookup"><span data-stu-id="c506f-113">This string can be displayed in dialog boxes, written out to a log file, or simply ignored.</span></span> <span data-ttu-id="c506f-114">_UlFlags_パラメーターに MAPI_UNICODE フラグが設定されている場合は、Unicode 形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="c506f-114">It must be in Unicode format if the MAPI_UNICODE flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="c506f-115">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="c506f-115">_cbEntryID_</span></span>
  
> <span data-ttu-id="c506f-116">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト単位のサイズです。</span><span class="sxs-lookup"><span data-stu-id="c506f-116">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="c506f-117">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="c506f-117">_lpEntryID_</span></span>
  
> <span data-ttu-id="c506f-118">[in]メッセージ ・ ストアのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c506f-118">[in] A pointer to the entry identifier for the message store.</span></span> <span data-ttu-id="c506f-119">_LpEntryID_パラメーターに NULL を渡すことは、メッセージ ストアが選択されていないと、メッセージ ストアを選択するユーザーを有効にする] ダイアログ ボックスを表示できることを示します。</span><span class="sxs-lookup"><span data-stu-id="c506f-119">Passing NULL in the  _lpEntryID_ parameter indicates that a message store has not yet been selected and that dialog boxes that enable the user to select a message store can be presented.</span></span> 
    
 <span data-ttu-id="c506f-120">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c506f-120">_ulFlags_</span></span>
  
> <span data-ttu-id="c506f-121">[in]ログオンを実行する方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="c506f-121">[in] A bitmask of flags that controls how the logon is performed.</span></span> <span data-ttu-id="c506f-122">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="c506f-122">The following flags can be set:</span></span>
    
<span data-ttu-id="c506f-123">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="c506f-123">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="c506f-124">呼び出しは、基になるオブジェクトが呼び出し元の実装に使用可能でない場合でも、成功するために許可されています。</span><span class="sxs-lookup"><span data-stu-id="c506f-124">The call is allowed to succeed even if the underlying object is not available to the calling implementation.</span></span> <span data-ttu-id="c506f-125">オブジェクトが使用できない場合は、オブジェクトへの後続の呼び出しはエラーを発生させる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c506f-125">If the object is not available, a subsequent call to the object might raise an error.</span></span>
    
<span data-ttu-id="c506f-126">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c506f-126">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c506f-127">渡された文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="c506f-127">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="c506f-128">MAPI_UNICODE が設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="c506f-128">If MAPI_UNICODE is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="c506f-129">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="c506f-129">MDB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="c506f-130">ログオン ダイアログ ボックスが表示できないようにします。</span><span class="sxs-lookup"><span data-stu-id="c506f-130">Prevents the display of logon dialog boxes.</span></span> <span data-ttu-id="c506f-131">このフラグが設定されている場合、ログオンが成功しない場合、エラー値 MAPI_E_LOGON_FAILED が返されます。</span><span class="sxs-lookup"><span data-stu-id="c506f-131">If this flag is set, the error value MAPI_E_LOGON_FAILED is returned if the logon is unsuccessful.</span></span> <span data-ttu-id="c506f-132">このフラグが設定されていない場合、メッセージ ストア プロバイダーはユーザー名またはパスワード、またはストアへの接続を確立するために必要な処理を実行するディスクを挿入するのにを修正するを求めることができます。</span><span class="sxs-lookup"><span data-stu-id="c506f-132">If this flag is not set, the message store provider can prompt the user to correct a name or password, to insert a disk, or to perform other actions necessary to establish connection to the store.</span></span>
    
<span data-ttu-id="c506f-133">MDB_WRITE</span><span class="sxs-lookup"><span data-stu-id="c506f-133">MDB_WRITE</span></span> 
  
> <span data-ttu-id="c506f-134">要求の読み取り/書き込みのアクセス許可</span><span class="sxs-lookup"><span data-stu-id="c506f-134">Requests read/write permission.</span></span>
    
 <span data-ttu-id="c506f-135">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="c506f-135">_lpInterface_</span></span>
  
> <span data-ttu-id="c506f-136">[in]メッセージ ・ ストアへのログオン用のインターフェイス id (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c506f-136">[in] A pointer to the interface identifier (IID) for the message store to log on to.</span></span> <span data-ttu-id="c506f-137">NULL を渡すには、メッセージ ・ ストア ([IMsgStore](imsgstoreimapiprop.md)) の MAPI インターフェイスが返されることを示します。</span><span class="sxs-lookup"><span data-stu-id="c506f-137">Passing NULL indicates the MAPI interface for the message store ([IMsgStore](imsgstoreimapiprop.md)) is returned.</span></span> <span data-ttu-id="c506f-138">などに対する (IID_IMAPIProp) は、メッセージ ストアの適切なインターフェイスの識別子を_lpInterface_パラメーターを設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="c506f-138">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the message store (for example IID_IUnknown or IID_IMAPIProp).</span></span> 
    
 <span data-ttu-id="c506f-139">_cbSpoolSecurity_</span><span class="sxs-lookup"><span data-stu-id="c506f-139">_cbSpoolSecurity_</span></span>
  
> <span data-ttu-id="c506f-140">[in]_LppbSpoolSecurity_パラメーターの検証データのバイト単位のサイズへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c506f-140">[in] A pointer to the size, in bytes, of validation data in the  _lppbSpoolSecurity_ parameter.</span></span> 
    
 <span data-ttu-id="c506f-141">_lpbSpoolSecurity_</span><span class="sxs-lookup"><span data-stu-id="c506f-141">_lpbSpoolSecurity_</span></span>
  
> <span data-ttu-id="c506f-142">[in]検証データへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c506f-142">[in] A pointer to a pointer to validation data.</span></span> <span data-ttu-id="c506f-143">**SpoolerLogon**メソッドでは、このデータを使用して、メッセージ ストア プロバイダーの[IMSProvider::Logon](imsprovider-logon.md)メソッドを使用してログオンするのに以前と同じストアに、MAPI スプーラーをログに記録します。</span><span class="sxs-lookup"><span data-stu-id="c506f-143">The **SpoolerLogon** method uses this data to log the MAPI spooler on to the same store as the message store provider previously logged on to by using the [IMSProvider::Logon](imsprovider-logon.md) method.</span></span> 
    
 <span data-ttu-id="c506f-144">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="c506f-144">_lppMAPIError_</span></span>
  
> <span data-ttu-id="c506f-145">[out]返された[MAPIERROR](mapierror.md)構造体、存在する場合エラーが発生するバージョン、コンポーネント、およびコンテキストの情報が含まれているへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c506f-145">[out] A pointer to a pointer to the returned [MAPIERROR](mapierror.md) structure, if any, that contains version, component, and context information for an error.</span></span> <span data-ttu-id="c506f-146">取得する**MAPIERROR**構造体がない場合、 _lppMAPIError_パラメーターを NULL に設定できます。</span><span class="sxs-lookup"><span data-stu-id="c506f-146">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
 <span data-ttu-id="c506f-147">_lppMSLogon_</span><span class="sxs-lookup"><span data-stu-id="c506f-147">_lppMSLogon_</span></span>
  
> <span data-ttu-id="c506f-148">[out]メッセージへのポインターへのポインターでは、MAPI にログオンするためのログオン オブジェクトを格納します。</span><span class="sxs-lookup"><span data-stu-id="c506f-148">[out] A pointer to the pointer to the message store logon object for MAPI to log on to.</span></span>
    
 <span data-ttu-id="c506f-149">_lppMDB_</span><span class="sxs-lookup"><span data-stu-id="c506f-149">_lppMDB_</span></span>
  
> <span data-ttu-id="c506f-150">[out]メッセージへのポインターへのポインターでは、MAPI スプーラーとクライアント アプリケーションにログオンするためのオブジェクトを格納します。</span><span class="sxs-lookup"><span data-stu-id="c506f-150">[out] A pointer to the pointer to the message store object for the MAPI spooler and client applications to log on to.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c506f-151">�߂�l</span><span class="sxs-lookup"><span data-stu-id="c506f-151">Return value</span></span>

<span data-ttu-id="c506f-152">S_OK</span><span class="sxs-lookup"><span data-stu-id="c506f-152">S_OK</span></span> 
  
> <span data-ttu-id="c506f-153">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="c506f-153">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="c506f-154">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="c506f-154">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="c506f-155">プロファイルにログオンを完了するのに十分な情報が含まれていません。</span><span class="sxs-lookup"><span data-stu-id="c506f-155">The profile does not contain enough information for the logon to complete.</span></span> <span data-ttu-id="c506f-156">この値が返された場合は、MAPI メッセージ ストア プロバイダーのメッセージ サービスのエントリ ポイント関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c506f-156">When this value is returned, MAPI calls the message store provider's message service entry point function.</span></span>
    
<span data-ttu-id="c506f-157">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="c506f-157">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="c506f-158">呼び出しが成功したが、メッセージ ストア プロバイダーが使用可能なエラー情報を持ちます。</span><span class="sxs-lookup"><span data-stu-id="c506f-158">The call succeeded, but the message store provider has error information available.</span></span> <span data-ttu-id="c506f-159">この警告が返されると、呼び出しを成功として処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c506f-159">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="c506f-160">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="c506f-160">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="c506f-161">詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c506f-161">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span> <span data-ttu-id="c506f-162">プロバイダーからエラー情報を取得するには、 [IMAPISession::GetLastError](imapisession-getlasterror.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c506f-162">To get the error information from the provider, call the [IMAPISession::GetLastError](imapisession-getlasterror.md) method.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c506f-163">注釈</span><span class="sxs-lookup"><span data-stu-id="c506f-163">Remarks</span></span>

<span data-ttu-id="c506f-164">MAPI スプーラーでは、メッセージ ストアにログオンするための**IMSProvider::SpoolerLogon**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c506f-164">The MAPI spooler calls the **IMSProvider::SpoolerLogon** method to log on to a message store.</span></span> <span data-ttu-id="c506f-165">MAPI スプーラーは、中に、ログオンした後に、 _lppMDB_パラメーターでは、メッセージ ストア プロバイダーによって返されるメッセージのストア オブジェクトを使用してください。</span><span class="sxs-lookup"><span data-stu-id="c506f-165">The MAPI spooler should use the message store object returned by the message store provider in the  _lppMDB_ parameter during and after logon.</span></span> 
  
<span data-ttu-id="c506f-166">[IMSProvider::Logon](imsprovider-logon.md)メソッドを使用して、一貫性のプロバイダーは、 _lppMSLogon_パラメーターにもデータのメッセージ ストア ログオン オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="c506f-166">For consistency with the [IMSProvider::Logon](imsprovider-logon.md) method, the provider also returns a message store logon object in the  _lppMSLogon_ parameter.</span></span> <span data-ttu-id="c506f-167">ストア オブジェクトとログオン オブジェクトの使用は同一の一般的なストア ログオンします。オブジェクトが 2 つのインターフェイスを公開する 1 つのオブジェクトであるかのように動作するよう、ログオン オブジェクトとストア オブジェクトとの間の 1 対 1 対応がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="c506f-167">The use of the store object and the logon object are identical for usual store logon; there should be a one-to-one correspondence between the logon object and the store object such that the objects act as if they are one object that exposes two interfaces.</span></span> <span data-ttu-id="c506f-168">2 つのオブジェクトは、同時解放と連携して作成されます。</span><span class="sxs-lookup"><span data-stu-id="c506f-168">The two objects are created together and freed together.</span></span> 
  
<span data-ttu-id="c506f-169">ストア プロバイダーは、ストアを MAPI スプーラーで使用されていることを示すために返されるメッセージのストア オブジェクトを内部的にマーク必要があります。</span><span class="sxs-lookup"><span data-stu-id="c506f-169">The store provider should internally mark the returned message store object to indicate that the store is being used by the MAPI spooler.</span></span> <span data-ttu-id="c506f-170">このストア オブジェクトのメソッドのいくつかがメッセージをクライアント アプリケーションに提供するオブジェクトを格納するいるとは異なる動作します。</span><span class="sxs-lookup"><span data-stu-id="c506f-170">Some of the methods for this store object behave differently than for the message store object provided to client applications.</span></span> <span data-ttu-id="c506f-171">この内部のマークを保持することは、MAPI スプーラーに固有の動作をトリガーする最も一般的な方法です。</span><span class="sxs-lookup"><span data-stu-id="c506f-171">Keeping this internal mark is the most common way of triggering the behavior specific to the MAPI spooler.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c506f-172">関連項目</span><span class="sxs-lookup"><span data-stu-id="c506f-172">See also</span></span>



[<span data-ttu-id="c506f-173">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="c506f-173">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="c506f-174">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="c506f-174">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="c506f-175">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c506f-175">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

