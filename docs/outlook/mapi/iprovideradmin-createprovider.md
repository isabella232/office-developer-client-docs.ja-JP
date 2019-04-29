---
title: IProviderAdminCreateProvider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.CreateProvider
api_type:
- COM
ms.assetid: 80c1449a-6cd9-4b93-a300-395979894b71
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 72dddca5a8079374600e05b96a24cbbc25e7f7f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430806"
---
# <a name="iprovideradmincreateprovider"></a><span data-ttu-id="fc1fb-103">IProviderAdmin::CreateProvider</span><span class="sxs-lookup"><span data-stu-id="fc1fb-103">IProviderAdmin::CreateProvider</span></span>

<span data-ttu-id="fc1fb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc1fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc1fb-105">メッセージサービスにサービスプロバイダーを追加します。</span><span class="sxs-lookup"><span data-stu-id="fc1fb-105">Adds a service provider to the message service.</span></span> 
  
```cpp
HRESULT CreateProvider(
  LPSTR lpszProvider,
  ULONG cValues,
  LPSPropValue lpProps,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  MAPIUID FAR * lpUID
);
```

## <a name="parameters"></a><span data-ttu-id="fc1fb-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="fc1fb-106">Parameters</span></span>

 <span data-ttu-id="fc1fb-107">_lpszprovider_</span><span class="sxs-lookup"><span data-stu-id="fc1fb-107">_lpszProvider_</span></span>
  
> <span data-ttu-id="fc1fb-108">順番追加するプロバイダーの名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fc1fb-108">[in] A pointer to the name of the provider to add.</span></span>
    
 <span data-ttu-id="fc1fb-109">_cvalues_</span><span class="sxs-lookup"><span data-stu-id="fc1fb-109">_cValues_</span></span>
  
> <span data-ttu-id="fc1fb-110">順番_lpprops_パラメーターによって示されるプロパティ値の数。</span><span class="sxs-lookup"><span data-stu-id="fc1fb-110">[in] The count of property values pointed to by the  _lpProps_ parameter.</span></span> 
    
 <span data-ttu-id="fc1fb-111">_lpprops_</span><span class="sxs-lookup"><span data-stu-id="fc1fb-111">_lpProps_</span></span>
  
> <span data-ttu-id="fc1fb-112">順番追加するプロバイダーのプロパティを記述するプロパティ値配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fc1fb-112">[in] A pointer to a property value array that describes the properties of the provider to add.</span></span>
    
 <span data-ttu-id="fc1fb-113">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="fc1fb-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="fc1fb-114">順番このメソッドが表示する任意のダイアログボックスまたはウィンドウの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="fc1fb-114">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="fc1fb-115">_uluiparam_パラメーターは、MAPI_DIALOG フラグが_ulflags_パラメーターで設定されている場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="fc1fb-115">The  _ulUIParam_ parameter is used if the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="fc1fb-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fc1fb-116">_ulFlags_</span></span>
  
> <span data-ttu-id="fc1fb-117">順番プロバイダーの追加を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="fc1fb-117">[in] A bitmask of flags that controls the provider addition.</span></span> <span data-ttu-id="fc1fb-118">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="fc1fb-118">The following flags can be set:</span></span>
    
  - <span data-ttu-id="fc1fb-119">MAPI_DIALOG: 構成情報を求めるダイアログボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="fc1fb-119">MAPI_DIALOG: Displays a dialog box to prompt for configuration information.</span></span>
      
  - <span data-ttu-id="fc1fb-120">MAPI_UNICODE: プロバイダー名と文字列プロパティは、UNICODE 形式です。</span><span class="sxs-lookup"><span data-stu-id="fc1fb-120">MAPI_UNICODE: The provider name and string properties are in Unicode format.</span></span> <span data-ttu-id="fc1fb-121">MAPI_UNICODE フラグが設定されていない場合、これらの文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="fc1fb-121">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="fc1fb-122">_lpuid_</span><span class="sxs-lookup"><span data-stu-id="fc1fb-122">_lpUID_</span></span>
  
> <span data-ttu-id="fc1fb-123">読み上げ追加するプロバイダーを表す一意の識別子を含む[MAPIUID](mapiuid.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fc1fb-123">[out] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier that represents the provider to add.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fc1fb-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="fc1fb-124">Return value</span></span>

<span data-ttu-id="fc1fb-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="fc1fb-125">S_OK</span></span> 
  
> <span data-ttu-id="fc1fb-126">プロバイダーがメッセージサービスに正常に追加されました。</span><span class="sxs-lookup"><span data-stu-id="fc1fb-126">The provider was successfully added to the message service.</span></span>
    
<span data-ttu-id="fc1fb-127">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="fc1fb-127">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="fc1fb-128">ユーザーが操作をキャンセルしました。通常は、ダイアログボックスの **[キャンセル**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc1fb-128">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fc1fb-129">注釈</span><span class="sxs-lookup"><span data-stu-id="fc1fb-129">Remarks</span></span>

<span data-ttu-id="fc1fb-130">**IProviderAdmin:: createprovider**メソッドによって、サービスプロバイダーがメッセージサービスに追加されます。</span><span class="sxs-lookup"><span data-stu-id="fc1fb-130">The **IProviderAdmin::CreateProvider** method adds a service provider to the message service.</span></span> <span data-ttu-id="fc1fb-131">_lpszprovider_パラメーターは、メッセージサービスに属するプロバイダーの名前を指している必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc1fb-131">The  _lpszProvider_ parameter must point to the name of a provider that belongs to the message service.</span></span> <span data-ttu-id="fc1fb-132">**createprovider**は、名前がサービスのプロバイダーの名前と一致しているかどうかを確認しません。渡された名前がサービス名と一致しない場合、呼び出しは成功しますが、結果は予測できません。</span><span class="sxs-lookup"><span data-stu-id="fc1fb-132">**CreateProvider** does not verify whether the name matches the name of a provider in the service; if the passed name does not match a service name, the call succeeds, but the results are unpredictable.</span></span> <span data-ttu-id="fc1fb-133">ほとんどのメッセージサービスでは、プロファイルが使用されている間、プロバイダーを追加または削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="fc1fb-133">Most message services do not allow providers to be added or deleted while the profile is in use.</span></span> 
  
<span data-ttu-id="fc1fb-134">サービスプロバイダーに関するすべての利用可能な情報が mapisvc.inf ファイルからプロファイルに追加された後、 **createprovider**は_ulcontext_パラメーターを MSG_SERVICE_ に設定したメッセージサービスのエントリポイント関数を呼び出します。PROVIDER_CREATE。</span><span class="sxs-lookup"><span data-stu-id="fc1fb-134">After all of the available information about the service provider has been added to the profile from the Mapisvc.inf file, **CreateProvider** calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_PROVIDER_CREATE.</span></span> <span data-ttu-id="fc1fb-135">MAPI_DIALOG が**createprovider**メソッドの_ulflags_パラメーターで設定されている場合、 _uluiparam_パラメーターと_ulflags_パラメーターの値もエントリポイント関数に渡されます。</span><span class="sxs-lookup"><span data-stu-id="fc1fb-135">If MAPI_DIALOG is set in the **CreateProvider** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed to the entry point function.</span></span> <span data-ttu-id="fc1fb-136">これらの追加パラメーターにより、サービスプロバイダーはプロパティシートを表示して、ユーザーが構成設定を入力できるようにします。</span><span class="sxs-lookup"><span data-stu-id="fc1fb-136">These additional parameters enable the service provider to display its property sheet so the user can enter configuration settings.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fc1fb-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="fc1fb-137">See also</span></span>

- [<span data-ttu-id="fc1fb-138">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="fc1fb-138">MAPIUID</span></span>](mapiuid.md)  
- [<span data-ttu-id="fc1fb-139">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="fc1fb-139">MSGSERVICEENTRY</span></span>](msgserviceentry.md)  
- [<span data-ttu-id="fc1fb-140">SPropValue</span><span class="sxs-lookup"><span data-stu-id="fc1fb-140">SPropValue</span></span>](spropvalue.md)  
- [<span data-ttu-id="fc1fb-141">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fc1fb-141">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

