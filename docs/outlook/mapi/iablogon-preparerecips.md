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
# <a name="iablogonpreparerecips"></a><span data-ttu-id="dd720-103">IABLogon::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="dd720-103">IABLogon::PrepareRecips</span></span>

<span data-ttu-id="dd720-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd720-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd720-105">メッセージングシステムで後で使用するために、受信者リストを準備します。</span><span class="sxs-lookup"><span data-stu-id="dd720-105">Prepares a recipient list for later use by the messaging system.</span></span>
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="dd720-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="dd720-106">Parameters</span></span>

<span data-ttu-id="dd720-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dd720-107">_ulFlags_</span></span>
  
> <span data-ttu-id="dd720-108">順番返される文字列内のテキストの種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="dd720-108">[in] A bitmask of flags that controls the type of the text in the returned strings.</span></span> <span data-ttu-id="dd720-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="dd720-109">The following flag can be set:</span></span>
    
  - <span data-ttu-id="dd720-110">MAPI_CACHE_ONLY: 名前解決を実行するのにオフラインアドレス帳のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="dd720-110">MAPI_CACHE_ONLY: Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="dd720-111">たとえば、このフラグを使用して、クライアントアプリケーションが exchange キャッシュモードでグローバルアドレス一覧 (GAL) を開き、クライアントとサーバーの間のトラフィックを作成せずに、キャッシュからそのアドレス帳のエントリにアクセスできるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="dd720-111">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="dd720-112">このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="dd720-112">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="dd720-113">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="dd720-113">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="dd720-114">順番更新が必要なプロパティがある場合は、そのプロパティを示すプロパティタグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="dd720-114">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags that indicate the properties that require updating, if any.</span></span> <span data-ttu-id="dd720-115">_lpPropTagArray_パラメーターは NULL にすることができます。</span><span class="sxs-lookup"><span data-stu-id="dd720-115">The  _lpPropTagArray_ parameter can be NULL.</span></span> 
    
<span data-ttu-id="dd720-116">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="dd720-116">_lpRecipList_</span></span>
  
> <span data-ttu-id="dd720-117">順番受信者の一覧を保持する[adrlist](adrlist.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="dd720-117">[in] A pointer to an [ADRLIST](adrlist.md) structure that holds the recipient list.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dd720-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="dd720-118">Return value</span></span>

<span data-ttu-id="dd720-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="dd720-119">S_OK</span></span> 
  
> <span data-ttu-id="dd720-120">受信者リストが正常に準備されました。</span><span class="sxs-lookup"><span data-stu-id="dd720-120">The recipient list was successfully prepared.</span></span>
    
<span data-ttu-id="dd720-121">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="dd720-121">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="dd720-122">_lpRecipList_パラメーターの1人以上の受信者が存在しません。</span><span class="sxs-lookup"><span data-stu-id="dd720-122">One or more of the recipients in the  _lpRecipList_ parameter do not exist.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dd720-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="dd720-123">Return value</span></span>

<span data-ttu-id="dd720-124">クライアントは、MAPI [IAddrBook::P reparerecips](iaddrbook-preparerecips.md)メソッドを呼び出して、1人以上の受信者の一連のプロパティを変更または並べ替えます。</span><span class="sxs-lookup"><span data-stu-id="dd720-124">A client calls the MAPI [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) method to modify or rearrange a set of properties for one or more recipients.</span></span> <span data-ttu-id="dd720-125">受信者は、送信メッセージの受信者の一覧に含まれていない場合もあれば、一部ではない場合もあります。</span><span class="sxs-lookup"><span data-stu-id="dd720-125">The recipients may or may not be part of the recipient list of an outgoing message.</span></span> <span data-ttu-id="dd720-126">MAPI は、この呼び出しをアドレス帳プロバイダーの**IABLogon::P reparerecips**メソッドに転送します。</span><span class="sxs-lookup"><span data-stu-id="dd720-126">MAPI transfers this call to an address book provider's **IABLogon::PrepareRecips** method.</span></span> 
  
<span data-ttu-id="dd720-127">**IABLogon::P reparerecips**は、次の4つの主要なタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="dd720-127">**IABLogon::PrepareRecips** performs four main tasks:</span></span> 
  
- <span data-ttu-id="dd720-128">_lpRecipList_パラメーターによって指定されるアドレス一覧内のすべての受信者が長期間のエントリ識別子を持つようにします。</span><span class="sxs-lookup"><span data-stu-id="dd720-128">Ensures that all recipients in the address list pointed to by the  _lpRecipList_ parameter have a long-term entry identifier.</span></span> 
    
- <span data-ttu-id="dd720-129">すべての受信者が、 _lpPropTagArray_パラメーターで指定されたプロパティ値配列で指定されたプロパティを持つことを確認します。</span><span class="sxs-lookup"><span data-stu-id="dd720-129">Ensures that all recipients have the properties specified in the property value array pointed to by the  _lpPropTagArray_ parameter.</span></span> 
    
- <span data-ttu-id="dd720-130">プロパティ値配列のプロパティが、呼び出し前に存在していた他のプロパティよりも前に表示されるようにします。</span><span class="sxs-lookup"><span data-stu-id="dd720-130">Ensures that the properties from the property value array appear before any other properties that existed before the call.</span></span>
    
- <span data-ttu-id="dd720-131">**adrentry**構造内の各受信者の[adrentry](adrentry.md)構造のプロパティの順序が、プロパティの値の配列と同じになるようにします。</span><span class="sxs-lookup"><span data-stu-id="dd720-131">Ensures that the order of the properties in each recipient's [ADRENTRY](adrentry.md) structure in the **ADRLIST** structure is the same as in the property value array.</span></span> 
    
<span data-ttu-id="dd720-132">_lpRecipList_パラメーターの**adrentry**構造には、各受信者の**adrentry**構造が1つ含まれています。</span><span class="sxs-lookup"><span data-stu-id="dd720-132">The **ADRENTRY** structure in the  _lpRecipList_ parameter contains one **ADRENTRY** structure for each recipient.</span></span> <span data-ttu-id="dd720-133">各**adrentry**構造には、受信者のプロパティを説明するための[spropvalue](spropvalue.md)構造の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="dd720-133">Each **ADRENTRY** structure contains an array of [SPropValue](spropvalue.md) structures to describe the recipient's properties.</span></span> <span data-ttu-id="dd720-134">**IABLogon::P reparerecips**が戻ると、各受信者の**spropvalue**構造体の配列には、 _lpPropTagArray_のプロパティと、受信者の他のプロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="dd720-134">When **IABLogon::PrepareRecips** returns, the **SPropValue** structure array for each recipient includes the properties from the  _lpPropTagArray_ followed by the other properties for the recipient.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="dd720-135">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="dd720-135">Notes to implementers</span></span>

<span data-ttu-id="dd720-136">IABLogon の実装 **::P reparerecips**は、特定の順序にプロパティを配置し、プロパティの値を取得し、短時間のエントリ識別子を長期のエントリ識別子に変換します。</span><span class="sxs-lookup"><span data-stu-id="dd720-136">Implementing **IABLogon::PrepareRecips** involves putting properties in a specific order, retrieving property values, and converting short-term entry identifiers to long-term entry identifiers.</span></span> <span data-ttu-id="dd720-137">_lpPropTagArray_パラメーターで要求されるプロパティは、 _lpRecipList_パラメーターの各受信者の**adrentry**構造に関連付けられているプロパティ値の配列の先頭にある必要があります。</span><span class="sxs-lookup"><span data-stu-id="dd720-137">The properties that are requested in the  _lpPropTagArray_ parameter must be at the start of the property value array associated with each recipient's **ADRENTRY** structure in the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="dd720-138">これらのプロパティの値が存在しない場合は、そのエントリ id を使用して、関連付けられているメッセージングユーザーまたは配布リストを開き、不足しているプロパティの値を取得します。</span><span class="sxs-lookup"><span data-stu-id="dd720-138">If values for these properties do not exist, open the associated messaging user or distribution list by using its entry identifier and retrieve the missing property values.</span></span> 
  
<span data-ttu-id="dd720-139">_lpRecipList_で渡された各**spropvalue**構造を個別に割り当てて、構造体を個別に解放できるようにします。</span><span class="sxs-lookup"><span data-stu-id="dd720-139">Allocate each **SPropValue** structure passed in  _lpRecipList_ separately so that the structures can be freed individually.</span></span> <span data-ttu-id="dd720-140">文字列プロパティのデータを格納するなど、 **spropvalue**構造に追加の領域を割り当てる必要がある場合は、 [MAPIAllocateBuffer](mapiallocatebuffer.md)関数を使用して、完全なプロパティ値の配列に追加の領域を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="dd720-140">If you must allocate additional space for any **SPropValue** structure, for example, to store the data for a string property, use the [MAPIAllocateBuffer](mapiallocatebuffer.md) function to allocate additional space for the full property value array.</span></span> <span data-ttu-id="dd720-141">[MAPIFreeBuffer](mapifreebuffer.md)関数を使用して、元のプロパティの値の配列を解放した後、 [MAPIAllocateMore](mapiallocatemore.md)関数を使用して必要な追加のメモリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="dd720-141">Use the [MAPIFreeBuffer](mapifreebuffer.md) function to free the original property value array, and then use the [MAPIAllocateMore](mapiallocatemore.md) function to allocate any additional memory that is required.</span></span> 
  
<span data-ttu-id="dd720-142">**IABLogon::P reparerecips**を実装するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="dd720-142">To implement **IABLogon::PrepareRecips**, use the following procedure:</span></span>
  
1. <span data-ttu-id="dd720-143">_lpPropTagArray_パラメーターのエントリを確認します。</span><span class="sxs-lookup"><span data-stu-id="dd720-143">Check for entries in the  _lpPropTagArray_ parameter.</span></span> <span data-ttu-id="dd720-144">プロパティの値の配列が空の場合、実行する作業はありません。</span><span class="sxs-lookup"><span data-stu-id="dd720-144">If the property value array is empty, there is no work to do.</span></span> <span data-ttu-id="dd720-145">成功の値を返します。</span><span class="sxs-lookup"><span data-stu-id="dd720-145">Return a success value.</span></span> 
    
2. <span data-ttu-id="dd720-146">各受信者を_lpRecipList_パラメーターで処理します。</span><span class="sxs-lookup"><span data-stu-id="dd720-146">Process each recipient in the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="dd720-147">リスト内の受信者ごとに1つの**adrentry**構造メンバーが存在します。</span><span class="sxs-lookup"><span data-stu-id="dd720-147">There is one **ADRENTRY** structure member for each recipient in the list.</span></span> <span data-ttu-id="dd720-148">次の種類の受信者を無視します。</span><span class="sxs-lookup"><span data-stu-id="dd720-148">Ignore the following types of recipients:</span></span> 
    
   - <span data-ttu-id="dd720-149">**adrentry**構造の**rgPropVals**メンバにエントリ識別子を持たない受信者 (つまり、未解決の受信者)。</span><span class="sxs-lookup"><span data-stu-id="dd720-149">Recipients without an entry identifier in the **rgPropVals** member of their **ADRENTRY** structure (that is, unresolved recipients).</span></span> 
    
   - <span data-ttu-id="dd720-150">プロバイダーに属さないエントリ識別子を持つ受信者。</span><span class="sxs-lookup"><span data-stu-id="dd720-150">Recipients with an entry identifier that does not belong to your provider.</span></span> <span data-ttu-id="dd720-151">これらの受信者は、別のアドレス帳プロバイダーに渡されます。</span><span class="sxs-lookup"><span data-stu-id="dd720-151">These recipients will be passed to another address book provider.</span></span>
    
3. <span data-ttu-id="dd720-152">受信者を開き、受信者に対して既に設定されているプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="dd720-152">Open the recipient and retrieve the properties that are already set for the recipient.</span></span>
    
4. <span data-ttu-id="dd720-153">_lpRecipList_で指定されているプロパティ値の配列を、 **GetProps**から返されるプロパティの配列にマージします。</span><span class="sxs-lookup"><span data-stu-id="dd720-153">Merge the property value array specified in the  _lpRecipList_ with the array of properties returned from **GetProps**.</span></span> <span data-ttu-id="dd720-154">両方のプロパティ配列で同じプロパティが発生する場合は、 _lpRecipList_の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="dd720-154">If the same property occurs in both property arrays, use the value from  _lpRecipList_.</span></span>
    
5. <span data-ttu-id="dd720-155">_lpRecipList_プロパティの値の配列が大きすぎて、必要なすべてのプロパティを保持できる場合は、結合された配列に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="dd720-155">If the  _lpRecipList_ property value array is big enough to hold all of the necessary properties, just replace it with the merged array.</span></span> <span data-ttu-id="dd720-156">_lpRecipList_プロパティの値の配列が十分でない場合は、新たに割り当てられた配列に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="dd720-156">If the  _lpRecipList_ property value array is not big enough, replace it with a newly allocated array.</span></span> <span data-ttu-id="dd720-157">新しい配列の各**cvalues**メンバーに、更新された値があることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="dd720-157">Be sure the new array has an updated value in each of its **cValues** members.</span></span> 
    
6. <span data-ttu-id="dd720-158">_lpPropTagArray_パラメーターで1つ以上のプロパティが認識されない場合は、受信者の**adrentry**構造のプロパティの種類を PT_ERROR に、プロパティ値を MAPI_E_NOT_FOUND またはその他の値に設定します。プロパティが利用できない特定の理由。</span><span class="sxs-lookup"><span data-stu-id="dd720-158">If you do not recognize one or more of the properties in the  _lpPropTagArray_ parameter, set the property type in the recipient's **ADRENTRY** structure to PT_ERROR and the property value either to MAPI_E_NOT_FOUND or to another value that gives a more specific reason for the unavailability of the property.</span></span> <span data-ttu-id="dd720-159">PT_ERROR の詳細については、「[プロパティの種類](property-types.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dd720-159">For information about PT_ERROR, see [Property Types](property-types.md).</span></span>
    
> [!NOTE]
> <span data-ttu-id="dd720-160">IABLogon に渡される**adrlist**構造体を再割り当てせずに、 **reparerecips**またはエントリ数を変更することはありません。</span><span class="sxs-lookup"><span data-stu-id="dd720-160">Never reallocate the **ADRLIST** structure that is passed into **IABLogon::PrepareRecips** or change its number of entries.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dd720-161">関連項目</span><span class="sxs-lookup"><span data-stu-id="dd720-161">See also</span></span>

- [<span data-ttu-id="dd720-162">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="dd720-162">ADRLIST</span></span>](adrlist.md)
- [<span data-ttu-id="dd720-163">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="dd720-163">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
- [<span data-ttu-id="dd720-164">PidTagEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="dd720-164">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
- [<span data-ttu-id="dd720-165">SPropValue</span><span class="sxs-lookup"><span data-stu-id="dd720-165">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="dd720-166">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dd720-166">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

