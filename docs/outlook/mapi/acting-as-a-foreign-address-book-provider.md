---
title: 外部アドレス帳プロバイダーとして機能
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6d532ed4-7dc5-46a9-995a-72bc97d16f6e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 300681bd585e9d534113404a82f43565f4e79bb4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331211"
---
# <a name="acting-as-a-foreign-address-book-provider"></a><span data-ttu-id="f8851-103">外部アドレス帳プロバイダーとして機能</span><span class="sxs-lookup"><span data-stu-id="f8851-103">Acting as a foreign address book provider</span></span>

<span data-ttu-id="f8851-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8851-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8851-105">外部プロバイダーとは、次のようなアドレス帳プロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="f8851-105">A foreign provider is an address book provider that:</span></span> 
  
- <span data-ttu-id="f8851-106">受信者のテンプレート識別子を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f8851-106">Assigns template identifiers for its recipients.</span></span>
    
- <span data-ttu-id="f8851-107">[IABLogon:: OpenTemplateID](iablogon-opentemplateid.md)メソッドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="f8851-107">Supports the [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) method.</span></span> 
    
- <span data-ttu-id="f8851-108">ホストプロバイダーと呼ばれる他のアドレス帳プロバイダーのコンテナーに存在する受信者を管理するためのコードを提供します。</span><span class="sxs-lookup"><span data-stu-id="f8851-108">Supplies code for maintaining recipients that exist in the containers of other address book providers known as host providers.</span></span> <span data-ttu-id="f8851-109">このコードには、property オブジェクト (通常は**imapiprop**インターフェイスの実装) が含まれています。これは、ホストプロバイダーから property オブジェクトをラップします。</span><span class="sxs-lookup"><span data-stu-id="f8851-109">This code involves a property object, typically an **IMAPIProp** interface implementation, which wraps a property object from the host provider.</span></span> 
    
<span data-ttu-id="f8851-110">外部プロバイダーとして機能するのはオプションの役割です。テンプレート識別子とそれに関連するコードをサポートする必要がないプロバイダーもあります。</span><span class="sxs-lookup"><span data-stu-id="f8851-110">Acting as a foreign provider is an optional role; not all providers need to support template identifiers and their related code.</span></span> <span data-ttu-id="f8851-111">プロバイダーから提供されるテンプレートを使用してプロバイダーをホストする受信者の制御を維持する場合は、プロバイダーを外部プロバイダーとして実装します。</span><span class="sxs-lookup"><span data-stu-id="f8851-111">Implement your provider as a foreign provider if you want to maintain control over recipients that host providers create using templates supplied by your provider.</span></span> 
  
<span data-ttu-id="f8851-112">プロバイダーがエントリ識別子に使用する形式は、そのテンプレート識別子にも使用できます。</span><span class="sxs-lookup"><span data-stu-id="f8851-112">The format that your provider uses for its entry identifiers can also be used for its template identifiers.</span></span> <span data-ttu-id="f8851-113">MAPI が受信者を適切なプロバイダーに正しくバインドできるようにするには、テンプレート識別子にプロバイダーの登録済み**MAPIUID**を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8851-113">Template identifiers must include your provider's registered **MAPIUID** to enable MAPI to successfully bind recipients to the appropriate providers.</span></span> 
  
<span data-ttu-id="f8851-114">MAPI は、ホストプロバイダーが[imapisupport:: OpenTemplateID](imapisupport-opentemplateid.md)を呼び出すときに、プロバイダーの**IABLogon:: OpenTemplateID**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f8851-114">MAPI calls your provider's **IABLogon::OpenTemplateID** method when a host provider calls [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md).</span></span> <span data-ttu-id="f8851-115">ホストプロバイダーは、 **imapisupport:: OpenTemplateID**への呼び出しで、受信者のテンプレート識別子を_lpTemplateID_パラメーターに渡します。</span><span class="sxs-lookup"><span data-stu-id="f8851-115">The host provider passes the template identifier of the recipient in the  _lpTemplateID_ parameter in its call to **IMAPISupport::OpenTemplateID**.</span></span> <span data-ttu-id="f8851-116">MAPI は、テンプレート識別子の[MAPIUID](mapiuid.md)とプロバイダーがログオン時に登録した**MAPIUID**を一致させることによって、テンプレート識別子がプロバイダーに属していると判断します。</span><span class="sxs-lookup"><span data-stu-id="f8851-116">MAPI determines that the template identifier belongs to your provider by matching the [MAPIUID](mapiuid.md) in the template identifier with the **MAPIUID** that your provider registered at logon time.</span></span> <span data-ttu-id="f8851-117">その後、MAPI は、 **IABLogon:: OpenTemplateID**メソッドを使用して、ホストプロバイダーの呼び出しをプロバイダーに転送します。</span><span class="sxs-lookup"><span data-stu-id="f8851-117">MAPI then forwards the host provider's call to your provider through the **IABLogon::OpenTemplateID** method.</span></span> 
  
<span data-ttu-id="f8851-118">また、ホストプロバイダーは、 _lpMAPIPropData_パラメーターの受信者に対するそのプロパティオブジェクトの実装へのポインターを渡します。 _lpinterface_パラメーターでインターフェイスの実装の種類に対応するインターフェイス識別子です。_lpMAPIPropData_で渡され、省略可能なフラグ FILL_ENTRY。</span><span class="sxs-lookup"><span data-stu-id="f8851-118">The host provider also passes a pointer to its property object implementation for the recipient in the  _lpMAPIPropData_ parameter, an interface identifier in the  _lpInterface_ parameter that corresponds to the type of interface implementation passed in  _lpMAPIPropData_, and an optional flag, FILL_ENTRY.</span></span> <span data-ttu-id="f8851-119">プロバイダーは、 _lpinterface_で指定された型の property オブジェクト実装へのポインターを_lppMAPIPropNew_パラメータで返すことが想定されています。</span><span class="sxs-lookup"><span data-stu-id="f8851-119">Your provider is expected to return in the  _lppMAPIPropNew_ parameter a pointer to a property object implementation of the type specified in  _lpInterface_.</span></span> <span data-ttu-id="f8851-120">返されるポインターは、プロバイダーによって実装されたラップされた property オブジェクト、または_lpMAPIPropData_のホストプロバイダーから提供されたオブジェクトのいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="f8851-120">The returned pointer can either be to the wrapped property object implemented by your provider or to the object supplied by the host provider in  _lpMAPIPropData_.</span></span> <span data-ttu-id="f8851-121">プロバイダーは、次の場合にラップされた property オブジェクトポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="f8851-121">Your provider should return a wrapped property object pointer when:</span></span>
  
- <span data-ttu-id="f8851-122">受信者の表示テーブルには、リストボックスコントロールが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f8851-122">The recipient's display table contains list box controls.</span></span>
    
- <span data-ttu-id="f8851-123">受信者の電子メールアドレスは、複数の表示テーブルコントロールのデータからアセンブルする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8851-123">The email address for the recipient must be assembled from data in multiple display table controls.</span></span>
    
- <span data-ttu-id="f8851-124">プロバイダーが表示テーブル通知を発行します。</span><span class="sxs-lookup"><span data-stu-id="f8851-124">Your provider issues display table notifications.</span></span>
    
<span data-ttu-id="f8851-125">FILL_ENTRY フラグは、ホストプロバイダーが受信者のすべてのプロパティを更新する必要があることをプロバイダーに示します。</span><span class="sxs-lookup"><span data-stu-id="f8851-125">The FILL_ENTRY flag indicates to your provider that the host provider requires all the properties of the recipient to be updated.</span></span> <span data-ttu-id="f8851-126">この要求を満たすには、プロバイダーが必要です。</span><span class="sxs-lookup"><span data-stu-id="f8851-126">Your provider is required to fulfill this request.</span></span>
  
<span data-ttu-id="f8851-127">ホストプロバイダーがプロバイダーの**OpenTemplateID**メソッドを呼び出す場合、プロバイダーは次のことを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="f8851-127">When a host provider calls your provider's **OpenTemplateID** method, your provider might:</span></span> 
  
- <span data-ttu-id="f8851-128">コピーしたエントリのデータを定期的に更新します。</span><span class="sxs-lookup"><span data-stu-id="f8851-128">Periodically update the data for a copied entry.</span></span>
    
- <span data-ttu-id="f8851-129">コピーしたエントリは、アドレス帳のエントリが個人用アドレス帳にコピーされたときのように、元の値と同期されたままにします。</span><span class="sxs-lookup"><span data-stu-id="f8851-129">Keep a copied entry synchronized with its original, such as when an address book entry is copied to the personal address book.</span></span>
    
- <span data-ttu-id="f8851-130">サーバー上のデータからコピーしたエントリの詳細表にリストボックスを動的に入力するなど、ホストプロバイダーによって実装できない機能を実装します。</span><span class="sxs-lookup"><span data-stu-id="f8851-130">Implement functionality that cannot be implemented by the host provider, such as dynamically populating list boxes in the copied entry's details table from data on a server.</span></span>
    
- <span data-ttu-id="f8851-131">コピーしたエントリまたはインスタンス化されたテンプレートで、プロパティ間の相互作用を制御します。</span><span class="sxs-lookup"><span data-stu-id="f8851-131">Control the interaction among properties in a copied entry or instantiated template.</span></span> <span data-ttu-id="f8851-132">たとえば、[詳細] テーブルに表示されている他のプロパティから**PR_EMAIL_ADDRESS**を計算します。</span><span class="sxs-lookup"><span data-stu-id="f8851-132">For example, computing **PR_EMAIL_ADDRESS** from other properties displayed in the details table.</span></span> 
    
<span data-ttu-id="f8851-133">最初の2つの項目は、ラップされた property オブジェクトを提供する必要がないタスクの例です。これは、ホストプロバイダーの実装に基づく**imapiprop**の実装です。</span><span class="sxs-lookup"><span data-stu-id="f8851-133">The first two items are examples of tasks that do not require your provider to supply a wrapped property object — an implementation of **IMAPIProp** that is based on the host provider's implementation.</span></span> <span data-ttu-id="f8851-134">プロバイダーは単に必要に応じてプロパティを更新し、戻り、ホストプロバイダーによって渡されるポインターをポイントするように_lppMAPIPropNew_パラメーターを_lpMAPIPropData_パラメーターで設定することができます。</span><span class="sxs-lookup"><span data-stu-id="f8851-134">Your provider can simply update the properties as necessary and return, setting the  _lppMAPIPropNew_ parameter to point to the pointer passed in by the host provider in the  _lpMAPIPropData_ parameter.</span></span> 
  
<span data-ttu-id="f8851-135">2番目の2つのタスクでは、エントリのプロパティシートを表示する機能など、追加機能を持つホストプロバイダーのオブジェクトをラップするプロパティオブジェクトをプロバイダーがホストプロバイダーに返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8851-135">The second two tasks require that your provider return to the host provider a property object that wraps the host provider's object with additional functionality, such as the ability to display a property sheet for the entry.</span></span> <span data-ttu-id="f8851-136">この property オブジェクトは、 _lpMAPIPropData_パラメータのホストプロバイダによって渡されたオブジェクトの種類に応じて、メッセージのユーザーまたは配布リストのいずれかになります。 _lpinterface_パラメーターのインターフェイス識別子で示されます。</span><span class="sxs-lookup"><span data-stu-id="f8851-136">This property object will either be a messaging user or distribution list, depending on the type of object passed in by the host provider in the  _lpMAPIPropData_ parameter and indicated by the interface identifier in the  _lpInterface_ parameter.</span></span> <span data-ttu-id="f8851-137">_lpMAPIPropData_パラメーターがメッセージングユーザーを指している場合、プロバイダーのラップされた property オブジェクトは、 **imailuser**の実装である必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8851-137">If the  _lpMAPIPropData_ parameter points to a messaging user, your provider's wrapped property object must be an **IMailUser** implementation.</span></span> <span data-ttu-id="f8851-138">_lpMAPIPropData_が配布リストを指す場合は、 **idistlist**の実装である必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8851-138">If  _lpMAPIPropData_ points to a distribution list, it must be an **IDistList** implementation.</span></span> 
  
<span data-ttu-id="f8851-139">プロバイダーのラップされた property オブジェクトは、ホストプロバイダーの受信者のコンテキスト固有の操作を実行するために、 **imapiprop**メソッド呼び出しをインターセプトします。これは、ラップしているオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="f8851-139">Your provider's wrapped property object intercepts **IMAPIProp** method calls to perform context-specific manipulation of the host provider's recipient—the object it is wrapping.</span></span> <span data-ttu-id="f8851-140">ラップされた property オブジェクトに MAPI のみが必要です。 **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティを要求する[imapiprop:: openproperty](imapiprop-openproperty.md)へのすべての呼び出しは、ホストプロバイダーに渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8851-140">MAPI only has one requirement for wrapped property objects: all calls to [IMAPIProp::OpenProperty](imapiprop-openproperty.md) requesting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property should be passed to the host provider.</span></span> <span data-ttu-id="f8851-141">プロバイダーの実装は、返されたテーブルを使用して、表示テーブル通知を受け取るか、必要に応じて独自に追加することができます。</span><span class="sxs-lookup"><span data-stu-id="f8851-141">Your provider's implementation can use the returned table to intercept display table notifications or to add its own if necessary.</span></span> 
  
<span data-ttu-id="f8851-142">次の一覧は、通常、外部プロバイダーによって実装されたラップされた property オブジェクトに実装されるタスクを示しています。</span><span class="sxs-lookup"><span data-stu-id="f8851-142">The following list includes tasks that are typically implemented in the wrapped property object implemented by foreign providers:</span></span>
  
- <span data-ttu-id="f8851-143">[imapiprop:: GetProps](imapiprop-getprops.md)でのホスト受信者の前処理および後処理プロパティの値。</span><span class="sxs-lookup"><span data-stu-id="f8851-143">Preprocessing and postprocessing property values for the host recipient in [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
    
- <span data-ttu-id="f8851-144">処理の詳細は、 **imapiprop:: openproperty**で、ボタンやリストボックスなどのテーブルコントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="f8851-144">Handling details display table controls, such as buttons and list boxes, in **IMAPIProp::OpenProperty**.</span></span>
    
- <span data-ttu-id="f8851-145">[imapiprop:: setprops](imapiprop-setprops.md)のホスト受信者のプロパティ値を検証または操作します。</span><span class="sxs-lookup"><span data-stu-id="f8851-145">Validating or manipulating property values for the host recipient in [IMAPIProp::SetProps](imapiprop-setprops.md).</span></span>
    
- <span data-ttu-id="f8851-146">**PR_EMAIL_ADDRESS**などの必要なプロパティを計算し、ホストの受信者を[imapiprop:: SaveChanges](imapiprop-savechanges.md)に保存する前に、必要なすべてのプロパティが設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f8851-146">Computing required properties such as **PR_EMAIL_ADDRESS** and verifying that all of the necessary properties have been set before saving the host recipient in [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
### <a name="to-implement-iablogonopentemplateid"></a><span data-ttu-id="f8851-147">IABLogon:: OpenTemplateID を実装するには</span><span class="sxs-lookup"><span data-stu-id="f8851-147">To implement IABLogon::OpenTemplateID</span></span>
  
1. <span data-ttu-id="f8851-148">_lpTemplateID_パラメーターで渡されたテンプレート識別子が有効で、プロバイダーが認識する形式であるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="f8851-148">Check if the template identifier passed in with the  _lpTemplateID_ parameter is valid and is in a format that your provider recognizes.</span></span> <span data-ttu-id="f8851-149">そうでない場合は、失敗して MAPI_E_INVALID_ENTRYID を返します。</span><span class="sxs-lookup"><span data-stu-id="f8851-149">If it is not, fail and return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="f8851-150">テンプレート識別子で指定された種類のオブジェクトを作成します。これには、メッセージングユーザー、配布リスト、または1回限りの受信者のいずれかが指定されます。</span><span class="sxs-lookup"><span data-stu-id="f8851-150">Create an object of the type indicated by the template identifier, either a messaging user, distribution list, or one-off recipient.</span></span> 
    
3. <span data-ttu-id="f8851-151">ホストプロバイダーの property オブジェクトで、 _lpMAPIPropData_パラメーターで指定されているオブジェクトである**IUnknown:: AddRef**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f8851-151">Call the **IUnknown::AddRef** method in the host provider's property object, which is the object pointed to by the  _lpMAPIPropData_ parameter.</span></span> 
    
4. <span data-ttu-id="f8851-152">_ultemplateflags_パラメーターが FILL_ENTRY に設定されている場合:</span><span class="sxs-lookup"><span data-stu-id="f8851-152">If the  _ulTemplateFlags_ parameter is set to FILL_ENTRY:</span></span> 
    
   1. <span data-ttu-id="f8851-153">新しいオブジェクトがメッセージングユーザーまたは配布リストの場合:</span><span class="sxs-lookup"><span data-stu-id="f8851-153">If the new object is a messaging user or distribution list:</span></span>
      
      1. <span data-ttu-id="f8851-154">**imapiprop:: GetProps**メソッドを呼び出すことによって、新しいオブジェクトのすべてのプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="f8851-154">Retrieve all of the properties of the new object, possibly by calling its **IMAPIProp::GetProps** method.</span></span> 
          
      2. <span data-ttu-id="f8851-155">ホストプロバイダーの**imapiprop:: setprops**メソッドを呼び出して、取得したすべてのプロパティをホストプロバイダーの property オブジェクトにコピーします。</span><span class="sxs-lookup"><span data-stu-id="f8851-155">Call the host provider's **IMAPIProp::SetProps** method to copy all of the retrieved properties to the host provider's property object.</span></span> 
      
   2. <span data-ttu-id="f8851-156">新しいオブジェクトが1回限りの受信者である場合は、ホストプロバイダーの**imapiprop:: setprops**メソッドを呼び出して、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="f8851-156">If the new object is a one-off recipient, call the host provider's **IMAPIProp::SetProps** method to set the following properties:</span></span> 
      
      - <span data-ttu-id="f8851-157">**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md)) は、プロバイダーによって処理されるアドレスの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="f8851-157">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) to the address type handled by your provider.</span></span>
        
      - <span data-ttu-id="f8851-158">**PR\_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) は、 _lpTemplateID_パラメーターおよび_cbTemplateID_パラメーターからテンプレート識別子に対して行います。</span><span class="sxs-lookup"><span data-stu-id="f8851-158">**PR\_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) to the template identifier from the  _lpTemplateID_ and  _cbTemplateID_ parameters.</span></span> 
        
      - <span data-ttu-id="f8851-159">**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) から DT_MAILUSER または DT_DISTLIST に適宜。</span><span class="sxs-lookup"><span data-stu-id="f8851-159">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) to DT_MAILUSER or DT_DISTLIST, as appropriate.</span></span>
    
5. <span data-ttu-id="f8851-160">_lppMAPIPropNew_パラメーターの内容を、プロバイダーの新しいオブジェクトまたは_lpMAPIPropData_パラメーターを使用して渡された property オブジェクトのいずれかを指すように設定します。これは、プロバイダーがラップされたオブジェクトを必要とするかどうかによって決まります。</span><span class="sxs-lookup"><span data-stu-id="f8851-160">Set the contents of the  _lppMAPIPropNew_ parameter to point to either your provider's new object or the property object passed in with the  _lpMAPIPropData_ parameter, depending on whether your provider determines a wrapped object is necessary.</span></span> 
    
6. <span data-ttu-id="f8851-161">ネットワーク障害やメモリ不足の状態などの重大なエラーが発生した場合は、適切なエラー値を返します。</span><span class="sxs-lookup"><span data-stu-id="f8851-161">If a critical error occurs, such as a network failure or an out of memory condition, return the appropriate error value.</span></span> <span data-ttu-id="f8851-162">この値は、ホストプロバイダーによって実行されるタスクである適切な[MAPIERROR](mapierror.md)構造を使用して、クライアントに伝達される必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8851-162">This value should get propagated to the client with the appropriate [MAPIERROR](mapierror.md) structure, a task performed by the host provider.</span></span> 
    

