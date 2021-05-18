---
title: MAPIInitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIInitialize
api_type:
- HeaderDef
ms.assetid: b9584226-79d2-4d83-8f31-dbfbc50f16c5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6464f16d9ad73b332ff20dc007ef162b9525c6d5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411177"
---
# <a name="mapiinitialize"></a><span data-ttu-id="65bbb-103">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="65bbb-103">MAPIInitialize</span></span>

  
  
<span data-ttu-id="65bbb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65bbb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65bbb-105">MAPI サブシステム参照カウントをインクリメントし、MAPI DLL のグローバル データを初期化します。</span><span class="sxs-lookup"><span data-stu-id="65bbb-105">Increments the MAPI subsystem reference count and initializes global data for the MAPI DLL.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="65bbb-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="65bbb-106">Header file:</span></span>  <br/> |<span data-ttu-id="65bbb-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="65bbb-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="65bbb-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="65bbb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="65bbb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="65bbb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="65bbb-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="65bbb-110">Called by:</span></span>  <br/> |<span data-ttu-id="65bbb-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="65bbb-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPIInitialize(
  LPVOID lpMapiInit
);
```

## <a name="parameters"></a><span data-ttu-id="65bbb-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="65bbb-112">Parameters</span></span>

 <span data-ttu-id="65bbb-113">_lpMapiInit_</span><span class="sxs-lookup"><span data-stu-id="65bbb-113">_lpMapiInit_</span></span>
  
> <span data-ttu-id="65bbb-114">[in]構造体への [ポインター](mapiinit_0.md) MAPIINIT_0します。</span><span class="sxs-lookup"><span data-stu-id="65bbb-114">[in] Pointer to a [MAPIINIT_0](mapiinit_0.md) structure.</span></span> <span data-ttu-id="65bbb-115">_lpMapiInit パラメーター_ は NULL に設定できます。</span><span class="sxs-lookup"><span data-stu-id="65bbb-115">The  _lpMapiInit_ parameter can be set to NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="65bbb-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="65bbb-116">Return value</span></span>

<span data-ttu-id="65bbb-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="65bbb-117">S_OK</span></span> 
  
> <span data-ttu-id="65bbb-118">MAPI サブシステムが正常に初期化されました。</span><span class="sxs-lookup"><span data-stu-id="65bbb-118">The MAPI subsystem was initialized successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="65bbb-119">注釈</span><span class="sxs-lookup"><span data-stu-id="65bbb-119">Remarks</span></span>

<span data-ttu-id="65bbb-120">**MAPIInitialize** 関数は MAPI サブシステムの MAPI 参照カウントをインクリメントし [、MAPIUninitialize](mapiuninitialize.md)関数は内部参照カウントをデクリメントします。</span><span class="sxs-lookup"><span data-stu-id="65bbb-120">The **MAPIInitialize** function increments the MAPI reference count for the MAPI subsystem, and the [MAPIUninitialize](mapiuninitialize.md) function decrements the internal reference count.</span></span> <span data-ttu-id="65bbb-121">したがって、1 つの関数に対する呼び出しの数は、もう一方の関数への呼び出しの数と等しくする必要があります。</span><span class="sxs-lookup"><span data-stu-id="65bbb-121">Thus, the number of calls to one function must equal the number of calls to the other.</span></span> <span data-ttu-id="65bbb-122">**MAPIInitialize は** 、MAPI S_OK初期化されていない場合は、この値を返します。</span><span class="sxs-lookup"><span data-stu-id="65bbb-122">**MAPIInitialize** returns S_OK if MAPI has not been previously initialized.</span></span> 
  
<span data-ttu-id="65bbb-123">クライアントまたはサービス プロバイダーは、他の MAPI 呼 **び出しを行う前に MAPIInitialize** を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="65bbb-123">A client or service provider must call **MAPIInitialize** before making any other MAPI call.</span></span> <span data-ttu-id="65bbb-124">そうしない場合、クライアントまたはサービス プロバイダーの呼び出しは、MAPI_E_NOT_INITIALIZEDします。</span><span class="sxs-lookup"><span data-stu-id="65bbb-124">Failure to do so causes client or service provider calls to return the MAPI_E_NOT_INITIALIZED value.</span></span> 
  
<span data-ttu-id="65bbb-125">マルチスレッド アプリケーション **から MAPIInitialize** を呼び出す場合は  _、lpMapiInit_ パラメーター [を次のように](mapiinit_0.md) 宣言された MAPIINIT_0 構造体に設定します。</span><span class="sxs-lookup"><span data-stu-id="65bbb-125">When calling **MAPIInitialize** from a multithreaded application, set the  _lpMapiInit_ parameter to a [MAPIINIT_0](mapiinit_0.md) structure that is declared as follows:</span></span> 
  
 <span data-ttu-id="65bbb-126">**MAPIINIT_0** MAPIINIT= { 0, MAPI_MULTITHREAD_NOTIFICATIONS}</span><span class="sxs-lookup"><span data-stu-id="65bbb-126">**MAPIINIT_0** MAPIINIT= { 0, MAPI_MULTITHREAD_NOTIFICATIONS}</span></span> 
  
<span data-ttu-id="65bbb-127">と呼び出し:</span><span class="sxs-lookup"><span data-stu-id="65bbb-127">and call:</span></span> 
  
 <span data-ttu-id="65bbb-128">**MAPIInitialize** &amp; (MAPIINIT);</span><span class="sxs-lookup"><span data-stu-id="65bbb-128">**MAPIInitialize** (&amp;MAPIINIT);</span></span> 
  
<span data-ttu-id="65bbb-129">この構造体を宣言すると、MAPI は通知ウィンドウを処理する別のスレッドを作成します。これは、初期化参照カウントが 0 になるまで続きます。</span><span class="sxs-lookup"><span data-stu-id="65bbb-129">When this structure is declared, MAPI creates a separate thread to handle the notification window, which continues until the initialize reference count falls to zero.</span></span> <span data-ttu-id="65bbb-130">サービス _Windows、lpMapiInit_ が指す MAPIINIT_0構造体の **ulflags** メンバーを、MAPI_NT_SERVICE。</span><span class="sxs-lookup"><span data-stu-id="65bbb-130">A Windows service must set the **ulflags** member of the **MAPIINIT_0** structure pointed to by  _lpMapiInit_ to MAPI_NT_SERVICE.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="65bbb-131">Win32 **DllMain** 関数またはスレッドを作成または終了するその他の関数内から **MAPIInitialize** または **MAPIUninitialize** を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="65bbb-131">You cannot call **MAPIInitialize** or **MAPIUninitialize** from within a Win32 **DllMain** function or any other function that creates or terminates threads.</span></span> <span data-ttu-id="65bbb-132">詳細については、「Using [Thread-Safe オブジェクト」を参照してください](using-thread-safe-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="65bbb-132">For more information, see [Using Thread-Safe Objects](using-thread-safe-objects.md).</span></span> 
  
 <span data-ttu-id="65bbb-133">**MAPIInitialize では** 、拡張エラー情報は返されません。</span><span class="sxs-lookup"><span data-stu-id="65bbb-133">**MAPIInitialize** does not return any extended error information.</span></span> <span data-ttu-id="65bbb-134">他のほとんどの MAPI 呼び出しとは異なり、戻り値の意味は、失敗した初期化の特定の手順に対応するために厳密に定義されます。</span><span class="sxs-lookup"><span data-stu-id="65bbb-134">Unlike most other MAPI calls, the meanings of its return values are strictly defined to correspond to the particular step of the initialization that failed:</span></span> 
  
1. <span data-ttu-id="65bbb-135">パラメーターとフラグをチェックします。</span><span class="sxs-lookup"><span data-stu-id="65bbb-135">Checks parameters and flags.</span></span>
    
    <span data-ttu-id="65bbb-136">MAPI_E_INVALID_PARAMETERまたはMAPI_E_UNKNOWN_FLAGS。</span><span class="sxs-lookup"><span data-stu-id="65bbb-136">MAPI_E_INVALID_PARAMETER or MAPI_E_UNKNOWN_FLAGS.</span></span> <span data-ttu-id="65bbb-137">呼び出し元が無効なパラメーターまたはフラグを渡しました。</span><span class="sxs-lookup"><span data-stu-id="65bbb-137">Caller passed invalid parameter or flag.</span></span>
    
2. <span data-ttu-id="65bbb-138">MAPI で必要なレジストリ キーを初期化し、オペレーティング システムの種類を確認します。</span><span class="sxs-lookup"><span data-stu-id="65bbb-138">Initializes registry keys required by MAPI and confirms the type of operating system.</span></span> <span data-ttu-id="65bbb-139">この手順は、クライアント プロセスが Windows の下でサービスとして実行され、MAPI_NT SERVICE フラグを MAPIINIT_0する **場合にのみMAPIINIT_0** されます。</span><span class="sxs-lookup"><span data-stu-id="65bbb-139">This step only happens if the client process is running as a service under Windows and sets the MAPI_NT SERVICE flag in the **MAPIINIT_0** structure.</span></span> 
    
    <span data-ttu-id="65bbb-140">MAPI_E_TOO_COMPLEX。</span><span class="sxs-lookup"><span data-stu-id="65bbb-140">MAPI_E_TOO_COMPLEX.</span></span> <span data-ttu-id="65bbb-141">呼び出しプロセスはWindowsサービスであり、MAPI で必要なレジストリ キーを初期化できませんでした。</span><span class="sxs-lookup"><span data-stu-id="65bbb-141">The calling process is a Windows service and registry keys required by MAPI could not be initialized.</span></span> 
    
    <span data-ttu-id="65bbb-142">その他の情報は、アプリケーション イベント ログで確認できます。</span><span class="sxs-lookup"><span data-stu-id="65bbb-142">Additional information may be available in the application event log.</span></span>
    
3. <span data-ttu-id="65bbb-143">MAPI と OLE の互換性を確認し、OLE を初期化します。</span><span class="sxs-lookup"><span data-stu-id="65bbb-143">Check for the compatibility of MAPI with OLE, then initialize OLE.</span></span>
    
1. <span data-ttu-id="65bbb-144">OLE と MAPI の現在のバージョン間の互換性を確認します。</span><span class="sxs-lookup"><span data-stu-id="65bbb-144">Checks for compatibility between the current versions of OLE and MAPI.</span></span> 
    
    <span data-ttu-id="65bbb-145">MAPI_E_VERSION。</span><span class="sxs-lookup"><span data-stu-id="65bbb-145">MAPI_E_VERSION.</span></span> <span data-ttu-id="65bbb-146">ワークステーションにインストールされている OLE のバージョンは、このバージョンの MAPI と互換性がありません。</span><span class="sxs-lookup"><span data-stu-id="65bbb-146">The version of OLE installed on the workstation is not compatible with this version of MAPI.</span></span>
    
2. <span data-ttu-id="65bbb-147">OLE を初期化します。</span><span class="sxs-lookup"><span data-stu-id="65bbb-147">Initializes OLE.</span></span> 
    
    <span data-ttu-id="65bbb-148">この手順の間のみ、この関数はここに記載されていないエラー コードを返す場合があります。</span><span class="sxs-lookup"><span data-stu-id="65bbb-148">During this step only, this function can return an error code not listed here.</span></span> <span data-ttu-id="65bbb-149">ここに記載  _されていない_ エラーは、OLE 関数 **CoInitialize からのエラーと見なす必要があります**。</span><span class="sxs-lookup"><span data-stu-id="65bbb-149">Any error  _not_ listed here should be assumed to come from the OLE function **CoInitialize**.</span></span>
    
4. <span data-ttu-id="65bbb-150">プロセスごとのグローバル変数を初期化します。</span><span class="sxs-lookup"><span data-stu-id="65bbb-150">Initializes per-process global variables.</span></span>
    
    <span data-ttu-id="65bbb-151">MAPI_E_SESSION_LIMIT。</span><span class="sxs-lookup"><span data-stu-id="65bbb-151">MAPI_E_SESSION_LIMIT.</span></span> <span data-ttu-id="65bbb-152">MAPI は、現在のプロセスに固有のコンテキストを設定します。</span><span class="sxs-lookup"><span data-stu-id="65bbb-152">MAPI sets up context specific to the current process.</span></span> <span data-ttu-id="65bbb-153">Win16 では、プロセス数が一定の数を超えた場合、または使用可能なメモリが使い果たされた場合はシステム上でエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="65bbb-153">Failures may occur on Win16 if the number of processes exceeds a certain number, or on any system if available memory is exhausted.</span></span>
    
5. <span data-ttu-id="65bbb-154">すべてのプロセスの共有グローバル変数を初期化します。</span><span class="sxs-lookup"><span data-stu-id="65bbb-154">Initializes shared global variables of all processes.</span></span>
    
    <span data-ttu-id="65bbb-155">MAPI_E_NOT_ENOUGH_RESOURCES。</span><span class="sxs-lookup"><span data-stu-id="65bbb-155">MAPI_E_NOT_ENOUGH_RESOURCES.</span></span> <span data-ttu-id="65bbb-156">操作を完了するのに十分なシステム リソースが使用できません。</span><span class="sxs-lookup"><span data-stu-id="65bbb-156">Not enough system resources were available to complete the operation.</span></span>
    
6. <span data-ttu-id="65bbb-157">通知エンジンを初期化し、ウィンドウとそのスレッドを作成します (このフラグで要求された場合MAPI_MULTITHREAD_NOTIFICATIONSします。</span><span class="sxs-lookup"><span data-stu-id="65bbb-157">Initializes the notification engine, creates its window and its thread if requested by the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> 
    
    <span data-ttu-id="65bbb-158">MAPI_E_INVALID_OBJECT。</span><span class="sxs-lookup"><span data-stu-id="65bbb-158">MAPI_E_INVALID_OBJECT.</span></span> <span data-ttu-id="65bbb-159">システム リソースが使い果たされた場合、失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="65bbb-159">May fail if system resources are exhausted.</span></span> 
    
7. <span data-ttu-id="65bbb-160">プロファイル プロバイダーを読み込み、初期化します。</span><span class="sxs-lookup"><span data-stu-id="65bbb-160">Loads and initializes the profile provider.</span></span> <span data-ttu-id="65bbb-161">**MAPIInitialize がプロファイル** データが格納されているレジストリ キーにアクセスできると確認します。</span><span class="sxs-lookup"><span data-stu-id="65bbb-161">Verifies that **MAPIInitialize** can access the registry key where profile data are stored.</span></span> 
    
    <span data-ttu-id="65bbb-162">MAPI_E_NOT_INITIALIZED。</span><span class="sxs-lookup"><span data-stu-id="65bbb-162">MAPI_E_NOT_INITIALIZED.</span></span> <span data-ttu-id="65bbb-163">プロファイル プロバイダーでエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="65bbb-163">The profile provider has encountered an error.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="65bbb-164">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="65bbb-164">MFCMAPI reference</span></span>

<span data-ttu-id="65bbb-165">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="65bbb-165">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="65bbb-166">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="65bbb-166">**File**</span></span>|<span data-ttu-id="65bbb-167">**関数**</span><span class="sxs-lookup"><span data-stu-id="65bbb-167">**Function**</span></span>|<span data-ttu-id="65bbb-168">**コメント**</span><span class="sxs-lookup"><span data-stu-id="65bbb-168">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="65bbb-169">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="65bbb-169">ContentsTableListCtrl.cpp</span></span>  <br/> ||<span data-ttu-id="65bbb-170">MFCMAPI では **、MAPIInitialize** メソッドを使用して、バックグラウンド スレッドで MAPI を初期化して、テーブル処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="65bbb-170">MFCMAPI uses the **MAPIInitialize** method to initialize MAPI on a background thread to do some table processing.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="65bbb-171">関連項目</span><span class="sxs-lookup"><span data-stu-id="65bbb-171">See also</span></span>



<span data-ttu-id="65bbb-172">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="65bbb-172">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

