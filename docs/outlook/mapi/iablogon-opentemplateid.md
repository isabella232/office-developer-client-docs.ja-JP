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
# <a name="iablogonopentemplateid"></a><span data-ttu-id="8a07d-103">IABLogon::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="8a07d-103">IABLogon::OpenTemplateID</span></span>

  
  
<span data-ttu-id="8a07d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a07d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a07d-105">ホストアドレス帳プロバイダーに存在するデータを持つ受信者エントリを開きます。</span><span class="sxs-lookup"><span data-stu-id="8a07d-105">Opens a recipient entry that has data residing in a host address book provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="8a07d-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8a07d-106">Parameters</span></span>

 <span data-ttu-id="8a07d-107">_cbTemplateID_</span><span class="sxs-lookup"><span data-stu-id="8a07d-107">_cbTemplateID_</span></span>
  
> <span data-ttu-id="8a07d-108">順番_lpTemplateID_パラメーターによって指定されるテンプレート識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="8a07d-108">[in] The byte count in the template identifier pointed to by the  _lpTemplateID_ parameter.</span></span> 
    
 <span data-ttu-id="8a07d-109">_lpTemplateID_</span><span class="sxs-lookup"><span data-stu-id="8a07d-109">_lpTemplateID_</span></span>
  
> <span data-ttu-id="8a07d-110">順番開く受信者エントリのテンプレート識別子または**PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) プロパティへのポインター。</span><span class="sxs-lookup"><span data-stu-id="8a07d-110">[in] A pointer to the template identifier, or **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property, of the recipient entry to be opened.</span></span>
    
 <span data-ttu-id="8a07d-111">_ultemplateflags_</span><span class="sxs-lookup"><span data-stu-id="8a07d-111">_ulTemplateFlags_</span></span>
  
> <span data-ttu-id="8a07d-112">順番テンプレート識別子で表されるエントリを開く方法を示すために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="8a07d-112">[in] A bitmask of flags used to indicate how to open the entry represented by the template identifier.</span></span> <span data-ttu-id="8a07d-113">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="8a07d-113">The following flag can be set:</span></span>
    
<span data-ttu-id="8a07d-114">FILL_ENTRY</span><span class="sxs-lookup"><span data-stu-id="8a07d-114">FILL_ENTRY</span></span> 
  
> <span data-ttu-id="8a07d-115">ホストプロバイダーは、テンプレート識別子によって表されるエントリに基づいて、コンテナー内に新しいエントリを作成しています。</span><span class="sxs-lookup"><span data-stu-id="8a07d-115">The host provider is creating a new entry in its container based on the entry represented by the template identifier.</span></span> <span data-ttu-id="8a07d-116">**IABLogon:: OpenTemplateID**メソッドは、 _lpMAPIPropData_パラメーターの[imapiprop: IUnknown](imapipropiunknown.md)実装を使用してホストプロバイダーのエントリの特定の初期化を実行するか、カスタム imapiprop を返す必要があります。 \*\*\*\* _lppMAPIPropNew_パラメーターでのインターフェイスの実装。</span><span class="sxs-lookup"><span data-stu-id="8a07d-116">The **IABLogon::OpenTemplateID** method should either perform specific initialization of the host provider's entry by using the [IMAPIProp : IUnknown](imapipropiunknown.md) implementation in the  _lpMAPIPropData_ parameter, or return a custom **IMAPIProp** interface implementation in the  _lppMAPIPropNew_ parameter.</span></span> 
    
 <span data-ttu-id="8a07d-117">_lpMAPIPropData_</span><span class="sxs-lookup"><span data-stu-id="8a07d-117">_lpMAPIPropData_</span></span>
  
> <span data-ttu-id="8a07d-118">順番ホストプロバイダーの property オブジェクトへのポインターと、 **imapiprop**から派生したインターフェイスの実装。</span><span class="sxs-lookup"><span data-stu-id="8a07d-118">[in] A pointer to the host provider's property object and implementation of an interface derived from **IMAPIProp**.</span></span>
    
 <span data-ttu-id="8a07d-119">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="8a07d-119">_lpInterface_</span></span>
  
> <span data-ttu-id="8a07d-120">順番_lppMAPIPropNew_パラメーターで返されるインターフェイスポインターの種類を表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="8a07d-120">[in] A pointer to the interface identifier (IID) that represents the type of interface pointer to be returned in the  _lppMAPIPropNew_ parameter.</span></span> <span data-ttu-id="8a07d-121">**null**を渡すと、標準のメッセージングユーザーインターフェイス、 [imailuser: imapiprop](imailuserimapiprop.md)が返されます。</span><span class="sxs-lookup"><span data-stu-id="8a07d-121">Passing **null** returns the standard messaging user interface, [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span>
    
 <span data-ttu-id="8a07d-122">_lppMAPIPropNew_</span><span class="sxs-lookup"><span data-stu-id="8a07d-122">_lppMAPIPropNew_</span></span>
  
> <span data-ttu-id="8a07d-123">読み上げバインドされた property オブジェクトへのポインターと、 **imapiprop**から派生したインターフェイスの実装。</span><span class="sxs-lookup"><span data-stu-id="8a07d-123">[out] A pointer to the bound property object and an implementation of an interface derived from **IMAPIProp**.</span></span>
    
 <span data-ttu-id="8a07d-124">_lpMAPIPropSibling_</span><span class="sxs-lookup"><span data-stu-id="8a07d-124">_lpMAPIPropSibling_</span></span>
  
> <span data-ttu-id="8a07d-125">読み上げ予約語**null**である必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a07d-125">[out] Reserved; must be **null**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8a07d-126">戻り値</span><span class="sxs-lookup"><span data-stu-id="8a07d-126">Return value</span></span>

<span data-ttu-id="8a07d-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="8a07d-127">S_OK</span></span> 
  
> <span data-ttu-id="8a07d-128">適切なコードがホストプロバイダーの関連データに正常にバインドされました。</span><span class="sxs-lookup"><span data-stu-id="8a07d-128">The appropriate code was successfully bound to related data in the host provider.</span></span>
    
<span data-ttu-id="8a07d-129">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="8a07d-129">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="8a07d-130">オブジェクトはテンプレート id をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="8a07d-130">The object does not support template IDs.</span></span>
    
<span data-ttu-id="8a07d-131">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="8a07d-131">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="8a07d-132">_lpTemplateID_パラメーターで渡されたテンプレート識別子がアドレス帳プロバイダーで認識されません。</span><span class="sxs-lookup"><span data-stu-id="8a07d-132">The template identifier passed in the  _lpTemplateID_ parameter is not recognized by the address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8a07d-133">解説</span><span class="sxs-lookup"><span data-stu-id="8a07d-133">Remarks</span></span>

<span data-ttu-id="8a07d-134">**IABLogon:: OpenTemplateID**メソッドは、ホストプロバイダーのコンテナーにあるエントリのコピーに対する制御を維持する必要があるアドレス帳プロバイダーによってのみ実装されます。</span><span class="sxs-lookup"><span data-stu-id="8a07d-134">The **IABLogon::OpenTemplateID** method is implemented only by address book providers that need to maintain control over copies of their entries that are located in the containers of host providers.</span></span> <span data-ttu-id="8a07d-135">**OpenTemplateID**を実装するプロバイダーは、外部アドレス帳プロバイダーと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="8a07d-135">Providers that implement **OpenTemplateID** are known as foreign address book providers.</span></span> <span data-ttu-id="8a07d-136">ホストプロバイダーは[imapisupport:: OpenTemplateID](imapisupport-opentemplateid.md)を呼び出してコピーされたエントリを作成するか、コピーされたエントリを開くと、 **IABLogon:: OpenTemplateID**の呼び出しに MAPI が渡されます。</span><span class="sxs-lookup"><span data-stu-id="8a07d-136">Host providers call [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) to create a copied entry or open the copied entry, and MAPI passes on the call to **IABLogon::OpenTemplateID**.</span></span> <span data-ttu-id="8a07d-137">**IABLogon:: OpenTemplateID**はエントリを開き、ホストプロバイダーのデータに制御するコードをバインドします。</span><span class="sxs-lookup"><span data-stu-id="8a07d-137">**IABLogon::OpenTemplateID** opens the entry and binds the code that controls it to data in the host provider.</span></span> 
  
<span data-ttu-id="8a07d-138">**IABLogon:: OpenTemplateID**は、エントリ識別子を使用するのではなく、別のプロパティ、エントリのテンプレート識別子、 **PR_TEMPLATEID**を使用します。</span><span class="sxs-lookup"><span data-stu-id="8a07d-138">Rather than use an entry identifier, **IABLogon::OpenTemplateID** uses another property, the entry's template identifier, **PR_TEMPLATEID**.</span></span> <span data-ttu-id="8a07d-139">ホストプロバイダーのデータにコードをバインドする必要があるエントリに対して、テンプレート識別子をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a07d-139">Template identifiers should be supported for entries whose code must be bound to data in a host provider.</span></span>
  
<span data-ttu-id="8a07d-140">アドレス帳プロバイダーが**IABLogon:: OpenTemplateID**を実装する必要がある場合の例としては、次のようなものがあります。</span><span class="sxs-lookup"><span data-stu-id="8a07d-140">Some examples of when an address book provider should implement **IABLogon::OpenTemplateID** are as follows:</span></span> 
  
- <span data-ttu-id="8a07d-141">コピーしたエントリのデータを定期的に更新して、元のデータと同期されたままにします。</span><span class="sxs-lookup"><span data-stu-id="8a07d-141">To periodically update the data for a copied entry so that it stays synchronized with the original.</span></span>
    
- <span data-ttu-id="8a07d-142">サーバー上のデータからエントリの詳細表に表示されるリストを動的に設定するなど、ホストプロバイダーが実装できない機能を実装します。</span><span class="sxs-lookup"><span data-stu-id="8a07d-142">To implement functionality that the host provider cannot implement, such as dynamically populating a list that appears in the entry's details table from data on a server.</span></span>
    
- <span data-ttu-id="8a07d-143">ホストプロバイダーのエントリ内のプロパティと元の項目の間の相互作用を制御するには、 **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) を、異なる詳細表示にある編集コントロールの値を使用して計算します。住所のコンポーネント。</span><span class="sxs-lookup"><span data-stu-id="8a07d-143">To control the interaction between properties in the host provider's entry and the original entry, such as computing the **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) from the values of the edit controls in the details display that contain different components of the address.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="8a07d-144">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="8a07d-144">Notes to implementers</span></span>

<span data-ttu-id="8a07d-145">ホストプロバイダーは、プロバイダーからエントリをコピーまたは作成するときに、 **IABLogon:: OpenTemplateID**を使用してプロパティオブジェクトの実装を提供するときに、エントリを維持するために、ほとんどの呼び出しを処理します。</span><span class="sxs-lookup"><span data-stu-id="8a07d-145">When a host provider copies or creates an entry from your provider and you supply a property object implementation through **IABLogon::OpenTemplateID**, you handle most of the calls to maintain the entry.</span></span> <span data-ttu-id="8a07d-146">ただし、ホストプロバイダーは、このような呼び出しを自分に転送する必要があるので、呼び出しを転送する前に、ホストプロバイダーは任意の呼び出しを受信し、カスタム処理を実行できます。</span><span class="sxs-lookup"><span data-stu-id="8a07d-146">However, because it is up to the host provider to forward these calls to you, the host provider can intercept any call and perform custom processing before forwarding the call.</span></span>
  
<span data-ttu-id="8a07d-147">property オブジェクトの実装では、次のガイドラインを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a07d-147">You should use the following guidelines in your property object implementations:</span></span>
  
- <span data-ttu-id="8a07d-148">[imapiprop:: GetProps](imapiprop-getprops.md)が呼び出されたときに、要求が計算されたプロパティを対象としているかどうかを判別し、ある場合は処理します。</span><span class="sxs-lookup"><span data-stu-id="8a07d-148">When [IMAPIProp::GetProps](imapiprop-getprops.md) is called, determine whether the request is for a computed property and, if it is, handle it.</span></span> <span data-ttu-id="8a07d-149">非計算プロパティのすべての要求をホストプロバイダーに転送します。</span><span class="sxs-lookup"><span data-stu-id="8a07d-149">Transfer all requests for noncomputed properties to the host provider.</span></span> 
    
- <span data-ttu-id="8a07d-150">[imapiprop:: openproperty](imapiprop-openproperty.md)を呼び出して、詳細表示テーブル以外の任意のテーブルを開いた場合は、要求を処理します。</span><span class="sxs-lookup"><span data-stu-id="8a07d-150">When [IMAPIProp::OpenProperty](imapiprop-openproperty.md) is called to open any table except the details display table, handle the request.</span></span> <span data-ttu-id="8a07d-151">ほとんどのテーブルは、ホストプロバイダに正確にコピーすることはできません。</span><span class="sxs-lookup"><span data-stu-id="8a07d-151">Most tables cannot be copied accurately to the host provider.</span></span> <span data-ttu-id="8a07d-152">これらの要求されたテーブルに対して**IMAPITable**実装を生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a07d-152">You must generate the **IMAPITable** implementation for these requested tables.</span></span> <span data-ttu-id="8a07d-153">詳細表**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティをホストプロバイダーにコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a07d-153">The details table **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property must be copied to the host provider.</span></span> <span data-ttu-id="8a07d-154">これにより、このプロバイダーはテーブルをローカルに生成できるようになります。</span><span class="sxs-lookup"><span data-stu-id="8a07d-154">This allows this provider to generate the table locally.</span></span> <span data-ttu-id="8a07d-155">表示テーブルの通知を生成するために、表示テーブルの実装をラップする必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="8a07d-155">You might want to wrap the display table implementation to generate display table notifications.</span></span> 
    
- <span data-ttu-id="8a07d-156">[imapiprop:: setprops](imapiprop-setprops.md)が呼び出されると、ホストプロバイダーはプロパティを設定する前にデータを検証することができます。</span><span class="sxs-lookup"><span data-stu-id="8a07d-156">When [IMAPIProp::SetProps](imapiprop-setprops.md) is called, the host provider can validate the data before letting you set the properties.</span></span> <span data-ttu-id="8a07d-157">必要なすべてのプロパティが設定または計算されたことを確認できます。</span><span class="sxs-lookup"><span data-stu-id="8a07d-157">You can verify that all of the necessary properties were set or computed.</span></span> <span data-ttu-id="8a07d-158">エラーが検出された場合は、適切なエラー値を返します。可能であれば、 [imapiprop:: GetLastError](imapiprop-getlasterror.md)から追加の説明を返します。</span><span class="sxs-lookup"><span data-stu-id="8a07d-158">If an error is detected, return the appropriate error value and, if you can, any additional explanation through [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span></span>
    
- <span data-ttu-id="8a07d-159">[imapiprop:: SaveChanges](imapiprop-savechanges.md)が呼び出されると、ホストプロバイダーはエントリを保存する前に処理を実行することができます。</span><span class="sxs-lookup"><span data-stu-id="8a07d-159">When [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called, the host provider might want to perform processing before you save the entry.</span></span> <span data-ttu-id="8a07d-160">新しいアドレスなど、変更されたプロパティの影響を受けるすべてのデータを、ホストプロバイダのエントリに保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a07d-160">You should save any data that is affected by the changed properties, such as a new address, in the host provider's entry.</span></span> 
    
<span data-ttu-id="8a07d-161">一般的には、ホストプロバイダーに渡すエントリの実装によって、関連するプロパティのコンテキスト固有の操作を実行するすべてのメソッドがインターセプトされます。</span><span class="sxs-lookup"><span data-stu-id="8a07d-161">In general, make your implementation of the entry that you pass back to the host provider intercept all of the methods to perform context-specific manipulation of the relevant properties.</span></span> <span data-ttu-id="8a07d-162">FILL_ENTRY フラグが_ultemplateflags_パラメーターに渡された場合は、エントリのすべてのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="8a07d-162">If the FILL_ENTRY flag is passed in the  _ulTemplateFlags_ parameter, set all properties for the entry.</span></span> 
  
<span data-ttu-id="8a07d-163">_lppMAPIPropNew_パラメーターで新しい property オブジェクトを取得する場合は、ホストプロバイダーの property オブジェクトの[IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx)メソッドを呼び出して、参照を維持します。</span><span class="sxs-lookup"><span data-stu-id="8a07d-163">If you return a new property object in the  _lppMAPIPropNew_ parameter, call the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method of the host provider's property object to maintain a reference.</span></span> <span data-ttu-id="8a07d-164">_lppMAPIPropNew_での**imapiprop**の実装によって返されたバインドオブジェクトを経由するすべての呼び出しは、バインドされたオブジェクトによって処理された後、host property オブジェクトの対応するメソッドにルーティングされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a07d-164">All calls through the bound object that the **IMAPIProp** implementation returned in  _lppMAPIPropNew_ should be routed to their corresponding method in the host property object after they are dealt with by the bound object.</span></span> 
  
<span data-ttu-id="8a07d-165">バインドされた property オブジェクトを通じて渡される名前付きプロパティのプロパティ識別子は、プロバイダーの識別子名前空間にあります。</span><span class="sxs-lookup"><span data-stu-id="8a07d-165">The property identifiers of any named properties that are passed through your bound property object are in your provider's identifier namespace.</span></span> <span data-ttu-id="8a07d-166">[imapiprop:: GetNamesFromIDs](imapiprop-getnamesfromids.md)メソッドを実装すると、テンプレート固有のタスクを実行できるように、プロパティの名前を決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a07d-166">Your implementation of the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) method should determine the names of the properties so that it can perform any template-specific tasks.</span></span> <span data-ttu-id="8a07d-167">同様に、プロバイダーがホストプロバイダーに渡すプロパティも、名前空間に存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a07d-167">Similarly, properties that your provider passes on to the host provider must also be in your namespace.</span></span> <span data-ttu-id="8a07d-168">たとえば、 **OpenTemplateID**で名前付きプロパティを設定する場合は、必要に応じて、 [imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)メソッドを呼び出すことによって、その名前に識別子の1つを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a07d-168">For example, if you set a named property in **OpenTemplateID**, you should use one of your identifiers for the name—creating it, if necessary, by calling the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> 
  
<span data-ttu-id="8a07d-169">_lpTemplateID_で渡されたエントリ識別子を認識しない場合は、MAPI_E_UNKNOWN_ENTRYID を返します。</span><span class="sxs-lookup"><span data-stu-id="8a07d-169">If you do not recognize the entry identifier passed in  _lpTemplateID_, return MAPI_E_UNKNOWN_ENTRYID.</span></span>
  
<span data-ttu-id="8a07d-170">アドレス帳テンプレート識別子を操作する方法の詳細については、「[外部アドレス帳プロバイダーとして機能](acting-as-a-foreign-address-book-provider.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8a07d-170">For more information about how to work with address book template identifiers, see [Acting as a Foreign Address Book Provider](acting-as-a-foreign-address-book-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8a07d-171">関連項目</span><span class="sxs-lookup"><span data-stu-id="8a07d-171">See also</span></span>



[<span data-ttu-id="8a07d-172">IMAPISupport::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="8a07d-172">IMAPISupport::OpenTemplateID</span></span>](imapisupport-opentemplateid.md)
  
[<span data-ttu-id="8a07d-173">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8a07d-173">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="8a07d-174">PidTagTemplateid 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8a07d-174">PidTagTemplateid Canonical Property</span></span>](pidtagtemplateid-canonical-property.md)
  
[<span data-ttu-id="8a07d-175">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8a07d-175">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

