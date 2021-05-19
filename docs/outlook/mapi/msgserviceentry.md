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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 56a5f153dbd563397b9216af32a715692d0876d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427879"
---
# <a name="msgserviceentry"></a><span data-ttu-id="5fa32-103">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="5fa32-103">MSGSERVICEENTRY</span></span>

  
  
<span data-ttu-id="5fa32-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5fa32-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5fa32-105">メッセージ サービスの構成をサポートするメッセージ サービス エントリ ポイント関数のプロトタイプを定義します。</span><span class="sxs-lookup"><span data-stu-id="5fa32-105">Defines a prototype for a message service entry point function to support message service configuration.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5fa32-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="5fa32-106">Header file:</span></span>  <br/> |<span data-ttu-id="5fa32-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="5fa32-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="5fa32-108">定義された関数は、次の方法で実装されます。</span><span class="sxs-lookup"><span data-stu-id="5fa32-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="5fa32-109">メッセージ サービス</span><span class="sxs-lookup"><span data-stu-id="5fa32-109">Message services</span></span>  <br/> |
|<span data-ttu-id="5fa32-110">によって呼び出される定義済み関数:</span><span class="sxs-lookup"><span data-stu-id="5fa32-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="5fa32-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="5fa32-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="5fa32-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5fa32-112">Parameters</span></span>

 <span data-ttu-id="5fa32-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="5fa32-113">_hInstance_</span></span>
  
> <span data-ttu-id="5fa32-114">[in]サービス プロバイダーDLL のインスタンスのハンドル。</span><span class="sxs-lookup"><span data-stu-id="5fa32-114">[in] Handle of the instance of the service providerDLL.</span></span> <span data-ttu-id="5fa32-115">ハンドルは通常、リソースの取得に使用されます。</span><span class="sxs-lookup"><span data-stu-id="5fa32-115">The handle is typically used to retrieve resources.</span></span> 
    
 <span data-ttu-id="5fa32-116">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="5fa32-116">_lpMalloc_</span></span>
  
> <span data-ttu-id="5fa32-117">[in]OLE **IMalloc** インターフェイスを公開するメモリ アロケーター オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5fa32-117">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="5fa32-118">メッセージ サービスは、IStream などの特定のインターフェイスを操作するときに、この割り当て方法を使用する **必要がある場合があります**。</span><span class="sxs-lookup"><span data-stu-id="5fa32-118">The message service may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="5fa32-119">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="5fa32-119">_lpMAPISup_</span></span>
  
> <span data-ttu-id="5fa32-120">[in] [IMAPISupport へのポインター : IUnknown インターフェイス](imapisupportiunknown.md) の実装。</span><span class="sxs-lookup"><span data-stu-id="5fa32-120">[in] Pointer to an [IMAPISupport : IUnknown](imapisupportiunknown.md) interface implementation.</span></span> 
    
 <span data-ttu-id="5fa32-121">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="5fa32-121">_ulUIParam_</span></span>
  
> <span data-ttu-id="5fa32-122">[in]ユーザー インターフェイス情報を関数または 0 に渡す場合に使用される実装固有の値。</span><span class="sxs-lookup"><span data-stu-id="5fa32-122">[in] An implementation-specific value used for passing user interface information to a function or zero.</span></span> <span data-ttu-id="5fa32-123">_ulUIParam_ パラメーターは、構成ダイアログ ボックスの親ウィンドウ ハンドルであり、HWND 型 (ULONG_PTR。</span><span class="sxs-lookup"><span data-stu-id="5fa32-123">The  _ulUIParam_ parameter is the parent window handle for the configuration dialog box and is of type HWND (cast to a ULONG_PTR).</span></span> <span data-ttu-id="5fa32-124">値が 0 の場合は、親ウィンドウが表示されません。</span><span class="sxs-lookup"><span data-stu-id="5fa32-124">A value of zero indicates that there is no parent window.</span></span> 
    
 <span data-ttu-id="5fa32-125">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5fa32-125">_ulFlags_</span></span>
  
> <span data-ttu-id="5fa32-126">[in]サービス エントリ関数のオプションを示すフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="5fa32-126">[in] Bitmask of flags indicating options for the service entry function.</span></span> <span data-ttu-id="5fa32-127">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="5fa32-127">The following flags can be set:</span></span>
    
<span data-ttu-id="5fa32-128">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5fa32-128">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="5fa32-129">渡された文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="5fa32-129">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="5fa32-130">このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="5fa32-130">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="5fa32-131">MSG_SERVICE_UI_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="5fa32-131">MSG_SERVICE_UI_READ_ONLY</span></span> 
  
> <span data-ttu-id="5fa32-132">サービスの構成ユーザー インターフェイスは、現在の構成を表示する必要がありますが、ユーザーが変更を許可しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="5fa32-132">The service's configuration user interface should display the current configuration but not allow the user to change it.</span></span> 
    
<span data-ttu-id="5fa32-133">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="5fa32-133">SERVICE_UI_ALLOWED</span></span> 
  
> <span data-ttu-id="5fa32-134">必要に応じて、構成ダイアログ ボックスを表示できます。</span><span class="sxs-lookup"><span data-stu-id="5fa32-134">Permits a configuration dialog box to be displayed if necessary.</span></span> <span data-ttu-id="5fa32-135">SERVICE_UI_ALLOWEDフラグを設定すると  _、lpProps_ プロパティ値配列が空か、有効な構成が含まれている場合にのみ、ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5fa32-135">When the SERVICE_UI_ALLOWED flag is set, the dialog box should be displayed only if the  _lpProps_ property value array is empty or does not contain a valid configuration.</span></span> <span data-ttu-id="5fa32-136">このSERVICE_UI_ALLOWED設定されていない場合、このフラグが設定されている場合は、SERVICE_UI_ALWAYS表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="5fa32-136">If SERVICE_UI_ALLOWED is not set, a dialog box might still be displayed if the SERVICE_UI_ALWAYS flag is set.</span></span> 
    
<span data-ttu-id="5fa32-137">UI_CURRENT_PROVIDER_FIRST</span><span class="sxs-lookup"><span data-stu-id="5fa32-137">UI_CURRENT_PROVIDER_FIRST</span></span> 
  
> <span data-ttu-id="5fa32-138">アクティブなプロバイダーの構成ダイアログ ボックスを他のダイアログ ボックスの上に表示する要求。</span><span class="sxs-lookup"><span data-stu-id="5fa32-138">Requests that the configuration dialog box for the active provider be displayed on top of other dialog boxes.</span></span> 
    
<span data-ttu-id="5fa32-139">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="5fa32-139">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="5fa32-140">構成ダイアログ ボックスを表示するには、メッセージ サービスが必要です。</span><span class="sxs-lookup"><span data-stu-id="5fa32-140">Requires the message service to display a configuration dialog box.</span></span> <span data-ttu-id="5fa32-141">SERVICE_UI_ALWAYS フラグが設定されていない場合、SERVICE_UI_ALLOWED フラグが設定され、有効な構成情報が  _lpProps_ プロパティ値配列から使用できない場合は、構成ダイアログ ボックスが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="5fa32-141">If the SERVICE_UI_ALWAYS flag is not set, a configuration dialog box might still be displayed if the SERVICE_UI_ALLOWED flag is set and valid configuration information is not available from the  _lpProps_ property value array.</span></span> <span data-ttu-id="5fa32-142">ユーザー SERVICE_UI_ALLOWED表示SERVICE_UI_ALWAYSを許可するには、ユーザー インターフェイスまたはユーザー インターフェイスを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5fa32-142">Either SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS must be set to allow a user interface to be displayed.</span></span> 
    
 <span data-ttu-id="5fa32-143">_ulContext_</span><span class="sxs-lookup"><span data-stu-id="5fa32-143">_ulContext_</span></span>
  
> <span data-ttu-id="5fa32-144">[in]MAPI が現在実行している構成操作。</span><span class="sxs-lookup"><span data-stu-id="5fa32-144">[in] The configuration operation that MAPI is currently performing.</span></span> <span data-ttu-id="5fa32-145">_ulContext パラメーター_ には、次のいずれかの値が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5fa32-145">The  _ulContext_ parameter will contain one of the following values:</span></span> 
    
<span data-ttu-id="5fa32-146">MSG_SERVICE_CONFIGURE</span><span class="sxs-lookup"><span data-stu-id="5fa32-146">MSG_SERVICE_CONFIGURE</span></span> 
  
> <span data-ttu-id="5fa32-147">サービスの構成に対する変更は、プロファイルで行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="5fa32-147">Changes to the service's configuration should be made in the profile.</span></span> <span data-ttu-id="5fa32-148">このフラグSERVICE_UI_ALWAYS設定されている場合、サービスは構成ダイアログ ボックスを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5fa32-148">If the SERVICE_UI_ALWAYS flag is set, the service should display its configuration dialog box.</span></span> <span data-ttu-id="5fa32-149">このダイアログ ボックスは、SERVICE_UI_ALLOWED フラグが設定され  _、lpProps_ パラメーターが空の場合、または有効な構成データが含まれている場合にも表示されます。</span><span class="sxs-lookup"><span data-stu-id="5fa32-149">The dialog box should also be displayed if the SERVICE_UI_ALLOWED flag is set and the  _lpProps_ parameter is empty or does not contain valid configuration data.</span></span> <span data-ttu-id="5fa32-150">_lpProps に有効_ なデータが含まれている場合は、ダイアログ ボックスを表示し、サービスは構成を変更するためにこのデータを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5fa32-150">If  _lpProps_ contains valid data, no dialog box should be displayed and the service should use this data for making the configuration change.</span></span> 
    
<span data-ttu-id="5fa32-151">MSG_SERVICE_CREATE</span><span class="sxs-lookup"><span data-stu-id="5fa32-151">MSG_SERVICE_CREATE</span></span> 
  
> <span data-ttu-id="5fa32-152">サービスがプロファイルに追加されています。</span><span class="sxs-lookup"><span data-stu-id="5fa32-152">The service is being added to a profile.</span></span> <span data-ttu-id="5fa32-153">サービスの構成SERVICE_UI_ALWAYSまたはSERVICE_UI_ALLOWEDが設定されている場合、サービスは構成ダイアログ ボックスを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5fa32-153">If either the SERVICE_UI_ALWAYS or SERVICE_UI_ALLOWED flag is set, the service should display its configuration dialog box.</span></span> <span data-ttu-id="5fa32-154">どちらのフラグも設定しない場合、サービスは失敗します。</span><span class="sxs-lookup"><span data-stu-id="5fa32-154">If neither flag is set, the service should fail.</span></span> 
    
<span data-ttu-id="5fa32-155">MSG_SERVICE_DELETE</span><span class="sxs-lookup"><span data-stu-id="5fa32-155">MSG_SERVICE_DELETE</span></span> 
  
> <span data-ttu-id="5fa32-156">サービスはプロファイルから削除されています。</span><span class="sxs-lookup"><span data-stu-id="5fa32-156">The service is being removed from a profile.</span></span> <span data-ttu-id="5fa32-157">このイベントを受け取った後、サービスはイベントをS_OK。</span><span class="sxs-lookup"><span data-stu-id="5fa32-157">After receiving this event, the service should return S_OK.</span></span>
    
<span data-ttu-id="5fa32-158">MSG_SERVICE_INSTALL</span><span class="sxs-lookup"><span data-stu-id="5fa32-158">MSG_SERVICE_INSTALL</span></span> 
  
> <span data-ttu-id="5fa32-159">サービスは、ネットワーク、フロッピー ディスク、または他の外部メディアからユーザーのワークステーションにインストールされています。</span><span class="sxs-lookup"><span data-stu-id="5fa32-159">The service has been installed to the user's workstation from a network, floppy disk, or other external medium.</span></span> <span data-ttu-id="5fa32-160">このイベントを受け取った後、サービスは通常、S_OK。</span><span class="sxs-lookup"><span data-stu-id="5fa32-160">After receiving this event, the service usually returns S_OK.</span></span> 
    
<span data-ttu-id="5fa32-161">MSG_SERVICE_PROVIDER_CREATE</span><span class="sxs-lookup"><span data-stu-id="5fa32-161">MSG_SERVICE_PROVIDER_CREATE</span></span> 
  
> <span data-ttu-id="5fa32-162">サービスがプロバイダーの追加インスタンスを作成する要求。</span><span class="sxs-lookup"><span data-stu-id="5fa32-162">Requests that the service create an additional instance of a provider.</span></span> <span data-ttu-id="5fa32-163">サービスがこの操作をサポートしている場合は [、IProviderAdmin::CreateProvider を呼び出す必要があります](iprovideradmin-createprovider.md)。</span><span class="sxs-lookup"><span data-stu-id="5fa32-163">If the service supports this operation, it should call [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md).</span></span> <span data-ttu-id="5fa32-164">サービスがこの操作をサポートしていない場合は、この操作をMAPI_E_NO_SUPPORT。</span><span class="sxs-lookup"><span data-stu-id="5fa32-164">If the service does not support this operation, it can return MAPI_E_NO_SUPPORT.</span></span> 
    
<span data-ttu-id="5fa32-165">MSG_SERVICE_PROVIDER_DELETE</span><span class="sxs-lookup"><span data-stu-id="5fa32-165">MSG_SERVICE_PROVIDER_DELETE</span></span> 
  
> <span data-ttu-id="5fa32-166">サービスがプロバイダー インスタンスを削除する要求。</span><span class="sxs-lookup"><span data-stu-id="5fa32-166">Requests that the service delete a provider instance.</span></span> <span data-ttu-id="5fa32-167">サービスがこの操作をサポートしている場合は [、IProviderAdmin::D eleteProvider を呼び出す必要があります](iprovideradmin-deleteprovider.md)。</span><span class="sxs-lookup"><span data-stu-id="5fa32-167">If the service supports this operation, it should call [IProviderAdmin::DeleteProvider](iprovideradmin-deleteprovider.md).</span></span> <span data-ttu-id="5fa32-168">サービスがこの操作をサポートしていない場合は、この操作をMAPI_E_NO_SUPPORT。</span><span class="sxs-lookup"><span data-stu-id="5fa32-168">If the service does not support this operation, it can return MAPI_E_NO_SUPPORT.</span></span>
    
<span data-ttu-id="5fa32-169">MSG_SERVICE_UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="5fa32-169">MSG_SERVICE_UNINSTALL</span></span> 
  
> <span data-ttu-id="5fa32-170">サービスが削除されています。</span><span class="sxs-lookup"><span data-stu-id="5fa32-170">The service is being removed.</span></span> <span data-ttu-id="5fa32-171">このイベントを受け取った後、サービスは、サービスが終了する前に実行する必要があるすべてのクリーンアップ タスクを実行し、成功した値で戻ります。</span><span class="sxs-lookup"><span data-stu-id="5fa32-171">After receiving this event, the service can perform any cleanup tasks that should be done before the service ends and then return with a success value.</span></span> <span data-ttu-id="5fa32-172">ユーザーが削除を取り消した場合、サービスは削除をMAPI_E_USER_CANCEL。</span><span class="sxs-lookup"><span data-stu-id="5fa32-172">If the user cancels the removal, the service should return MAPI_E_USER_CANCEL.</span></span> 
    
 <span data-ttu-id="5fa32-173">_cValues_</span><span class="sxs-lookup"><span data-stu-id="5fa32-173">_cValues_</span></span>
  
> <span data-ttu-id="5fa32-174">[in]  _lpProps_ パラメーターが指す配列内のプロパティ値の数。</span><span class="sxs-lookup"><span data-stu-id="5fa32-174">[in] Count of property values in the array pointed to by the  _lpProps_ parameter.</span></span> <span data-ttu-id="5fa32-175">MAPI がプロパティ値を渡す場合  _、cValues_ パラメーターの値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="5fa32-175">The value of the  _cValues_ parameter is zero if MAPI is passing no property values.</span></span> 
    
 <span data-ttu-id="5fa32-176">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="5fa32-176">_lpProps_</span></span>
  
> <span data-ttu-id="5fa32-177">[in]メッセージ サービスの構成で関数が使用するプロバイダーがサポートするプロパティの値を示す [SPropValue](spropvalue.md) 構造体の省略可能な配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5fa32-177">[in] Pointer to an optional array of [SPropValue](spropvalue.md) structures indicating values for provider-supported properties that the function will use in configuring the message service.</span></span> <span data-ttu-id="5fa32-178">この関数は  _、ulContext_ パラメーターがパラメーターに設定されている場合にのみ、このパラメーターをMSG_SERVICE_CONFIGURE。</span><span class="sxs-lookup"><span data-stu-id="5fa32-178">The function only uses this parameter if the  _ulContext_ parameter is set to MSG_SERVICE_CONFIGURE.</span></span> <span data-ttu-id="5fa32-179">このパラメーターは、通常、個人用アドレス帳サービスなどのファイル ベースのサービスのファイルにパスを渡す場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="5fa32-179">This parameter is commonly used to pass the path to a file for a file-based service, such as a personal address book service.</span></span> <span data-ttu-id="5fa32-180">_ulFlags_ パラメーター MSG_SERVICE_CONFIGUREフラグが渡されない場合 _、lpProps_ パラメーターは 0 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="5fa32-180">If the MSG_SERVICE_CONFIGURE flag is not passed in the  _ulFlags_ parameter, the  _lpProps_ parameter must be zero.</span></span> 
    
 <span data-ttu-id="5fa32-181">_lpProviderAdmin_</span><span class="sxs-lookup"><span data-stu-id="5fa32-181">_lpProviderAdmin_</span></span>
  
> <span data-ttu-id="5fa32-182">[in]現在のメッセージ サービス内の特定のプロバイダーのプロファイル セクションを検索するために関数が使用できる [IProviderAdmin:IUnknown](iprovideradminiunknown.md) インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5fa32-182">[in] Pointer to an [IProviderAdmin:IUnknown](iprovideradminiunknown.md) interface that the function can use to locate profile sections for a specific provider in the current message service.</span></span> 
    
 <span data-ttu-id="5fa32-183">_lppMapiError_</span><span class="sxs-lookup"><span data-stu-id="5fa32-183">_lppMapiError_</span></span>
  
> <span data-ttu-id="5fa32-184">[out] [MAPIERROR 構造体への](mapierror.md) ポインター。</span><span class="sxs-lookup"><span data-stu-id="5fa32-184">[out] Pointer to a [MAPIERROR](mapierror.md) structure.</span></span> <span data-ttu-id="5fa32-185">この構造体は [、MAPIAllocateBuffer 関数で割り当](mapiallocatebuffer.md) てされます。</span><span class="sxs-lookup"><span data-stu-id="5fa32-185">The structure is allocated with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> <span data-ttu-id="5fa32-186">ほとんどの構造体には  _lpszError_ メンバーに有効なエラー メッセージ文字列が含まれますが、すべてのメンバーは省略可能です。</span><span class="sxs-lookup"><span data-stu-id="5fa32-186">All members are optional, although most structures will contain a valid error message string in the  _lpszError_ member.</span></span> <span data-ttu-id="5fa32-187">構造体の  _lpszComponent_ メンバーまたは  _lpszError_ メンバーが存在する場合、基本構造の [MAPIFreeBuffer](mapifreebuffer.md) を 1 回呼び出してメモリを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5fa32-187">If the  _lpszComponent_ or  _lpszError_ members of the structure are present, their memory must eventually be freed by a single call to [MAPIFreeBuffer](mapifreebuffer.md) on the base structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5fa32-188">戻り値</span><span class="sxs-lookup"><span data-stu-id="5fa32-188">Return value</span></span>

<span data-ttu-id="5fa32-189">S_OK</span><span class="sxs-lookup"><span data-stu-id="5fa32-189">S_OK</span></span> 
  
> <span data-ttu-id="5fa32-190">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="5fa32-190">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="5fa32-191">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="5fa32-191">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="5fa32-192">サービス プロバイダーが構成されていません。</span><span class="sxs-lookup"><span data-stu-id="5fa32-192">The service provider has not been configured.</span></span> 
    
<span data-ttu-id="5fa32-193">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="5fa32-193">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="5fa32-194">通常、ユーザーはダイアログ ボックスの [キャンセル] ボタンをクリック **して操作を** キャンセルしました。</span><span class="sxs-lookup"><span data-stu-id="5fa32-194">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
<span data-ttu-id="5fa32-195">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="5fa32-195">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="5fa32-196">プロバイダーは、オブジェクトの変更をサポートしないか、変更の通知をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="5fa32-196">The provider either does not support changes to its objects or does not support notification of changes.</span></span> 
    
<span data-ttu-id="5fa32-197">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="5fa32-197">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="5fa32-198">このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定MAPI_UNICODE実装が Unicode のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="5fa32-198">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation only supports Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5fa32-199">注釈</span><span class="sxs-lookup"><span data-stu-id="5fa32-199">Remarks</span></span>

<span data-ttu-id="5fa32-200">**MSGSERVICEENTRY** 関数プロトタイプを使用して定義された関数を使用すると、メッセージ サービスは自分自身を構成したり、他のサービス固有のアクションを実行したりできます。</span><span class="sxs-lookup"><span data-stu-id="5fa32-200">A function defined using the **MSGSERVICEENTRY** function prototype enables message services to configure themselves or to perform other service-specific actions.</span></span> <span data-ttu-id="5fa32-201">この関数は、主に、ユーザーがメッセージ サービスに固有の設定を変更できるダイアログ ボックスを提供します。</span><span class="sxs-lookup"><span data-stu-id="5fa32-201">The function primarily furnishes a dialog box in which the user can change settings specific to the message service.</span></span> <span data-ttu-id="5fa32-202">lpProps パラメーターで渡されたプロパティ値配列を使用して、プログラムによる構成  _をサポート_ することもできます。</span><span class="sxs-lookup"><span data-stu-id="5fa32-202">It can also support programmatic configuration by using the property value array passed in the  _lpProps_ parameter.</span></span> <span data-ttu-id="5fa32-203">プログラムによる構成は、必要なプロファイル ウィザードがサービスでサポートされていない限り、オプションです。</span><span class="sxs-lookup"><span data-stu-id="5fa32-203">Programmatic configuration is optional unless the service supports the Profile Wizard, for which it is required.</span></span> 
  
<span data-ttu-id="5fa32-204">MAPI は、コントロール パネル アプリケーションから、または [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) または [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)を呼び出すクライアント アプリケーションに応答して、このエントリ ポイントを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5fa32-204">MAPI calls this entry point from the Control Panel application or in response to a client application calling [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) or [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
<span data-ttu-id="5fa32-205">MAPI は、メッセージ サービスが **MSGSERVICEENTRY** プロトタイプに使用する関数名に制限を設定しませんが **、ServiceEntry** という名前を優先します。</span><span class="sxs-lookup"><span data-stu-id="5fa32-205">MAPI places no restriction on the function name that a message service uses for the **MSGSERVICEENTRY** prototype but prefers the name **ServiceEntry**.</span></span> <span data-ttu-id="5fa32-206">関数の序数に制限はありません。また、1 つのプロバイダー DLL に複数の関数を含めできます。</span><span class="sxs-lookup"><span data-stu-id="5fa32-206">There is no restriction on the ordinal for the function, and a single provider DLL can contain more than one function.</span></span> <span data-ttu-id="5fa32-207">ただし、ServiceEntry という名前の関数は **1 つのみです**。</span><span class="sxs-lookup"><span data-stu-id="5fa32-207">However, only one of the functions can be named **ServiceEntry**.</span></span> 
  
<span data-ttu-id="5fa32-208">メッセージ サービスは [、BuildDisplayTable](builddisplaytable.md) 関数と [IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) メソッドを使用して、構成ダイアログ ボックスの実装を簡略化できます。</span><span class="sxs-lookup"><span data-stu-id="5fa32-208">A message service can use the [BuildDisplayTable](builddisplaytable.md) function and the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method to simplify configuration dialog box implementation.</span></span> 
  
<span data-ttu-id="5fa32-209">ユーザーがユーザー操作をキャンセルMSG_SERVICE_UNINSTALLできます。</span><span class="sxs-lookup"><span data-stu-id="5fa32-209">It is possible for a user to cancel a MSG_SERVICE_UNINSTALL operation.</span></span> <span data-ttu-id="5fa32-210">この場合 **、ServiceEntry** 関数はユーザーに確認して、サービスを削除し、サービスがインストールされたままMAPI_E_USER_CANCELを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="5fa32-210">In this case, the **ServiceEntry** function should check with the user to verify that the service should not be removed and return MAPI_E_USER_CANCEL if the service remains installed.</span></span> 
  
<span data-ttu-id="5fa32-211">**MSGSERVICEENTRY プロトタイプに基づく** 関数は、一覧表示されている HRESULT 値のいずれかを返します。</span><span class="sxs-lookup"><span data-stu-id="5fa32-211">A function based on the **MSGSERVICEENTRY** prototype returns one of the HRESULT values listed.</span></span> <span data-ttu-id="5fa32-212">MAPI は、クライアントの呼び出しに応答するときにこの値を [IMsgServiceAdmin::ConfigureMsgService に転送します](imsgserviceadmin-configuremsgservice.md)。</span><span class="sxs-lookup"><span data-stu-id="5fa32-212">MAPI forwards this value when responding to a client's call to [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
<span data-ttu-id="5fa32-213">サービス エントリ関数をエクスポートするメッセージ サービスには **、MAPISVC.INF** のメッセージ サービス セクションに PR_SERVICE_DLL_NAME ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) プロパティと **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) プロパティが含まれる必要があります。</span><span class="sxs-lookup"><span data-stu-id="5fa32-213">Message services that export a service entry function must include the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) and **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) properties in the message service section of MAPISVC.INF.</span></span> 
  

