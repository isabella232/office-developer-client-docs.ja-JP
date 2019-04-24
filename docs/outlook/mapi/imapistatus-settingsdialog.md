---
title: imapistatussettingsdialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.SettingsDialog
api_type:
- COM
ms.assetid: e931246e-7fff-4116-a9fc-f685988e21e8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1e9d390a895490f2f7445c5f1ed6e0bde3a87639
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331543"
---
# <a name="imapistatussettingsdialog"></a><span data-ttu-id="08d91-103">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="08d91-103">IMAPIStatus::SettingsDialog</span></span>

  
  
<span data-ttu-id="08d91-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08d91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08d91-105">ユーザーがサービスプロバイダーの構成を変更できるようにするプロパティシートを表示します。このメソッドは、MAPI が実装する status オブジェクトではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="08d91-105">Displays a property sheet that enables the user to change a service provider's configuration This method is not supported in status objects that MAPI implements.</span></span>
  
```cpp
HRESULT SettingsDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="08d91-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="08d91-106">Parameters</span></span>

 <span data-ttu-id="08d91-107">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="08d91-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="08d91-108">順番構成プロパティシートの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="08d91-108">[in] A handle to the parent window of the configuration property sheet.</span></span>
    
 <span data-ttu-id="08d91-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="08d91-109">_ulFlags_</span></span>
  
> <span data-ttu-id="08d91-110">順番プロパティシートの表示を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="08d91-110">[in] A bitmask of flags that controls the display of the property sheet.</span></span> <span data-ttu-id="08d91-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="08d91-111">The following flag can be set:</span></span>
    
<span data-ttu-id="08d91-112">UI_READONLY</span><span class="sxs-lookup"><span data-stu-id="08d91-112">UI_READONLY</span></span> 
  
> <span data-ttu-id="08d91-113">プロバイダーが、ユーザーが構成プロパティを変更できないようにすることを提案します。</span><span class="sxs-lookup"><span data-stu-id="08d91-113">Suggests that the provider should not enable users to change configuration properties.</span></span> <span data-ttu-id="08d91-114">このフラグは、提案のみです。無視できます。</span><span class="sxs-lookup"><span data-stu-id="08d91-114">This flag is only a suggestion; it can be ignored.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="08d91-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="08d91-115">Return value</span></span>

<span data-ttu-id="08d91-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="08d91-116">S_OK</span></span> 
  
> <span data-ttu-id="08d91-117">構成プロパティシートが正常に表示されました。</span><span class="sxs-lookup"><span data-stu-id="08d91-117">The configuration property sheet was displayed successfully.</span></span>
    
<span data-ttu-id="08d91-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="08d91-118">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="08d91-119">status オブジェクトは、 **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) プロパティの STATUS_SETTINGS_DIALOG フラグが指定されていないため、このメソッドをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="08d91-119">The status object does not support this method, as indicated by the absence of the STATUS_SETTINGS_DIALOG flag in the **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="08d91-120">解説</span><span class="sxs-lookup"><span data-stu-id="08d91-120">Remarks</span></span>

<span data-ttu-id="08d91-121">**imapistatus:: settingsdialog**メソッドは、構成プロパティシートを表示します。</span><span class="sxs-lookup"><span data-stu-id="08d91-121">The **IMAPIStatus::SettingsDialog** method displays a configuration property sheet.</span></span> <span data-ttu-id="08d91-122">すべてのサービスプロバイダーは**settingsdialog**メソッドをサポートする必要がありますが、必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="08d91-122">All service providers should support the **SettingsDialog** method, but it is not required.</span></span> <span data-ttu-id="08d91-123">サービスプロバイダーは、独自のプロパティシートを実装するか、support オブジェクトの[imapisupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md)メソッドで提供される実装を使用できます。</span><span class="sxs-lookup"><span data-stu-id="08d91-123">Service providers can implement their own property sheets or use the implementation supplied in the support object's [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method.</span></span> <span data-ttu-id="08d91-124">**doconfigpropsheet**は、読み取り/書き込み可能なプロパティシートを作成します。</span><span class="sxs-lookup"><span data-stu-id="08d91-124">**DoConfigPropsheet** builds a read/write property sheet.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="08d91-125">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="08d91-125">Notes to implementers</span></span>

<span data-ttu-id="08d91-126">リモートトランスポートプロバイダーに設定がある場合は、次の操作を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="08d91-126">If a remote transport provider has any settings, it should do the following:</span></span>
  
- <span data-ttu-id="08d91-127">[トランスポートプロバイダーのプロファイル] セクションを開きます。</span><span class="sxs-lookup"><span data-stu-id="08d91-127">Open the transport provider's profile section.</span></span>
    
- <span data-ttu-id="08d91-128">プロファイルからトランスポートプロバイダーのプロパティ設定を取得します。</span><span class="sxs-lookup"><span data-stu-id="08d91-128">Get the transport provider's property settings from the profile.</span></span>
    
- <span data-ttu-id="08d91-129">プロパティの設定をダイアログボックスに表示します。</span><span class="sxs-lookup"><span data-stu-id="08d91-129">Display the property settings in a dialog box.</span></span>
    
- <span data-ttu-id="08d91-130">ダイアログボックスでプロパティの設定を編集できる場合は、新しい設定が有効になっていることを確認し、それをトランスポートプロバイダーの [プロファイル] セクションに保存します。</span><span class="sxs-lookup"><span data-stu-id="08d91-130">If the dialog box allows editing of the property settings, check that the new settings are valid and store them back in the transport provider's profile section.</span></span>
    
- <span data-ttu-id="08d91-131">S_OK、または前の手順で返されたエラー値を返します。</span><span class="sxs-lookup"><span data-stu-id="08d91-131">Return S_OK, or any error values returned during the preceding steps.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="08d91-132">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="08d91-132">Notes to callers</span></span>

<span data-ttu-id="08d91-133">**settingsdialog**を使用して表示されるプロパティシートを使用して、次のようなさまざまなタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="08d91-133">You can use the property sheet displayed through **SettingsDialog** to perform a variety of tasks, such as the following:</span></span> 
  
- <span data-ttu-id="08d91-134">既定のメッセージストアを指定します。</span><span class="sxs-lookup"><span data-stu-id="08d91-134">Specify a default message store.</span></span>
    
- <span data-ttu-id="08d91-135">トランスポート順序を指定します。</span><span class="sxs-lookup"><span data-stu-id="08d91-135">Specify a transport order.</span></span>
    
- <span data-ttu-id="08d91-136">参照用の既定のアドレス帳コンテナーを指定します。</span><span class="sxs-lookup"><span data-stu-id="08d91-136">Specify a default address book container for browsing.</span></span>
    
- <span data-ttu-id="08d91-137">あいまいな名前を解決するための検索順序を指定します。</span><span class="sxs-lookup"><span data-stu-id="08d91-137">Specify a search order for resolving ambiguous names.</span></span>
    
- <span data-ttu-id="08d91-138">既定の個人用アドレス帳を指定します。</span><span class="sxs-lookup"><span data-stu-id="08d91-138">Specify a default personal address book.</span></span>
    
<span data-ttu-id="08d91-139">サービスプロバイダーは、プロパティに応じて、読み取り/書き込み可能なプロパティシート、読み取り専用の権限、または複数の権限を組み合わせて実装することができます。</span><span class="sxs-lookup"><span data-stu-id="08d91-139">Service providers can implement property sheets that are read/write, read-only, or a mixture of permissions, depending on the property.</span></span> <span data-ttu-id="08d91-140">サービスプロバイダーは、プロパティ制限を設定することによって、個々のプロパティに対して異なる権限を実装できます。</span><span class="sxs-lookup"><span data-stu-id="08d91-140">Service providers can implement different permissions on individual properties by setting property restrictions.</span></span> <span data-ttu-id="08d91-141">プロパティシートの既定のモードは、値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="08d91-141">The default mode for property sheets is read/write.</span></span> <span data-ttu-id="08d91-142">読み取り専用のプロパティシートを要求するには、 **settingsdialog**の呼び出しで UI_READONLY フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="08d91-142">You can request read-only property sheets by setting the UI_READONLY flag in your calls to **SettingsDialog**.</span></span> <span data-ttu-id="08d91-143">読み取り専用のプロパティシートを実装できるサービスプロバイダーは、これを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="08d91-143">Service providers that are able to implement read-only property sheets can do so.</span></span> <span data-ttu-id="08d91-144">ただし、一部のサービスプロバイダーは既定のモードを上書きできないため、どちらかの種類のプロパティシートを処理できるように準備しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="08d91-144">However, because some service providers cannot override the default mode, you must be prepared to handle property sheets of either type.</span></span> 
  
<span data-ttu-id="08d91-145">ユーザーインターフェイスは常にこの操作に関係するため、interactive クライアントだけが**settingsdialog**を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="08d91-145">Because a user interface is always involved in this operation, only interactive clients should call **SettingsDialog**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="08d91-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="08d91-146">See also</span></span>



[<span data-ttu-id="08d91-147">IMAPISupport::DoConfigPropsheet</span><span class="sxs-lookup"><span data-stu-id="08d91-147">IMAPISupport::DoConfigPropsheet</span></span>](imapisupport-doconfigpropsheet.md)
  
[<span data-ttu-id="08d91-148">PidTagResourceMethods 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="08d91-148">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="08d91-149">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="08d91-149">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

