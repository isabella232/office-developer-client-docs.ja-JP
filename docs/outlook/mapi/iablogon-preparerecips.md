---
title: IABLogonPrepareRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.PrepareRecips
api_type:
- COM
ms.assetid: 3c1845ea-e291-4855-9afd-51d2c64d7e85
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 82a7ecc8fbad0baf67b49c80c5a62cb8df94dfd1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800353"
---
# <a name="iablogonpreparerecips"></a><span data-ttu-id="d56f1-103">IABLogon::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="d56f1-103">IABLogon::PrepareRecips</span></span>

<span data-ttu-id="d56f1-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d56f1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d56f1-105">メッセージング システムによって後で使用できる受信者のリストを準備します。</span><span class="sxs-lookup"><span data-stu-id="d56f1-105">Prepares a recipient list for later use by the messaging system.</span></span>
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="d56f1-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="d56f1-106">Parameters</span></span>

<span data-ttu-id="d56f1-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d56f1-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d56f1-108">[in]返される文字列内のテキストの種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="d56f1-108">[in] A bitmask of flags that controls the type of the text in the returned strings.</span></span> <span data-ttu-id="d56f1-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="d56f1-109">The following flag can be set:</span></span>
    
  - <span data-ttu-id="d56f1-110">MAPI_CACHE_ONLY: は、名前解決を実行するのには、オフライン アドレス帳のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="d56f1-110">MAPI_CACHE_ONLY: Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="d56f1-111">たとえば、このフラグを使用すると、exchange キャッシュ モードでグローバル アドレス一覧 (GAL) を開き、クライアントとサーバー間のトラフィックを作成することがなく、キャッシュからそのアドレス帳のエントリにアクセスするのにクライアント アプリケーションを許可します。</span><span class="sxs-lookup"><span data-stu-id="d56f1-111">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="d56f1-112">このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。</span><span class="sxs-lookup"><span data-stu-id="d56f1-112">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="d56f1-113">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="d56f1-113">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="d56f1-114">[in]更新を必要とするプロパティを指定するプロパティ タグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d56f1-114">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags that indicate the properties that require updating, if any.</span></span> <span data-ttu-id="d56f1-115">_LpPropTagArray_パラメーターは NULL にできます。</span><span class="sxs-lookup"><span data-stu-id="d56f1-115">The  _lpPropTagArray_ parameter can be NULL.</span></span> 
    
<span data-ttu-id="d56f1-116">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="d56f1-116">_lpRecipList_</span></span>
  
> <span data-ttu-id="d56f1-117">[in]受信者の一覧を保持する[ADRLIST](adrlist.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d56f1-117">[in] A pointer to an [ADRLIST](adrlist.md) structure that holds the recipient list.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d56f1-118">�߂�l</span><span class="sxs-lookup"><span data-stu-id="d56f1-118">Return value</span></span>

<span data-ttu-id="d56f1-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="d56f1-119">S_OK</span></span> 
  
> <span data-ttu-id="d56f1-120">宛先リストの準備ができました。</span><span class="sxs-lookup"><span data-stu-id="d56f1-120">The recipient list was successfully prepared.</span></span>
    
<span data-ttu-id="d56f1-121">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="d56f1-121">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="d56f1-122">_LpRecipList_パラメーター内の受信者のいずれかが存在しません。</span><span class="sxs-lookup"><span data-stu-id="d56f1-122">One or more of the recipients in the  _lpRecipList_ parameter do not exist.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d56f1-123">�߂�l</span><span class="sxs-lookup"><span data-stu-id="d56f1-123">Return value</span></span>

<span data-ttu-id="d56f1-124">クライアントでは、1 つまたは複数の受信者のプロパティのセットを再配置を変更または MAPI の[IAddrBook::PrepareRecips](iaddrbook-preparerecips.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d56f1-124">A client calls the MAPI [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) method to modify or rearrange a set of properties for one or more recipients.</span></span> <span data-ttu-id="d56f1-125">受信者は、送信メッセージの受信者の一覧の一部ではないです。</span><span class="sxs-lookup"><span data-stu-id="d56f1-125">The recipients may or may not be part of the recipient list of an outgoing message.</span></span> <span data-ttu-id="d56f1-126">MAPI は、アドレス帳プロバイダーの**IABLogon::PrepareRecips**メソッドへの呼び出しを転送します。</span><span class="sxs-lookup"><span data-stu-id="d56f1-126">MAPI transfers this call to an address book provider's **IABLogon::PrepareRecips** method.</span></span> 
  
<span data-ttu-id="d56f1-127">**IABLogon::PrepareRecips**は、4 つの主要なタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="d56f1-127">**IABLogon::PrepareRecips** performs four main tasks:</span></span> 
  
- <span data-ttu-id="d56f1-128">アドレス] ボックスの一覧のすべての受信者が指す_lpRecipList_パラメーターで、長期のエントリ id があることを保証します。</span><span class="sxs-lookup"><span data-stu-id="d56f1-128">Ensures that all recipients in the address list pointed to by the  _lpRecipList_ parameter have a long-term entry identifier.</span></span> 
    
- <span data-ttu-id="d56f1-129">すべての受信者に、 _lpPropTagArray_パラメーターで指定されたプロパティ値の配列で指定されたプロパティがあることを保証します。</span><span class="sxs-lookup"><span data-stu-id="d56f1-129">Ensures that all recipients have the properties specified in the property value array pointed to by the  _lpPropTagArray_ parameter.</span></span> 
    
- <span data-ttu-id="d56f1-130">呼び出しの前に存在していた他のすべてのプロパティの前に、プロパティ値の配列からプロパティが表示されることを保証します。</span><span class="sxs-lookup"><span data-stu-id="d56f1-130">Ensures that the properties from the property value array appear before any other properties that existed before the call.</span></span>
    
- <span data-ttu-id="d56f1-131">確実に**ADRLIST**構造体の各宛て先用の[ADRENTRY](adrentry.md)の構造体のプロパティの順序は、プロパティ値の配列の場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="d56f1-131">Ensures that the order of the properties in each recipient's [ADRENTRY](adrentry.md) structure in the **ADRLIST** structure is the same as in the property value array.</span></span> 
    
<span data-ttu-id="d56f1-132">_LpRecipList_パラメーターに**ADRENTRY**構造体には、受信者ごとに 1 つの**ADRENTRY**構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d56f1-132">The **ADRENTRY** structure in the  _lpRecipList_ parameter contains one **ADRENTRY** structure for each recipient.</span></span> <span data-ttu-id="d56f1-133">**ADRENTRY**の各構造体には、受信者のプロパティを記述する[SPropValue](spropvalue.md)構造体の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d56f1-133">Each **ADRENTRY** structure contains an array of [SPropValue](spropvalue.md) structures to describe the recipient's properties.</span></span> <span data-ttu-id="d56f1-134">**IABLogon::PrepareRecips**が返されると、受信者ごとに**SPropValue**構造体の配列には、受信者の他のプロパティの後に_lpPropTagArray_からのプロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d56f1-134">When **IABLogon::PrepareRecips** returns, the **SPropValue** structure array for each recipient includes the properties from the  _lpPropTagArray_ followed by the other properties for the recipient.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d56f1-135">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="d56f1-135">Notes to implementers</span></span>

<span data-ttu-id="d56f1-136">**IABLogon::PrepareRecips**を実装するには、プロパティの値を取得する、短期的なエントリの識別子を長期的なエントリの識別子に変換するプロパティを特定の順序で配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d56f1-136">Implementing **IABLogon::PrepareRecips** involves putting properties in a specific order, retrieving property values, and converting short-term entry identifiers to long-term entry identifiers.</span></span> <span data-ttu-id="d56f1-137">_LpPropTagArray_パラメーターで要求されたプロパティは、 _lpRecipList_パラメーターで、各受信者の**ADRENTRY**の構造体に関連付けられているプロパティ値の配列の先頭にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d56f1-137">The properties that are requested in the  _lpPropTagArray_ parameter must be at the start of the property value array associated with each recipient's **ADRENTRY** structure in the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="d56f1-138">これらのプロパティの値が存在しない場合のエントリ id を使用して、関連付けられているメッセージのユーザーまたは配布リストを開くし、欠落しているプロパティ値を取得します。</span><span class="sxs-lookup"><span data-stu-id="d56f1-138">If values for these properties do not exist, open the associated messaging user or distribution list by using its entry identifier and retrieve the missing property values.</span></span> 
  
<span data-ttu-id="d56f1-139">渡された_lpRecipList_とは別に個別に構造体を解放することができるように、各**SPropValue**構造体を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="d56f1-139">Allocate each **SPropValue** structure passed in  _lpRecipList_ separately so that the structures can be freed individually.</span></span> <span data-ttu-id="d56f1-140">**SPropValue**構造体に追加の空き領域を割り当てる必要があります場合、たとえば、文字列のプロパティのデータを格納するのに関数を使用[MAPIAllocateBuffer](mapiallocatebuffer.md)全プロパティの値の配列に追加の領域を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="d56f1-140">If you must allocate additional space for any **SPropValue** structure, for example, to store the data for a string property, use the [MAPIAllocateBuffer](mapiallocatebuffer.md) function to allocate additional space for the full property value array.</span></span> <span data-ttu-id="d56f1-141">[MAPIFreeBuffer](mapifreebuffer.md)関数を使用して、元のプロパティ値の配列を解放して、 [MAPIAllocateMore](mapiallocatemore.md)関数を使用して必要な追加のメモリを割り当てることです。</span><span class="sxs-lookup"><span data-stu-id="d56f1-141">Use the [MAPIFreeBuffer](mapifreebuffer.md) function to free the original property value array, and then use the [MAPIAllocateMore](mapiallocatemore.md) function to allocate any additional memory that is required.</span></span> 
  
<span data-ttu-id="d56f1-142">**IABLogon::PrepareRecips**を実装するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="d56f1-142">To implement **IABLogon::PrepareRecips**, use the following procedure:</span></span>
  
1. <span data-ttu-id="d56f1-143">_LpPropTagArray_パラメーターのエントリを確認します。</span><span class="sxs-lookup"><span data-stu-id="d56f1-143">Check for entries in the  _lpPropTagArray_ parameter.</span></span> <span data-ttu-id="d56f1-144">プロパティの値の配列が空の場合は、実行する作業はありません。</span><span class="sxs-lookup"><span data-stu-id="d56f1-144">If the property value array is empty, there is no work to do.</span></span> <span data-ttu-id="d56f1-145">成功値を返します。</span><span class="sxs-lookup"><span data-stu-id="d56f1-145">Return a success value.</span></span> 
    
2. <span data-ttu-id="d56f1-146">_LpRecipList_パラメーターでは、各受信者を処理します。</span><span class="sxs-lookup"><span data-stu-id="d56f1-146">Process each recipient in the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="d56f1-147">リスト内の受信者ごとに 1 つの**ADRENTRY**構造体のメンバーがあります。</span><span class="sxs-lookup"><span data-stu-id="d56f1-147">There is one **ADRENTRY** structure member for each recipient in the list.</span></span> <span data-ttu-id="d56f1-148">次の種類の受信者を無視するには。</span><span class="sxs-lookup"><span data-stu-id="d56f1-148">Ignore the following types of recipients:</span></span> 
    
   - <span data-ttu-id="d56f1-149">エントリ id、 **ADRENTRY**の構造 (つまり、未解決の受信者) の**rgPropVals**のメンバーでない受信者を指定します。</span><span class="sxs-lookup"><span data-stu-id="d56f1-149">Recipients without an entry identifier in the **rgPropVals** member of their **ADRENTRY** structure (that is, unresolved recipients).</span></span> 
    
   - <span data-ttu-id="d56f1-150">プロバイダーに属していないエントリの識別子を持つ受信者。</span><span class="sxs-lookup"><span data-stu-id="d56f1-150">Recipients with an entry identifier that does not belong to your provider.</span></span> <span data-ttu-id="d56f1-151">これらの受信者は、別のアドレス帳プロバイダーに渡されます。</span><span class="sxs-lookup"><span data-stu-id="d56f1-151">These recipients will be passed to another address book provider.</span></span>
    
3. <span data-ttu-id="d56f1-152">受信者を開き、受信者に対して既に設定されているプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="d56f1-152">Open the recipient and retrieve the properties that are already set for the recipient.</span></span>
    
4. <span data-ttu-id="d56f1-153">**GetProps**から返されるプロパティの配列を_lpRecipList_で指定されたプロパティ値の配列をマージします。</span><span class="sxs-lookup"><span data-stu-id="d56f1-153">Merge the property value array specified in the  _lpRecipList_ with the array of properties returned from **GetProps**.</span></span> <span data-ttu-id="d56f1-154">プロパティの両方のアレイでは、同じプロパティが発生する場合は、 _lpRecipList_の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="d56f1-154">If the same property occurs in both property arrays, use the value from  _lpRecipList_.</span></span>
    
5. <span data-ttu-id="d56f1-155">_LpRecipList_プロパティの値の配列がすべての必要なプロパティを保持するのに十分な大きさの場合は、結合配列を使用して置き換えるだけです。</span><span class="sxs-lookup"><span data-stu-id="d56f1-155">If the  _lpRecipList_ property value array is big enough to hold all of the necessary properties, just replace it with the merged array.</span></span> <span data-ttu-id="d56f1-156">_LpRecipList_プロパティの値の配列が十分な大きさでない場合は、新しく割り当てられた配列を使用して交換してください。</span><span class="sxs-lookup"><span data-stu-id="d56f1-156">If the  _lpRecipList_ property value array is not big enough, replace it with a newly allocated array.</span></span> <span data-ttu-id="d56f1-157">新しい配列価値がある更新されたそれぞれの**あう**メンバーのことを確認してあります。</span><span class="sxs-lookup"><span data-stu-id="d56f1-157">Be sure the new array has an updated value in each of its **cValues** members.</span></span> 
    
6. <span data-ttu-id="d56f1-158">_LpPropTagArray_パラメーターのプロパティのいずれかを認識していない場合は、プロパティの型を設定 PT_ERROR と MAPI_E_NOT_FOUND をまたはよりは、別の値にプロパティの値を受信者の**ADRENTRY**の構造体にプロパティの使用不可時間の特定の理由です。</span><span class="sxs-lookup"><span data-stu-id="d56f1-158">If you do not recognize one or more of the properties in the  _lpPropTagArray_ parameter, set the property type in the recipient's **ADRENTRY** structure to PT_ERROR and the property value either to MAPI_E_NOT_FOUND or to another value that gives a more specific reason for the unavailability of the property.</span></span> <span data-ttu-id="d56f1-159">PT_ERROR 詳細については、[プロパティの型](property-types.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d56f1-159">For information about PT_ERROR, see [Property Types](property-types.md).</span></span>
    
> [!NOTE]
> <span data-ttu-id="d56f1-160">**IABLogon::PrepareRecips**に渡される**ADRLIST**構造体を割り当て直すことはありませんか、エントリの数を変更します。</span><span class="sxs-lookup"><span data-stu-id="d56f1-160">Never reallocate the **ADRLIST** structure that is passed into **IABLogon::PrepareRecips** or change its number of entries.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d56f1-161">関連項目</span><span class="sxs-lookup"><span data-stu-id="d56f1-161">See also</span></span>

- [<span data-ttu-id="d56f1-162">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="d56f1-162">ADRLIST</span></span>](adrlist.md)
- [<span data-ttu-id="d56f1-163">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="d56f1-163">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
- [<span data-ttu-id="d56f1-164">PidTagEntryId の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="d56f1-164">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
- [<span data-ttu-id="d56f1-165">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d56f1-165">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="d56f1-166">IABLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d56f1-166">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

