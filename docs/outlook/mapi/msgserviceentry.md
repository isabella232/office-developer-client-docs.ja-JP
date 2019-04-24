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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 56a5f153dbd563397b9216af32a715692d0876d7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341609"
---
# <a name="msgserviceentry"></a><span data-ttu-id="2e6e3-103">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="2e6e3-103">MSGSERVICEENTRY</span></span>

  
  
<span data-ttu-id="2e6e3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e6e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e6e3-105">メッセージサービスのエントリポイント関数のプロトタイプを定義して、メッセージサービスの構成をサポートします。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-105">Defines a prototype for a message service entry point function to support message service configuration.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2e6e3-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2e6e3-106">Header file:</span></span>  <br/> |<span data-ttu-id="2e6e3-107">Mapispi</span><span class="sxs-lookup"><span data-stu-id="2e6e3-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="2e6e3-108">定義された関数の実装:</span><span class="sxs-lookup"><span data-stu-id="2e6e3-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="2e6e3-109">メッセージサービス</span><span class="sxs-lookup"><span data-stu-id="2e6e3-109">Message services</span></span>  <br/> |
|<span data-ttu-id="2e6e3-110">によって呼び出された定義済み関数:</span><span class="sxs-lookup"><span data-stu-id="2e6e3-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="2e6e3-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="2e6e3-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="2e6e3-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2e6e3-112">Parameters</span></span>

 <span data-ttu-id="2e6e3-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="2e6e3-113">_hInstance_</span></span>
  
> <span data-ttu-id="2e6e3-114">順番サービスプロバイダー dll のインスタンスのハンドル。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-114">[in] Handle of the instance of the service providerDLL.</span></span> <span data-ttu-id="2e6e3-115">通常、ハンドルはリソースを取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-115">The handle is typically used to retrieve resources.</span></span> 
    
 <span data-ttu-id="2e6e3-116">_lpmalloc_</span><span class="sxs-lookup"><span data-stu-id="2e6e3-116">_lpMalloc_</span></span>
  
> <span data-ttu-id="2e6e3-117">順番OLE **imalloc**インターフェイスを公開するメモリアロケーターオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-117">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="2e6e3-118">**IStream**などの特定のインターフェイスを使用する場合、メッセージサービスはこの割り当て方法を使用する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-118">The message service may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="2e6e3-119">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="2e6e3-119">_lpMAPISup_</span></span>
  
> <span data-ttu-id="2e6e3-120">順番[imapisupport: IUnknown](imapisupportiunknown.md)インターフェイスの実装へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-120">[in] Pointer to an [IMAPISupport : IUnknown](imapisupportiunknown.md) interface implementation.</span></span> 
    
 <span data-ttu-id="2e6e3-121">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="2e6e3-121">_ulUIParam_</span></span>
  
> <span data-ttu-id="2e6e3-122">順番関数またはゼロにユーザーインターフェイス情報を渡すために使用される実装固有の値。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-122">[in] An implementation-specific value used for passing user interface information to a function or zero.</span></span> <span data-ttu-id="2e6e3-123">_uluiparam_パラメーターは、構成ダイアログボックスの親ウィンドウハンドルで、型 HWND (ULONG_PTR へのキャスト) です。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-123">The  _ulUIParam_ parameter is the parent window handle for the configuration dialog box and is of type HWND (cast to a ULONG_PTR).</span></span> <span data-ttu-id="2e6e3-124">値が0の場合は、親ウィンドウがないことを示します。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-124">A value of zero indicates that there is no parent window.</span></span> 
    
 <span data-ttu-id="2e6e3-125">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2e6e3-125">_ulFlags_</span></span>
  
> <span data-ttu-id="2e6e3-126">順番サービスエントリ関数のオプションを示すフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-126">[in] Bitmask of flags indicating options for the service entry function.</span></span> <span data-ttu-id="2e6e3-127">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-127">The following flags can be set:</span></span>
    
<span data-ttu-id="2e6e3-128">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2e6e3-128">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="2e6e3-129">渡された文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-129">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="2e6e3-130">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-130">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="2e6e3-131">MSG_SERVICE_UI_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="2e6e3-131">MSG_SERVICE_UI_READ_ONLY</span></span> 
  
> <span data-ttu-id="2e6e3-132">サービスの構成ユーザーインターフェイスは現在の構成を表示しますが、ユーザーはそれを変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-132">The service's configuration user interface should display the current configuration but not allow the user to change it.</span></span> 
    
<span data-ttu-id="2e6e3-133">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="2e6e3-133">SERVICE_UI_ALLOWED</span></span> 
  
> <span data-ttu-id="2e6e3-134">必要に応じて、構成ダイアログボックスを表示することを許可します。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-134">Permits a configuration dialog box to be displayed if necessary.</span></span> <span data-ttu-id="2e6e3-135">SERVICE_UI_ALLOWED フラグが設定されている場合、 _lpprops_プロパティの値の配列が空であるか、有効な構成が含まれていない場合にのみ、ダイアログボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-135">When the SERVICE_UI_ALLOWED flag is set, the dialog box should be displayed only if the  _lpProps_ property value array is empty or does not contain a valid configuration.</span></span> <span data-ttu-id="2e6e3-136">SERVICE_UI_ALLOWED が設定されていない場合、SERVICE_UI_ALWAYS フラグが設定されている場合は、ダイアログボックスが表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-136">If SERVICE_UI_ALLOWED is not set, a dialog box might still be displayed if the SERVICE_UI_ALWAYS flag is set.</span></span> 
    
<span data-ttu-id="2e6e3-137">UI_CURRENT_PROVIDER_FIRST</span><span class="sxs-lookup"><span data-stu-id="2e6e3-137">UI_CURRENT_PROVIDER_FIRST</span></span> 
  
> <span data-ttu-id="2e6e3-138">他のダイアログボックスの上に、アクティブなプロバイダーの構成ダイアログボックスが表示されるように要求します。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-138">Requests that the configuration dialog box for the active provider be displayed on top of other dialog boxes.</span></span> 
    
<span data-ttu-id="2e6e3-139">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="2e6e3-139">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="2e6e3-140">構成ダイアログボックスを表示するには、メッセージサービスが必要です。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-140">Requires the message service to display a configuration dialog box.</span></span> <span data-ttu-id="2e6e3-141">SERVICE_UI_ALWAYS フラグが設定されていない場合でも、SERVICE_UI_ALLOWED フラグが設定されており、有効な構成情報が_lpprops_プロパティ値の配列から利用できない場合は、構成ダイアログボックスが表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-141">If the SERVICE_UI_ALWAYS flag is not set, a configuration dialog box might still be displayed if the SERVICE_UI_ALLOWED flag is set and valid configuration information is not available from the  _lpProps_ property value array.</span></span> <span data-ttu-id="2e6e3-142">ユーザーインターフェイスを表示できるようにするには、SERVICE_UI_ALLOWED または SERVICE_UI_ALWAYS のいずれかを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-142">Either SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS must be set to allow a user interface to be displayed.</span></span> 
    
 <span data-ttu-id="2e6e3-143">_ulcontext_</span><span class="sxs-lookup"><span data-stu-id="2e6e3-143">_ulContext_</span></span>
  
> <span data-ttu-id="2e6e3-144">順番MAPI が現在実行している構成操作。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-144">[in] The configuration operation that MAPI is currently performing.</span></span> <span data-ttu-id="2e6e3-145">_ulcontext_パラメーターには、次のいずれかの値を格納します。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-145">The  _ulContext_ parameter will contain one of the following values:</span></span> 
    
<span data-ttu-id="2e6e3-146">MSG_SERVICE_CONFIGURE</span><span class="sxs-lookup"><span data-stu-id="2e6e3-146">MSG_SERVICE_CONFIGURE</span></span> 
  
> <span data-ttu-id="2e6e3-147">サービスの構成の変更は、プロファイルで行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-147">Changes to the service's configuration should be made in the profile.</span></span> <span data-ttu-id="2e6e3-148">SERVICE_UI_ALWAYS フラグが設定されている場合、サービスはその構成ダイアログボックスを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-148">If the SERVICE_UI_ALWAYS flag is set, the service should display its configuration dialog box.</span></span> <span data-ttu-id="2e6e3-149">SERVICE_UI_ALLOWED フラグが設定されていて、 _lpprops_パラメーターが空であるか、有効な構成データが含まれていない場合にも、ダイアログボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-149">The dialog box should also be displayed if the SERVICE_UI_ALLOWED flag is set and the  _lpProps_ parameter is empty or does not contain valid configuration data.</span></span> <span data-ttu-id="2e6e3-150">_lpprops_に有効なデータが含まれている場合、ダイアログボックスは表示されず、サービスはこのデータを使用して構成の変更を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-150">If  _lpProps_ contains valid data, no dialog box should be displayed and the service should use this data for making the configuration change.</span></span> 
    
<span data-ttu-id="2e6e3-151">MSG_SERVICE_CREATE</span><span class="sxs-lookup"><span data-stu-id="2e6e3-151">MSG_SERVICE_CREATE</span></span> 
  
> <span data-ttu-id="2e6e3-152">サービスはプロファイルに追加されています。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-152">The service is being added to a profile.</span></span> <span data-ttu-id="2e6e3-153">SERVICE_UI_ALWAYS または SERVICE_UI_ALLOWED フラグのどちらかが設定されている場合、サービスはその構成ダイアログボックスを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-153">If either the SERVICE_UI_ALWAYS or SERVICE_UI_ALLOWED flag is set, the service should display its configuration dialog box.</span></span> <span data-ttu-id="2e6e3-154">どちらのフラグも設定されていない場合、サービスは失敗します。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-154">If neither flag is set, the service should fail.</span></span> 
    
<span data-ttu-id="2e6e3-155">MSG_SERVICE_DELETE</span><span class="sxs-lookup"><span data-stu-id="2e6e3-155">MSG_SERVICE_DELETE</span></span> 
  
> <span data-ttu-id="2e6e3-156">サービスがプロファイルから削除されています。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-156">The service is being removed from a profile.</span></span> <span data-ttu-id="2e6e3-157">このイベントを受け取った後、サービスは S_OK を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-157">After receiving this event, the service should return S_OK.</span></span>
    
<span data-ttu-id="2e6e3-158">MSG_SERVICE_INSTALL</span><span class="sxs-lookup"><span data-stu-id="2e6e3-158">MSG_SERVICE_INSTALL</span></span> 
  
> <span data-ttu-id="2e6e3-159">サービスは、ネットワーク、フロッピーディスク、またはその他の外部メディアからユーザーのワークステーションにインストールされています。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-159">The service has been installed to the user's workstation from a network, floppy disk, or other external medium.</span></span> <span data-ttu-id="2e6e3-160">このイベントを受け取った後、サービスは通常 S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-160">After receiving this event, the service usually returns S_OK.</span></span> 
    
<span data-ttu-id="2e6e3-161">MSG_SERVICE_PROVIDER_CREATE</span><span class="sxs-lookup"><span data-stu-id="2e6e3-161">MSG_SERVICE_PROVIDER_CREATE</span></span> 
  
> <span data-ttu-id="2e6e3-162">プロバイダーの追加のインスタンスを作成するようにサービスに要求します。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-162">Requests that the service create an additional instance of a provider.</span></span> <span data-ttu-id="2e6e3-163">サービスがこの操作をサポートしている場合は、 [IProviderAdmin:: createprovider](iprovideradmin-createprovider.md)を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-163">If the service supports this operation, it should call [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md).</span></span> <span data-ttu-id="2e6e3-164">サービスがこの操作をサポートしていない場合は、MAPI_E_NO_SUPPORT を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-164">If the service does not support this operation, it can return MAPI_E_NO_SUPPORT.</span></span> 
    
<span data-ttu-id="2e6e3-165">MSG_SERVICE_PROVIDER_DELETE</span><span class="sxs-lookup"><span data-stu-id="2e6e3-165">MSG_SERVICE_PROVIDER_DELETE</span></span> 
  
> <span data-ttu-id="2e6e3-166">プロバイダーインスタンスを削除するようにサービスに要求します。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-166">Requests that the service delete a provider instance.</span></span> <span data-ttu-id="2e6e3-167">サービスがこの操作をサポートしている場合は、 [IProviderAdmin::D eleteprovider](iprovideradmin-deleteprovider.md)を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-167">If the service supports this operation, it should call [IProviderAdmin::DeleteProvider](iprovideradmin-deleteprovider.md).</span></span> <span data-ttu-id="2e6e3-168">サービスがこの操作をサポートしていない場合は、MAPI_E_NO_SUPPORT を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-168">If the service does not support this operation, it can return MAPI_E_NO_SUPPORT.</span></span>
    
<span data-ttu-id="2e6e3-169">MSG_SERVICE_UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="2e6e3-169">MSG_SERVICE_UNINSTALL</span></span> 
  
> <span data-ttu-id="2e6e3-170">サービスが削除されています。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-170">The service is being removed.</span></span> <span data-ttu-id="2e6e3-171">このイベントを受け取った後、サービスは、サービスが終了する前に実行する必要があるクリーンアップタスクを実行してから、成功の値を返します。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-171">After receiving this event, the service can perform any cleanup tasks that should be done before the service ends and then return with a success value.</span></span> <span data-ttu-id="2e6e3-172">ユーザーが削除をキャンセルすると、サービスは MAPI_E_USER_CANCEL を返します。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-172">If the user cancels the removal, the service should return MAPI_E_USER_CANCEL.</span></span> 
    
 <span data-ttu-id="2e6e3-173">_cvalues_</span><span class="sxs-lookup"><span data-stu-id="2e6e3-173">_cValues_</span></span>
  
> <span data-ttu-id="2e6e3-174">順番_lpprops_パラメーターによって指定された配列内のプロパティ値の数。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-174">[in] Count of property values in the array pointed to by the  _lpProps_ parameter.</span></span> <span data-ttu-id="2e6e3-175">MAPI がプロパティ値を渡さない場合、 _cvalues_パラメーターの値は0になります。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-175">The value of the  _cValues_ parameter is zero if MAPI is passing no property values.</span></span> 
    
 <span data-ttu-id="2e6e3-176">_lpprops_</span><span class="sxs-lookup"><span data-stu-id="2e6e3-176">_lpProps_</span></span>
  
> <span data-ttu-id="2e6e3-177">順番関数がメッセージサービスを構成するときに使用する、プロバイダーでサポートされているプロパティの値を示す[spropvalue](spropvalue.md)構造のオプションの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-177">[in] Pointer to an optional array of [SPropValue](spropvalue.md) structures indicating values for provider-supported properties that the function will use in configuring the message service.</span></span> <span data-ttu-id="2e6e3-178">この関数は、 _ulcontext_パラメーターが MSG_SERVICE_CONFIGURE に設定されている場合にのみ、このパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-178">The function only uses this parameter if the  _ulContext_ parameter is set to MSG_SERVICE_CONFIGURE.</span></span> <span data-ttu-id="2e6e3-179">このパラメーターは、通常、個人用アドレス帳サービスなど、ファイルベースのサービスのファイルへのパスを渡すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-179">This parameter is commonly used to pass the path to a file for a file-based service, such as a personal address book service.</span></span> <span data-ttu-id="2e6e3-180">MSG_SERVICE_CONFIGURE フラグが_ulflags_パラメーターに渡されていない場合、 _lpprops_パラメーターは0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-180">If the MSG_SERVICE_CONFIGURE flag is not passed in the  _ulFlags_ parameter, the  _lpProps_ parameter must be zero.</span></span> 
    
 <span data-ttu-id="2e6e3-181">_lpprovideradmin_</span><span class="sxs-lookup"><span data-stu-id="2e6e3-181">_lpProviderAdmin_</span></span>
  
> <span data-ttu-id="2e6e3-182">順番IProviderAdmin へのポインター [: IUnknown](iprovideradminiunknown.md)インターフェイスは、現在のメッセージサービスの特定のプロバイダーのプロファイルセクションを検索するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-182">[in] Pointer to an [IProviderAdmin:IUnknown](iprovideradminiunknown.md) interface that the function can use to locate profile sections for a specific provider in the current message service.</span></span> 
    
 <span data-ttu-id="2e6e3-183">_lppMapiError_</span><span class="sxs-lookup"><span data-stu-id="2e6e3-183">_lppMapiError_</span></span>
  
> <span data-ttu-id="2e6e3-184">読み上げ[MAPIERROR](mapierror.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-184">[out] Pointer to a [MAPIERROR](mapierror.md) structure.</span></span> <span data-ttu-id="2e6e3-185">この構造体は、 [MAPIAllocateBuffer](mapiallocatebuffer.md)関数を使用して割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-185">The structure is allocated with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> <span data-ttu-id="2e6e3-186">すべてのメンバーはオプションですが、ほとんどの構造体には_lpszerror_メンバーに有効なエラーメッセージ文字列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-186">All members are optional, although most structures will contain a valid error message string in the  _lpszError_ member.</span></span> <span data-ttu-id="2e6e3-187">構造体の_lpszcomponent_または_lpszcomponent_メンバーが存在する場合は、基本構造で[MAPIFreeBuffer](mapifreebuffer.md)を1回呼び出すことによって、最終的にメモリを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-187">If the  _lpszComponent_ or  _lpszError_ members of the structure are present, their memory must eventually be freed by a single call to [MAPIFreeBuffer](mapifreebuffer.md) on the base structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2e6e3-188">戻り値</span><span class="sxs-lookup"><span data-stu-id="2e6e3-188">Return value</span></span>

<span data-ttu-id="2e6e3-189">S_OK</span><span class="sxs-lookup"><span data-stu-id="2e6e3-189">S_OK</span></span> 
  
> <span data-ttu-id="2e6e3-190">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="2e6e3-190">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="2e6e3-191">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="2e6e3-191">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="2e6e3-192">サービスプロバイダーが構成されていません。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-192">The service provider has not been configured.</span></span> 
    
<span data-ttu-id="2e6e3-193">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="2e6e3-193">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="2e6e3-194">ユーザーが操作をキャンセルしました。通常は、ダイアログボックスの **[キャンセル**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-194">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
<span data-ttu-id="2e6e3-195">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="2e6e3-195">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="2e6e3-196">プロバイダーは、オブジェクトへの変更をサポートしていないか、変更の通知をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-196">The provider either does not support changes to its objects or does not support notification of changes.</span></span> 
    
<span data-ttu-id="2e6e3-197">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="2e6e3-197">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="2e6e3-198">MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode がサポートされているかどうか。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-198">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation only supports Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2e6e3-199">解説</span><span class="sxs-lookup"><span data-stu-id="2e6e3-199">Remarks</span></span>

<span data-ttu-id="2e6e3-200">**msgserviceentry**関数プロトタイプを使用して定義された関数は、メッセージサービスが自分自身を構成したり、その他のサービス固有のアクションを実行したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-200">A function defined using the **MSGSERVICEENTRY** function prototype enables message services to configure themselves or to perform other service-specific actions.</span></span> <span data-ttu-id="2e6e3-201">この関数は、主に、ユーザーがメッセージサービスに固有の設定を変更できるダイアログボックスを furnishes します。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-201">The function primarily furnishes a dialog box in which the user can change settings specific to the message service.</span></span> <span data-ttu-id="2e6e3-202">_lpprops_パラメーターで渡されたプロパティ値の配列を使用して、プログラムによる構成をサポートすることもできます。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-202">It can also support programmatic configuration by using the property value array passed in the  _lpProps_ parameter.</span></span> <span data-ttu-id="2e6e3-203">プログラムによる構成は、サービスが必要なプロファイルウィザードをサポートしていない限り、オプションです。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-203">Programmatic configuration is optional unless the service supports the Profile Wizard, for which it is required.</span></span> 
  
<span data-ttu-id="2e6e3-204">MAPI は、このエントリポイントをコントロールパネルアプリケーションから呼び出すか、 [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md)または[IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)を呼び出しているクライアントアプリケーションに応答して呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-204">MAPI calls this entry point from the Control Panel application or in response to a client application calling [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) or [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
<span data-ttu-id="2e6e3-205">MAPI では、メッセージサービスが**msgserviceentry** prototype に使用する関数名に制限はありませんが、name **serviceentry**が優先されます。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-205">MAPI places no restriction on the function name that a message service uses for the **MSGSERVICEENTRY** prototype but prefers the name **ServiceEntry**.</span></span> <span data-ttu-id="2e6e3-206">関数の序数には制限がありません。1つのプロバイダー DLL に複数の関数を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-206">There is no restriction on the ordinal for the function, and a single provider DLL can contain more than one function.</span></span> <span data-ttu-id="2e6e3-207">ただし、 **serviceentry**という名前の関数は1つだけにすることができます。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-207">However, only one of the functions can be named **ServiceEntry**.</span></span> 
  
<span data-ttu-id="2e6e3-208">メッセージサービスでは、 [builddisplaytable](builddisplaytable.md)関数と[imapisupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md)メソッドを使用して、構成ダイアログボックスの実装を簡単にすることができます。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-208">A message service can use the [BuildDisplayTable](builddisplaytable.md) function and the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method to simplify configuration dialog box implementation.</span></span> 
  
<span data-ttu-id="2e6e3-209">ユーザーは MSG_SERVICE_UNINSTALL 操作を取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-209">It is possible for a user to cancel a MSG_SERVICE_UNINSTALL operation.</span></span> <span data-ttu-id="2e6e3-210">この場合、 **serviceentry**関数は、サービスが削除されないことを確認するためにユーザーに確認し、サービスがインストールされたままの場合は MAPI_E_USER_CANCEL を返します。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-210">In this case, the **ServiceEntry** function should check with the user to verify that the service should not be removed and return MAPI_E_USER_CANCEL if the service remains installed.</span></span> 
  
<span data-ttu-id="2e6e3-211">**msgserviceentry**プロトタイプに基づく関数は、表示されている HRESULT 値の1つを返します。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-211">A function based on the **MSGSERVICEENTRY** prototype returns one of the HRESULT values listed.</span></span> <span data-ttu-id="2e6e3-212">MAPI は、 [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)へのクライアントの呼び出しに応答するときにこの値を転送します。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-212">MAPI forwards this value when responding to a client's call to [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
<span data-ttu-id="2e6e3-213">サービスエントリ関数をエクスポートするメッセージサービスには、 **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) および**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) のプロパティが含まれている必要があります。MAPISVC.INF。</span><span class="sxs-lookup"><span data-stu-id="2e6e3-213">Message services that export a service entry function must include the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) and **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) properties in the message service section of MAPISVC.INF.</span></span> 
  

