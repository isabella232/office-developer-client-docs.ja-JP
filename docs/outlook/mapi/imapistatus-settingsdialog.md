---
title: IMAPIStatusSettingsDialog
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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 09a14a3cc9f77527c6bc254dc703328f2c9ce9f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800718"
---
# <a name="imapistatussettingsdialog"></a><span data-ttu-id="e7a32-103">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="e7a32-103">IMAPIStatus::SettingsDialog</span></span>

  
  
<span data-ttu-id="e7a32-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e7a32-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e7a32-105">MAPI が実装している状態のオブジェクトでこのメソッドがサポートされていないサービス ・ プロバイダーの構成を変更するユーザーを有効にするプロパティ シートを表示します。</span><span class="sxs-lookup"><span data-stu-id="e7a32-105">Displays a property sheet that enables the user to change a service provider's configuration This method is not supported in status objects that MAPI implements.</span></span>
  
```cpp
HRESULT SettingsDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e7a32-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e7a32-106">Parameters</span></span>

 <span data-ttu-id="e7a32-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="e7a32-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="e7a32-108">[in]構成のプロパティ シートの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="e7a32-108">[in] A handle to the parent window of the configuration property sheet.</span></span>
    
 <span data-ttu-id="e7a32-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e7a32-109">_ulFlags_</span></span>
  
> <span data-ttu-id="e7a32-110">[in]プロパティ シートの表示を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="e7a32-110">[in] A bitmask of flags that controls the display of the property sheet.</span></span> <span data-ttu-id="e7a32-111">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="e7a32-111">The following flag can be set:</span></span>
    
<span data-ttu-id="e7a32-112">UI_READONLY</span><span class="sxs-lookup"><span data-stu-id="e7a32-112">UI_READONLY</span></span> 
  
> <span data-ttu-id="e7a32-113">プロバイダーをユーザー設定のプロパティを変更するのには有効にする必要があることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e7a32-113">Suggests that the provider should not enable users to change configuration properties.</span></span> <span data-ttu-id="e7a32-114">このフラグは、単なる提案です。無視することができます。</span><span class="sxs-lookup"><span data-stu-id="e7a32-114">This flag is only a suggestion; it can be ignored.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e7a32-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="e7a32-115">Return value</span></span>

<span data-ttu-id="e7a32-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="e7a32-116">S_OK</span></span> 
  
> <span data-ttu-id="e7a32-117">構成のプロパティ シートが正常に表示されます。</span><span class="sxs-lookup"><span data-stu-id="e7a32-117">The configuration property sheet was displayed successfully.</span></span>
    
<span data-ttu-id="e7a32-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="e7a32-118">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="e7a32-119">状態オブジェクトは、このメソッドをサポートしていません**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) のプロパティに STATUS_SETTINGS_DIALOG フラグがない場合で示される。</span><span class="sxs-lookup"><span data-stu-id="e7a32-119">The status object does not support this method, as indicated by the absence of the STATUS_SETTINGS_DIALOG flag in the **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e7a32-120">注釈</span><span class="sxs-lookup"><span data-stu-id="e7a32-120">Remarks</span></span>

<span data-ttu-id="e7a32-121">**IMAPIStatus::SettingsDialog**メソッドでは、[設定] プロパティ シートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e7a32-121">The **IMAPIStatus::SettingsDialog** method displays a configuration property sheet.</span></span> <span data-ttu-id="e7a32-122">すべてのサービス プロバイダーは、 **SettingsDialog**メソッドをサポートする必要がありますが、必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="e7a32-122">All service providers should support the **SettingsDialog** method, but it is not required.</span></span> <span data-ttu-id="e7a32-123">サービス プロバイダーでは、独自のプロパティ シートを実装したり、サポート オブジェクトの[IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md)メソッドで指定された実装を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="e7a32-123">Service providers can implement their own property sheets or use the implementation supplied in the support object's [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method.</span></span> <span data-ttu-id="e7a32-124">**DoConfigPropsheet**は、読み取り/書き込みプロパティ シートを作成します。</span><span class="sxs-lookup"><span data-stu-id="e7a32-124">**DoConfigPropsheet** builds a read/write property sheet.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e7a32-125">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="e7a32-125">Notes to implementers</span></span>

<span data-ttu-id="e7a32-126">リモート トランスポート プロバイダーに設定がある場合は、以下を実行にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e7a32-126">If a remote transport provider has any settings, it should do the following:</span></span>
  
- <span data-ttu-id="e7a32-127">トランスポート プロバイダーのプロファイル セクションを開きます。</span><span class="sxs-lookup"><span data-stu-id="e7a32-127">Open the transport provider's profile section.</span></span>
    
- <span data-ttu-id="e7a32-128">プロファイルから、トランスポート プロバイダーのプロパティの設定値を取得します。</span><span class="sxs-lookup"><span data-stu-id="e7a32-128">Get the transport provider's property settings from the profile.</span></span>
    
- <span data-ttu-id="e7a32-129">ダイアログ ボックスでプロパティの設定を表示します。</span><span class="sxs-lookup"><span data-stu-id="e7a32-129">Display the property settings in a dialog box.</span></span>
    
- <span data-ttu-id="e7a32-130">ダイアログ ボックスは、プロパティの設定の編集を許可している場合は、新しい設定が有効ですし、トランスポート プロバイダーのプロファイル セクションに保存を確認してください。</span><span class="sxs-lookup"><span data-stu-id="e7a32-130">If the dialog box allows editing of the property settings, check that the new settings are valid and store them back in the transport provider's profile section.</span></span>
    
- <span data-ttu-id="e7a32-131">S_OK、または上記の手順の実行中に返されたエラー値を返します。</span><span class="sxs-lookup"><span data-stu-id="e7a32-131">Return S_OK, or any error values returned during the preceding steps.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="e7a32-132">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="e7a32-132">Notes to callers</span></span>

<span data-ttu-id="e7a32-133">**SettingsDialog**を使用して表示されるプロパティ シートを使用して、さまざまな次のように、タスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="e7a32-133">You can use the property sheet displayed through **SettingsDialog** to perform a variety of tasks, such as the following:</span></span> 
  
- <span data-ttu-id="e7a32-134">既定のメッセージ ストアを指定します。</span><span class="sxs-lookup"><span data-stu-id="e7a32-134">Specify a default message store.</span></span>
    
- <span data-ttu-id="e7a32-135">トランスポートの順番を指定します。</span><span class="sxs-lookup"><span data-stu-id="e7a32-135">Specify a transport order.</span></span>
    
- <span data-ttu-id="e7a32-136">参照の既定のアドレス帳コンテナーを指定します。</span><span class="sxs-lookup"><span data-stu-id="e7a32-136">Specify a default address book container for browsing.</span></span>
    
- <span data-ttu-id="e7a32-137">あいまいな名前を解決するための検索順序を指定します。</span><span class="sxs-lookup"><span data-stu-id="e7a32-137">Specify a search order for resolving ambiguous names.</span></span>
    
- <span data-ttu-id="e7a32-138">既定の個人用アドレス帳を指定します。</span><span class="sxs-lookup"><span data-stu-id="e7a32-138">Specify a default personal address book.</span></span>
    
<span data-ttu-id="e7a32-139">サービス プロバイダーには、読み取り/書き込み、読み取り専用プロパティ シートまたはプロパティによって、アクセス許可の両方を実装できます。</span><span class="sxs-lookup"><span data-stu-id="e7a32-139">Service providers can implement property sheets that are read/write, read-only, or a mixture of permissions, depending on the property.</span></span> <span data-ttu-id="e7a32-140">サービス プロバイダーは、プロパティの制限を設定することにより、個々 のプロパティに異なるアクセス許可を実装できます。</span><span class="sxs-lookup"><span data-stu-id="e7a32-140">Service providers can implement different permissions on individual properties by setting property restrictions.</span></span> <span data-ttu-id="e7a32-141">プロパティ シートの既定のモードは、読み取り/書き込みです。</span><span class="sxs-lookup"><span data-stu-id="e7a32-141">The default mode for property sheets is read/write.</span></span> <span data-ttu-id="e7a32-142">**SettingsDialog**の呼び出しで、UI_READONLY フラグを設定することにより、読み取り専用のプロパティ シートを要求できます。</span><span class="sxs-lookup"><span data-stu-id="e7a32-142">You can request read-only property sheets by setting the UI_READONLY flag in your calls to **SettingsDialog**.</span></span> <span data-ttu-id="e7a32-143">サービス ・ プロバイダーは読み取り専用のプロパティ シートを実装することはできます。</span><span class="sxs-lookup"><span data-stu-id="e7a32-143">Service providers that are able to implement read-only property sheets can do so.</span></span> <span data-ttu-id="e7a32-144">ただし、一部のサービス プロバイダーは、既定のモードをオーバーライドできません、ためいずれかの種類のプロパティ シートを処理するために準備する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e7a32-144">However, because some service providers cannot override the default mode, you must be prepared to handle property sheets of either type.</span></span> 
  
<span data-ttu-id="e7a32-145">ユーザー インターフェイスが常にこの操作の関係を対話型のクライアントのみが**SettingsDialog**を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e7a32-145">Because a user interface is always involved in this operation, only interactive clients should call **SettingsDialog**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e7a32-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="e7a32-146">See also</span></span>



[<span data-ttu-id="e7a32-147">IMAPISupport::DoConfigPropsheet</span><span class="sxs-lookup"><span data-stu-id="e7a32-147">IMAPISupport::DoConfigPropsheet</span></span>](imapisupport-doconfigpropsheet.md)
  
[<span data-ttu-id="e7a32-148">PidTagResourceMethods 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e7a32-148">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="e7a32-149">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e7a32-149">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

