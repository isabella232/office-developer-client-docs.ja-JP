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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 0a9b88d762ca88cebd6d9acecf06db53a0b778f6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423861"
---
# <a name="iablogonpreparerecips"></a><span data-ttu-id="d6e10-103">IABLogon::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="d6e10-103">IABLogon::PrepareRecips</span></span>

<span data-ttu-id="d6e10-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6e10-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6e10-105">メッセージング システムで後で使用する受信者リストを準備します。</span><span class="sxs-lookup"><span data-stu-id="d6e10-105">Prepares a recipient list for later use by the messaging system.</span></span>
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="d6e10-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d6e10-106">Parameters</span></span>

<span data-ttu-id="d6e10-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d6e10-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d6e10-108">[in]返される文字列内のテキストの種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="d6e10-108">[in] A bitmask of flags that controls the type of the text in the returned strings.</span></span> <span data-ttu-id="d6e10-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="d6e10-109">The following flag can be set:</span></span>
    
  - <span data-ttu-id="d6e10-110">MAPI_CACHE_ONLY: 名前解決を実行するには、オフライン アドレス帳のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="d6e10-110">MAPI_CACHE_ONLY: Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="d6e10-111">たとえば、このフラグを使用すると、クライアント アプリケーションがキャッシュされた Exchange モードでグローバル アドレス一覧 (GAL) を開き、クライアントとサーバー間のトラフィックを作成せずにキャッシュからそのアドレス帳のエントリにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="d6e10-111">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="d6e10-112">このフラグは、アドレス帳プロバイダー Exchangeサポートされます。</span><span class="sxs-lookup"><span data-stu-id="d6e10-112">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="d6e10-113">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="d6e10-113">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="d6e10-114">[in]更新が必要なプロパティを示すプロパティ タグの配列を含む [SPropTagArray](sproptagarray.md) 構造体へのポインター (該当する場合)。</span><span class="sxs-lookup"><span data-stu-id="d6e10-114">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags that indicate the properties that require updating, if any.</span></span> <span data-ttu-id="d6e10-115">_lpPropTagArray パラメーター_ には NULL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="d6e10-115">The  _lpPropTagArray_ parameter can be NULL.</span></span> 
    
<span data-ttu-id="d6e10-116">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="d6e10-116">_lpRecipList_</span></span>
  
> <span data-ttu-id="d6e10-117">[in]受信者リストを [保持する ADRLIST](adrlist.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d6e10-117">[in] A pointer to an [ADRLIST](adrlist.md) structure that holds the recipient list.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d6e10-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="d6e10-118">Return value</span></span>

<span data-ttu-id="d6e10-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="d6e10-119">S_OK</span></span> 
  
> <span data-ttu-id="d6e10-120">受信者リストが正常に準備されました。</span><span class="sxs-lookup"><span data-stu-id="d6e10-120">The recipient list was successfully prepared.</span></span>
    
<span data-ttu-id="d6e10-121">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="d6e10-121">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="d6e10-122">_lpRecipList_ パラメーター内の 1 つ以上の受信者が存在しません。</span><span class="sxs-lookup"><span data-stu-id="d6e10-122">One or more of the recipients in the  _lpRecipList_ parameter do not exist.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d6e10-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="d6e10-123">Return value</span></span>

<span data-ttu-id="d6e10-124">クライアントは、MAPI [IAddrBook::P repareRecips](iaddrbook-preparerecips.md) メソッドを呼び出して、1 つ以上の受信者のプロパティのセットを変更または再配置します。</span><span class="sxs-lookup"><span data-stu-id="d6e10-124">A client calls the MAPI [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) method to modify or rearrange a set of properties for one or more recipients.</span></span> <span data-ttu-id="d6e10-125">受信者は、送信メッセージの受信者リストの一部である場合と一部ではない場合があります。</span><span class="sxs-lookup"><span data-stu-id="d6e10-125">The recipients may or may not be part of the recipient list of an outgoing message.</span></span> <span data-ttu-id="d6e10-126">MAPI は、アドレス帳プロバイダーの **IABLogon::P repareRecips メソッドにこの呼び出しを転送** します。</span><span class="sxs-lookup"><span data-stu-id="d6e10-126">MAPI transfers this call to an address book provider's **IABLogon::PrepareRecips** method.</span></span> 
  
<span data-ttu-id="d6e10-127">**IABLogon::P repareRecips は** 、次の 4 つの主要なタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="d6e10-127">**IABLogon::PrepareRecips** performs four main tasks:</span></span> 
  
- <span data-ttu-id="d6e10-128">_lpRecipList_ パラメーターが指すアドレス一覧のすべての受信者に、長期的なエントリ識別子が設定されます。</span><span class="sxs-lookup"><span data-stu-id="d6e10-128">Ensures that all recipients in the address list pointed to by the  _lpRecipList_ parameter have a long-term entry identifier.</span></span> 
    
- <span data-ttu-id="d6e10-129">すべての受信者が  _、lpPropTagArray_ パラメーターが指すプロパティ値配列で指定されたプロパティを持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="d6e10-129">Ensures that all recipients have the properties specified in the property value array pointed to by the  _lpPropTagArray_ parameter.</span></span> 
    
- <span data-ttu-id="d6e10-130">プロパティ値配列のプロパティが、呼び出し前に存在していた他のプロパティの前に表示されます。</span><span class="sxs-lookup"><span data-stu-id="d6e10-130">Ensures that the properties from the property value array appear before any other properties that existed before the call.</span></span>
    
- <span data-ttu-id="d6e10-131">**ADRLIST** 構造内の各受信者の [ADRENTRY](adrentry.md)構造のプロパティの順序がプロパティ値配列と同じことを確認します。</span><span class="sxs-lookup"><span data-stu-id="d6e10-131">Ensures that the order of the properties in each recipient's [ADRENTRY](adrentry.md) structure in the **ADRLIST** structure is the same as in the property value array.</span></span> 
    
<span data-ttu-id="d6e10-132">**lpRecipList** パラメーターの _ADRENTRY_ 構造には、受信者ごとに **1 つの ADRENTRY** 構造が含まれる。</span><span class="sxs-lookup"><span data-stu-id="d6e10-132">The **ADRENTRY** structure in the  _lpRecipList_ parameter contains one **ADRENTRY** structure for each recipient.</span></span> <span data-ttu-id="d6e10-133">各 **ADRENTRY 構造体** には、受信者のプロパティを記述する [SPropValue](spropvalue.md) 構造体の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d6e10-133">Each **ADRENTRY** structure contains an array of [SPropValue](spropvalue.md) structures to describe the recipient's properties.</span></span> <span data-ttu-id="d6e10-134">**IABLogon::P repareRecips** が返される場合、各受信者の **SPropValue** 構造体配列には _、lpPropTagArray_ のプロパティと受信者の他のプロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d6e10-134">When **IABLogon::PrepareRecips** returns, the **SPropValue** structure array for each recipient includes the properties from the  _lpPropTagArray_ followed by the other properties for the recipient.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d6e10-135">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="d6e10-135">Notes to implementers</span></span>

<span data-ttu-id="d6e10-136">**IABLogon::P repareRecips** を実装するには、プロパティを特定の順序で設定し、プロパティ値を取得し、短期エントリ識別子を長期エントリ識別子に変換します。</span><span class="sxs-lookup"><span data-stu-id="d6e10-136">Implementing **IABLogon::PrepareRecips** involves putting properties in a specific order, retrieving property values, and converting short-term entry identifiers to long-term entry identifiers.</span></span> <span data-ttu-id="d6e10-137">_lpPropTagArray_ パラメーターで要求されるプロパティは _、lpRecipList_ パラメーター内の各受信者の **ADRENTRY** 構造に関連付けられたプロパティ値配列の最初にある必要があります。</span><span class="sxs-lookup"><span data-stu-id="d6e10-137">The properties that are requested in the  _lpPropTagArray_ parameter must be at the start of the property value array associated with each recipient's **ADRENTRY** structure in the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="d6e10-138">これらのプロパティの値が存在しない場合は、そのエントリ識別子を使用して関連付けられたメッセージング ユーザーまたは配布リストを開き、不足しているプロパティ値を取得します。</span><span class="sxs-lookup"><span data-stu-id="d6e10-138">If values for these properties do not exist, open the associated messaging user or distribution list by using its entry identifier and retrieve the missing property values.</span></span> 
  
<span data-ttu-id="d6e10-139">_lpRecipList_ **で渡される各 SPropValue** 構造体を個別に割り当て、構造体を個別に解放できます。</span><span class="sxs-lookup"><span data-stu-id="d6e10-139">Allocate each **SPropValue** structure passed in  _lpRecipList_ separately so that the structures can be freed individually.</span></span> <span data-ttu-id="d6e10-140">文字列プロパティのデータを格納する **場合など、SPropValue** 構造体に追加の領域を割り当てる必要がある場合は [、MAPIAllocateBuffer](mapiallocatebuffer.md) 関数を使用して、完全なプロパティ値配列に追加の領域を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="d6e10-140">If you must allocate additional space for any **SPropValue** structure, for example, to store the data for a string property, use the [MAPIAllocateBuffer](mapiallocatebuffer.md) function to allocate additional space for the full property value array.</span></span> <span data-ttu-id="d6e10-141">[MAPIFreeBuffer](mapifreebuffer.md)関数を使用して元のプロパティ値配列を解放し[、MAPIAllocateMore](mapiallocatemore.md)関数を使用して、必要な追加のメモリを割り当てる。</span><span class="sxs-lookup"><span data-stu-id="d6e10-141">Use the [MAPIFreeBuffer](mapifreebuffer.md) function to free the original property value array, and then use the [MAPIAllocateMore](mapiallocatemore.md) function to allocate any additional memory that is required.</span></span> 
  
<span data-ttu-id="d6e10-142">**IABLogon::P repareRecips** を実装するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="d6e10-142">To implement **IABLogon::PrepareRecips**, use the following procedure:</span></span>
  
1. <span data-ttu-id="d6e10-143">_lpPropTagArray パラメーターのエントリを確認_ します。</span><span class="sxs-lookup"><span data-stu-id="d6e10-143">Check for entries in the  _lpPropTagArray_ parameter.</span></span> <span data-ttu-id="d6e10-144">プロパティ値の配列が空の場合、実行する作業はありません。</span><span class="sxs-lookup"><span data-stu-id="d6e10-144">If the property value array is empty, there is no work to do.</span></span> <span data-ttu-id="d6e10-145">成功の値を返します。</span><span class="sxs-lookup"><span data-stu-id="d6e10-145">Return a success value.</span></span> 
    
2. <span data-ttu-id="d6e10-146">_lpRecipList パラメーターで各受信者を処理_ します。</span><span class="sxs-lookup"><span data-stu-id="d6e10-146">Process each recipient in the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="d6e10-147">リストには、 **受信者ごとに 1 つの ADRENTRY** 構造メンバーがあります。</span><span class="sxs-lookup"><span data-stu-id="d6e10-147">There is one **ADRENTRY** structure member for each recipient in the list.</span></span> <span data-ttu-id="d6e10-148">次の種類の受信者を無視します。</span><span class="sxs-lookup"><span data-stu-id="d6e10-148">Ignore the following types of recipients:</span></span> 
    
   - <span data-ttu-id="d6e10-149">**ADRENTRY** 構造体の **rgPropVals** メンバーにエントリ識別子がない受信者 (つまり、未解決の受信者)。</span><span class="sxs-lookup"><span data-stu-id="d6e10-149">Recipients without an entry identifier in the **rgPropVals** member of their **ADRENTRY** structure (that is, unresolved recipients).</span></span> 
    
   - <span data-ttu-id="d6e10-150">プロバイダーに属していないエントリ識別子を持つ受信者。</span><span class="sxs-lookup"><span data-stu-id="d6e10-150">Recipients with an entry identifier that does not belong to your provider.</span></span> <span data-ttu-id="d6e10-151">これらの受信者は、別のアドレス帳プロバイダーに渡されます。</span><span class="sxs-lookup"><span data-stu-id="d6e10-151">These recipients will be passed to another address book provider.</span></span>
    
3. <span data-ttu-id="d6e10-152">受信者を開き、受信者に対して既に設定されているプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="d6e10-152">Open the recipient and retrieve the properties that are already set for the recipient.</span></span>
    
4. <span data-ttu-id="d6e10-153">_lpRecipList_ で指定されたプロパティ値の配列と **、GetProps** から返されるプロパティの配列を結合します。</span><span class="sxs-lookup"><span data-stu-id="d6e10-153">Merge the property value array specified in the  _lpRecipList_ with the array of properties returned from **GetProps**.</span></span> <span data-ttu-id="d6e10-154">両方のプロパティ配列で同じプロパティが発生する場合は  _、lpRecipList の値を使用します_。</span><span class="sxs-lookup"><span data-stu-id="d6e10-154">If the same property occurs in both property arrays, use the value from  _lpRecipList_.</span></span>
    
5. <span data-ttu-id="d6e10-155">_lpRecipList_ プロパティの値配列が必要なすべてのプロパティを保持するのに十分な大きい場合は、結合された配列に置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="d6e10-155">If the  _lpRecipList_ property value array is big enough to hold all of the necessary properties, just replace it with the merged array.</span></span> <span data-ttu-id="d6e10-156">_lpRecipList プロパティ_ 値配列のサイズが十分ではない場合は、新しく割り当てられた配列に置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="d6e10-156">If the  _lpRecipList_ property value array is not big enough, replace it with a newly allocated array.</span></span> <span data-ttu-id="d6e10-157">新しい配列の各 cValues メンバーに更新された値 **が設定されている必要** があります。</span><span class="sxs-lookup"><span data-stu-id="d6e10-157">Be sure the new array has an updated value in each of its **cValues** members.</span></span> 
    
6. <span data-ttu-id="d6e10-158">_lpPropTagArray_ パラメーター内の 1 つ以上のプロパティが認識されない場合は、受信者の **ADRENTRY** 構造体のプロパティの種類を PT_ERROR に設定し、プロパティ値を MAPI_E_NOT_FOUND または別の値に設定します。</span><span class="sxs-lookup"><span data-stu-id="d6e10-158">If you do not recognize one or more of the properties in the  _lpPropTagArray_ parameter, set the property type in the recipient's **ADRENTRY** structure to PT_ERROR and the property value either to MAPI_E_NOT_FOUND or to another value that gives a more specific reason for the unavailability of the property.</span></span> <span data-ttu-id="d6e10-159">プロパティの詳細についてはPT_ERRORプロパティの [種類を参照してください](property-types.md)。</span><span class="sxs-lookup"><span data-stu-id="d6e10-159">For information about PT_ERROR, see [Property Types](property-types.md).</span></span>
    
> [!NOTE]
> <span data-ttu-id="d6e10-160">**IABLogon::P repareRecips** に渡される **ADRLIST** 構造体を再割り当てしたり、エントリの数を変更したりしない。</span><span class="sxs-lookup"><span data-stu-id="d6e10-160">Never reallocate the **ADRLIST** structure that is passed into **IABLogon::PrepareRecips** or change its number of entries.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d6e10-161">関連項目</span><span class="sxs-lookup"><span data-stu-id="d6e10-161">See also</span></span>

- [<span data-ttu-id="d6e10-162">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="d6e10-162">ADRLIST</span></span>](adrlist.md)
- [<span data-ttu-id="d6e10-163">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="d6e10-163">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
- [<span data-ttu-id="d6e10-164">PidTagEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d6e10-164">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
- [<span data-ttu-id="d6e10-165">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d6e10-165">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="d6e10-166">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d6e10-166">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

