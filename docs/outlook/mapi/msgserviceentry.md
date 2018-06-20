---
title: MSGSERVICEENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MSGSERVICEENTRY
api_type:
- COM
ms.assetid: 655774a6-588c-44c7-903b-4497b7eccbc2
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 9af170f3445757eb96b9fe78c7cbea2c29ef4612
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801673"
---
# <a name="msgserviceentry"></a><span data-ttu-id="c5a20-103">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="c5a20-103">MSGSERVICEENTRY</span></span>

  
  
<span data-ttu-id="c5a20-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c5a20-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c5a20-105">メッセージ サービスの構成をサポートするメッセージ サービスのエントリ ポイント関数のプロトタイプを定義します。</span><span class="sxs-lookup"><span data-stu-id="c5a20-105">Defines a prototype for a message service entry point function to support message service configuration.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c5a20-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="c5a20-106">Header file:</span></span>  <br/> |<span data-ttu-id="c5a20-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="c5a20-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="c5a20-108">によって実装される関数の定義:</span><span class="sxs-lookup"><span data-stu-id="c5a20-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="c5a20-109">メッセージ サービス</span><span class="sxs-lookup"><span data-stu-id="c5a20-109">Message services</span></span>  <br/> |
|<span data-ttu-id="c5a20-110">によって呼び出される関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="c5a20-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="c5a20-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="c5a20-111">MAPI</span></span>  <br/> |
   
```cpp
HRESULT MSGSERVICEENTRY(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulContext,
  ULONG cValues,
  LPSPropValue lpProps,
  LPPROVIDERADMIN lpProviderAdmin,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a><span data-ttu-id="c5a20-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="c5a20-112">Parameters</span></span>

 <span data-ttu-id="c5a20-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="c5a20-113">_hInstance_</span></span>
  
> <span data-ttu-id="c5a20-114">[in]サービス providerDLL のインスタンスのハンドル。</span><span class="sxs-lookup"><span data-stu-id="c5a20-114">[in] Handle of the instance of the service providerDLL.</span></span> <span data-ttu-id="c5a20-115">ハンドルは通常、リソースを取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="c5a20-115">The handle is typically used to retrieve resources.</span></span> 
    
 <span data-ttu-id="c5a20-116">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="c5a20-116">_lpMalloc_</span></span>
  
> <span data-ttu-id="c5a20-117">[in]OLE **IMalloc**インターフェイスを公開すること、メモリ アロケーター オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c5a20-117">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="c5a20-118">メッセージ サービスは、 **IStream**などの特定のインターフェイスを使用する場合、この割り当て方法を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5a20-118">The message service may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="c5a20-119">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="c5a20-119">_lpMAPISup_</span></span>
  
> <span data-ttu-id="c5a20-120">[in]ポインター、 [IMAPISupport: IUnknown](imapisupportiunknown.md)インターフェイスの実装です。</span><span class="sxs-lookup"><span data-stu-id="c5a20-120">[in] Pointer to an [IMAPISupport : IUnknown](imapisupportiunknown.md) interface implementation.</span></span> 
    
 <span data-ttu-id="c5a20-121">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c5a20-121">_ulUIParam_</span></span>
  
> <span data-ttu-id="c5a20-122">[in]関数にユーザー インターフェイスの情報を渡すための実装に固有の値です。</span><span class="sxs-lookup"><span data-stu-id="c5a20-122">[in] An implementation-specific value used for passing user interface information to a function or zero.</span></span> <span data-ttu-id="c5a20-123">_UlUIParam_パラメーターの構成] ダイアログ ボックスの親ウィンドウのハンドル、HWND 型にキャスト、ULONG_PTR) の種類の。</span><span class="sxs-lookup"><span data-stu-id="c5a20-123">The  _ulUIParam_ parameter is the parent window handle for the configuration dialog box and is of type HWND (cast to a ULONG_PTR).</span></span> <span data-ttu-id="c5a20-124">0 の値は、親ウィンドウがないことを示します。</span><span class="sxs-lookup"><span data-stu-id="c5a20-124">A value of zero indicates that there is no parent window.</span></span> 
    
 <span data-ttu-id="c5a20-125">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c5a20-125">_ulFlags_</span></span>
  
> <span data-ttu-id="c5a20-126">[in]サービスの関数のエントリのオプションを示すフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="c5a20-126">[in] Bitmask of flags indicating options for the service entry function.</span></span> <span data-ttu-id="c5a20-127">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="c5a20-127">The following flags can be set:</span></span>
    
<span data-ttu-id="c5a20-128">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c5a20-128">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c5a20-129">渡された文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="c5a20-129">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="c5a20-130">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="c5a20-130">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="c5a20-131">MSG_SERVICE_UI_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="c5a20-131">MSG_SERVICE_UI_READ_ONLY</span></span> 
  
> <span data-ttu-id="c5a20-132">サービスの構成のユーザー インターフェイスは現在の構成を表示する必要がありますが、それを変更するユーザーを許可しません。</span><span class="sxs-lookup"><span data-stu-id="c5a20-132">The service's configuration user interface should display the current configuration but not allow the user to change it.</span></span> 
    
<span data-ttu-id="c5a20-133">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="c5a20-133">SERVICE_UI_ALLOWED</span></span> 
  
> <span data-ttu-id="c5a20-134">必要な場合に表示される、[構成] ダイアログ ボックスを許可します。</span><span class="sxs-lookup"><span data-stu-id="c5a20-134">Permits a configuration dialog box to be displayed if necessary.</span></span> <span data-ttu-id="c5a20-135">SERVICE_UI_ALLOWED フラグを設定すると、 _lpProps_プロパティの値の配列が空または無効な構成が含まれていない場合にのみ、ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c5a20-135">When the SERVICE_UI_ALLOWED flag is set, the dialog box should be displayed only if the  _lpProps_ property value array is empty or does not contain a valid configuration.</span></span> <span data-ttu-id="c5a20-136">SERVICE_UI_ALLOWED が設定されていない場合、SERVICE_UI_ALWAYS フラグが設定されている場合、ダイアログ ボックスが表示されますも可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c5a20-136">If SERVICE_UI_ALLOWED is not set, a dialog box might still be displayed if the SERVICE_UI_ALWAYS flag is set.</span></span> 
    
<span data-ttu-id="c5a20-137">UI_CURRENT_PROVIDER_FIRST</span><span class="sxs-lookup"><span data-stu-id="c5a20-137">UI_CURRENT_PROVIDER_FIRST</span></span> 
  
> <span data-ttu-id="c5a20-138">その他のダイアログ ボックスの上にアクティブなプロバイダーの構成] ダイアログ ボックスを表示するように要求します。</span><span class="sxs-lookup"><span data-stu-id="c5a20-138">Requests that the configuration dialog box for the active provider be displayed on top of other dialog boxes.</span></span> 
    
<span data-ttu-id="c5a20-139">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="c5a20-139">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="c5a20-140">メッセージ サービスの構成] ダイアログ ボックスを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5a20-140">Requires the message service to display a configuration dialog box.</span></span> <span data-ttu-id="c5a20-141">SERVICE_UI_ALWAYS フラグが設定されていない場合、SERVICE_UI_ALLOWED フラグが設定されていて有効な構成情報は、 _lpProps_プロパティの値の配列から、[構成] ダイアログ ボックスが表示されますも可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c5a20-141">If the SERVICE_UI_ALWAYS flag is not set, a configuration dialog box might still be displayed if the SERVICE_UI_ALLOWED flag is set and valid configuration information is not available from the  _lpProps_ property value array.</span></span> <span data-ttu-id="c5a20-142">ユーザー インターフェイスを表示するを許可するには、SERVICE_UI_ALLOWED または SERVICE_UI_ALWAYS のいずれかを設定しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="c5a20-142">Either SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS must be set to allow a user interface to be displayed.</span></span> 
    
 <span data-ttu-id="c5a20-143">_ulContext_</span><span class="sxs-lookup"><span data-stu-id="c5a20-143">_ulContext_</span></span>
  
> <span data-ttu-id="c5a20-144">[in]MAPI を現在実行している構成の処理。</span><span class="sxs-lookup"><span data-stu-id="c5a20-144">[in] The configuration operation that MAPI is currently performing.</span></span> <span data-ttu-id="c5a20-145">_UlContext_パラメーターは、次の値のいずれかに含まれます。</span><span class="sxs-lookup"><span data-stu-id="c5a20-145">The  _ulContext_ parameter will contain one of the following values:</span></span> 
    
<span data-ttu-id="c5a20-146">MSG_SERVICE_CONFIGURE</span><span class="sxs-lookup"><span data-stu-id="c5a20-146">MSG_SERVICE_CONFIGURE</span></span> 
  
> <span data-ttu-id="c5a20-147">サービスの構成には、プロファイルに変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5a20-147">Changes to the service's configuration should be made in the profile.</span></span> <span data-ttu-id="c5a20-148">SERVICE_UI_ALWAYS フラグが設定されている場合、サービスは、[構成] ダイアログ ボックスに表示されます。</span><span class="sxs-lookup"><span data-stu-id="c5a20-148">If the SERVICE_UI_ALWAYS flag is set, the service should display its configuration dialog box.</span></span> <span data-ttu-id="c5a20-149">ダイアログ ボックスは、SERVICE_UI_ALLOWED フラグが設定されており、 _lpProps_パラメーターが空か、無効な構成データが含まれていない場合にも表示されます。</span><span class="sxs-lookup"><span data-stu-id="c5a20-149">The dialog box should also be displayed if the SERVICE_UI_ALLOWED flag is set and the  _lpProps_ parameter is empty or does not contain valid configuration data.</span></span> <span data-ttu-id="c5a20-150">_LpProps_に有効なデータが含まれている場合は、ダイアログ ボックスを表示する必要があり、サービスは、構成の変更を行うためこのデータを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5a20-150">If  _lpProps_ contains valid data, no dialog box should be displayed and the service should use this data for making the configuration change.</span></span> 
    
<span data-ttu-id="c5a20-151">MSG_SERVICE_CREATE</span><span class="sxs-lookup"><span data-stu-id="c5a20-151">MSG_SERVICE_CREATE</span></span> 
  
> <span data-ttu-id="c5a20-152">サービスは、プロファイルに追加されます。</span><span class="sxs-lookup"><span data-stu-id="c5a20-152">The service is being added to a profile.</span></span> <span data-ttu-id="c5a20-153">SERVICE_UI_ALWAYS または SERVICE_UI_ALLOWED のいずれかのフラグが設定されている場合、サービスは、[構成] ダイアログ ボックスに表示されます。</span><span class="sxs-lookup"><span data-stu-id="c5a20-153">If either the SERVICE_UI_ALWAYS or SERVICE_UI_ALLOWED flag is set, the service should display its configuration dialog box.</span></span> <span data-ttu-id="c5a20-154">どちらのフラグが設定されている場合、サービスが失敗する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5a20-154">If neither flag is set, the service should fail.</span></span> 
    
<span data-ttu-id="c5a20-155">MSG_SERVICE_DELETE</span><span class="sxs-lookup"><span data-stu-id="c5a20-155">MSG_SERVICE_DELETE</span></span> 
  
> <span data-ttu-id="c5a20-156">プロファイルからサービスを削除しています。</span><span class="sxs-lookup"><span data-stu-id="c5a20-156">The service is being removed from a profile.</span></span> <span data-ttu-id="c5a20-157">このイベントを受け取ると、サービスは、S_OK を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5a20-157">After receiving this event, the service should return S_OK.</span></span>
    
<span data-ttu-id="c5a20-158">MSG_SERVICE_INSTALL</span><span class="sxs-lookup"><span data-stu-id="c5a20-158">MSG_SERVICE_INSTALL</span></span> 
  
> <span data-ttu-id="c5a20-159">サービスは、ネットワーク、フロッピー ディスク、またはその他の外部メディアからユーザーのワークステーションにインストールされました。</span><span class="sxs-lookup"><span data-stu-id="c5a20-159">The service has been installed to the user's workstation from a network, floppy disk, or other external medium.</span></span> <span data-ttu-id="c5a20-160">このイベントを受信した後、サービスは、通常、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="c5a20-160">After receiving this event, the service usually returns S_OK.</span></span> 
    
<span data-ttu-id="c5a20-161">MSG_SERVICE_PROVIDER_CREATE</span><span class="sxs-lookup"><span data-stu-id="c5a20-161">MSG_SERVICE_PROVIDER_CREATE</span></span> 
  
> <span data-ttu-id="c5a20-162">サービスがプロバイダーの追加のインスタンスを作成することを要求します。</span><span class="sxs-lookup"><span data-stu-id="c5a20-162">Requests that the service create an additional instance of a provider.</span></span> <span data-ttu-id="c5a20-163">サービスは、この操作をサポートする場合は、 [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md)をに呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5a20-163">If the service supports this operation, it should call [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md).</span></span> <span data-ttu-id="c5a20-164">サービスがこの操作をサポートしていない場合は、MAPI_E_NO_SUPPORT を返すことです。</span><span class="sxs-lookup"><span data-stu-id="c5a20-164">If the service does not support this operation, it can return MAPI_E_NO_SUPPORT.</span></span> 
    
<span data-ttu-id="c5a20-165">MSG_SERVICE_PROVIDER_DELETE</span><span class="sxs-lookup"><span data-stu-id="c5a20-165">MSG_SERVICE_PROVIDER_DELETE</span></span> 
  
> <span data-ttu-id="c5a20-166">サービスがプロバイダーのインスタンスを削除することを要求します。</span><span class="sxs-lookup"><span data-stu-id="c5a20-166">Requests that the service delete a provider instance.</span></span> <span data-ttu-id="c5a20-167">サービスは、この操作をサポートする場合は、 [IProviderAdmin::DeleteProvider](iprovideradmin-deleteprovider.md)をに呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5a20-167">If the service supports this operation, it should call [IProviderAdmin::DeleteProvider](iprovideradmin-deleteprovider.md).</span></span> <span data-ttu-id="c5a20-168">サービスがこの操作をサポートしていない場合は、MAPI_E_NO_SUPPORT を返すことです。</span><span class="sxs-lookup"><span data-stu-id="c5a20-168">If the service does not support this operation, it can return MAPI_E_NO_SUPPORT.</span></span>
    
<span data-ttu-id="c5a20-169">MSG_SERVICE_UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="c5a20-169">MSG_SERVICE_UNINSTALL</span></span> 
  
> <span data-ttu-id="c5a20-170">サービスを削除しています。</span><span class="sxs-lookup"><span data-stu-id="c5a20-170">The service is being removed.</span></span> <span data-ttu-id="c5a20-171">このイベントを受信した後、サービスはサービスを終了し、成功した場合の値を返す前に行う必要があります任意のクリーンアップ タスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="c5a20-171">After receiving this event, the service can perform any cleanup tasks that should be done before the service ends and then return with a success value.</span></span> <span data-ttu-id="c5a20-172">ユーザーは、削除をキャンセルした場合、サービスは、MAPI_E_USER_CANCEL を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5a20-172">If the user cancels the removal, the service should return MAPI_E_USER_CANCEL.</span></span> 
    
 <span data-ttu-id="c5a20-173">_あう_</span><span class="sxs-lookup"><span data-stu-id="c5a20-173">_cValues_</span></span>
  
> <span data-ttu-id="c5a20-174">[in]_LpProps_パラメーターが指す配列内のプロパティ値の数です。</span><span class="sxs-lookup"><span data-stu-id="c5a20-174">[in] Count of property values in the array pointed to by the  _lpProps_ parameter.</span></span> <span data-ttu-id="c5a20-175">_あう_パラメーターの値は、プロパティの値を渡すことは、MAPI がない場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="c5a20-175">The value of the  _cValues_ parameter is zero if MAPI is passing no property values.</span></span> 
    
 <span data-ttu-id="c5a20-176">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="c5a20-176">_lpProps_</span></span>
  
> <span data-ttu-id="c5a20-177">[in][SPropValue](spropvalue.md)の省略可能な配列へのポインターでは、メッセージ サービスを構成する際にこの関数を使用するプロバイダーでサポートされているプロパティの値を示す構造体します。</span><span class="sxs-lookup"><span data-stu-id="c5a20-177">[in] Pointer to an optional array of [SPropValue](spropvalue.md) structures indicating values for provider-supported properties that the function will use in configuring the message service.</span></span> <span data-ttu-id="c5a20-178">関数は、 _ulContext_パラメーターを MSG_SERVICE_CONFIGURE に設定されている場合にだけこのパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="c5a20-178">The function only uses this parameter if the  _ulContext_ parameter is set to MSG_SERVICE_CONFIGURE.</span></span> <span data-ttu-id="c5a20-179">このパラメーターは、個人用アドレス帳サービスなどのファイル ・ ベースのサービスのファイルへのパスを渡すに通常使用されます。</span><span class="sxs-lookup"><span data-stu-id="c5a20-179">This parameter is commonly used to pass the path to a file for a file-based service, such as a personal address book service.</span></span> <span data-ttu-id="c5a20-180">_UlFlags_パラメーターに MSG_SERVICE_CONFIGURE フラグが渡されない場合、 _lpProps_パラメーターは 0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5a20-180">If the MSG_SERVICE_CONFIGURE flag is not passed in the  _ulFlags_ parameter, the  _lpProps_ parameter must be zero.</span></span> 
    
 <span data-ttu-id="c5a20-181">_lpProviderAdmin_</span><span class="sxs-lookup"><span data-stu-id="c5a20-181">_lpProviderAdmin_</span></span>
  
> <span data-ttu-id="c5a20-182">[in]関数は、現在のメッセージ サービスで特定のプロバイダーのプロファイル セクションを検索に使用できる[IProviderAdmin:IUnknown](iprovideradminiunknown.md)インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c5a20-182">[in] Pointer to an [IProviderAdmin:IUnknown](iprovideradminiunknown.md) interface that the function can use to locate profile sections for a specific provider in the current message service.</span></span> 
    
 <span data-ttu-id="c5a20-183">_lppMapiError_</span><span class="sxs-lookup"><span data-stu-id="c5a20-183">_lppMapiError_</span></span>
  
> <span data-ttu-id="c5a20-184">[out][MAPIERROR](mapierror.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c5a20-184">[out] Pointer to a [MAPIERROR](mapierror.md) structure.</span></span> <span data-ttu-id="c5a20-185">[MAPIAllocateBuffer](mapiallocatebuffer.md)関数では、構造体が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="c5a20-185">The structure is allocated with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> <span data-ttu-id="c5a20-186">ほとんどの構造体は_lpszError_のメンバーで有効なエラー メッセージ文字列を含むすべてのメンバーはオプションですが。</span><span class="sxs-lookup"><span data-stu-id="c5a20-186">All members are optional, although most structures will contain a valid error message string in the  _lpszError_ member.</span></span> <span data-ttu-id="c5a20-187">構造体の_lpszComponent_または_lpszError_のメンバーが存在する場合は、基本構造に[MAPIFreeBuffer](mapifreebuffer.md)を 1 回の呼び出しによって、メモリを解放最終的にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5a20-187">If the  _lpszComponent_ or  _lpszError_ members of the structure are present, their memory must eventually be freed by a single call to [MAPIFreeBuffer](mapifreebuffer.md) on the base structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c5a20-188">�߂�l</span><span class="sxs-lookup"><span data-stu-id="c5a20-188">Return value</span></span>

<span data-ttu-id="c5a20-189">S_OK</span><span class="sxs-lookup"><span data-stu-id="c5a20-189">S_OK</span></span> 
  
> <span data-ttu-id="c5a20-190">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="c5a20-190">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="c5a20-191">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="c5a20-191">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="c5a20-192">サービス プロバイダーが構成されていません。</span><span class="sxs-lookup"><span data-stu-id="c5a20-192">The service provider has not been configured.</span></span> 
    
<span data-ttu-id="c5a20-193">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="c5a20-193">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="c5a20-194">ユーザー操作がキャンセルされました、通常ダイアログ ボックスで [**キャンセル**] ボタンをクリックするとします。</span><span class="sxs-lookup"><span data-stu-id="c5a20-194">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
<span data-ttu-id="c5a20-195">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="c5a20-195">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="c5a20-196">プロバイダーは、そのオブジェクトへの変更をサポートしていないか、または変更の通知をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="c5a20-196">The provider either does not support changes to its objects or does not support notification of changes.</span></span> 
    
<span data-ttu-id="c5a20-197">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="c5a20-197">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="c5a20-198">か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装には、Unicode のみサポートしています。</span><span class="sxs-lookup"><span data-stu-id="c5a20-198">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation only supports Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c5a20-199">備考</span><span class="sxs-lookup"><span data-stu-id="c5a20-199">Remarks</span></span>

<span data-ttu-id="c5a20-200">**MSGSERVICEENTRY**関数のプロトタイプを使用して定義された関数は、それ自体を構成するのにはまたはその他のサービスに固有のアクションを実行するのには、メッセージ サービスを使用できます。</span><span class="sxs-lookup"><span data-stu-id="c5a20-200">A function defined using the **MSGSERVICEENTRY** function prototype enables message services to configure themselves or to perform other service-specific actions.</span></span> <span data-ttu-id="c5a20-201">関数は、主にユーザーがメッセージ サービスに固有の設定を変更できるダイアログ ボックスを提供します。</span><span class="sxs-lookup"><span data-stu-id="c5a20-201">The function primarily furnishes a dialog box in which the user can change settings specific to the message service.</span></span> <span data-ttu-id="c5a20-202">_LpProps_パラメーターで渡されたプロパティ値の配列を使用して、プログラムによる構成もサポートできます。</span><span class="sxs-lookup"><span data-stu-id="c5a20-202">It can also support programmatic configuration by using the property value array passed in the  _lpProps_ parameter.</span></span> <span data-ttu-id="c5a20-203">プログラムによる構成は、サービスがサポートするプロファイル ウィザードでは、することが必要な場合を除き、省略可能です。</span><span class="sxs-lookup"><span data-stu-id="c5a20-203">Programmatic configuration is optional unless the service supports the Profile Wizard, for which it is required.</span></span> 
  
<span data-ttu-id="c5a20-204">MAPI は、コントロール パネルのアプリケーションまたは[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)または[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)を呼び出すクライアント アプリケーションへの応答として、このエントリ ポイントを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c5a20-204">MAPI calls this entry point from the Control Panel application or in response to a client application calling [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) or [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
<span data-ttu-id="c5a20-205">MAPI でないを配置制限関数の名前をメッセージ サービス**MSGSERVICEENTRY**のプロトタイプを使用してですが、 **ServiceEntry**の名前を希望します。</span><span class="sxs-lookup"><span data-stu-id="c5a20-205">MAPI places no restriction on the function name that a message service uses for the **MSGSERVICEENTRY** prototype but prefers the name **ServiceEntry**.</span></span> <span data-ttu-id="c5a20-206">関数の序数に制限はありませんし、1 つのプロバイダー DLL が 1 つ以上の関数を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="c5a20-206">There is no restriction on the ordinal for the function, and a single provider DLL can contain more than one function.</span></span> <span data-ttu-id="c5a20-207">ただし、関数の 1 つだけに**ServiceEntry**を付けることができます。</span><span class="sxs-lookup"><span data-stu-id="c5a20-207">However, only one of the functions can be named **ServiceEntry**.</span></span> 
  
<span data-ttu-id="c5a20-208">メッセージ サービスでは、構成ダイアログ ボックスの実装を簡略化するのに、 [BuildDisplayTable](builddisplaytable.md)関数、および[IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md)メソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="c5a20-208">A message service can use the [BuildDisplayTable](builddisplaytable.md) function and the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method to simplify configuration dialog box implementation.</span></span> 
  
<span data-ttu-id="c5a20-209">MSG_SERVICE_UNINSTALL 操作をキャンセルするのにはユーザーのことができます。</span><span class="sxs-lookup"><span data-stu-id="c5a20-209">It is possible for a user to cancel a MSG_SERVICE_UNINSTALL operation.</span></span> <span data-ttu-id="c5a20-210">この例では、 **ServiceEntry**関数では、ユーザーがサービスを削除することはできませんし、サービスがインストールされている場合は、MAPI_E_USER_CANCEL を返すことを確認して確認してください。</span><span class="sxs-lookup"><span data-stu-id="c5a20-210">In this case, the **ServiceEntry** function should check with the user to verify that the service should not be removed and return MAPI_E_USER_CANCEL if the service remains installed.</span></span> 
  
<span data-ttu-id="c5a20-211">**MSGSERVICEENTRY**プロトタイプでは関数では、HRESULT の値のいずれかを返します。</span><span class="sxs-lookup"><span data-stu-id="c5a20-211">A function based on the **MSGSERVICEENTRY** prototype returns one of the HRESULT values listed.</span></span> <span data-ttu-id="c5a20-212">MAPI は、 [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)へのクライアントの呼び出しに応答する場合にこの値を転送します。</span><span class="sxs-lookup"><span data-stu-id="c5a20-212">MAPI forwards this value when responding to a client's call to [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
<span data-ttu-id="c5a20-213">サービス エントリ関数をエクスポートするメッセージ サービスは、メッセージ サービスのセクションで、 **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) と**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) のプロパティを含める必要があります。MAPISVC.INF。</span><span class="sxs-lookup"><span data-stu-id="c5a20-213">Message services that export a service entry function must include the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) and **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) properties in the message service section of MAPISVC.INF.</span></span> 
  

