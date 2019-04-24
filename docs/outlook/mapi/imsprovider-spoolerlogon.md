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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309738"
---
# <a name="imsproviderspoolerlogon"></a><span data-ttu-id="cf2f6-103">IMSProvider::SpoolerLogon</span><span class="sxs-lookup"><span data-stu-id="cf2f6-103">IMSProvider::SpoolerLogon</span></span>

  
  
<span data-ttu-id="cf2f6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf2f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf2f6-105">MAPI スプーラーをメッセージストアに記録します。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-105">Logs the MAPI spooler on to a message store.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="cf2f6-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cf2f6-106">Parameters</span></span>

 <span data-ttu-id="cf2f6-107">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="cf2f6-107">_lpMAPISup_</span></span>
  
> <span data-ttu-id="cf2f6-108">順番メッセージストアの MAPI サポートオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-108">[in] A pointer to the MAPI support object for the message store.</span></span>
    
 <span data-ttu-id="cf2f6-109">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="cf2f6-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="cf2f6-110">順番このメソッドが表示する任意のダイアログボックスまたはウィンドウの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-110">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> 
    
 <span data-ttu-id="cf2f6-111">_lpszprofilename_</span><span class="sxs-lookup"><span data-stu-id="cf2f6-111">_lpszProfileName_</span></span>
  
> <span data-ttu-id="cf2f6-112">順番MAPI スプーラーログオンに使用されているプロファイルの名前を含む文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-112">[in] A pointer to a string that contains the name of the profile being used for the MAPI spooler logon.</span></span> <span data-ttu-id="cf2f6-113">この文字列は、ダイアログボックスに表示したり、ログファイルに書き込んだたり、単に無視したりできます。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-113">This string can be displayed in dialog boxes, written out to a log file, or simply ignored.</span></span> <span data-ttu-id="cf2f6-114">MAPI_UNICODE フラグが_ulflags_パラメーターで設定されている場合は、Unicode 形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-114">It must be in Unicode format if the MAPI_UNICODE flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="cf2f6-115">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="cf2f6-115">_cbEntryID_</span></span>
  
> <span data-ttu-id="cf2f6-116">順番_lな tryid_パラメーターで指定されたエントリ識別子のサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-116">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="cf2f6-117">_lて tryid_</span><span class="sxs-lookup"><span data-stu-id="cf2f6-117">_lpEntryID_</span></span>
  
> <span data-ttu-id="cf2f6-118">順番メッセージストアのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-118">[in] A pointer to the entry identifier for the message store.</span></span> <span data-ttu-id="cf2f6-119">_lな tryid_パラメーターで NULL を渡すと、メッセージストアがまだ選択されていないことと、ユーザーがメッセージストアを選択できるようにするダイアログボックスが表示されることを示します。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-119">Passing NULL in the  _lpEntryID_ parameter indicates that a message store has not yet been selected and that dialog boxes that enable the user to select a message store can be presented.</span></span> 
    
 <span data-ttu-id="cf2f6-120">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cf2f6-120">_ulFlags_</span></span>
  
> <span data-ttu-id="cf2f6-121">順番ログオンの実行方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-121">[in] A bitmask of flags that controls how the logon is performed.</span></span> <span data-ttu-id="cf2f6-122">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-122">The following flags can be set:</span></span>
    
<span data-ttu-id="cf2f6-123">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="cf2f6-123">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="cf2f6-124">呼び出し元のオブジェクトが呼び出し側の実装で使用できない場合でも、呼び出しを成功させることができます。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-124">The call is allowed to succeed even if the underlying object is not available to the calling implementation.</span></span> <span data-ttu-id="cf2f6-125">オブジェクトが使用できない場合は、その後のオブジェクトの呼び出しでエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-125">If the object is not available, a subsequent call to the object might raise an error.</span></span>
    
<span data-ttu-id="cf2f6-126">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="cf2f6-126">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="cf2f6-127">渡された文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-127">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="cf2f6-128">MAPI_UNICODE が設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-128">If MAPI_UNICODE is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="cf2f6-129">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="cf2f6-129">MDB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="cf2f6-130">ログオンダイアログボックスを表示しないようにします。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-130">Prevents the display of logon dialog boxes.</span></span> <span data-ttu-id="cf2f6-131">このフラグが設定されている場合は、ログオンが失敗した場合にエラー値 MAPI_E_LOGON_FAILED が返されます。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-131">If this flag is set, the error value MAPI_E_LOGON_FAILED is returned if the logon is unsuccessful.</span></span> <span data-ttu-id="cf2f6-132">このフラグが設定されていない場合、メッセージストアプロバイダーはユーザーに対して、名前またはパスワードを修正するか、ディスクを挿入するか、またはストアへの接続を確立するために必要なその他の操作を実行するように求めることができます。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-132">If this flag is not set, the message store provider can prompt the user to correct a name or password, to insert a disk, or to perform other actions necessary to establish connection to the store.</span></span>
    
<span data-ttu-id="cf2f6-133">MDB_WRITE</span><span class="sxs-lookup"><span data-stu-id="cf2f6-133">MDB_WRITE</span></span> 
  
> <span data-ttu-id="cf2f6-134">読み取り/書き込みアクセス許可を要求します。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-134">Requests read/write permission.</span></span>
    
 <span data-ttu-id="cf2f6-135">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="cf2f6-135">_lpInterface_</span></span>
  
> <span data-ttu-id="cf2f6-136">順番ログオンするメッセージストアのインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-136">[in] A pointer to the interface identifier (IID) for the message store to log on to.</span></span> <span data-ttu-id="cf2f6-137">NULL を渡すと、メッセージストア ([IMsgStore](imsgstoreimapiprop.md)) の MAPI インターフェイスが返されます。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-137">Passing NULL indicates the MAPI interface for the message store ([IMsgStore](imsgstoreimapiprop.md)) is returned.</span></span> <span data-ttu-id="cf2f6-138">_lpinterface_パラメーターは、メッセージストアの適切なインターフェイスの識別子に設定することもできます (たとえば、IID_IUnknown または IID_IMAPIProp)。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-138">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the message store (for example IID_IUnknown or IID_IMAPIProp).</span></span> 
    
 <span data-ttu-id="cf2f6-139">_cbSpoolSecurity_</span><span class="sxs-lookup"><span data-stu-id="cf2f6-139">_cbSpoolSecurity_</span></span>
  
> <span data-ttu-id="cf2f6-140">順番_lppbSpoolSecurity_パラメーターの検証データのサイズ (バイト単位) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-140">[in] A pointer to the size, in bytes, of validation data in the  _lppbSpoolSecurity_ parameter.</span></span> 
    
 <span data-ttu-id="cf2f6-141">_lpbSpoolSecurity_</span><span class="sxs-lookup"><span data-stu-id="cf2f6-141">_lpbSpoolSecurity_</span></span>
  
> <span data-ttu-id="cf2f6-142">順番検証データへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-142">[in] A pointer to a pointer to validation data.</span></span> <span data-ttu-id="cf2f6-143">**SpoolerLogon**メソッドは、このデータを使用して、 [IMSProvider:: Logon](imsprovider-logon.md)メソッドを使用して、以前にログオンしたメッセージストアプロバイダーと同じストアに MAPI スプーラーを記録します。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-143">The **SpoolerLogon** method uses this data to log the MAPI spooler on to the same store as the message store provider previously logged on to by using the [IMSProvider::Logon](imsprovider-logon.md) method.</span></span> 
    
 <span data-ttu-id="cf2f6-144">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="cf2f6-144">_lppMAPIError_</span></span>
  
> <span data-ttu-id="cf2f6-145">読み上げエラーのバージョン、コンポーネント、およびコンテキスト情報を含む返された[MAPIERROR](mapierror.md)構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-145">[out] A pointer to a pointer to the returned [MAPIERROR](mapierror.md) structure, if any, that contains version, component, and context information for an error.</span></span> <span data-ttu-id="cf2f6-146">返す**MAPIERROR**構造体がない場合は、 _lppMAPIError_パラメーターを NULL に設定できます。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-146">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
 <span data-ttu-id="cf2f6-147">_lppmslogon_</span><span class="sxs-lookup"><span data-stu-id="cf2f6-147">_lppMSLogon_</span></span>
  
> <span data-ttu-id="cf2f6-148">読み上げMAPI がログオンするためのメッセージストアログオンオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-148">[out] A pointer to the pointer to the message store logon object for MAPI to log on to.</span></span>
    
 <span data-ttu-id="cf2f6-149">_lppmdb_</span><span class="sxs-lookup"><span data-stu-id="cf2f6-149">_lppMDB_</span></span>
  
> <span data-ttu-id="cf2f6-150">読み上げログオンする MAPI スプーラーおよびクライアントアプリケーションのメッセージストアオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-150">[out] A pointer to the pointer to the message store object for the MAPI spooler and client applications to log on to.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cf2f6-151">戻り値</span><span class="sxs-lookup"><span data-stu-id="cf2f6-151">Return value</span></span>

<span data-ttu-id="cf2f6-152">S_OK</span><span class="sxs-lookup"><span data-stu-id="cf2f6-152">S_OK</span></span> 
  
> <span data-ttu-id="cf2f6-153">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="cf2f6-153">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="cf2f6-154">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="cf2f6-154">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="cf2f6-155">このプロファイルには、ログオンが完了するのに十分な情報が含まれていません。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-155">The profile does not contain enough information for the logon to complete.</span></span> <span data-ttu-id="cf2f6-156">この値が返されると、MAPI はメッセージストアプロバイダーのメッセージサービスエントリポイント関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-156">When this value is returned, MAPI calls the message store provider's message service entry point function.</span></span>
    
<span data-ttu-id="cf2f6-157">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="cf2f6-157">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="cf2f6-158">呼び出しは成功しましたが、メッセージストアプロバイダーにエラー情報があります。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-158">The call succeeded, but the message store provider has error information available.</span></span> <span data-ttu-id="cf2f6-159">この警告が返された場合、呼び出しは正常に処理されます。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-159">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="cf2f6-160">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-160">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="cf2f6-161">詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-161">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span> <span data-ttu-id="cf2f6-162">プロバイダーからエラー情報を取得するには、 [imapisession:: GetLastError](imapisession-getlasterror.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-162">To get the error information from the provider, call the [IMAPISession::GetLastError](imapisession-getlasterror.md) method.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="cf2f6-163">解説</span><span class="sxs-lookup"><span data-stu-id="cf2f6-163">Remarks</span></span>

<span data-ttu-id="cf2f6-164">MAPI スプーラーは、 **IMSProvider:: SpoolerLogon**メソッドを呼び出して、メッセージストアにログオンします。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-164">The MAPI spooler calls the **IMSProvider::SpoolerLogon** method to log on to a message store.</span></span> <span data-ttu-id="cf2f6-165">MAPI スプーラーは、ログオン時および_lppmdb_パラメーターのメッセージストアプロバイダーから返されるメッセージストアオブジェクトを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-165">The MAPI spooler should use the message store object returned by the message store provider in the  _lppMDB_ parameter during and after logon.</span></span> 
  
<span data-ttu-id="cf2f6-166">[IMSProvider:: Logon](imsprovider-logon.md)メソッドとの一貫性を保つため、プロバイダーは_lppmslogon_パラメーターにメッセージストアのログオンオブジェクトも返します。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-166">For consistency with the [IMSProvider::Logon](imsprovider-logon.md) method, the provider also returns a message store logon object in the  _lppMSLogon_ parameter.</span></span> <span data-ttu-id="cf2f6-167">store オブジェクトと logon オブジェクトの使用方法は、通常のストアログオンの場合と同じです。これらのオブジェクトは、2つのインターフェイスを公開する1つのオブジェクトとして機能するように、ログオンオブジェクトと store オブジェクトの間に1対1で対応する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-167">The use of the store object and the logon object are identical for usual store logon; there should be a one-to-one correspondence between the logon object and the store object such that the objects act as if they are one object that exposes two interfaces.</span></span> <span data-ttu-id="cf2f6-168">2つのオブジェクトが一緒に作成され、一緒に解放されます。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-168">The two objects are created together and freed together.</span></span> 
  
<span data-ttu-id="cf2f6-169">ストアプロバイダーは、返されたメッセージストアオブジェクトを内部的にマークして、ストアが MAPI スプーラーによって使用されていることを示す必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-169">The store provider should internally mark the returned message store object to indicate that the store is being used by the MAPI spooler.</span></span> <span data-ttu-id="cf2f6-170">このストアオブジェクトのメソッドの動作は、クライアントアプリケーションに提供されるメッセージストアオブジェクトとは異なります。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-170">Some of the methods for this store object behave differently than for the message store object provided to client applications.</span></span> <span data-ttu-id="cf2f6-171">この内部マークを保持することは、MAPI スプーラーに固有の動作をトリガーする最も一般的な方法です。</span><span class="sxs-lookup"><span data-stu-id="cf2f6-171">Keeping this internal mark is the most common way of triggering the behavior specific to the MAPI spooler.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cf2f6-172">関連項目</span><span class="sxs-lookup"><span data-stu-id="cf2f6-172">See also</span></span>



[<span data-ttu-id="cf2f6-173">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="cf2f6-173">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="cf2f6-174">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="cf2f6-174">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="cf2f6-175">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cf2f6-175">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

