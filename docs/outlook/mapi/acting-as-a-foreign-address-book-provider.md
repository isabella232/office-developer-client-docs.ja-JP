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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435741"
---
# <a name="acting-as-a-foreign-address-book-provider"></a><span data-ttu-id="cd6f1-103">外部アドレス帳プロバイダーとして機能</span><span class="sxs-lookup"><span data-stu-id="cd6f1-103">Acting as a foreign address book provider</span></span>

<span data-ttu-id="cd6f1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd6f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd6f1-105">外部プロバイダーは、次のようなアドレス帳プロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-105">A foreign provider is an address book provider that:</span></span> 
  
- <span data-ttu-id="cd6f1-106">受信者のテンプレート識別子を割り当てる。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-106">Assigns template identifiers for its recipients.</span></span>
    
- <span data-ttu-id="cd6f1-107">[IABLogon::OpenTemplateID メソッドをサポート](iablogon-opentemplateid.md)します。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-107">Supports the [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) method.</span></span> 
    
- <span data-ttu-id="cd6f1-108">ホスト プロバイダーと呼ばれる他のアドレス帳プロバイダーのコンテナーに存在する受信者を維持するためのコードを提供します。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-108">Supplies code for maintaining recipients that exist in the containers of other address book providers known as host providers.</span></span> <span data-ttu-id="cd6f1-109">このコードには、ホスト プロバイダーからプロパティ オブジェクトをラップするプロパティ オブジェクト ( **通常は IMAPIProp** インターフェイス実装) が含まれる。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-109">This code involves a property object, typically an **IMAPIProp** interface implementation, which wraps a property object from the host provider.</span></span> 
    
<span data-ttu-id="cd6f1-110">外部プロバイダーとしての役割はオプションの役割です。すべてのプロバイダーがテンプレート識別子とその関連コードをサポートする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-110">Acting as a foreign provider is an optional role; not all providers need to support template identifiers and their related code.</span></span> <span data-ttu-id="cd6f1-111">プロバイダーによって提供されるテンプレートを使用してホスト プロバイダーが作成する受信者に対する制御を維持する場合は、プロバイダーを外部プロバイダーとして実装します。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-111">Implement your provider as a foreign provider if you want to maintain control over recipients that host providers create using templates supplied by your provider.</span></span> 
  
<span data-ttu-id="cd6f1-112">プロバイダーがエントリ識別子に使用する形式は、テンプレート識別子にも使用できます。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-112">The format that your provider uses for its entry identifiers can also be used for its template identifiers.</span></span> <span data-ttu-id="cd6f1-113">MAPI が適切なプロバイダーに受信者を正常にバインドするには、テンプレート識別子にプロバイダーの登録済み **MAPIUID** が含まれる必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-113">Template identifiers must include your provider's registered **MAPIUID** to enable MAPI to successfully bind recipients to the appropriate providers.</span></span> 
  
<span data-ttu-id="cd6f1-114">MAPI は、ホスト プロバイダーが [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)を呼び出す場合に、プロバイダーの **IABLogon::OpenTemplateID** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-114">MAPI calls your provider's **IABLogon::OpenTemplateID** method when a host provider calls [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md).</span></span> <span data-ttu-id="cd6f1-115">ホスト プロバイダーは **、IMAPISupport::OpenTemplateID** を呼び出す _lpTemplateID_ パラメーター内の受信者のテンプレート識別子を渡します。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-115">The host provider passes the template identifier of the recipient in the  _lpTemplateID_ parameter in its call to **IMAPISupport::OpenTemplateID**.</span></span> <span data-ttu-id="cd6f1-116">MAPI は、テンプレート識別子の [MAPIUID](mapiuid.md) を、ログオン時にプロバイダーが登録した **MAPIUID** と照合することで、テンプレート識別子がプロバイダーに属すると判断します。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-116">MAPI determines that the template identifier belongs to your provider by matching the [MAPIUID](mapiuid.md) in the template identifier with the **MAPIUID** that your provider registered at logon time.</span></span> <span data-ttu-id="cd6f1-117">MAPI は **、IABLogon::OpenTemplateID** メソッドを使用してホスト プロバイダーの呼び出しをプロバイダーに転送します。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-117">MAPI then forwards the host provider's call to your provider through the **IABLogon::OpenTemplateID** method.</span></span> 
  
<span data-ttu-id="cd6f1-118">ホスト プロバイダーは _、lpMAPIPropData_ パラメーターの受信者のプロパティ オブジェクト実装へのポインター _、lpMAPIPropData_ で渡されるインターフェイス実装の種類に対応する _lpInterface_ パラメーターのインターフェイス識別子、およびオプションのフラグ FILL_ENTRY を渡します。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-118">The host provider also passes a pointer to its property object implementation for the recipient in the  _lpMAPIPropData_ parameter, an interface identifier in the  _lpInterface_ parameter that corresponds to the type of interface implementation passed in  _lpMAPIPropData_, and an optional flag, FILL_ENTRY.</span></span> <span data-ttu-id="cd6f1-119">プロバイダーは  _、lppMAPIPropNew_ パラメーターに lpInterface で指定された型のプロパティ オブジェクト実装へのポインター  _を返す必要があります_。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-119">Your provider is expected to return in the  _lppMAPIPropNew_ parameter a pointer to a property object implementation of the type specified in  _lpInterface_.</span></span> <span data-ttu-id="cd6f1-120">返されるポインターは、プロバイダーによって実装されたラップされたプロパティ オブジェクト、または  _lpMAPIPropData_ のホスト プロバイダーによって提供されるオブジェクトのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-120">The returned pointer can either be to the wrapped property object implemented by your provider or to the object supplied by the host provider in  _lpMAPIPropData_.</span></span> <span data-ttu-id="cd6f1-121">プロバイダーは、次の場合にラップされたプロパティ オブジェクト ポインターを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-121">Your provider should return a wrapped property object pointer when:</span></span>
  
- <span data-ttu-id="cd6f1-122">受信者の表示テーブルには、リスト ボックス コントロールが含まれています。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-122">The recipient's display table contains list box controls.</span></span>
    
- <span data-ttu-id="cd6f1-123">受信者の電子メール アドレスは、複数の表示テーブル コントロールのデータから組み立てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-123">The email address for the recipient must be assembled from data in multiple display table controls.</span></span>
    
- <span data-ttu-id="cd6f1-124">プロバイダーは、表示テーブル通知を発行します。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-124">Your provider issues display table notifications.</span></span>
    
<span data-ttu-id="cd6f1-125">[FILL_ENTRY] フラグは、ホスト プロバイダーが受信者のすべてのプロパティを更新する必要があるというメッセージをプロバイダーに示します。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-125">The FILL_ENTRY flag indicates to your provider that the host provider requires all the properties of the recipient to be updated.</span></span> <span data-ttu-id="cd6f1-126">プロバイダーは、この要求を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-126">Your provider is required to fulfill this request.</span></span>
  
<span data-ttu-id="cd6f1-127">ホスト プロバイダーがプロバイダーの **OpenTemplateID** メソッドを呼び出す場合、プロバイダーは次の場合があります。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-127">When a host provider calls your provider's **OpenTemplateID** method, your provider might:</span></span> 
  
- <span data-ttu-id="cd6f1-128">コピーされたエントリのデータを定期的に更新します。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-128">Periodically update the data for a copied entry.</span></span>
    
- <span data-ttu-id="cd6f1-129">コピーされたエントリを、アドレス帳エントリが個人用アドレス帳にコピーされる場合など、元のエントリと同期された状態に保つ。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-129">Keep a copied entry synchronized with its original, such as when an address book entry is copied to the personal address book.</span></span>
    
- <span data-ttu-id="cd6f1-130">サーバー上のデータからコピーされたエントリの詳細テーブルにリスト ボックスを動的に設定するなど、ホスト プロバイダーが実装できない機能を実装します。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-130">Implement functionality that cannot be implemented by the host provider, such as dynamically populating list boxes in the copied entry's details table from data on a server.</span></span>
    
- <span data-ttu-id="cd6f1-131">コピーされたエントリまたはインスタンス化されたテンプレート内のプロパティ間の相互作用を制御します。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-131">Control the interaction among properties in a copied entry or instantiated template.</span></span> <span data-ttu-id="cd6f1-132">たとえば、詳細テーブル **PR_EMAIL_ADDRESS** 他のプロパティからデータを計算します。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-132">For example, computing **PR_EMAIL_ADDRESS** from other properties displayed in the details table.</span></span> 
    
<span data-ttu-id="cd6f1-133">最初の 2 つの項目は、プロバイダーがラップされたプロパティ オブジェクト (ホスト プロバイダーの実装に基づく **IMAPIProp** の実装) を提供する必要としないタスクの例です。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-133">The first two items are examples of tasks that do not require your provider to supply a wrapped property object — an implementation of **IMAPIProp** that is based on the host provider's implementation.</span></span> <span data-ttu-id="cd6f1-134">プロバイダーは、必要に応じてプロパティを更新して返すだけで  _、lppMAPIPropNew_ パラメーターを  _lpMAPIPropData_ パラメーターでホスト プロバイダーが渡すポインターをポイントする設定を行います。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-134">Your provider can simply update the properties as necessary and return, setting the  _lppMAPIPropNew_ parameter to point to the pointer passed in by the host provider in the  _lpMAPIPropData_ parameter.</span></span> 
  
<span data-ttu-id="cd6f1-135">2 番目の 2 つのタスクでは、プロバイダーがホスト プロバイダーに戻り、ホスト プロバイダーのオブジェクトを折り返すプロパティ オブジェクト (エントリのプロパティ シートを表示する機能など) を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-135">The second two tasks require that your provider return to the host provider a property object that wraps the host provider's object with additional functionality, such as the ability to display a property sheet for the entry.</span></span> <span data-ttu-id="cd6f1-136">このプロパティ オブジェクトは  _、lpMAPIPropData_ パラメーターでホスト プロバイダーによって渡され  _、lpInterface_ パラメーターのインターフェイス識別子によって示されるオブジェクトの種類に応じて、メッセージング ユーザーまたは配布リストになります。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-136">This property object will either be a messaging user or distribution list, depending on the type of object passed in by the host provider in the  _lpMAPIPropData_ parameter and indicated by the interface identifier in the  _lpInterface_ parameter.</span></span> <span data-ttu-id="cd6f1-137">_lpMAPIPropData_ パラメーターがメッセージング ユーザーをポイントする場合、プロバイダーのラップされたプロパティ オブジェクトは **IMailUser 実装である必要** があります。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-137">If the  _lpMAPIPropData_ parameter points to a messaging user, your provider's wrapped property object must be an **IMailUser** implementation.</span></span> <span data-ttu-id="cd6f1-138">_lpMAPIPropData が_ 配布リストをポイントする場合は **、IDistList 実装である必要** があります。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-138">If  _lpMAPIPropData_ points to a distribution list, it must be an **IDistList** implementation.</span></span> 
  
<span data-ttu-id="cd6f1-139">プロバイダーのラップされたプロパティ オブジェクトは **、IMAPIProp** メソッドの呼び出しをインターセプトして、ホスト プロバイダーの受信者 (ラップしているオブジェクト) のコンテキスト固有の操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-139">Your provider's wrapped property object intercepts **IMAPIProp** method calls to perform context-specific manipulation of the host provider's recipient—the object it is wrapping.</span></span> <span data-ttu-id="cd6f1-140">MAPI には、ラップされたプロパティ オブジェクトの要件が **1** つのみです。PR_DETAILS_TABLE ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティを要求する [IMAPIProp::OpenProperty](imapiprop-openproperty.md)へのすべての呼び出しをホスト プロバイダーに渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-140">MAPI only has one requirement for wrapped property objects: all calls to [IMAPIProp::OpenProperty](imapiprop-openproperty.md) requesting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property should be passed to the host provider.</span></span> <span data-ttu-id="cd6f1-141">プロバイダーの実装では、返されるテーブルを使用して、表示テーブルの通知を傍受したり、必要に応じて独自の通知を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-141">Your provider's implementation can use the returned table to intercept display table notifications or to add its own if necessary.</span></span> 
  
<span data-ttu-id="cd6f1-142">次の一覧には、外部プロバイダーによって実装されるラップされたプロパティ オブジェクトに通常実装されるタスクが含まれています。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-142">The following list includes tasks that are typically implemented in the wrapped property object implemented by foreign providers:</span></span>
  
- <span data-ttu-id="cd6f1-143">[IMAPIProp::GetProps](imapiprop-getprops.md)でホスト受信者のプロパティ値を前処理および後処理します。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-143">Preprocessing and postprocessing property values for the host recipient in [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
    
- <span data-ttu-id="cd6f1-144">**IMAPIProp::OpenProperty** で、ボタンやリスト ボックスなどの詳細表示テーブル コントロールを処理します。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-144">Handling details display table controls, such as buttons and list boxes, in **IMAPIProp::OpenProperty**.</span></span>
    
- <span data-ttu-id="cd6f1-145">[IMAPIProp::SetProps](imapiprop-setprops.md)でホスト受信者のプロパティ値を検証または操作します。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-145">Validating or manipulating property values for the host recipient in [IMAPIProp::SetProps](imapiprop-setprops.md).</span></span>
    
- <span data-ttu-id="cd6f1-146">ホスト受信者を[IMAPIProp::SaveChanges](imapiprop-savechanges.md)に保存する前に、PR_EMAIL_ADDRESS などの必須プロパティを計算し、必要なすべてのプロパティが設定されているのを確認します。 </span><span class="sxs-lookup"><span data-stu-id="cd6f1-146">Computing required properties such as **PR_EMAIL_ADDRESS** and verifying that all of the necessary properties have been set before saving the host recipient in [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
### <a name="to-implement-iablogonopentemplateid"></a><span data-ttu-id="cd6f1-147">IABLogon::OpenTemplateID を実装するには</span><span class="sxs-lookup"><span data-stu-id="cd6f1-147">To implement IABLogon::OpenTemplateID</span></span>
  
1. <span data-ttu-id="cd6f1-148">_lpTemplateID_ パラメーターで渡されたテンプレート識別子が有効で、プロバイダーが認識する形式にあるか確認します。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-148">Check if the template identifier passed in with the  _lpTemplateID_ parameter is valid and is in a format that your provider recognizes.</span></span> <span data-ttu-id="cd6f1-149">エラーが発生しない場合は、エラーが発生し、MAPI_E_INVALID_ENTRYID。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-149">If it is not, fail and return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="cd6f1-150">テンプレート識別子で示される種類のオブジェクト (メッセージング ユーザー、配布リスト、または一時受信者) を作成します。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-150">Create an object of the type indicated by the template identifier, either a messaging user, distribution list, or one-off recipient.</span></span> 
    
3. <span data-ttu-id="cd6f1-151">_lpMAPIPropData_ パラメーターが指すオブジェクトであるホスト プロバイダーのプロパティ オブジェクトで **、IUnknown::AddRef** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-151">Call the **IUnknown::AddRef** method in the host provider's property object, which is the object pointed to by the  _lpMAPIPropData_ parameter.</span></span> 
    
4. <span data-ttu-id="cd6f1-152">_ulTemplateFlags_ パラメーターが次の値に設定FILL_ENTRY。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-152">If the  _ulTemplateFlags_ parameter is set to FILL_ENTRY:</span></span> 
    
   1. <span data-ttu-id="cd6f1-153">新しいオブジェクトがメッセージング ユーザーまたは配布リストの場合:</span><span class="sxs-lookup"><span data-stu-id="cd6f1-153">If the new object is a messaging user or distribution list:</span></span>
      
      1. <span data-ttu-id="cd6f1-154">**IMAPIProp::GetProps** メソッドを呼び出して、新しいオブジェクトのすべてのプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-154">Retrieve all of the properties of the new object, possibly by calling its **IMAPIProp::GetProps** method.</span></span> 
          
      2. <span data-ttu-id="cd6f1-155">ホスト プロバイダーの **IMAPIProp::SetProps** メソッドを呼び出して、取得したプロパティをホスト プロバイダーのプロパティ オブジェクトにコピーします。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-155">Call the host provider's **IMAPIProp::SetProps** method to copy all of the retrieved properties to the host provider's property object.</span></span> 
      
   2. <span data-ttu-id="cd6f1-156">新しいオブジェクトが 1 回の受信者である場合は、ホスト プロバイダーの **IMAPIProp::SetProps** メソッドを呼び出して、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-156">If the new object is a one-off recipient, call the host provider's **IMAPIProp::SetProps** method to set the following properties:</span></span> 
      
      - <span data-ttu-id="cd6f1-157">**PR_ADDRTYPE** [(PidTagAddressType)](pidtagaddresstype-canonical-property.md)をプロバイダーが処理するアドレスの種類に設定します。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-157">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) to the address type handled by your provider.</span></span>
        
      - <span data-ttu-id="cd6f1-158">**PR \_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) を  _lpTemplateID_ パラメーターと  _cbTemplateID_ パラメーターからテンプレート識別子に指定します。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-158">**PR\_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) to the template identifier from the  _lpTemplateID_ and  _cbTemplateID_ parameters.</span></span> 
        
      - <span data-ttu-id="cd6f1-159">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) を使用して、DT_MAILUSERまたはDT_DISTLISTに設定します。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-159">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) to DT_MAILUSER or DT_DISTLIST, as appropriate.</span></span>
    
5. <span data-ttu-id="cd6f1-160">プロバイダーがラップされたオブジェクトが必要であると判断するかどうかに応じて  _、lppMAPIPropNew_ パラメーターの内容を、プロバイダーの新しいオブジェクトまたは  _lpMAPIPropData_ パラメーターで渡されたプロパティ オブジェクトを指す値を設定します。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-160">Set the contents of the  _lppMAPIPropNew_ parameter to point to either your provider's new object or the property object passed in with the  _lpMAPIPropData_ parameter, depending on whether your provider determines a wrapped object is necessary.</span></span> 
    
6. <span data-ttu-id="cd6f1-161">ネットワーク障害やメモリ切れなどの重大なエラーが発生した場合は、適切なエラー値を返します。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-161">If a critical error occurs, such as a network failure or an out of memory condition, return the appropriate error value.</span></span> <span data-ttu-id="cd6f1-162">この値は、ホスト プロバイダーによって実行されるタスクである [、適切な MAPIERROR](mapierror.md) 構造を使用してクライアントに伝達される必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd6f1-162">This value should get propagated to the client with the appropriate [MAPIERROR](mapierror.md) structure, a task performed by the host provider.</span></span> 
    

