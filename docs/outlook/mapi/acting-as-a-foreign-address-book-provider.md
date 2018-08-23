---
title: 外部のアドレス帳プロバイダーとして動作しています。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6d532ed4-7dc5-46a9-995a-72bc97d16f6e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 16c3518ab4efddbd68765d9de94db64b4fdc0b64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799621"
---
# <a name="acting-as-a-foreign-address-book-provider"></a><span data-ttu-id="3d41c-103">外部のアドレス帳プロバイダーとして動作しています。</span><span class="sxs-lookup"><span data-stu-id="3d41c-103">Acting as a foreign address book provider</span></span>

<span data-ttu-id="3d41c-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3d41c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3d41c-105">外部のプロバイダーは、アドレス帳プロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="3d41c-105">A foreign provider is an address book provider that:</span></span> 
  
- <span data-ttu-id="3d41c-106">その受信者のテンプレートの識別子を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="3d41c-106">Assigns template identifiers for its recipients.</span></span>
    
- <span data-ttu-id="3d41c-107">[IABLogon::OpenTemplateID](iablogon-opentemplateid.md)メソッドをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="3d41c-107">Supports the [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) method.</span></span> 
    
- <span data-ttu-id="3d41c-108">ホスト プロバイダーと呼ばれるその他のアドレス帳のプロバイダーのコンテナー内に存在する受信者を管理するためのコードを提供します。</span><span class="sxs-lookup"><span data-stu-id="3d41c-108">Supplies code for maintaining recipients that exist in the containers of other address book providers known as host providers.</span></span> <span data-ttu-id="3d41c-109">このコードでは、プロパティ オブジェクト、通常**IMAPIProp**インターフェイスの実装、ホスト プロバイダーからのプロパティのオブジェクトをラップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d41c-109">This code involves a property object, typically an **IMAPIProp** interface implementation, which wraps a property object from the host provider.</span></span> 
    
<span data-ttu-id="3d41c-110">外部のプロバイダーとしての機能は、オプションの役割です。すべてのプロバイダーでは、テンプレートの識別子と、関連するコードをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d41c-110">Acting as a foreign provider is an optional role; not all providers need to support template identifiers and their related code.</span></span> <span data-ttu-id="3d41c-111">ホスト プロバイダーは、プロバイダーから提供されたテンプレートを使用するを作成する受信者の管理を維持する場合は、外部プロバイダーとしてプロバイダーを実装します。</span><span class="sxs-lookup"><span data-stu-id="3d41c-111">Implement your provider as a foreign provider if you want to maintain control over recipients that host providers create using templates supplied by your provider.</span></span> 
  
<span data-ttu-id="3d41c-112">エントリ id は、プロバイダーを使用する形式は、そのテンプレートの識別子も使用できます。</span><span class="sxs-lookup"><span data-stu-id="3d41c-112">The format that your provider uses for its entry identifiers can also be used for its template identifiers.</span></span> <span data-ttu-id="3d41c-113">テンプレート識別子には、正常に受信者を適切なプロバイダーにバインドするための MAPI を有効にするのには、プロバイダーの登録されている**MAPIUID**を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d41c-113">Template identifiers must include your provider's registered **MAPIUID** to enable MAPI to successfully bind recipients to the appropriate providers.</span></span> 
  
<span data-ttu-id="3d41c-114">MAPI では、ホスト プロバイダーの呼び出し[IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)するときに、プロバイダーの**IABLogon::OpenTemplateID**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3d41c-114">MAPI calls your provider's **IABLogon::OpenTemplateID** method when a host provider calls [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md).</span></span> <span data-ttu-id="3d41c-115">ホスト プロバイダーは、 **IMAPISupport::OpenTemplateID**への呼び出し内の_lpTemplateID_パラメーターで、受信者のテンプレートの識別子を渡します。</span><span class="sxs-lookup"><span data-stu-id="3d41c-115">The host provider passes the template identifier of the recipient in the  _lpTemplateID_ parameter in its call to **IMAPISupport::OpenTemplateID**.</span></span> <span data-ttu-id="3d41c-116">MAPI では、テンプレートの識別子が、 [MAPIUID](mapiuid.md)テンプレート id でログオン時に、プロバイダーが登録されている**MAPIUID**とを照合することによって、プロバイダーに属しているを決定します。</span><span class="sxs-lookup"><span data-stu-id="3d41c-116">MAPI determines that the template identifier belongs to your provider by matching the [MAPIUID](mapiuid.md) in the template identifier with the **MAPIUID** that your provider registered at logon time.</span></span> <span data-ttu-id="3d41c-117">MAPI は、 **IABLogon::OpenTemplateID**メソッドを使用し、プロバイダーのホスト プロバイダーの呼び出しを転送します。</span><span class="sxs-lookup"><span data-stu-id="3d41c-117">MAPI then forwards the host provider's call to your provider through the **IABLogon::OpenTemplateID** method.</span></span> 
  
<span data-ttu-id="3d41c-118">ホスト プロバイダーもポインターを渡します、プロパティ オブジェクトの実装に、 _lpMAPIPropData_パラメーター内の受信者、インターフェイスの実装の種類に対応する_lpInterface_パラメーターにインターフェイス識別子_lpMAPIPropData_、およびオプションのフラグ、FILL_ENTRY に渡されます。</span><span class="sxs-lookup"><span data-stu-id="3d41c-118">The host provider also passes a pointer to its property object implementation for the recipient in the  _lpMAPIPropData_ parameter, an interface identifier in the  _lpInterface_ parameter that corresponds to the type of interface implementation passed in  _lpMAPIPropData_, and an optional flag, FILL_ENTRY.</span></span> <span data-ttu-id="3d41c-119">プロバイダーは、 _lpInterface_で指定された型のプロパティ オブジェクトの実装に_lppMAPIPropNew_パラメーターにポインターを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d41c-119">Your provider is expected to return in the  _lppMAPIPropNew_ parameter a pointer to a property object implementation of the type specified in  _lpInterface_.</span></span> <span data-ttu-id="3d41c-120">返されたポインターできる、プロバイダーによって実装されているプロパティをラップされたオブジェクトにまたは_lpMAPIPropData_のホスト プロバイダーから提供されたオブジェクトにします。</span><span class="sxs-lookup"><span data-stu-id="3d41c-120">The returned pointer can either be to the wrapped property object implemented by your provider or to the object supplied by the host provider in  _lpMAPIPropData_.</span></span> <span data-ttu-id="3d41c-121">プロバイダーがプロパティをラップされたオブジェクトのポインターを返す必要がある場合。</span><span class="sxs-lookup"><span data-stu-id="3d41c-121">Your provider should return a wrapped property object pointer when:</span></span>
  
- <span data-ttu-id="3d41c-122">受信者の表示のテーブルには、リスト ボックス コントロールが含まれています。</span><span class="sxs-lookup"><span data-stu-id="3d41c-122">The recipient's display table contains list box controls.</span></span>
    
- <span data-ttu-id="3d41c-123">受信者の電子メール アドレスは、複数のディスプレイ テーブル コントロール内のデータで組み立てられる必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d41c-123">The email address for the recipient must be assembled from data in multiple display table controls.</span></span>
    
- <span data-ttu-id="3d41c-124">プロバイダーの問題では、テーブルの通知を表示します。</span><span class="sxs-lookup"><span data-stu-id="3d41c-124">Your provider issues display table notifications.</span></span>
    
<span data-ttu-id="3d41c-125">FILL_ENTRY フラグは、ホスト プロバイダーを更新する受信者のすべてのプロパティが必要である、プロバイダーに指示します。</span><span class="sxs-lookup"><span data-stu-id="3d41c-125">The FILL_ENTRY flag indicates to your provider that the host provider requires all the properties of the recipient to be updated.</span></span> <span data-ttu-id="3d41c-126">プロバイダーは、この要求を満たすために必要です。</span><span class="sxs-lookup"><span data-stu-id="3d41c-126">Your provider is required to fulfill this request.</span></span>
  
<span data-ttu-id="3d41c-127">ホスト プロバイダーが、プロバイダーの**OpenTemplateID**メソッドを呼び出すと、プロバイダー可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3d41c-127">When a host provider calls your provider's **OpenTemplateID** method, your provider might:</span></span> 
  
- <span data-ttu-id="3d41c-128">コピーしたエントリのデータを定期的に更新します。</span><span class="sxs-lookup"><span data-stu-id="3d41c-128">Periodically update the data for a copied entry.</span></span>
    
- <span data-ttu-id="3d41c-129">コピーしたエントリが個人用アドレス帳にアドレス帳エントリをコピーするときなど、元と同期してください。</span><span class="sxs-lookup"><span data-stu-id="3d41c-129">Keep a copied entry synchronized with its original, such as when an address book entry is copied to the personal address book.</span></span>
    
- <span data-ttu-id="3d41c-130">サーバー上のデータからコピーしたエントリの詳細の表でボックスの実装の機能リストを動的に生成するなど、ホスト プロバイダーが実装することはできません。</span><span class="sxs-lookup"><span data-stu-id="3d41c-130">Implement functionality that cannot be implemented by the host provider, such as dynamically populating list boxes in the copied entry's details table from data on a server.</span></span>
    
- <span data-ttu-id="3d41c-131">コピーしたエントリまたはインスタンス化されたテンプレートのプロパティ間の相互作用を制御します。</span><span class="sxs-lookup"><span data-stu-id="3d41c-131">Control the interaction among properties in a copied entry or instantiated template.</span></span> <span data-ttu-id="3d41c-132">[明細] テーブルに表示されるその他のプロパティから、たとえば、 **PR_EMAIL_ADDRESS**を計算しています。</span><span class="sxs-lookup"><span data-stu-id="3d41c-132">For example, computing **PR_EMAIL_ADDRESS** from other properties displayed in the details table.</span></span> 
    
<span data-ttu-id="3d41c-133">プロパティをラップされたオブジェクトを指定するのには、プロバイダーを必要としないタスクの例としては、最初の 2 つの項目、ホスト プロバイダーの実装に基づく**IMAPIProp**を実装します。</span><span class="sxs-lookup"><span data-stu-id="3d41c-133">The first two items are examples of tasks that do not require your provider to supply a wrapped property object — an implementation of **IMAPIProp** that is based on the host provider's implementation.</span></span> <span data-ttu-id="3d41c-134">プロバイダーは、必要に応じて、戻り値、 _lpMAPIPropData_パラメーターでは、ホスト プロバイダーから渡されたポインターを指すように_lppMAPIPropNew_パラメーターを設定するとプロパティを更新できますだけです。</span><span class="sxs-lookup"><span data-stu-id="3d41c-134">Your provider can simply update the properties as necessary and return, setting the  _lppMAPIPropNew_ parameter to point to the pointer passed in by the host provider in the  _lpMAPIPropData_ parameter.</span></span> 
  
<span data-ttu-id="3d41c-135">2 つ目は 2 つのタスクでは、エントリのプロパティ シートを表示する機能などの追加機能によって、ホスト プロバイダーのオブジェクトをラップするプロパティ オブジェクトのホスト プロバイダーには、プロバイダーが返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d41c-135">The second two tasks require that your provider return to the host provider a property object that wraps the host provider's object with additional functionality, such as the ability to display a property sheet for the entry.</span></span> <span data-ttu-id="3d41c-136">このプロパティ オブジェクトはメッセージのユーザーまたは配布リスト、 _lpMAPIPropData_パラメーターでは、ホスト プロバイダーによって渡される_lpInterface_パラメーターにインターフェイス識別子で指定されたオブジェクトの種類に応じて。</span><span class="sxs-lookup"><span data-stu-id="3d41c-136">This property object will either be a messaging user or distribution list, depending on the type of object passed in by the host provider in the  _lpMAPIPropData_ parameter and indicated by the interface identifier in the  _lpInterface_ parameter.</span></span> <span data-ttu-id="3d41c-137">_LpMAPIPropData_パラメーターは、メッセージングのユーザーをポイントしている場合、プロバイダーのプロパティをラップされたオブジェクトは、 **IMailUser**実装をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d41c-137">If the  _lpMAPIPropData_ parameter points to a messaging user, your provider's wrapped property object must be an **IMailUser** implementation.</span></span> <span data-ttu-id="3d41c-138">_LpMAPIPropData_は、配布リストをポイントしている場合、 **IDistList**の実装があります。</span><span class="sxs-lookup"><span data-stu-id="3d41c-138">If  _lpMAPIPropData_ points to a distribution list, it must be an **IDistList** implementation.</span></span> 
  
<span data-ttu-id="3d41c-139">**IMAPIProp**ホスト プロバイダーの受信者のコンテキストに固有の操作を実行するメソッドの呼び出しをインターセプトする、プロバイダーのプロパティをラップされたオブジェクトのそれをラップするオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="3d41c-139">Your provider's wrapped property object intercepts **IMAPIProp** method calls to perform context-specific manipulation of the host provider's recipient—the object it is wrapping.</span></span> <span data-ttu-id="3d41c-140">MAPI では、オブジェクトの折り返しが設定されたプロパティの要件の 1 つだけは、: [IMAPIProp::OpenProperty](imapiprop-openproperty.md) **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) のプロパティを要求するすべての呼び出しは、ホスト プロバイダーに渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d41c-140">MAPI only has one requirement for wrapped property objects: all calls to [IMAPIProp::OpenProperty](imapiprop-openproperty.md) requesting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property should be passed to the host provider.</span></span> <span data-ttu-id="3d41c-141">プロバイダーの実装は、表示テーブルの通知を受け取るかに応じて、独自に追加するのには、返されるテーブルを使用できます。</span><span class="sxs-lookup"><span data-stu-id="3d41c-141">Your provider's implementation can use the returned table to intercept display table notifications or to add its own if necessary.</span></span> 
  
<span data-ttu-id="3d41c-142">次の一覧には、外部プロバイダーによって実装されるプロパティをラップされたオブジェクトの実装は、通常のタスクが含まれています。</span><span class="sxs-lookup"><span data-stu-id="3d41c-142">The following list includes tasks that are typically implemented in the wrapped property object implemented by foreign providers:</span></span>
  
- <span data-ttu-id="3d41c-143">前処理スクリプトと[IMAPIProp::GetProps](imapiprop-getprops.md)のホストの受信者のプロパティの値を後処理します。</span><span class="sxs-lookup"><span data-stu-id="3d41c-143">Preprocessing and postprocessing property values for the host recipient in [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
    
- <span data-ttu-id="3d41c-144">処理の詳細は、 **IMAPIProp::OpenProperty**のボタンやリスト ボックスなど、テーブルのコントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="3d41c-144">Handling details display table controls, such as buttons and list boxes, in **IMAPIProp::OpenProperty**.</span></span>
    
- <span data-ttu-id="3d41c-145">検証または[IMAPIProp::SetProps](imapiprop-setprops.md)でホストの受信者のプロパティの値を操作します。</span><span class="sxs-lookup"><span data-stu-id="3d41c-145">Validating or manipulating property values for the host recipient in [IMAPIProp::SetProps](imapiprop-setprops.md).</span></span>
    
- <span data-ttu-id="3d41c-146">**PR_EMAIL_ADDRESS**などの必要なプロパティを計算し、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)でホストの受信者を保存する前に設定されているすべての必要なプロパティを確認します。</span><span class="sxs-lookup"><span data-stu-id="3d41c-146">Computing required properties such as **PR_EMAIL_ADDRESS** and verifying that all of the necessary properties have been set before saving the host recipient in [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
### <a name="to-implement-iablogonopentemplateid"></a><span data-ttu-id="3d41c-147">IABLogon::OpenTemplateID を実装するには</span><span class="sxs-lookup"><span data-stu-id="3d41c-147">To implement IABLogon::OpenTemplateID</span></span>
  
1. <span data-ttu-id="3d41c-148">テンプレート識別子が渡された場合、 _lpTemplateID_パラメーターが有効なでは、プロバイダーで認識される形式でを確認します。</span><span class="sxs-lookup"><span data-stu-id="3d41c-148">Check if the template identifier passed in with the  _lpTemplateID_ parameter is valid and is in a format that your provider recognizes.</span></span> <span data-ttu-id="3d41c-149">そうでない場合は失敗し、MAPI_E_INVALID_ENTRYID を返します。</span><span class="sxs-lookup"><span data-stu-id="3d41c-149">If it is not, fail and return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="3d41c-150">テンプレート識別子で指定された型のオブジェクトを作成するメッセージングのユーザー、配布リスト、または 1 回限りの受信者のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="3d41c-150">Create an object of the type indicated by the template identifier, either a messaging user, distribution list, or one-off recipient.</span></span> 
    
3. <span data-ttu-id="3d41c-151">ホスト プロバイダーのプロパティ オブジェクトは、 _lpMAPIPropData_パラメーターが指すオブジェクトの**IUnknown::AddRef**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3d41c-151">Call the **IUnknown::AddRef** method in the host provider's property object, which is the object pointed to by the  _lpMAPIPropData_ parameter.</span></span> 
    
4. <span data-ttu-id="3d41c-152">場合は、 _ulTemplateFlags_パラメーターを FILL_ENTRY に設定するとします。</span><span class="sxs-lookup"><span data-stu-id="3d41c-152">If the  _ulTemplateFlags_ parameter is set to FILL_ENTRY:</span></span> 
    
   1. <span data-ttu-id="3d41c-153">新しいオブジェクトがメッセージのユーザーまたは配布リストの場合。</span><span class="sxs-lookup"><span data-stu-id="3d41c-153">If the new object is a messaging user or distribution list:</span></span>
      
      1. <span data-ttu-id="3d41c-154">すべてを取得、新しいオブジェクトのプロパティの可能性があります、 **IMAPIProp::GetProps**メソッドを呼び出してください。</span><span class="sxs-lookup"><span data-stu-id="3d41c-154">Retrieve all of the properties of the new object, possibly by calling its **IMAPIProp::GetProps** method.</span></span> 
          
      2. <span data-ttu-id="3d41c-155">ホスト プロバイダーのプロパティ オブジェクトを取得したプロパティのすべてをコピーするのには、ホスト プロバイダーの**IMAPIProp::SetProps**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3d41c-155">Call the host provider's **IMAPIProp::SetProps** method to copy all of the retrieved properties to the host provider's property object.</span></span> 
      
   2. <span data-ttu-id="3d41c-156">新しいオブジェクトが 1 回限りの受信者の場合は、次のプロパティを設定するのには、ホスト プロバイダーの**IMAPIProp::SetProps**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3d41c-156">If the new object is a one-off recipient, call the host provider's **IMAPIProp::SetProps** method to set the following properties:</span></span> 
      
      - <span data-ttu-id="3d41c-157">**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md)) は、プロバイダーによって処理されるアドレスの種類にします。</span><span class="sxs-lookup"><span data-stu-id="3d41c-157">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) to the address type handled by your provider.</span></span>
        
      - <span data-ttu-id="3d41c-158">**PR\_テンプレート ID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md))、 _lpTemplateID_および_cbTemplateID_パラメーターからテンプレート識別子にします。</span><span class="sxs-lookup"><span data-stu-id="3d41c-158">**PR\_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) to the template identifier from the  _lpTemplateID_ and  _cbTemplateID_ parameters.</span></span> 
        
      - <span data-ttu-id="3d41c-159">**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) DT_MAILUSER または DT_DISTLIST では、必要に応じてします。</span><span class="sxs-lookup"><span data-stu-id="3d41c-159">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) to DT_MAILUSER or DT_DISTLIST, as appropriate.</span></span>
    
5. <span data-ttu-id="3d41c-160">プロバイダーの新しいオブジェクトまたはいずれかが必要で、ラップされたオブジェクトをプロバイダーが判断するかどうかに応じて、 _lpMAPIPropData_パラメーターで渡されたプロパティのオブジェクトを指すように_lppMAPIPropNew_パラメーターの内容を設定します。</span><span class="sxs-lookup"><span data-stu-id="3d41c-160">Set the contents of the  _lppMAPIPropNew_ parameter to point to either your provider's new object or the property object passed in with the  _lpMAPIPropData_ parameter, depending on whether your provider determines a wrapped object is necessary.</span></span> 
    
6. <span data-ttu-id="3d41c-161">ネットワーク障害や、メモリ不足の状態などの重大なエラーが発生した場合は、適切なエラー値を返します。</span><span class="sxs-lookup"><span data-stu-id="3d41c-161">If a critical error occurs, such as a network failure or an out of memory condition, return the appropriate error value.</span></span> <span data-ttu-id="3d41c-162">この値の適切な[MAPIERROR](mapierror.md)構造体、ホスト プロバイダーによって実行されるタスクをクライアントに反映される必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d41c-162">This value should get propagated to the client with the appropriate [MAPIERROR](mapierror.md) structure, a task performed by the host provider.</span></span> 
    

