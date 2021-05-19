---
title: IABLogonOpenTemplateID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenTemplateID
api_type:
- COM
ms.assetid: 751c36d3-c39e-4357-a60a-88685a378de0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: bc68878a25873533162df7e1671e483c3bb77865
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334749"
---
# <a name="iablogonopentemplateid"></a><span data-ttu-id="1e801-103">IABLogon::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="1e801-103">IABLogon::OpenTemplateID</span></span>

  
  
<span data-ttu-id="1e801-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e801-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e801-105">ホスト アドレス帳プロバイダーに存在するデータを含む受信者エントリを開きます。</span><span class="sxs-lookup"><span data-stu-id="1e801-105">Opens a recipient entry that has data residing in a host address book provider.</span></span>
  
```cpp
HRESULT OpenTemplateID(
  ULONG cbTemplateID,
  LPENTRYID lpTemplateID,
  ULONG ulTemplateFlags,
  LPMAPIPROP lpMAPIPropData,
  LPCIID lpInterface,
  LPMAPIPROP FAR * lppMAPIPropNew,
  LPMAPIPROP lpMAPIPropSibling
);
```

## <a name="parameters"></a><span data-ttu-id="1e801-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1e801-106">Parameters</span></span>

 <span data-ttu-id="1e801-107">_cbTemplateID_</span><span class="sxs-lookup"><span data-stu-id="1e801-107">_cbTemplateID_</span></span>
  
> <span data-ttu-id="1e801-108">[in]  _lpTemplateID_ パラメーターが指すテンプレート識別子のバイト 数。</span><span class="sxs-lookup"><span data-stu-id="1e801-108">[in] The byte count in the template identifier pointed to by the  _lpTemplateID_ parameter.</span></span> 
    
 <span data-ttu-id="1e801-109">_lpTemplateID_</span><span class="sxs-lookup"><span data-stu-id="1e801-109">_lpTemplateID_</span></span>
  
> <span data-ttu-id="1e801-110">[in]開く受信者エントリのテンプレート **識別子または** PR_TEMPLATEID ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) プロパティへのポインター。</span><span class="sxs-lookup"><span data-stu-id="1e801-110">[in] A pointer to the template identifier, or **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property, of the recipient entry to be opened.</span></span>
    
 <span data-ttu-id="1e801-111">_ulTemplateFlags_</span><span class="sxs-lookup"><span data-stu-id="1e801-111">_ulTemplateFlags_</span></span>
  
> <span data-ttu-id="1e801-112">[in]テンプレート識別子で表されるエントリを開く方法を示すために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="1e801-112">[in] A bitmask of flags used to indicate how to open the entry represented by the template identifier.</span></span> <span data-ttu-id="1e801-113">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="1e801-113">The following flag can be set:</span></span>
    
<span data-ttu-id="1e801-114">FILL_ENTRY</span><span class="sxs-lookup"><span data-stu-id="1e801-114">FILL_ENTRY</span></span> 
  
> <span data-ttu-id="1e801-115">ホスト プロバイダーは、テンプレート識別子で表されるエントリに基づいて、コンテナー内に新しいエントリを作成しています。</span><span class="sxs-lookup"><span data-stu-id="1e801-115">The host provider is creating a new entry in its container based on the entry represented by the template identifier.</span></span> <span data-ttu-id="1e801-116">**IABLogon::OpenTemplateID** メソッドは [、imapIProp : iUnknown](imapipropiunknown.md)実装を _lpMAPIPropData_ パラメーターで使用してホスト プロバイダーのエントリの特定の初期化を実行するか _、lppMAPIPropNew_ パラメーターでカスタム **IMAPIProp** インターフェイス実装を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e801-116">The **IABLogon::OpenTemplateID** method should either perform specific initialization of the host provider's entry by using the [IMAPIProp : IUnknown](imapipropiunknown.md) implementation in the  _lpMAPIPropData_ parameter, or return a custom **IMAPIProp** interface implementation in the  _lppMAPIPropNew_ parameter.</span></span> 
    
 <span data-ttu-id="1e801-117">_lpMAPIPropData_</span><span class="sxs-lookup"><span data-stu-id="1e801-117">_lpMAPIPropData_</span></span>
  
> <span data-ttu-id="1e801-118">[in]ホスト プロバイダーのプロパティ オブジェクトへのポインターと **IMAPIProp** から派生したインターフェイスの実装。</span><span class="sxs-lookup"><span data-stu-id="1e801-118">[in] A pointer to the host provider's property object and implementation of an interface derived from **IMAPIProp**.</span></span>
    
 <span data-ttu-id="1e801-119">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="1e801-119">_lpInterface_</span></span>
  
> <span data-ttu-id="1e801-120">[in]  _lppMAPIPropNew_ パラメーターで返されるインターフェイス ポインターの種類を表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1e801-120">[in] A pointer to the interface identifier (IID) that represents the type of interface pointer to be returned in the  _lppMAPIPropNew_ parameter.</span></span> <span data-ttu-id="1e801-121">**null を渡** すと、標準のメッセージング ユーザー インターフェイス [IMailUser : IMAPIProp が返されます](imailuserimapiprop.md)。</span><span class="sxs-lookup"><span data-stu-id="1e801-121">Passing **null** returns the standard messaging user interface, [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span>
    
 <span data-ttu-id="1e801-122">_lppMAPIPropNew_</span><span class="sxs-lookup"><span data-stu-id="1e801-122">_lppMAPIPropNew_</span></span>
  
> <span data-ttu-id="1e801-123">[out]バインドされたプロパティ オブジェクトへのポインターと **IMAPIProp** から派生したインターフェイスの実装。</span><span class="sxs-lookup"><span data-stu-id="1e801-123">[out] A pointer to the bound property object and an implementation of an interface derived from **IMAPIProp**.</span></span>
    
 <span data-ttu-id="1e801-124">_lpMAPIPropSibling_</span><span class="sxs-lookup"><span data-stu-id="1e801-124">_lpMAPIPropSibling_</span></span>
  
> <span data-ttu-id="1e801-125">[out]予約済み。null である **必要があります**。</span><span class="sxs-lookup"><span data-stu-id="1e801-125">[out] Reserved; must be **null**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1e801-126">戻り値</span><span class="sxs-lookup"><span data-stu-id="1e801-126">Return value</span></span>

<span data-ttu-id="1e801-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="1e801-127">S_OK</span></span> 
  
> <span data-ttu-id="1e801-128">適切なコードがホスト プロバイダーの関連データに正常にバインドされました。</span><span class="sxs-lookup"><span data-stu-id="1e801-128">The appropriate code was successfully bound to related data in the host provider.</span></span>
    
<span data-ttu-id="1e801-129">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="1e801-129">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="1e801-130">オブジェクトはテンプレートの ID をサポートしていない。</span><span class="sxs-lookup"><span data-stu-id="1e801-130">The object does not support template IDs.</span></span>
    
<span data-ttu-id="1e801-131">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="1e801-131">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="1e801-132">_lpTemplateID_ パラメーターで渡されたテンプレート識別子は、アドレス帳プロバイダーによって認識されません。</span><span class="sxs-lookup"><span data-stu-id="1e801-132">The template identifier passed in the  _lpTemplateID_ parameter is not recognized by the address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1e801-133">注釈</span><span class="sxs-lookup"><span data-stu-id="1e801-133">Remarks</span></span>

<span data-ttu-id="1e801-134">**IABLogon::OpenTemplateID** メソッドは、ホスト プロバイダーのコンテナーにあるエントリのコピーを管理する必要があるアドレス帳プロバイダーによってのみ実装されます。</span><span class="sxs-lookup"><span data-stu-id="1e801-134">The **IABLogon::OpenTemplateID** method is implemented only by address book providers that need to maintain control over copies of their entries that are located in the containers of host providers.</span></span> <span data-ttu-id="1e801-135">**OpenTemplateID を実装するプロバイダー** は、外部アドレス帳プロバイダーと呼ばれる。</span><span class="sxs-lookup"><span data-stu-id="1e801-135">Providers that implement **OpenTemplateID** are known as foreign address book providers.</span></span> <span data-ttu-id="1e801-136">ホスト プロバイダーは [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) を呼び出してコピーされたエントリを作成するか、コピーしたエントリを開き、MAPI は **IABLogon::OpenTemplateID** に呼び出しを渡します。</span><span class="sxs-lookup"><span data-stu-id="1e801-136">Host providers call [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) to create a copied entry or open the copied entry, and MAPI passes on the call to **IABLogon::OpenTemplateID**.</span></span> <span data-ttu-id="1e801-137">**IABLogon::OpenTemplateID は** エントリを開き、それを制御するコードをホスト プロバイダーのデータにバインドします。</span><span class="sxs-lookup"><span data-stu-id="1e801-137">**IABLogon::OpenTemplateID** opens the entry and binds the code that controls it to data in the host provider.</span></span> 
  
<span data-ttu-id="1e801-138">**IABLogon::OpenTemplateID** は、エントリ識別子を使用するのではなく、別のプロパティ (エントリのテンプレート識別子) を使用 **PR_TEMPLATEID。**</span><span class="sxs-lookup"><span data-stu-id="1e801-138">Rather than use an entry identifier, **IABLogon::OpenTemplateID** uses another property, the entry's template identifier, **PR_TEMPLATEID**.</span></span> <span data-ttu-id="1e801-139">ホスト プロバイダーのデータにコードをバインドする必要があるエントリでは、テンプレート識別子をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e801-139">Template identifiers should be supported for entries whose code must be bound to data in a host provider.</span></span>
  
<span data-ttu-id="1e801-140">アドレス帳プロバイダーが **IABLogon::OpenTemplateID** を実装する必要がある場合の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="1e801-140">Some examples of when an address book provider should implement **IABLogon::OpenTemplateID** are as follows:</span></span> 
  
- <span data-ttu-id="1e801-141">コピーしたエントリのデータを定期的に更新して、元のエントリと同期を維持するには。</span><span class="sxs-lookup"><span data-stu-id="1e801-141">To periodically update the data for a copied entry so that it stays synchronized with the original.</span></span>
    
- <span data-ttu-id="1e801-142">サーバー上のデータからエントリの詳細テーブルに表示されるリストを動的に設定するなど、ホスト プロバイダーが実装できない機能を実装する。</span><span class="sxs-lookup"><span data-stu-id="1e801-142">To implement functionality that the host provider cannot implement, such as dynamically populating a list that appears in the entry's details table from data on a server.</span></span>
    
- <span data-ttu-id="1e801-143">アドレスの異なるコンポーネントを含む詳細表示の編集コントロールの値から **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) の計算など、ホスト プロバイダーのエントリのプロパティと元のエントリの間の相互作用を制御します。</span><span class="sxs-lookup"><span data-stu-id="1e801-143">To control the interaction between properties in the host provider's entry and the original entry, such as computing the **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) from the values of the edit controls in the details display that contain different components of the address.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="1e801-144">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="1e801-144">Notes to implementers</span></span>

<span data-ttu-id="1e801-145">ホスト プロバイダーがプロバイダーからエントリをコピーまたは作成し **、IABLogon::OpenTemplateID** を使用してプロパティ オブジェクトの実装を指定すると、ほとんどの呼び出しを処理してエントリを維持します。</span><span class="sxs-lookup"><span data-stu-id="1e801-145">When a host provider copies or creates an entry from your provider and you supply a property object implementation through **IABLogon::OpenTemplateID**, you handle most of the calls to maintain the entry.</span></span> <span data-ttu-id="1e801-146">ただし、ホスト プロバイダーがこれらの呼び出しを転送する必要がある場合、ホスト プロバイダーは任意の呼び出しを傍受し、呼び出しを転送する前にカスタム処理を実行できます。</span><span class="sxs-lookup"><span data-stu-id="1e801-146">However, because it is up to the host provider to forward these calls to you, the host provider can intercept any call and perform custom processing before forwarding the call.</span></span>
  
<span data-ttu-id="1e801-147">プロパティ オブジェクトの実装では、次のガイドラインを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e801-147">You should use the following guidelines in your property object implementations:</span></span>
  
- <span data-ttu-id="1e801-148">[IMAPIProp::GetProps](imapiprop-getprops.md)が呼び出された場合は、要求が計算されたプロパティ用であるかどうかを判断し、その場合は処理します。</span><span class="sxs-lookup"><span data-stu-id="1e801-148">When [IMAPIProp::GetProps](imapiprop-getprops.md) is called, determine whether the request is for a computed property and, if it is, handle it.</span></span> <span data-ttu-id="1e801-149">非計算プロパティのすべての要求をホスト プロバイダーに転送します。</span><span class="sxs-lookup"><span data-stu-id="1e801-149">Transfer all requests for noncomputed properties to the host provider.</span></span> 
    
- <span data-ttu-id="1e801-150">[IMAPIProp::OpenProperty](imapiprop-openproperty.md)が呼び出され、詳細表示テーブル以外のテーブルを開く場合は、要求を処理します。</span><span class="sxs-lookup"><span data-stu-id="1e801-150">When [IMAPIProp::OpenProperty](imapiprop-openproperty.md) is called to open any table except the details display table, handle the request.</span></span> <span data-ttu-id="1e801-151">ほとんどのテーブルをホスト プロバイダーに正確にコピーすることはできません。</span><span class="sxs-lookup"><span data-stu-id="1e801-151">Most tables cannot be copied accurately to the host provider.</span></span> <span data-ttu-id="1e801-152">これらの要求されたテーブルに **対して IMAPITable** 実装を生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e801-152">You must generate the **IMAPITable** implementation for these requested tables.</span></span> <span data-ttu-id="1e801-153">プロパティの詳細 **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティをホスト プロバイダーにコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e801-153">The details table **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property must be copied to the host provider.</span></span> <span data-ttu-id="1e801-154">これにより、このプロバイダーはテーブルをローカルで生成できます。</span><span class="sxs-lookup"><span data-stu-id="1e801-154">This allows this provider to generate the table locally.</span></span> <span data-ttu-id="1e801-155">表示テーブルの実装をラップして、表示テーブル通知を生成する場合があります。</span><span class="sxs-lookup"><span data-stu-id="1e801-155">You might want to wrap the display table implementation to generate display table notifications.</span></span> 
    
- <span data-ttu-id="1e801-156">[IMAPIProp::SetProps](imapiprop-setprops.md)が呼び出された場合、ホスト プロバイダーは、プロパティを設定する前にデータを検証できます。</span><span class="sxs-lookup"><span data-stu-id="1e801-156">When [IMAPIProp::SetProps](imapiprop-setprops.md) is called, the host provider can validate the data before letting you set the properties.</span></span> <span data-ttu-id="1e801-157">必要なすべてのプロパティが設定または計算されたと確認できます。</span><span class="sxs-lookup"><span data-stu-id="1e801-157">You can verify that all of the necessary properties were set or computed.</span></span> <span data-ttu-id="1e801-158">エラーが検出された場合は、適切なエラー値を返し、可能な場合は [IMAPIProp::GetLastError](imapiprop-getlasterror.md)を使用して追加の説明を返します。</span><span class="sxs-lookup"><span data-stu-id="1e801-158">If an error is detected, return the appropriate error value and, if you can, any additional explanation through [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span></span>
    
- <span data-ttu-id="1e801-159">[IMAPIProp::SaveChanges](imapiprop-savechanges.md)が呼び出された場合、ホスト プロバイダーは、エントリを保存する前に処理を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e801-159">When [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called, the host provider might want to perform processing before you save the entry.</span></span> <span data-ttu-id="1e801-160">変更されたプロパティ (新しいアドレスなど) の影響を受けるデータは、ホスト プロバイダーのエントリに保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e801-160">You should save any data that is affected by the changed properties, such as a new address, in the host provider's entry.</span></span> 
    
<span data-ttu-id="1e801-161">一般に、ホスト プロバイダーに返すエントリの実装を、関連するプロパティのコンテキスト固有の操作を実行するために、すべてのメソッドをインターセプトします。</span><span class="sxs-lookup"><span data-stu-id="1e801-161">In general, make your implementation of the entry that you pass back to the host provider intercept all of the methods to perform context-specific manipulation of the relevant properties.</span></span> <span data-ttu-id="1e801-162">_ulTemplateFlags_ パラメーター FILL_ENTRYフラグが渡される場合は、エントリのすべてのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="1e801-162">If the FILL_ENTRY flag is passed in the  _ulTemplateFlags_ parameter, set all properties for the entry.</span></span> 
  
<span data-ttu-id="1e801-163">_lppMAPIPropNew_ パラメーターで新しいプロパティ オブジェクトを返す場合は、ホスト プロバイダーのプロパティ オブジェクトの [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx)メソッドを呼び出して参照を維持します。</span><span class="sxs-lookup"><span data-stu-id="1e801-163">If you return a new property object in the  _lppMAPIPropNew_ parameter, call the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method of the host provider's property object to maintain a reference.</span></span> <span data-ttu-id="1e801-164">_lppMAPIPropNew_ で **返された IMAPIProp** 実装がバインドされたオブジェクトを介してのすべての呼び出しは、バインドされたオブジェクトによって処理された後、ホスト プロパティ オブジェクト内の対応するメソッドにルーティングする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e801-164">All calls through the bound object that the **IMAPIProp** implementation returned in  _lppMAPIPropNew_ should be routed to their corresponding method in the host property object after they are dealt with by the bound object.</span></span> 
  
<span data-ttu-id="1e801-165">バインドされたプロパティ オブジェクトを介して渡される名前付きプロパティのプロパティ識別子は、プロバイダーの識別子名前空間にあります。</span><span class="sxs-lookup"><span data-stu-id="1e801-165">The property identifiers of any named properties that are passed through your bound property object are in your provider's identifier namespace.</span></span> <span data-ttu-id="1e801-166">[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)メソッドの実装では、テンプレート固有のタスクを実行できるよう、プロパティの名前を決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e801-166">Your implementation of the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) method should determine the names of the properties so that it can perform any template-specific tasks.</span></span> <span data-ttu-id="1e801-167">同様に、プロバイダーがホスト プロバイダーに渡すプロパティも名前空間に含む必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e801-167">Similarly, properties that your provider passes on to the host provider must also be in your namespace.</span></span> <span data-ttu-id="1e801-168">**たとえば、OpenTemplateID** で名前付きプロパティを設定する場合は [、IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)メソッドを呼び出して、名前の識別子の 1 つを使用する必要があります。必要に応じて作成します。</span><span class="sxs-lookup"><span data-stu-id="1e801-168">For example, if you set a named property in **OpenTemplateID**, you should use one of your identifiers for the name—creating it, if necessary, by calling the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> 
  
<span data-ttu-id="1e801-169">_lpTemplateID_ で渡されたエントリ識別子が認識されない場合は、MAPI_E_UNKNOWN_ENTRYID。</span><span class="sxs-lookup"><span data-stu-id="1e801-169">If you do not recognize the entry identifier passed in  _lpTemplateID_, return MAPI_E_UNKNOWN_ENTRYID.</span></span>
  
<span data-ttu-id="1e801-170">アドレス帳テンプレート識別子を使用する方法の詳細については、「外部アドレス帳プロバイダーとして機能する [」を参照してください](acting-as-a-foreign-address-book-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="1e801-170">For more information about how to work with address book template identifiers, see [Acting as a Foreign Address Book Provider](acting-as-a-foreign-address-book-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1e801-171">関連項目</span><span class="sxs-lookup"><span data-stu-id="1e801-171">See also</span></span>



[<span data-ttu-id="1e801-172">IMAPISupport::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="1e801-172">IMAPISupport::OpenTemplateID</span></span>](imapisupport-opentemplateid.md)
  
[<span data-ttu-id="1e801-173">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1e801-173">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="1e801-174">PidTagTemplateid 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1e801-174">PidTagTemplateid Canonical Property</span></span>](pidtagtemplateid-canonical-property.md)
  
[<span data-ttu-id="1e801-175">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1e801-175">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

