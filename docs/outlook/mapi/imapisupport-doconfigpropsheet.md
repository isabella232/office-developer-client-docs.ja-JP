---
title: IMAPISupportDoConfigPropsheet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoConfigPropsheet
api_type:
- COM
ms.assetid: 3899c49c-a0ec-4dca-92e8-e801cd4908cf
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 3b3499de9446c83cfc3b97b4d6b02e7c430b65f6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586397"
---
# <a name="imapisupportdoconfigpropsheet"></a><span data-ttu-id="ee6a8-103">IMAPISupport::DoConfigPropsheet</span><span class="sxs-lookup"><span data-stu-id="ee6a8-103">IMAPISupport::DoConfigPropsheet</span></span>

  
  
<span data-ttu-id="ee6a8-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee6a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee6a8-105">構成のプロパティ シートを表示します。</span><span class="sxs-lookup"><span data-stu-id="ee6a8-105">Displays a configuration property sheet.</span></span>
  
```cpp
HRESULT DoConfigPropsheet(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszTitle,
  LPMAPITABLE lpDisplayTable,
  LPMAPIPROP lpConfigData,
  ULONG ulTopPage
);
```

## <a name="parameters"></a><span data-ttu-id="ee6a8-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ee6a8-106">Parameters</span></span>

 <span data-ttu-id="ee6a8-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="ee6a8-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="ee6a8-108">[in]プロパティ シートの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="ee6a8-108">[in] A handle to the parent window of the property sheet.</span></span>
    
 <span data-ttu-id="ee6a8-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ee6a8-109">_ulFlags_</span></span>
  
> <span data-ttu-id="ee6a8-110">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="ee6a8-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="ee6a8-111">_lpszTitle_</span><span class="sxs-lookup"><span data-stu-id="ee6a8-111">_lpszTitle_</span></span>
  
> <span data-ttu-id="ee6a8-112">[in]プロパティ シートのタイトルへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ee6a8-112">[in] A pointer to the title of the property sheet.</span></span>
    
 <span data-ttu-id="ee6a8-113">_lpDisplayTable_</span><span class="sxs-lookup"><span data-stu-id="ee6a8-113">_lpDisplayTable_</span></span>
  
> <span data-ttu-id="ee6a8-114">[in]プロパティ シート上のコントロールを表示するを記述する表示のテーブルへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ee6a8-114">[in] A pointer to the display table that describes the controls to appear on the property sheet.</span></span>
    
 <span data-ttu-id="ee6a8-115">_lpConfigData_</span><span class="sxs-lookup"><span data-stu-id="ee6a8-115">_lpConfigData_</span></span>
  
> <span data-ttu-id="ee6a8-116">[in]プロパティ シートに表示される設定のプロパティにアクセスするために使用する[IMAPIProp](imapipropiunknown.md)実装へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ee6a8-116">[in] A pointer to the [IMAPIProp](imapipropiunknown.md) implementation to be used for accessing the configuration properties to be displayed on the property sheet.</span></span> 
    
 <span data-ttu-id="ee6a8-117">_ulTopPage_</span><span class="sxs-lookup"><span data-stu-id="ee6a8-117">_ulTopPage_</span></span>
  
> <span data-ttu-id="ee6a8-118">[in]プロパティ ・ シートの一番上の既定ページの 0 から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="ee6a8-118">[in] A zero-based index to the default top page of the property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ee6a8-119">�߂�l</span><span class="sxs-lookup"><span data-stu-id="ee6a8-119">Return value</span></span>

<span data-ttu-id="ee6a8-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="ee6a8-120">S_OK</span></span> 
  
> <span data-ttu-id="ee6a8-121">構成のプロパティ シートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ee6a8-121">The configuration property sheet was displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ee6a8-122">注釈</span><span class="sxs-lookup"><span data-stu-id="ee6a8-122">Remarks</span></span>

<span data-ttu-id="ee6a8-123">サポートのすべてのオブジェクトの**IMAPISupport::DoConfigPropsheet**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="ee6a8-123">The **IMAPISupport::DoConfigPropsheet** method is implemented for all support objects.</span></span> <span data-ttu-id="ee6a8-124">**DoConfigPropSheet**は、サービス プロバイダーとサービスのメッセージのプロパティを表示するための標準のユーザー インターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="ee6a8-124">**DoConfigPropSheet** provides a standard user interface for displaying the properties of service providers and message services.</span></span> <span data-ttu-id="ee6a8-125">ユーザーは、一貫性のある Windows のインターフェイスから利用できるように、すべての構成プロパティが表示されますのこの標準のダイアログ ボックスを使用してください。</span><span class="sxs-lookup"><span data-stu-id="ee6a8-125">You should use this standard dialog box for all configuration property displays so that users benefit from a consistent Windows interface.</span></span> 
  
<span data-ttu-id="ee6a8-126">サービス プロバイダーは、 [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)メソッドまたはプロパティの詳細を表示するボタンですから、それぞれの実装の一部として**DoConfigPropSheet**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ee6a8-126">Service providers call **DoConfigPropSheet** as part of their implementation of the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method or from a button used to display details on properties.</span></span> <span data-ttu-id="ee6a8-127">メッセージ サービスは、メッセージ サービスのエントリ ポイント関数から**DoConfigPropSheet**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ee6a8-127">Message services call **DoConfigPropSheet** from their message service entry point function.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ee6a8-128">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="ee6a8-128">Notes to callers</span></span>

<span data-ttu-id="ee6a8-129">[BuildDisplayTable](builddisplaytable.md)関数を呼び出すことによって、またはカスタム コードと、 _lpDisplayTable_パラメーターが指す、表示された表を作成できます。</span><span class="sxs-lookup"><span data-stu-id="ee6a8-129">You can create the display table pointed to by the  _lpDisplayTable_ parameter by calling the [BuildDisplayTable](builddisplaytable.md) function or with custom code.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ee6a8-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="ee6a8-130">See also</span></span>



[<span data-ttu-id="ee6a8-131">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="ee6a8-131">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="ee6a8-132">CreateIProp</span><span class="sxs-lookup"><span data-stu-id="ee6a8-132">CreateIProp</span></span>](createiprop.md)
  
[<span data-ttu-id="ee6a8-133">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="ee6a8-133">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="ee6a8-134">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ee6a8-134">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="ee6a8-135">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="ee6a8-135">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="ee6a8-136">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ee6a8-136">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="ee6a8-137">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="ee6a8-137">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="ee6a8-138">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="ee6a8-138">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="ee6a8-139">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ee6a8-139">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

