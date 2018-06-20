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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 01cc8a8a54137b72091abab3671c08b526ef9e31
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801172"
---
# <a name="iprovideradmincreateprovider"></a><span data-ttu-id="e6fe9-103">IProviderAdmin::CreateProvider</span><span class="sxs-lookup"><span data-stu-id="e6fe9-103">IProviderAdmin::CreateProvider</span></span>

<span data-ttu-id="e6fe9-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e6fe9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e6fe9-105">メッセージ サービスにサービス プロバイダーを追加します。</span><span class="sxs-lookup"><span data-stu-id="e6fe9-105">Adds a service provider to the message service.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="e6fe9-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="e6fe9-106">Parameters</span></span>

 <span data-ttu-id="e6fe9-107">_lpszProvider_</span><span class="sxs-lookup"><span data-stu-id="e6fe9-107">_lpszProvider_</span></span>
  
> <span data-ttu-id="e6fe9-108">[in]追加するプロバイダーの名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e6fe9-108">[in] A pointer to the name of the provider to add.</span></span>
    
 <span data-ttu-id="e6fe9-109">_あう_</span><span class="sxs-lookup"><span data-stu-id="e6fe9-109">_cValues_</span></span>
  
> <span data-ttu-id="e6fe9-110">[in]_LpProps_パラメーターで指定されたプロパティ値の数。</span><span class="sxs-lookup"><span data-stu-id="e6fe9-110">[in] The count of property values pointed to by the  _lpProps_ parameter.</span></span> 
    
 <span data-ttu-id="e6fe9-111">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="e6fe9-111">_lpProps_</span></span>
  
> <span data-ttu-id="e6fe9-112">[in]追加するプロバイダーのプロパティを記述するプロパティ値の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e6fe9-112">[in] A pointer to a property value array that describes the properties of the provider to add.</span></span>
    
 <span data-ttu-id="e6fe9-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="e6fe9-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="e6fe9-114">[in]ダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドルを表示します。</span><span class="sxs-lookup"><span data-stu-id="e6fe9-114">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="e6fe9-115">_UlFlags_パラメーターで、MAPI_DIALOG フラグが設定されている場合、 _ulUIParam_パラメーターが使用されます。</span><span class="sxs-lookup"><span data-stu-id="e6fe9-115">The  _ulUIParam_ parameter is used if the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="e6fe9-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e6fe9-116">_ulFlags_</span></span>
  
> <span data-ttu-id="e6fe9-117">[in]プロバイダーの追加を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="e6fe9-117">[in] A bitmask of flags that controls the provider addition.</span></span> <span data-ttu-id="e6fe9-118">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="e6fe9-118">The following flags can be set:</span></span>
    
  - <span data-ttu-id="e6fe9-119">MAPI_DIALOG:、構成情報の入力を求めるダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e6fe9-119">MAPI_DIALOG: Displays a dialog box to prompt for configuration information.</span></span>
      
  - <span data-ttu-id="e6fe9-120">MAPI_UNICODE: Unicode 形式では、プロバイダーの名前と文字列のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="e6fe9-120">MAPI_UNICODE: The provider name and string properties are in Unicode format.</span></span> <span data-ttu-id="e6fe9-121">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式でこれらの文字列です。</span><span class="sxs-lookup"><span data-stu-id="e6fe9-121">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="e6fe9-122">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="e6fe9-122">_lpUID_</span></span>
  
> <span data-ttu-id="e6fe9-123">[out]追加するプロバイダーを表す一意の識別子を格納する[MAPIUID](mapiuid.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e6fe9-123">[out] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier that represents the provider to add.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e6fe9-124">�߂�l</span><span class="sxs-lookup"><span data-stu-id="e6fe9-124">Return value</span></span>

<span data-ttu-id="e6fe9-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="e6fe9-125">S_OK</span></span> 
  
> <span data-ttu-id="e6fe9-126">プロバイダーはメッセージ サービスに正常に追加されました。</span><span class="sxs-lookup"><span data-stu-id="e6fe9-126">The provider was successfully added to the message service.</span></span>
    
<span data-ttu-id="e6fe9-127">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="e6fe9-127">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="e6fe9-128">ユーザー操作がキャンセルされました、通常ダイアログ ボックスで [**キャンセル**] ボタンをクリックするとします。</span><span class="sxs-lookup"><span data-stu-id="e6fe9-128">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e6fe9-129">備考</span><span class="sxs-lookup"><span data-stu-id="e6fe9-129">Remarks</span></span>

<span data-ttu-id="e6fe9-130">**IProviderAdmin::CreateProvider**メソッドでは、メッセージ サービスにサービス プロバイダーを追加します。</span><span class="sxs-lookup"><span data-stu-id="e6fe9-130">The **IProviderAdmin::CreateProvider** method adds a service provider to the message service.</span></span> <span data-ttu-id="e6fe9-131">_LpszProvider_パラメーターは、メッセージ サービスに属しているプロバイダーの名前をポイントする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e6fe9-131">The  _lpszProvider_ parameter must point to the name of a provider that belongs to the message service.</span></span> <span data-ttu-id="e6fe9-132">**CreateProvider**は名前がサービスのプロバイダーの名前と一致するかどうかを確認していません。渡された名前がサービス名に一致しない場合、呼び出しが成功したが、結果は予測できません。</span><span class="sxs-lookup"><span data-stu-id="e6fe9-132">**CreateProvider** does not verify whether the name matches the name of a provider in the service; if the passed name does not match a service name, the call succeeds, but the results are unpredictable.</span></span> <span data-ttu-id="e6fe9-133">ほとんどのメッセージ サービスでは、プロバイダーを追加または削除、プロファイルを使用している間は許可されません。</span><span class="sxs-lookup"><span data-stu-id="e6fe9-133">Most message services do not allow providers to be added or deleted while the profile is in use.</span></span> 
  
<span data-ttu-id="e6fe9-134">結局のところ、サービスに関する情報のプロバイダーはプロファイルに追加されて、Mapisvc.inf ファイルの**CreateProvider**は、 _ulContext_パラメーターを MSG_SERVICE_ を設定したメッセージ サービスのエントリ ポイント関数を呼び出しますPROVIDER_CREATE。</span><span class="sxs-lookup"><span data-stu-id="e6fe9-134">After all of the available information about the service provider has been added to the profile from the Mapisvc.inf file, **CreateProvider** calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_PROVIDER_CREATE.</span></span> <span data-ttu-id="e6fe9-135">MAPI_DIALOG は、 **CreateProvider**メソッドの_ulFlags_パラメーターで設定されている場合、 _ulUIParam_と_ulFlags_パラメーターの値も、エントリ ポイント関数に渡されます。</span><span class="sxs-lookup"><span data-stu-id="e6fe9-135">If MAPI_DIALOG is set in the **CreateProvider** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed to the entry point function.</span></span> <span data-ttu-id="e6fe9-136">これらの追加パラメーターは、構成設定を入力できるように、プロパティ シートを表示するサービス プロバイダーを有効にします。</span><span class="sxs-lookup"><span data-stu-id="e6fe9-136">These additional parameters enable the service provider to display its property sheet so the user can enter configuration settings.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e6fe9-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="e6fe9-137">See also</span></span>

- [<span data-ttu-id="e6fe9-138">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="e6fe9-138">MAPIUID</span></span>](mapiuid.md)  
- [<span data-ttu-id="e6fe9-139">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="e6fe9-139">MSGSERVICEENTRY</span></span>](msgserviceentry.md)  
- [<span data-ttu-id="e6fe9-140">SPropValue</span><span class="sxs-lookup"><span data-stu-id="e6fe9-140">SPropValue</span></span>](spropvalue.md)  
- [<span data-ttu-id="e6fe9-141">IProviderAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e6fe9-141">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

