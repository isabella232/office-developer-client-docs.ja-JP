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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a120fb1710bf2bd351d956e4d05eb0af346ef4c5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583387"
---
# <a name="iablogonopentemplateid"></a><span data-ttu-id="37abf-103">IABLogon::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="37abf-103">IABLogon::OpenTemplateID</span></span>

  
  
<span data-ttu-id="37abf-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37abf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37abf-105">ホストのアドレス帳プロバイダーに存在するデータが含まれている受信者のエントリが表示されます。</span><span class="sxs-lookup"><span data-stu-id="37abf-105">Opens a recipient entry that has data residing in a host address book provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="37abf-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37abf-106">Parameters</span></span>

 <span data-ttu-id="37abf-107">_cbTemplateID_</span><span class="sxs-lookup"><span data-stu-id="37abf-107">_cbTemplateID_</span></span>
  
> <span data-ttu-id="37abf-108">[in]_LpTemplateID_パラメーターで指定されたテンプレートの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="37abf-108">[in] The byte count in the template identifier pointed to by the  _lpTemplateID_ parameter.</span></span> 
    
 <span data-ttu-id="37abf-109">_lpTemplateID_</span><span class="sxs-lookup"><span data-stu-id="37abf-109">_lpTemplateID_</span></span>
  
> <span data-ttu-id="37abf-110">[in]テンプレート識別子、または受信者のエントリを開くことの**PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) のプロパティへのポインター。</span><span class="sxs-lookup"><span data-stu-id="37abf-110">[in] A pointer to the template identifier, or **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property, of the recipient entry to be opened.</span></span>
    
 <span data-ttu-id="37abf-111">_ulTemplateFlags_</span><span class="sxs-lookup"><span data-stu-id="37abf-111">_ulTemplateFlags_</span></span>
  
> <span data-ttu-id="37abf-112">[in]テンプレート識別子によって表される項目を開く方法を指定するためのフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="37abf-112">[in] A bitmask of flags used to indicate how to open the entry represented by the template identifier.</span></span> <span data-ttu-id="37abf-113">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="37abf-113">The following flag can be set:</span></span>
    
<span data-ttu-id="37abf-114">FILL_ENTRY</span><span class="sxs-lookup"><span data-stu-id="37abf-114">FILL_ENTRY</span></span> 
  
> <span data-ttu-id="37abf-115">テンプレート識別子によって表される項目に基づいて、コンテナーでホスト プロバイダーに新しいエントリを作成しています。</span><span class="sxs-lookup"><span data-stu-id="37abf-115">The host provider is creating a new entry in its container based on the entry represented by the template identifier.</span></span> <span data-ttu-id="37abf-116">**IABLogon::OpenTemplateID**メソッドを使用してホスト プロバイダーのエントリの特定の初期化を実行する必要がありますか、 [IMAPIProp: IUnknown](imapipropiunknown.md) _lpMAPIPropData_のパラメーターまたは戻り値のカスタム**IMAPIProp の実装**インターフェイスの実装は、 _lppMAPIPropNew_パラメーターにします。</span><span class="sxs-lookup"><span data-stu-id="37abf-116">The **IABLogon::OpenTemplateID** method should either perform specific initialization of the host provider's entry by using the [IMAPIProp : IUnknown](imapipropiunknown.md) implementation in the  _lpMAPIPropData_ parameter, or return a custom **IMAPIProp** interface implementation in the  _lppMAPIPropNew_ parameter.</span></span> 
    
 <span data-ttu-id="37abf-117">_lpMAPIPropData_</span><span class="sxs-lookup"><span data-stu-id="37abf-117">_lpMAPIPropData_</span></span>
  
> <span data-ttu-id="37abf-118">[in]**IMAPIProp**から派生したホスト プロバイダーのプロパティのオブジェクトとインターフェイスの実装へのポインター。</span><span class="sxs-lookup"><span data-stu-id="37abf-118">[in] A pointer to the host provider's property object and implementation of an interface derived from **IMAPIProp**.</span></span>
    
 <span data-ttu-id="37abf-119">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="37abf-119">_lpInterface_</span></span>
  
> <span data-ttu-id="37abf-120">[in]_LppMAPIPropNew_パラメーターで返されるインターフェイス ポインターの型を表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="37abf-120">[in] A pointer to the interface identifier (IID) that represents the type of interface pointer to be returned in the  _lppMAPIPropNew_ parameter.</span></span> <span data-ttu-id="37abf-121">標準のユーザー インターフェイスのメッセージを返します**null**を渡す[IMailUser: IMAPIProp](imailuserimapiprop.md)。</span><span class="sxs-lookup"><span data-stu-id="37abf-121">Passing **null** returns the standard messaging user interface, [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span>
    
 <span data-ttu-id="37abf-122">_lppMAPIPropNew_</span><span class="sxs-lookup"><span data-stu-id="37abf-122">_lppMAPIPropNew_</span></span>
  
> <span data-ttu-id="37abf-123">[out]**IMAPIProp**から派生したプロパティがバインドされているオブジェクトとインターフェイスの実装へのポインター。</span><span class="sxs-lookup"><span data-stu-id="37abf-123">[out] A pointer to the bound property object and an implementation of an interface derived from **IMAPIProp**.</span></span>
    
 <span data-ttu-id="37abf-124">_lpMAPIPropSibling_</span><span class="sxs-lookup"><span data-stu-id="37abf-124">_lpMAPIPropSibling_</span></span>
  
> <span data-ttu-id="37abf-125">[out]予約されています。**null**にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="37abf-125">[out] Reserved; must be **null**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="37abf-126">�߂�l</span><span class="sxs-lookup"><span data-stu-id="37abf-126">Return value</span></span>

<span data-ttu-id="37abf-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="37abf-127">S_OK</span></span> 
  
> <span data-ttu-id="37abf-128">適切なコードは、ホスト プロバイダーに関連するデータを正常にバインドされました。</span><span class="sxs-lookup"><span data-stu-id="37abf-128">The appropriate code was successfully bound to related data in the host provider.</span></span>
    
<span data-ttu-id="37abf-129">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="37abf-129">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="37abf-130">オブジェクトは、テンプレートの Id をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="37abf-130">The object does not support template IDs.</span></span>
    
<span data-ttu-id="37abf-131">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="37abf-131">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="37abf-132">アドレス帳プロバイダーでは、 _lpTemplateID_パラメーターに渡されるテンプレート識別子は認識されません。</span><span class="sxs-lookup"><span data-stu-id="37abf-132">The template identifier passed in the  _lpTemplateID_ parameter is not recognized by the address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="37abf-133">注釈</span><span class="sxs-lookup"><span data-stu-id="37abf-133">Remarks</span></span>

<span data-ttu-id="37abf-134">**IABLogon::OpenTemplateID**メソッドは、ホスト プロバイダーのコンテナー内にあるそれぞれのエントリのコピーの制御を維持する必要のあるアドレス帳プロバイダーによってのみ実装されます。</span><span class="sxs-lookup"><span data-stu-id="37abf-134">The **IABLogon::OpenTemplateID** method is implemented only by address book providers that need to maintain control over copies of their entries that are located in the containers of host providers.</span></span> <span data-ttu-id="37abf-135">**OpenTemplateID**を実装するプロバイダーは、外部のアドレス帳プロバイダーと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="37abf-135">Providers that implement **OpenTemplateID** are known as foreign address book providers.</span></span> <span data-ttu-id="37abf-136">ホスト プロバイダーがコピーしたエントリを作成またはコピーした項目を開くには、 [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)を呼び出すし、MAPI は、 **IABLogon::OpenTemplateID**の呼び出しに渡されます。</span><span class="sxs-lookup"><span data-stu-id="37abf-136">Host providers call [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) to create a copied entry or open the copied entry, and MAPI passes on the call to **IABLogon::OpenTemplateID**.</span></span> <span data-ttu-id="37abf-137">**IABLogon::OpenTemplateID**は、エントリを表示し、ホスト プロバイダー内のデータにそれを制御するコードをバインドします。</span><span class="sxs-lookup"><span data-stu-id="37abf-137">**IABLogon::OpenTemplateID** opens the entry and binds the code that controls it to data in the host provider.</span></span> 
  
<span data-ttu-id="37abf-138">エントリ id を使用するのではなく、 **IABLogon::OpenTemplateID**は、エントリのテンプレートの識別子、 **PR_TEMPLATEID**、別のプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="37abf-138">Rather than use an entry identifier, **IABLogon::OpenTemplateID** uses another property, the entry's template identifier, **PR_TEMPLATEID**.</span></span> <span data-ttu-id="37abf-139">テンプレート識別子は、ホスト プロバイダーでのデータにバインドする必要がありますコードを持つエントリをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="37abf-139">Template identifiers should be supported for entries whose code must be bound to data in a host provider.</span></span>
  
<span data-ttu-id="37abf-140">いくつかのアドレス帳プロバイダーが**IABLogon::OpenTemplateID**を実装する場合の例は次のとおり。</span><span class="sxs-lookup"><span data-stu-id="37abf-140">Some examples of when an address book provider should implement **IABLogon::OpenTemplateID** are as follows:</span></span> 
  
- <span data-ttu-id="37abf-141">そのままとするためにコピーしたエントリのデータを定期的に更新するには、元と同期されます。</span><span class="sxs-lookup"><span data-stu-id="37abf-141">To periodically update the data for a copied entry so that it stays synchronized with the original.</span></span>
    
- <span data-ttu-id="37abf-142">機能を実装する動的にサーバー上のデータからのエントリの詳細の表に表示される一覧の作成など、ホスト プロバイダーを実装できません。</span><span class="sxs-lookup"><span data-stu-id="37abf-142">To implement functionality that the host provider cannot implement, such as dynamically populating a list that appears in the entry's details table from data on a server.</span></span>
    
- <span data-ttu-id="37abf-143">ホスト プロバイダーのエントリのプロパティと、 **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) を含む別の詳細表示の編集コントロールの値からの計算など、元のエントリとの間の対話を制御するにはアドレスのコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="37abf-143">To control the interaction between properties in the host provider's entry and the original entry, such as computing the **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) from the values of the edit controls in the details display that contain different components of the address.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="37abf-144">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="37abf-144">Notes to implementers</span></span>

<span data-ttu-id="37abf-145">ホスト プロバイダーにコピーまたは、プロバイダーからのエントリを作成し、 **IABLogon::OpenTemplateID**を通じてプロパティ オブジェクトの実装を指定する、ほとんどのエントリを維持するために呼び出しを処理します。</span><span class="sxs-lookup"><span data-stu-id="37abf-145">When a host provider copies or creates an entry from your provider and you supply a property object implementation through **IABLogon::OpenTemplateID**, you handle most of the calls to maintain the entry.</span></span> <span data-ttu-id="37abf-146">ただし、ホスト プロバイダーにこれらの呼び出しを転送するため、ホスト プロバイダーの呼び出しを傍受でき、呼び出しを転送する前にカスタム処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="37abf-146">However, because it is up to the host provider to forward these calls to you, the host provider can intercept any call and perform custom processing before forwarding the call.</span></span>
  
<span data-ttu-id="37abf-147">プロパティのオブジェクトの実装では、次のガイドラインを使用してください。</span><span class="sxs-lookup"><span data-stu-id="37abf-147">You should use the following guidelines in your property object implementations:</span></span>
  
- <span data-ttu-id="37abf-148">[IMAPIProp::GetProps](imapiprop-getprops.md)が呼び出されると場合は、処理と計算されたプロパティは、要求するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="37abf-148">When [IMAPIProp::GetProps](imapiprop-getprops.md) is called, determine whether the request is for a computed property and, if it is, handle it.</span></span> <span data-ttu-id="37abf-149">ホスト プロバイダーには、メジャーのプロパティに対するすべての要求を転送します。</span><span class="sxs-lookup"><span data-stu-id="37abf-149">Transfer all requests for noncomputed properties to the host provider.</span></span> 
    
- <span data-ttu-id="37abf-150">開くには[IMAPIProp::OpenProperty](imapiprop-openproperty.md)が呼び出されたときに詳細を除く任意のテーブルはテーブルを表示する、要求を処理します。</span><span class="sxs-lookup"><span data-stu-id="37abf-150">When [IMAPIProp::OpenProperty](imapiprop-openproperty.md) is called to open any table except the details display table, handle the request.</span></span> <span data-ttu-id="37abf-151">ほとんどのテーブルは、ホスト プロバイダーに正確にコピーできません。</span><span class="sxs-lookup"><span data-stu-id="37abf-151">Most tables cannot be copied accurately to the host provider.</span></span> <span data-ttu-id="37abf-152">**IMAPITable**実装これらの要求されたテーブルを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="37abf-152">You must generate the **IMAPITable** implementation for these requested tables.</span></span> <span data-ttu-id="37abf-153">ホスト プロバイダーに詳細テーブルの**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) のプロパティをコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="37abf-153">The details table **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property must be copied to the host provider.</span></span> <span data-ttu-id="37abf-154">これにより、ローカルにテーブルを生成するには、このプロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="37abf-154">This allows this provider to generate the table locally.</span></span> <span data-ttu-id="37abf-155">表示テーブルの通知を生成するテーブルの表示の実装をラップすることもできます。</span><span class="sxs-lookup"><span data-stu-id="37abf-155">You might want to wrap the display table implementation to generate display table notifications.</span></span> 
    
- <span data-ttu-id="37abf-156">[IMAPIProp::SetProps](imapiprop-setprops.md)が呼び出されると、ホスト プロバイダーは、プロパティを設定するを許可する前にデータを検証できます。</span><span class="sxs-lookup"><span data-stu-id="37abf-156">When [IMAPIProp::SetProps](imapiprop-setprops.md) is called, the host provider can validate the data before letting you set the properties.</span></span> <span data-ttu-id="37abf-157">すべての必要なプロパティが設定された計算を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="37abf-157">You can verify that all of the necessary properties were set or computed.</span></span> <span data-ttu-id="37abf-158">エラーが検出された場合は、適切なエラー値を返すと、可能なら、 [IMAPIProp::GetLastError](imapiprop-getlasterror.md)で、追加の説明です。</span><span class="sxs-lookup"><span data-stu-id="37abf-158">If an error is detected, return the appropriate error value and, if you can, any additional explanation through [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span></span>
    
- <span data-ttu-id="37abf-159">[IMAPIProp::SaveChanges](imapiprop-savechanges.md)が呼び出されると、ホスト プロバイダーすることも、エントリを保存する前に、処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="37abf-159">When [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called, the host provider might want to perform processing before you save the entry.</span></span> <span data-ttu-id="37abf-160">ホスト プロバイダーのエントリで、新しいアドレスなど、変更されたプロパティの影響を受けるすべてのデータを保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="37abf-160">You should save any data that is affected by the changed properties, such as a new address, in the host provider's entry.</span></span> 
    
<span data-ttu-id="37abf-161">一般に、ホスト プロバイダーに渡されたエントリの実装を行うすべての関連するプロパティのコンテキストに固有の操作を実行するメソッドをインターセプトします。</span><span class="sxs-lookup"><span data-stu-id="37abf-161">In general, make your implementation of the entry that you pass back to the host provider intercept all of the methods to perform context-specific manipulation of the relevant properties.</span></span> <span data-ttu-id="37abf-162">FILL_ENTRY フラグが_ulTemplateFlags_パラメーターで渡された場合は、エントリのすべてのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="37abf-162">If the FILL_ENTRY flag is passed in the  _ulTemplateFlags_ parameter, set all properties for the entry.</span></span> 
  
<span data-ttu-id="37abf-163">_LppMAPIPropNew_パラメーターで新しい property オブジェクトを取得する場合は、参照を維持するために、ホスト プロバイダーのプロパティのオブジェクトの[IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="37abf-163">If you return a new property object in the  _lppMAPIPropNew_ parameter, call the [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) method of the host provider's property object to maintain a reference.</span></span> <span data-ttu-id="37abf-164">**IMAPIProp**実装は、 _lppMAPIPropNew_で返されるバインドされたオブジェクトをすべての呼び出しをルーティングするプロパティのホスト オブジェクトのそれぞれの対応するメソッドにバインドされたオブジェクトによって処理される、後。</span><span class="sxs-lookup"><span data-stu-id="37abf-164">All calls through the bound object that the **IMAPIProp** implementation returned in  _lppMAPIPropNew_ should be routed to their corresponding method in the host property object after they are dealt with by the bound object.</span></span> 
  
<span data-ttu-id="37abf-165">バインドされたプロパティ オブジェクトを通じて渡される任意の名前付きプロパティのプロパティ id は、プロバイダーの識別子の名前空間には。</span><span class="sxs-lookup"><span data-stu-id="37abf-165">The property identifiers of any named properties that are passed through your bound property object are in your provider's identifier namespace.</span></span> <span data-ttu-id="37abf-166">[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)メソッドの実装は、任意のテンプレートに固有のタスクを実行できるようにするプロパティの名前を判断します。</span><span class="sxs-lookup"><span data-stu-id="37abf-166">Your implementation of the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) method should determine the names of the properties so that it can perform any template-specific tasks.</span></span> <span data-ttu-id="37abf-167">同様に、ホスト プロバイダーに渡す、プロバイダーのプロパティは、名前空間である必要があります。</span><span class="sxs-lookup"><span data-stu-id="37abf-167">Similarly, properties that your provider passes on to the host provider must also be in your namespace.</span></span> <span data-ttu-id="37abf-168">などの**OpenTemplateID**では、名前付きプロパティを設定する場合必要がありますを使用する、識別子の 1 つの名前- [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)メソッドを呼び出すことによって、必要に応じて、作成します。</span><span class="sxs-lookup"><span data-stu-id="37abf-168">For example, if you set a named property in **OpenTemplateID**, you should use one of your identifiers for the name—creating it, if necessary, by calling the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> 
  
<span data-ttu-id="37abf-169">_LpTemplateID_に渡されたエントリ id を認識していない場合は、MAPI_E_UNKNOWN_ENTRYID を返します。</span><span class="sxs-lookup"><span data-stu-id="37abf-169">If you do not recognize the entry identifier passed in  _lpTemplateID_, return MAPI_E_UNKNOWN_ENTRYID.</span></span>
  
<span data-ttu-id="37abf-170">アドレス帳テンプレートの識別子を操作する方法の詳細については、[外部のアドレス帳プロバイダーとしての機能](acting-as-a-foreign-address-book-provider.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="37abf-170">For more information about how to work with address book template identifiers, see [Acting as a Foreign Address Book Provider](acting-as-a-foreign-address-book-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="37abf-171">関連項目</span><span class="sxs-lookup"><span data-stu-id="37abf-171">See also</span></span>



[<span data-ttu-id="37abf-172">IMAPISupport::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="37abf-172">IMAPISupport::OpenTemplateID</span></span>](imapisupport-opentemplateid.md)
  
[<span data-ttu-id="37abf-173">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="37abf-173">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="37abf-174">PidTagTemplateid 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="37abf-174">PidTagTemplateid Canonical Property</span></span>](pidtagtemplateid-canonical-property.md)
  
[<span data-ttu-id="37abf-175">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="37abf-175">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

