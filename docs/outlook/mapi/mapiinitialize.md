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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d22c24088960debcd18ccd818dad23656f6a01f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801513"
---
# <a name="mapiinitialize"></a><span data-ttu-id="d99d5-103">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="d99d5-103">MAPIInitialize</span></span>

  
  
<span data-ttu-id="d99d5-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d99d5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d99d5-105">MAPI サブシステムの参照カウントをインクリメントし、MAPI DLL のグローバル データを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d99d5-105">Increments the MAPI subsystem reference count and initializes global data for the MAPI DLL.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d99d5-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="d99d5-106">Header file:</span></span>  <br/> |<span data-ttu-id="d99d5-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="d99d5-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="d99d5-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="d99d5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d99d5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d99d5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d99d5-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d99d5-110">Called by:</span></span>  <br/> |<span data-ttu-id="d99d5-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="d99d5-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPIInitialize(
  LPVOID lpMapiInit
);
```

## <a name="parameters"></a><span data-ttu-id="d99d5-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d99d5-112">Parameters</span></span>

 <span data-ttu-id="d99d5-113">_lpMapiInit_</span><span class="sxs-lookup"><span data-stu-id="d99d5-113">_lpMapiInit_</span></span>
  
> <span data-ttu-id="d99d5-114">[in][MAPIINIT_0](mapiinit_0.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d99d5-114">[in] Pointer to a [MAPIINIT_0](mapiinit_0.md) structure.</span></span> <span data-ttu-id="d99d5-115">_LpMapiInit_パラメーターを NULL に設定することができます。</span><span class="sxs-lookup"><span data-stu-id="d99d5-115">The  _lpMapiInit_ parameter can be set to NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d99d5-116">�߂�l</span><span class="sxs-lookup"><span data-stu-id="d99d5-116">Return value</span></span>

<span data-ttu-id="d99d5-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="d99d5-117">S_OK</span></span> 
  
> <span data-ttu-id="d99d5-118">MAPI サブシステムの初期化に成功しました。</span><span class="sxs-lookup"><span data-stu-id="d99d5-118">The MAPI subsystem was initialized successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d99d5-119">注釈</span><span class="sxs-lookup"><span data-stu-id="d99d5-119">Remarks</span></span>

<span data-ttu-id="d99d5-120">MAPI のサブシステム、および[MAPIUninitialize](mapiuninitialize.md)関数をデクリメントの MAPI リファレンス カウントが**生じます**関数単位の内部参照カウントします。</span><span class="sxs-lookup"><span data-stu-id="d99d5-120">The **MAPIInitialize** function increments the MAPI reference count for the MAPI subsystem, and the [MAPIUninitialize](mapiuninitialize.md) function decrements the internal reference count.</span></span> <span data-ttu-id="d99d5-121">したがって、1 つの関数への呼び出しの数は、他の呼び出しの数に等しくなければなりません。</span><span class="sxs-lookup"><span data-stu-id="d99d5-121">Thus, the number of calls to one function must equal the number of calls to the other.</span></span> <span data-ttu-id="d99d5-122">**生じます**は、MAPI が以前に初期化されていない場合は S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="d99d5-122">**MAPIInitialize** returns S_OK if MAPI has not been previously initialized.</span></span> 
  
<span data-ttu-id="d99d5-123">クライアントまたはサービス プロバイダーは、他のすべての MAPI 呼び出しを行う前に**生じます**を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="d99d5-123">A client or service provider must call **MAPIInitialize** before making any other MAPI call.</span></span> <span data-ttu-id="d99d5-124">これを行うには、障害が発生すると、MAPI_E_NOT_INITIALIZED の値を取得するクライアントまたはサービス プロバイダーの呼び出しです。</span><span class="sxs-lookup"><span data-stu-id="d99d5-124">Failure to do so causes client or service provider calls to return the MAPI_E_NOT_INITIALIZED value.</span></span> 
  
<span data-ttu-id="d99d5-125">**生じます**マルチ スレッド アプリケーションから呼び出すと、次のように宣言されている[MAPIINIT_0](mapiinit_0.md)構造体に、 _lpMapiInit_パラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="d99d5-125">When calling **MAPIInitialize** from a multithreaded application, set the  _lpMapiInit_ parameter to a [MAPIINIT_0](mapiinit_0.md) structure that is declared as follows:</span></span> 
  
 <span data-ttu-id="d99d5-126">**MAPIINIT_0**MAPIINIT = {0, MAPI_MULTITHREAD_NOTIFICATIONS}</span><span class="sxs-lookup"><span data-stu-id="d99d5-126">**MAPIINIT_0** MAPIINIT= { 0, MAPI_MULTITHREAD_NOTIFICATIONS}</span></span> 
  
<span data-ttu-id="d99d5-127">呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d99d5-127">and call:</span></span> 
  
 <span data-ttu-id="d99d5-128">**生じます**(&amp;MAPIINIT)。</span><span class="sxs-lookup"><span data-stu-id="d99d5-128">**MAPIInitialize** (&amp;MAPIINIT);</span></span> 
  
<span data-ttu-id="d99d5-129">この構造体が宣言されると、MAPI は初期化の参照カウントがゼロに達するまで、通知ウィンドウを処理するために別のスレッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="d99d5-129">When this structure is declared, MAPI creates a separate thread to handle the notification window, which continues until the initialize reference count falls to zero.</span></span> <span data-ttu-id="d99d5-130">Windows サービスは、 **ulflags** 、 **MAPIINIT_0**構造体のメンバー MAPI_NT_SERVICE に_lpMapiInit_が指すを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d99d5-130">A Windows service must set the **ulflags** member of the **MAPIINIT_0** structure pointed to by  _lpMapiInit_ to MAPI_NT_SERVICE.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d99d5-131">Win32 **DllMain**関数またはその他の機能を作成するか、スレッドを終了するのには**生じます**かから**MAPIUninitialize**を呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="d99d5-131">You cannot call **MAPIInitialize** or **MAPIUninitialize** from within a Win32 **DllMain** function or any other function that creates or terminates threads.</span></span> <span data-ttu-id="d99d5-132">詳細については、[スレッド セーフであるオブジェクトを使用する](using-thread-safe-objects.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d99d5-132">For more information, see [Using Thread-Safe Objects](using-thread-safe-objects.md).</span></span> 
  
 <span data-ttu-id="d99d5-133">**生じます**が、拡張エラー情報を返しません。</span><span class="sxs-lookup"><span data-stu-id="d99d5-133">**MAPIInitialize** does not return any extended error information.</span></span> <span data-ttu-id="d99d5-134">その他のほとんどの MAPI 呼び出しとは異なり、戻り値の意味は厳密には定義の初期化に失敗した特定の手順に対応します。</span><span class="sxs-lookup"><span data-stu-id="d99d5-134">Unlike most other MAPI calls, the meanings of its return values are strictly defined to correspond to the particular step of the initialization that failed:</span></span> 
  
1. <span data-ttu-id="d99d5-135">パラメーターとフラグをチェックします。</span><span class="sxs-lookup"><span data-stu-id="d99d5-135">Checks parameters and flags.</span></span>
    
    <span data-ttu-id="d99d5-136">MAPI_E_INVALID_PARAMETER または MAPI_E_UNKNOWN_FLAGS です。</span><span class="sxs-lookup"><span data-stu-id="d99d5-136">MAPI_E_INVALID_PARAMETER or MAPI_E_UNKNOWN_FLAGS.</span></span> <span data-ttu-id="d99d5-137">呼び出し元には、無効なパラメーターまたはフラグが渡されます。</span><span class="sxs-lookup"><span data-stu-id="d99d5-137">Caller passed invalid parameter or flag.</span></span>
    
2. <span data-ttu-id="d99d5-138">MAPI によって必要なレジストリ キーを初期化し、オペレーティング システムの種類を確認します。</span><span class="sxs-lookup"><span data-stu-id="d99d5-138">Initializes registry keys required by MAPI and confirms the type of operating system.</span></span> <span data-ttu-id="d99d5-139">この手順は、クライアント プロセスは、windows サービスとして実行されているし、 **MAPIINIT_0**構造体の MAPI_NT サービス フラグを設定する場合にのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="d99d5-139">This step only happens if the client process is running as a service under Windows and sets the MAPI_NT SERVICE flag in the **MAPIINIT_0** structure.</span></span> 
    
    <span data-ttu-id="d99d5-140">MAPI_E_TOO_COMPLEX。</span><span class="sxs-lookup"><span data-stu-id="d99d5-140">MAPI_E_TOO_COMPLEX.</span></span> <span data-ttu-id="d99d5-141">呼び出し元のプロセスは、Windows サービスと、MAPI によって必要なレジストリ キーを初期化できませんでした。</span><span class="sxs-lookup"><span data-stu-id="d99d5-141">The calling process is a Windows service and registry keys required by MAPI could not be initialized.</span></span> 
    
    <span data-ttu-id="d99d5-142">詳細については、アプリケーション イベント ログで使用できる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d99d5-142">Additional information may be available in the application event log.</span></span>
    
3. <span data-ttu-id="d99d5-143">Ole では、MAPI との互換性をチェックし、OLE を初期化します。</span><span class="sxs-lookup"><span data-stu-id="d99d5-143">Check for the compatibility of MAPI with OLE, then initialize OLE.</span></span>
    
1. <span data-ttu-id="d99d5-144">OLE の現在のバージョンと MAPI との互換性をチェックします。</span><span class="sxs-lookup"><span data-stu-id="d99d5-144">Checks for compatibility between the current versions of OLE and MAPI.</span></span> 
    
    <span data-ttu-id="d99d5-145">MAPI_E_VERSION。</span><span class="sxs-lookup"><span data-stu-id="d99d5-145">MAPI_E_VERSION.</span></span> <span data-ttu-id="d99d5-146">ワークステーションにインストールされている OLE のバージョンがこのバージョンの MAPI と互換性のあるされません。</span><span class="sxs-lookup"><span data-stu-id="d99d5-146">The version of OLE installed on the workstation is not compatible with this version of MAPI.</span></span>
    
2. <span data-ttu-id="d99d5-147">OLE を初期化します。</span><span class="sxs-lookup"><span data-stu-id="d99d5-147">Initializes OLE.</span></span> 
    
    <span data-ttu-id="d99d5-148">この手順の場合にのみ、この関数は、記載されていないエラー コードを返すことができます。</span><span class="sxs-lookup"><span data-stu-id="d99d5-148">During this step only, this function can return an error code not listed here.</span></span> <span data-ttu-id="d99d5-149">何らかのエラーが表示_されない_ここでする必要がありますと見なされます、OLE 関数**CoInitialize**に由来します。</span><span class="sxs-lookup"><span data-stu-id="d99d5-149">Any error  _not_ listed here should be assumed to come from the OLE function **CoInitialize**.</span></span>
    
4. <span data-ttu-id="d99d5-150">初期化は、プロセスごとのグローバル変数です。</span><span class="sxs-lookup"><span data-stu-id="d99d5-150">Initializes per-process global variables.</span></span>
    
    <span data-ttu-id="d99d5-151">MAPI_E_SESSION_LIMIT。</span><span class="sxs-lookup"><span data-stu-id="d99d5-151">MAPI_E_SESSION_LIMIT.</span></span> <span data-ttu-id="d99d5-152">MAPI 設定コンテキストを現在のプロセスを特定します。</span><span class="sxs-lookup"><span data-stu-id="d99d5-152">MAPI sets up context specific to the current process.</span></span> <span data-ttu-id="d99d5-153">障害は、可能性がある場合に発生するプロセスの数は、特定の数を超えた場合、Win16 または任意のシステムで使用可能なメモリが不足します。</span><span class="sxs-lookup"><span data-stu-id="d99d5-153">Failures may occur on Win16 if the number of processes exceeds a certain number, or on any system if available memory is exhausted.</span></span>
    
5. <span data-ttu-id="d99d5-154">初期化は、すべてのプロセスのグローバル変数を共有します。</span><span class="sxs-lookup"><span data-stu-id="d99d5-154">Initializes shared global variables of all processes.</span></span>
    
    <span data-ttu-id="d99d5-155">MAPI_E_NOT_ENOUGH_RESOURCES。</span><span class="sxs-lookup"><span data-stu-id="d99d5-155">MAPI_E_NOT_ENOUGH_RESOURCES.</span></span> <span data-ttu-id="d99d5-156">十分なシステム リソースは、操作を完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="d99d5-156">Not enough system resources were available to complete the operation.</span></span>
    
6. <span data-ttu-id="d99d5-157">通知エンジンを初期化、MAPI_MULTITHREAD_NOTIFICATIONS フラグによって要求された場合、そのウィンドウとそのスレッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="d99d5-157">Initializes the notification engine, creates its window and its thread if requested by the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> 
    
    <span data-ttu-id="d99d5-158">MAPI_E_INVALID_OBJECT。</span><span class="sxs-lookup"><span data-stu-id="d99d5-158">MAPI_E_INVALID_OBJECT.</span></span> <span data-ttu-id="d99d5-159">システム リソースが使い果たされる場合があります。</span><span class="sxs-lookup"><span data-stu-id="d99d5-159">May fail if system resources are exhausted.</span></span> 
    
7. <span data-ttu-id="d99d5-160">読み込み、プロファイル プロバイダーを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d99d5-160">Loads and initializes the profile provider.</span></span> <span data-ttu-id="d99d5-161">**生じます**が、プロファイル データが格納されているレジストリ キーにアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d99d5-161">Verifies that **MAPIInitialize** can access the registry key where profile data are stored.</span></span> 
    
    <span data-ttu-id="d99d5-162">MAPI_E_NOT_INITIALIZED。</span><span class="sxs-lookup"><span data-stu-id="d99d5-162">MAPI_E_NOT_INITIALIZED.</span></span> <span data-ttu-id="d99d5-163">プロファイル プロバイダー エラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="d99d5-163">The profile provider has encountered an error.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="d99d5-164">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="d99d5-164">MFCMAPI reference</span></span>

<span data-ttu-id="d99d5-165">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="d99d5-165">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d99d5-166">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="d99d5-166">**File**</span></span>|<span data-ttu-id="d99d5-167">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="d99d5-167">**Function**</span></span>|<span data-ttu-id="d99d5-168">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="d99d5-168">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d99d5-169">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="d99d5-169">ContentsTableListCtrl.cpp</span></span>  <br/> ||<span data-ttu-id="d99d5-170">MFCMAPI では、いくつかのテーブルの処理を実行するのにバック グラウンド スレッドで MAPI を初期化するために**生じます**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d99d5-170">MFCMAPI uses the **MAPIInitialize** method to initialize MAPI on a background thread to do some table processing.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d99d5-171">関連項目</span><span class="sxs-lookup"><span data-stu-id="d99d5-171">See also</span></span>



<span data-ttu-id="d99d5-172">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="d99d5-172">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

