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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 794674df38266743cac8c947ec93dc1fcfff438b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430575"
---
# <a name="imsproviderspoolerlogon"></a><span data-ttu-id="09f39-103">IMSProvider::SpoolerLogon</span><span class="sxs-lookup"><span data-stu-id="09f39-103">IMSProvider::SpoolerLogon</span></span>

  
  
<span data-ttu-id="09f39-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="09f39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="09f39-105">MAPI スプーラーをメッセージ ストアにログに記録します。</span><span class="sxs-lookup"><span data-stu-id="09f39-105">Logs the MAPI spooler on to a message store.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="09f39-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="09f39-106">Parameters</span></span>

 <span data-ttu-id="09f39-107">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="09f39-107">_lpMAPISup_</span></span>
  
> <span data-ttu-id="09f39-108">[in]メッセージ ストアの MAPI サポート オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="09f39-108">[in] A pointer to the MAPI support object for the message store.</span></span>
    
 <span data-ttu-id="09f39-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="09f39-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="09f39-110">[in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="09f39-110">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> 
    
 <span data-ttu-id="09f39-111">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="09f39-111">_lpszProfileName_</span></span>
  
> <span data-ttu-id="09f39-112">[in]MAPI スプーラー ログオンに使用されているプロファイルの名前を含む文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="09f39-112">[in] A pointer to a string that contains the name of the profile being used for the MAPI spooler logon.</span></span> <span data-ttu-id="09f39-113">この文字列は、ダイアログ ボックスに表示したり、ログ ファイルに書き出したり、単に無視することができます。</span><span class="sxs-lookup"><span data-stu-id="09f39-113">This string can be displayed in dialog boxes, written out to a log file, or simply ignored.</span></span> <span data-ttu-id="09f39-114">_ulFlags_ パラメーターでフラグを設定MAPI_UNICODE Unicode 形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="09f39-114">It must be in Unicode format if the MAPI_UNICODE flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="09f39-115">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="09f39-115">_cbEntryID_</span></span>
  
> <span data-ttu-id="09f39-116">[in]  _lpEntryID_ パラメーターが指すエントリ識別子のサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="09f39-116">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="09f39-117">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="09f39-117">_lpEntryID_</span></span>
  
> <span data-ttu-id="09f39-118">[in]メッセージ ストアのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="09f39-118">[in] A pointer to the entry identifier for the message store.</span></span> <span data-ttu-id="09f39-119">_lpEntryID_ パラメーターに NULL を渡す場合は、メッセージ ストアがまだ選択されていないと、ユーザーがメッセージ ストアを選択できるダイアログ ボックスを表示できます。</span><span class="sxs-lookup"><span data-stu-id="09f39-119">Passing NULL in the  _lpEntryID_ parameter indicates that a message store has not yet been selected and that dialog boxes that enable the user to select a message store can be presented.</span></span> 
    
 <span data-ttu-id="09f39-120">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="09f39-120">_ulFlags_</span></span>
  
> <span data-ttu-id="09f39-121">[in]ログオンの実行方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="09f39-121">[in] A bitmask of flags that controls how the logon is performed.</span></span> <span data-ttu-id="09f39-122">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="09f39-122">The following flags can be set:</span></span>
    
<span data-ttu-id="09f39-123">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="09f39-123">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="09f39-124">呼び出し元のオブジェクトが呼び出し元の実装で使用できない場合でも、呼び出しは成功できます。</span><span class="sxs-lookup"><span data-stu-id="09f39-124">The call is allowed to succeed even if the underlying object is not available to the calling implementation.</span></span> <span data-ttu-id="09f39-125">オブジェクトが使用できない場合は、そのオブジェクトに対する後続の呼び出しでエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="09f39-125">If the object is not available, a subsequent call to the object might raise an error.</span></span>
    
<span data-ttu-id="09f39-126">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="09f39-126">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="09f39-127">渡された文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="09f39-127">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="09f39-128">このMAPI_UNICODE設定されていない場合、文字列は ANSI 形式です。</span><span class="sxs-lookup"><span data-stu-id="09f39-128">If MAPI_UNICODE is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="09f39-129">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="09f39-129">MDB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="09f39-130">ログオン ダイアログ ボックスの表示を防止します。</span><span class="sxs-lookup"><span data-stu-id="09f39-130">Prevents the display of logon dialog boxes.</span></span> <span data-ttu-id="09f39-131">このフラグを設定すると、ログオンが失敗MAPI_E_LOGON_FAILEDエラー値が返されます。</span><span class="sxs-lookup"><span data-stu-id="09f39-131">If this flag is set, the error value MAPI_E_LOGON_FAILED is returned if the logon is unsuccessful.</span></span> <span data-ttu-id="09f39-132">このフラグが設定されていない場合、メッセージ ストア プロバイダーは、名前またはパスワードの修正、ディスクの挿入、またはストアへの接続を確立するために必要なその他のアクションを実行するようユーザーに求めできます。</span><span class="sxs-lookup"><span data-stu-id="09f39-132">If this flag is not set, the message store provider can prompt the user to correct a name or password, to insert a disk, or to perform other actions necessary to establish connection to the store.</span></span>
    
<span data-ttu-id="09f39-133">MDB_WRITE</span><span class="sxs-lookup"><span data-stu-id="09f39-133">MDB_WRITE</span></span> 
  
> <span data-ttu-id="09f39-134">読み取り/書き込みアクセス許可を要求します。</span><span class="sxs-lookup"><span data-stu-id="09f39-134">Requests read/write permission.</span></span>
    
 <span data-ttu-id="09f39-135">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="09f39-135">_lpInterface_</span></span>
  
> <span data-ttu-id="09f39-136">[in]ログオンするメッセージ ストアのインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="09f39-136">[in] A pointer to the interface identifier (IID) for the message store to log on to.</span></span> <span data-ttu-id="09f39-137">NULL を渡す場合は、メッセージ ストア[(IMsgStore)](imsgstoreimapiprop.md)の MAPI インターフェイスが返されます。</span><span class="sxs-lookup"><span data-stu-id="09f39-137">Passing NULL indicates the MAPI interface for the message store ([IMsgStore](imsgstoreimapiprop.md)) is returned.</span></span> <span data-ttu-id="09f39-138">_lpInterface パラメーター_ は、メッセージ ストアの適切なインターフェイスの識別子 (たとえば、IID_IUnknown または IID_IMAPIProp) に設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="09f39-138">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the message store (for example IID_IUnknown or IID_IMAPIProp).</span></span> 
    
 <span data-ttu-id="09f39-139">_cbSpoolSecurity_</span><span class="sxs-lookup"><span data-stu-id="09f39-139">_cbSpoolSecurity_</span></span>
  
> <span data-ttu-id="09f39-140">[in]  _lppbSpoolSecurity_ パラメーター内の検証データのサイズ (バイト単位) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="09f39-140">[in] A pointer to the size, in bytes, of validation data in the  _lppbSpoolSecurity_ parameter.</span></span> 
    
 <span data-ttu-id="09f39-141">_lpbSpoolSecurity_</span><span class="sxs-lookup"><span data-stu-id="09f39-141">_lpbSpoolSecurity_</span></span>
  
> <span data-ttu-id="09f39-142">[in]検証データへのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="09f39-142">[in] A pointer to a pointer to validation data.</span></span> <span data-ttu-id="09f39-143">**SpoolerLogon** メソッドは、このデータを使用して [、IMSProvider::Logon](imsprovider-logon.md)メソッドを使用して以前にログオンしたメッセージ ストア プロバイダーと同じストアに MAPI スプーラーをログオンします。</span><span class="sxs-lookup"><span data-stu-id="09f39-143">The **SpoolerLogon** method uses this data to log the MAPI spooler on to the same store as the message store provider previously logged on to by using the [IMSProvider::Logon](imsprovider-logon.md) method.</span></span> 
    
 <span data-ttu-id="09f39-144">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="09f39-144">_lppMAPIError_</span></span>
  
> <span data-ttu-id="09f39-145">[out]エラーのバージョン、コンポーネント、コンテキスト情報を含む、返される [MAPIERROR](mapierror.md) 構造体へのポインター (該当する場合) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="09f39-145">[out] A pointer to a pointer to the returned [MAPIERROR](mapierror.md) structure, if any, that contains version, component, and context information for an error.</span></span> <span data-ttu-id="09f39-146">_戻す MAPIERROR 構造体がない場合、lppMAPIError_ パラメーターを **NULL に** 設定できます。</span><span class="sxs-lookup"><span data-stu-id="09f39-146">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
 <span data-ttu-id="09f39-147">_lppMSLogon_</span><span class="sxs-lookup"><span data-stu-id="09f39-147">_lppMSLogon_</span></span>
  
> <span data-ttu-id="09f39-148">[out]MAPI がログオンするメッセージ ストア ログオン オブジェクトへのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="09f39-148">[out] A pointer to the pointer to the message store logon object for MAPI to log on to.</span></span>
    
 <span data-ttu-id="09f39-149">_lppMDB_</span><span class="sxs-lookup"><span data-stu-id="09f39-149">_lppMDB_</span></span>
  
> <span data-ttu-id="09f39-150">[out]MAPI スプーラーおよびクライアント アプリケーションがログオンするメッセージ ストア オブジェクトへのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="09f39-150">[out] A pointer to the pointer to the message store object for the MAPI spooler and client applications to log on to.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="09f39-151">戻り値</span><span class="sxs-lookup"><span data-stu-id="09f39-151">Return value</span></span>

<span data-ttu-id="09f39-152">S_OK</span><span class="sxs-lookup"><span data-stu-id="09f39-152">S_OK</span></span> 
  
> <span data-ttu-id="09f39-153">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="09f39-153">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="09f39-154">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="09f39-154">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="09f39-155">プロファイルには、ログオンが完了するのに十分な情報が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="09f39-155">The profile does not contain enough information for the logon to complete.</span></span> <span data-ttu-id="09f39-156">この値が返された場合、MAPI はメッセージ ストア プロバイダーのメッセージ サービス エントリ ポイント関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="09f39-156">When this value is returned, MAPI calls the message store provider's message service entry point function.</span></span>
    
<span data-ttu-id="09f39-157">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="09f39-157">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="09f39-158">呼び出しは成功しましたが、メッセージ ストア プロバイダーにエラー情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="09f39-158">The call succeeded, but the message store provider has error information available.</span></span> <span data-ttu-id="09f39-159">この警告が返されると、呼び出しは正常に処理されます。</span><span class="sxs-lookup"><span data-stu-id="09f39-159">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="09f39-160">この警告をテストするには、次のマクロ **HR_FAILED** します。</span><span class="sxs-lookup"><span data-stu-id="09f39-160">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="09f39-161">詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。</span><span class="sxs-lookup"><span data-stu-id="09f39-161">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span> <span data-ttu-id="09f39-162">プロバイダーからエラー情報を取得するには [、IMAPISession::GetLastError メソッドを呼び出](imapisession-getlasterror.md) します。</span><span class="sxs-lookup"><span data-stu-id="09f39-162">To get the error information from the provider, call the [IMAPISession::GetLastError](imapisession-getlasterror.md) method.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="09f39-163">注釈</span><span class="sxs-lookup"><span data-stu-id="09f39-163">Remarks</span></span>

<span data-ttu-id="09f39-164">MAPI スプーラーは **、IMSProvider::SpoolerLogon** メソッドを呼び出して、メッセージ ストアにログオンします。</span><span class="sxs-lookup"><span data-stu-id="09f39-164">The MAPI spooler calls the **IMSProvider::SpoolerLogon** method to log on to a message store.</span></span> <span data-ttu-id="09f39-165">MAPI スプーラーは、ログオン中とログオン後に  _lppMDB_ パラメーター内のメッセージ ストア プロバイダーによって返されるメッセージ ストア オブジェクトを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="09f39-165">The MAPI spooler should use the message store object returned by the message store provider in the  _lppMDB_ parameter during and after logon.</span></span> 
  
<span data-ttu-id="09f39-166">[IMSProvider::Logon](imsprovider-logon.md)メソッドとの整合性を保つには、プロバイダーは _lppMSLogon_ パラメーターにメッセージ ストア ログオン オブジェクトも返します。</span><span class="sxs-lookup"><span data-stu-id="09f39-166">For consistency with the [IMSProvider::Logon](imsprovider-logon.md) method, the provider also returns a message store logon object in the  _lppMSLogon_ parameter.</span></span> <span data-ttu-id="09f39-167">ストア オブジェクトとログオン オブジェクトの使用は、通常のストア ログオンと同じです。オブジェクトが 2 つのインターフェイスを公開する 1 つのオブジェクトである場合と同様に、ログオン オブジェクトとストア オブジェクトの間には 1 対 1 の対応が必要です。</span><span class="sxs-lookup"><span data-stu-id="09f39-167">The use of the store object and the logon object are identical for usual store logon; there should be a one-to-one correspondence between the logon object and the store object such that the objects act as if they are one object that exposes two interfaces.</span></span> <span data-ttu-id="09f39-168">2 つのオブジェクトは一緒に作成され、一緒に解放されます。</span><span class="sxs-lookup"><span data-stu-id="09f39-168">The two objects are created together and freed together.</span></span> 
  
<span data-ttu-id="09f39-169">ストア プロバイダーは、MAPI スプーラーによってストアが使用されているかどうかを示すために、返されるメッセージ ストア オブジェクトを内部的にマークする必要があります。</span><span class="sxs-lookup"><span data-stu-id="09f39-169">The store provider should internally mark the returned message store object to indicate that the store is being used by the MAPI spooler.</span></span> <span data-ttu-id="09f39-170">このストア オブジェクトの一部のメソッドは、クライアント アプリケーションに提供されるメッセージ ストア オブジェクトとは異なる動作をします。</span><span class="sxs-lookup"><span data-stu-id="09f39-170">Some of the methods for this store object behave differently than for the message store object provided to client applications.</span></span> <span data-ttu-id="09f39-171">この内部マークを保持すると、MAPI スプーラーに固有の動作をトリガーする最も一般的な方法です。</span><span class="sxs-lookup"><span data-stu-id="09f39-171">Keeping this internal mark is the most common way of triggering the behavior specific to the MAPI spooler.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="09f39-172">関連項目</span><span class="sxs-lookup"><span data-stu-id="09f39-172">See also</span></span>



[<span data-ttu-id="09f39-173">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="09f39-173">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="09f39-174">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="09f39-174">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="09f39-175">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="09f39-175">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

