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
# <a name="mapiinitialize"></a><span data-ttu-id="6950c-103">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="6950c-103">MAPIInitialize</span></span>

  
  
<span data-ttu-id="6950c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6950c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6950c-105">mapi サブシステムの参照カウントを増分し、mapi DLL のグローバルデータを初期化します。</span><span class="sxs-lookup"><span data-stu-id="6950c-105">Increments the MAPI subsystem reference count and initializes global data for the MAPI DLL.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6950c-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="6950c-106">Header file:</span></span>  <br/> |<span data-ttu-id="6950c-107">mapix</span><span class="sxs-lookup"><span data-stu-id="6950c-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="6950c-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="6950c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6950c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6950c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6950c-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="6950c-110">Called by:</span></span>  <br/> |<span data-ttu-id="6950c-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="6950c-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPIInitialize(
  LPVOID lpMapiInit
);
```

## <a name="parameters"></a><span data-ttu-id="6950c-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6950c-112">Parameters</span></span>

 <span data-ttu-id="6950c-113">_lpMapiInit_</span><span class="sxs-lookup"><span data-stu-id="6950c-113">_lpMapiInit_</span></span>
  
> <span data-ttu-id="6950c-114">順番[MAPIINIT_0](mapiinit_0.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6950c-114">[in] Pointer to a [MAPIINIT_0](mapiinit_0.md) structure.</span></span> <span data-ttu-id="6950c-115">_lpMapiInit_パラメーターは NULL に設定できます。</span><span class="sxs-lookup"><span data-stu-id="6950c-115">The  _lpMapiInit_ parameter can be set to NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6950c-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="6950c-116">Return value</span></span>

<span data-ttu-id="6950c-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="6950c-117">S_OK</span></span> 
  
> <span data-ttu-id="6950c-118">MAPI サブシステムは正常に初期化されました。</span><span class="sxs-lookup"><span data-stu-id="6950c-118">The MAPI subsystem was initialized successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6950c-119">注釈</span><span class="sxs-lookup"><span data-stu-id="6950c-119">Remarks</span></span>

<span data-ttu-id="6950c-120">**MAPIInitialize**関数は mapi サブシステムの mapi 参照カウントをインクリメントし、 [MAPIUninitialize](mapiuninitialize.md)関数は内部参照カウントをデクリメントします。</span><span class="sxs-lookup"><span data-stu-id="6950c-120">The **MAPIInitialize** function increments the MAPI reference count for the MAPI subsystem, and the [MAPIUninitialize](mapiuninitialize.md) function decrements the internal reference count.</span></span> <span data-ttu-id="6950c-121">そのため、1つの関数への呼び出しの数は、もう一方への呼び出しの数と等しくなければなりません。</span><span class="sxs-lookup"><span data-stu-id="6950c-121">Thus, the number of calls to one function must equal the number of calls to the other.</span></span> <span data-ttu-id="6950c-122">MAPI が以前に初期化されていない場合、 **MAPIInitialize**は S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="6950c-122">**MAPIInitialize** returns S_OK if MAPI has not been previously initialized.</span></span> 
  
<span data-ttu-id="6950c-123">クライアントまたはサービスプロバイダーは、他の MAPI 呼び出しを行う前に**MAPIInitialize**を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="6950c-123">A client or service provider must call **MAPIInitialize** before making any other MAPI call.</span></span> <span data-ttu-id="6950c-124">失敗すると、クライアントまたはサービスプロバイダーの呼び出しが MAPI_E_NOT_INITIALIZED の値を返します。</span><span class="sxs-lookup"><span data-stu-id="6950c-124">Failure to do so causes client or service provider calls to return the MAPI_E_NOT_INITIALIZED value.</span></span> 
  
<span data-ttu-id="6950c-125">マルチスレッドアプリケーションから**MAPIInitialize**を呼び出すときは、 _lpMapiInit_パラメーターを次のように宣言されている[MAPIINIT_0](mapiinit_0.md)構造に設定します。</span><span class="sxs-lookup"><span data-stu-id="6950c-125">When calling **MAPIInitialize** from a multithreaded application, set the  _lpMapiInit_ parameter to a [MAPIINIT_0](mapiinit_0.md) structure that is declared as follows:</span></span> 
  
 <span data-ttu-id="6950c-126">**MAPIINIT_0**MAPIINIT = {0, MAPI_MULTITHREAD_NOTIFICATIONS}</span><span class="sxs-lookup"><span data-stu-id="6950c-126">**MAPIINIT_0** MAPIINIT= { 0, MAPI_MULTITHREAD_NOTIFICATIONS}</span></span> 
  
<span data-ttu-id="6950c-127">そして、次のように呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6950c-127">and call:</span></span> 
  
 <span data-ttu-id="6950c-128">**MAPIInitialize**(&amp;MAPIINIT);</span><span class="sxs-lookup"><span data-stu-id="6950c-128">**MAPIInitialize** (&amp;MAPIINIT);</span></span> 
  
<span data-ttu-id="6950c-129">この構造体を宣言すると、MAPI は通知ウィンドウを処理する別のスレッドを作成します。これは、初期化の参照カウントが0になるまで続行します。</span><span class="sxs-lookup"><span data-stu-id="6950c-129">When this structure is declared, MAPI creates a separate thread to handle the notification window, which continues until the initialize reference count falls to zero.</span></span> <span data-ttu-id="6950c-130">Windows サービスでは、 _lpMapiInit_によって参照されている**MAPIINIT_0**構造体の**ulflags**メンバーを MAPI_NT_SERVICE に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6950c-130">A Windows service must set the **ulflags** member of the **MAPIINIT_0** structure pointed to by  _lpMapiInit_ to MAPI_NT_SERVICE.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6950c-131">**MAPIInitialize**または**MAPIUninitialize**は、Win32 **DllMain**関数から、またはスレッドを作成または終了する他の関数内から呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="6950c-131">You cannot call **MAPIInitialize** or **MAPIUninitialize** from within a Win32 **DllMain** function or any other function that creates or terminates threads.</span></span> <span data-ttu-id="6950c-132">詳細については、「[スレッドセーフオブジェクトの使用](using-thread-safe-objects.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6950c-132">For more information, see [Using Thread-Safe Objects](using-thread-safe-objects.md).</span></span> 
  
 <span data-ttu-id="6950c-133">**MAPIInitialize**では、拡張エラー情報は返されません。</span><span class="sxs-lookup"><span data-stu-id="6950c-133">**MAPIInitialize** does not return any extended error information.</span></span> <span data-ttu-id="6950c-134">他のほとんどの MAPI 呼び出しとは異なり、戻り値の意味は、エラーが発生した初期化の特定の手順に対応するように厳密に定義されます。</span><span class="sxs-lookup"><span data-stu-id="6950c-134">Unlike most other MAPI calls, the meanings of its return values are strictly defined to correspond to the particular step of the initialization that failed:</span></span> 
  
1. <span data-ttu-id="6950c-135">パラメーターとフラグをチェックします。</span><span class="sxs-lookup"><span data-stu-id="6950c-135">Checks parameters and flags.</span></span>
    
    <span data-ttu-id="6950c-136">MAPI_E_INVALID_PARAMETER または MAPI_E_UNKNOWN_FLAGS。</span><span class="sxs-lookup"><span data-stu-id="6950c-136">MAPI_E_INVALID_PARAMETER or MAPI_E_UNKNOWN_FLAGS.</span></span> <span data-ttu-id="6950c-137">発信者が無効なパラメーターまたはフラグを渡しました。</span><span class="sxs-lookup"><span data-stu-id="6950c-137">Caller passed invalid parameter or flag.</span></span>
    
2. <span data-ttu-id="6950c-138">MAPI に必要なレジストリキーを初期化し、オペレーティングシステムの種類を確認します。</span><span class="sxs-lookup"><span data-stu-id="6950c-138">Initializes registry keys required by MAPI and confirms the type of operating system.</span></span> <span data-ttu-id="6950c-139">この手順は、クライアントプロセスが Windows でサービスとして実行されていて、 **MAPIINIT_0**構造の MAPI_NT サービスフラグを設定している場合にのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="6950c-139">This step only happens if the client process is running as a service under Windows and sets the MAPI_NT SERVICE flag in the **MAPIINIT_0** structure.</span></span> 
    
    <span data-ttu-id="6950c-140">MAPI_E_TOO_COMPLEX。</span><span class="sxs-lookup"><span data-stu-id="6950c-140">MAPI_E_TOO_COMPLEX.</span></span> <span data-ttu-id="6950c-141">呼び出し元のプロセスは Windows サービスであり、MAPI に必要なレジストリキーを初期化できませんでした。</span><span class="sxs-lookup"><span data-stu-id="6950c-141">The calling process is a Windows service and registry keys required by MAPI could not be initialized.</span></span> 
    
    <span data-ttu-id="6950c-142">アプリケーションイベントログで追加情報を入手できる場合があります。</span><span class="sxs-lookup"><span data-stu-id="6950c-142">Additional information may be available in the application event log.</span></span>
    
3. <span data-ttu-id="6950c-143">MAPI と ole が互換性があるかどうかを確認し、ole を初期化します。</span><span class="sxs-lookup"><span data-stu-id="6950c-143">Check for the compatibility of MAPI with OLE, then initialize OLE.</span></span>
    
1. <span data-ttu-id="6950c-144">現在のバージョンの OLE と MAPI の間に互換性があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="6950c-144">Checks for compatibility between the current versions of OLE and MAPI.</span></span> 
    
    <span data-ttu-id="6950c-145">MAPI_E_VERSION。</span><span class="sxs-lookup"><span data-stu-id="6950c-145">MAPI_E_VERSION.</span></span> <span data-ttu-id="6950c-146">ワークステーションにインストールされている OLE のバージョンは、このバージョンの MAPI と互換性がありません。</span><span class="sxs-lookup"><span data-stu-id="6950c-146">The version of OLE installed on the workstation is not compatible with this version of MAPI.</span></span>
    
2. <span data-ttu-id="6950c-147">OLE を初期化します。</span><span class="sxs-lookup"><span data-stu-id="6950c-147">Initializes OLE.</span></span> 
    
    <span data-ttu-id="6950c-148">この手順では、この関数では、ここに記載されていないエラーコードを返すことができます。</span><span class="sxs-lookup"><span data-stu-id="6950c-148">During this step only, this function can return an error code not listed here.</span></span> <span data-ttu-id="6950c-149">ここに記載さ_れていない_エラーは、OLE 関数**CoInitialize**からのものであることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="6950c-149">Any error  _not_ listed here should be assumed to come from the OLE function **CoInitialize**.</span></span>
    
4. <span data-ttu-id="6950c-150">プロセスごとのグローバル変数を初期化します。</span><span class="sxs-lookup"><span data-stu-id="6950c-150">Initializes per-process global variables.</span></span>
    
    <span data-ttu-id="6950c-151">MAPI_E_SESSION_LIMIT。</span><span class="sxs-lookup"><span data-stu-id="6950c-151">MAPI_E_SESSION_LIMIT.</span></span> <span data-ttu-id="6950c-152">MAPI は、現在のプロセスに固有のコンテキストを設定します。</span><span class="sxs-lookup"><span data-stu-id="6950c-152">MAPI sets up context specific to the current process.</span></span> <span data-ttu-id="6950c-153">プロセスの数が特定の数を超えた場合、または使用可能なメモリが不足している場合は、Win16 でエラーが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="6950c-153">Failures may occur on Win16 if the number of processes exceeds a certain number, or on any system if available memory is exhausted.</span></span>
    
5. <span data-ttu-id="6950c-154">すべてのプロセスの共有グローバル変数を初期化します。</span><span class="sxs-lookup"><span data-stu-id="6950c-154">Initializes shared global variables of all processes.</span></span>
    
    <span data-ttu-id="6950c-155">MAPI_E_NOT_ENOUGH_RESOURCES。</span><span class="sxs-lookup"><span data-stu-id="6950c-155">MAPI_E_NOT_ENOUGH_RESOURCES.</span></span> <span data-ttu-id="6950c-156">システムリソースが不足しているため、操作を完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="6950c-156">Not enough system resources were available to complete the operation.</span></span>
    
6. <span data-ttu-id="6950c-157">通知エンジンを初期化し、MAPI_MULTITHREAD_NOTIFICATIONS フラグによって要求された場合は、ウィンドウとそのスレッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="6950c-157">Initializes the notification engine, creates its window and its thread if requested by the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> 
    
    <span data-ttu-id="6950c-158">MAPI_E_INVALID_OBJECT。</span><span class="sxs-lookup"><span data-stu-id="6950c-158">MAPI_E_INVALID_OBJECT.</span></span> <span data-ttu-id="6950c-159">システムリソースが不足すると、エラーが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="6950c-159">May fail if system resources are exhausted.</span></span> 
    
7. <span data-ttu-id="6950c-160">プロファイルプロバイダーを読み込んで初期化します。</span><span class="sxs-lookup"><span data-stu-id="6950c-160">Loads and initializes the profile provider.</span></span> <span data-ttu-id="6950c-161">**MAPIInitialize**がプロファイルデータが格納されているレジストリキーにアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6950c-161">Verifies that **MAPIInitialize** can access the registry key where profile data are stored.</span></span> 
    
    <span data-ttu-id="6950c-162">MAPI_E_NOT_INITIALIZED。</span><span class="sxs-lookup"><span data-stu-id="6950c-162">MAPI_E_NOT_INITIALIZED.</span></span> <span data-ttu-id="6950c-163">プロファイルプロバイダーでエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="6950c-163">The profile provider has encountered an error.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="6950c-164">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="6950c-164">MFCMAPI reference</span></span>

<span data-ttu-id="6950c-165">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6950c-165">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6950c-166">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="6950c-166">**File**</span></span>|<span data-ttu-id="6950c-167">**関数**</span><span class="sxs-lookup"><span data-stu-id="6950c-167">**Function**</span></span>|<span data-ttu-id="6950c-168">**コメント**</span><span class="sxs-lookup"><span data-stu-id="6950c-168">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6950c-169">ContentsTableListCtrl</span><span class="sxs-lookup"><span data-stu-id="6950c-169">ContentsTableListCtrl.cpp</span></span>  <br/> ||<span data-ttu-id="6950c-170">mfcmapi は、 **MAPIInitialize**メソッドを使用して、バックグラウンドスレッドで MAPI を初期化し、一部のテーブル処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="6950c-170">MFCMAPI uses the **MAPIInitialize** method to initialize MAPI on a background thread to do some table processing.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6950c-171">関連項目</span><span class="sxs-lookup"><span data-stu-id="6950c-171">See also</span></span>



<span data-ttu-id="6950c-172">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="6950c-172">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

