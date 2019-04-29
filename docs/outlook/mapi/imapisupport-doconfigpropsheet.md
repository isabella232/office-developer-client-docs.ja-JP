---
title: imapisupportdoconfigpropsheet
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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: cd8727104af694d456074614b5ea7c222c9b91b9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429017"
---
# <a name="imapisupportdoconfigpropsheet"></a><span data-ttu-id="52c6c-103">IMAPISupport::DoConfigPropsheet</span><span class="sxs-lookup"><span data-stu-id="52c6c-103">IMAPISupport::DoConfigPropsheet</span></span>

  
  
<span data-ttu-id="52c6c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="52c6c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="52c6c-105">構成プロパティシートを表示します。</span><span class="sxs-lookup"><span data-stu-id="52c6c-105">Displays a configuration property sheet.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="52c6c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="52c6c-106">Parameters</span></span>

 <span data-ttu-id="52c6c-107">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="52c6c-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="52c6c-108">順番プロパティシートの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="52c6c-108">[in] A handle to the parent window of the property sheet.</span></span>
    
 <span data-ttu-id="52c6c-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="52c6c-109">_ulFlags_</span></span>
  
> <span data-ttu-id="52c6c-110">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="52c6c-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="52c6c-111">_lpsztitle_</span><span class="sxs-lookup"><span data-stu-id="52c6c-111">_lpszTitle_</span></span>
  
> <span data-ttu-id="52c6c-112">順番プロパティシートのタイトルへのポインター。</span><span class="sxs-lookup"><span data-stu-id="52c6c-112">[in] A pointer to the title of the property sheet.</span></span>
    
 <span data-ttu-id="52c6c-113">_lpdisplaytable_</span><span class="sxs-lookup"><span data-stu-id="52c6c-113">_lpDisplayTable_</span></span>
  
> <span data-ttu-id="52c6c-114">順番プロパティシートに表示されるコントロールを説明する表示テーブルへのポインター。</span><span class="sxs-lookup"><span data-stu-id="52c6c-114">[in] A pointer to the display table that describes the controls to appear on the property sheet.</span></span>
    
 <span data-ttu-id="52c6c-115">_lpconfigdata_</span><span class="sxs-lookup"><span data-stu-id="52c6c-115">_lpConfigData_</span></span>
  
> <span data-ttu-id="52c6c-116">順番プロパティシートに表示される構成プロパティにアクセスするために使用される[imapiprop](imapipropiunknown.md)実装へのポインター。</span><span class="sxs-lookup"><span data-stu-id="52c6c-116">[in] A pointer to the [IMAPIProp](imapipropiunknown.md) implementation to be used for accessing the configuration properties to be displayed on the property sheet.</span></span> 
    
 <span data-ttu-id="52c6c-117">_ultoppage_</span><span class="sxs-lookup"><span data-stu-id="52c6c-117">_ulTopPage_</span></span>
  
> <span data-ttu-id="52c6c-118">順番プロパティシートの既定のトップページの0から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="52c6c-118">[in] A zero-based index to the default top page of the property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="52c6c-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="52c6c-119">Return value</span></span>

<span data-ttu-id="52c6c-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="52c6c-120">S_OK</span></span> 
  
> <span data-ttu-id="52c6c-121">構成プロパティシートが表示されました。</span><span class="sxs-lookup"><span data-stu-id="52c6c-121">The configuration property sheet was displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="52c6c-122">注釈</span><span class="sxs-lookup"><span data-stu-id="52c6c-122">Remarks</span></span>

<span data-ttu-id="52c6c-123">**imapisupport::D oconfigpropsheet**メソッドは、すべてのサポートオブジェクトに実装されています。</span><span class="sxs-lookup"><span data-stu-id="52c6c-123">The **IMAPISupport::DoConfigPropsheet** method is implemented for all support objects.</span></span> <span data-ttu-id="52c6c-124">**doconfigpropsheet**は、サービスプロバイダーとメッセージサービスのプロパティを表示するための標準的なユーザーインターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="52c6c-124">**DoConfigPropSheet** provides a standard user interface for displaying the properties of service providers and message services.</span></span> <span data-ttu-id="52c6c-125">ユーザーが一貫した Windows インターフェイスを利用できるようにするには、すべての構成プロパティでこの標準ダイアログボックスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="52c6c-125">You should use this standard dialog box for all configuration property displays so that users benefit from a consistent Windows interface.</span></span> 
  
<span data-ttu-id="52c6c-126">サービスプロバイダーは、 [imapistatus:: settingsdialog](imapistatus-settingsdialog.md)メソッドの実装の一部として、またはプロパティの詳細を表示するために使用されるボタンから、 **doconfigpropsheet**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="52c6c-126">Service providers call **DoConfigPropSheet** as part of their implementation of the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method or from a button used to display details on properties.</span></span> <span data-ttu-id="52c6c-127">メッセージサービスは、メッセージサービスエントリポイント関数から**doconfigpropsheet**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="52c6c-127">Message services call **DoConfigPropSheet** from their message service entry point function.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="52c6c-128">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="52c6c-128">Notes to callers</span></span>

<span data-ttu-id="52c6c-129">_lpdisplaytable_パラメーターによって示される表示テーブルは、 [builddisplaytable](builddisplaytable.md)関数またはカスタムコードを呼び出すことによって作成できます。</span><span class="sxs-lookup"><span data-stu-id="52c6c-129">You can create the display table pointed to by the  _lpDisplayTable_ parameter by calling the [BuildDisplayTable](builddisplaytable.md) function or with custom code.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="52c6c-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="52c6c-130">See also</span></span>



[<span data-ttu-id="52c6c-131">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="52c6c-131">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="52c6c-132">CreateIProp</span><span class="sxs-lookup"><span data-stu-id="52c6c-132">CreateIProp</span></span>](createiprop.md)
  
[<span data-ttu-id="52c6c-133">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="52c6c-133">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="52c6c-134">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="52c6c-134">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="52c6c-135">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="52c6c-135">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="52c6c-136">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="52c6c-136">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="52c6c-137">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="52c6c-137">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="52c6c-138">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="52c6c-138">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="52c6c-139">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="52c6c-139">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

