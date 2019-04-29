---
title: ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ENTRYID
api_type:
- COM
ms.assetid: 8ebb21ca-5ad1-4dcc-97b6-2390664b5d8d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c77acb5226361ce31a7f6b1694de7fe23f8dd71b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415272"
---
# <a name="entryid"></a><span data-ttu-id="c7ad4-103">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="c7ad4-103">ENTRYID</span></span>

  
  
<span data-ttu-id="c7ad4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7ad4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7ad4-105">MAPI オブジェクトのエントリ識別子を含みます。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-105">Contains an entry identifier for a MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c7ad4-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="c7ad4-106">Header file:</span></span>  <br/> |<span data-ttu-id="c7ad4-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c7ad4-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c7ad4-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="c7ad4-108">Related macros:</span></span>  <br/> |<span data-ttu-id="c7ad4-109">[cbnewentryid](cbnewentryid.md)、 [sizedentryid](sizedentryid.md)</span><span class="sxs-lookup"><span data-stu-id="c7ad4-109">[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  BYTE abFlags[4];
  BYTE ab[MAPI_DIM];
} ENTRYID, FAR *LPENTRYID;

```

## <a name="members"></a><span data-ttu-id="c7ad4-110">メンバー</span><span class="sxs-lookup"><span data-stu-id="c7ad4-110">Members</span></span>

 <span data-ttu-id="c7ad4-111">**abflags**</span><span class="sxs-lookup"><span data-stu-id="c7ad4-111">**abFlags**</span></span>
  
> <span data-ttu-id="c7ad4-112">オブジェクトを説明する情報を提供するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-112">Bitmask of flags that provide information that describes the object.</span></span> <span data-ttu-id="c7ad4-113">フラグの先頭バイトだけ ( **abflags [0]**) は、プロバイダーによって設定されます。他の3つは予約されています。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-113">Only the first byte of the flags, **abFlags[0]**, may be set by the provider; the other three are reserved.</span></span> <span data-ttu-id="c7ad4-114">これらのフラグは、永続的なエントリ識別子に対して設定しないでください。これらは、短期的なエントリ識別子に対してのみ設定されます。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-114">These flags must not be set for permanent entry identifiers; they are only set for short-term entry identifiers.</span></span> <span data-ttu-id="c7ad4-115">クライアントにとっては、この構造体は読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-115">To clients, this structure is read-only.</span></span> <span data-ttu-id="c7ad4-116">次のフラグは、 **abflags [0]** で設定できます。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-116">The following flags can be set in **abFlags[0]**:</span></span>
    
<span data-ttu-id="c7ad4-117">MAPI_NOTRECIP</span><span class="sxs-lookup"><span data-stu-id="c7ad4-117">MAPI_NOTRECIP</span></span> 
  
> <span data-ttu-id="c7ad4-118">このエントリ id は、メッセージの受信者として使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-118">The entry identifier cannot be used as a recipient on a message.</span></span>
    
<span data-ttu-id="c7ad4-119">MAPI_NOTRESERVED</span><span class="sxs-lookup"><span data-stu-id="c7ad4-119">MAPI_NOTRESERVED</span></span> 
  
> <span data-ttu-id="c7ad4-120">他のユーザーは、エントリ識別子にアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-120">Other users cannot access the entry identifier.</span></span>
    
<span data-ttu-id="c7ad4-121">MAPI_NOW</span><span class="sxs-lookup"><span data-stu-id="c7ad4-121">MAPI_NOW</span></span> 
  
> <span data-ttu-id="c7ad4-122">その他の場合は、エントリ識別子を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-122">The entry identifier cannot be used at other times.</span></span>
    
<span data-ttu-id="c7ad4-123">MAPI_SHORTTERM</span><span class="sxs-lookup"><span data-stu-id="c7ad4-123">MAPI_SHORTTERM</span></span> 
  
> <span data-ttu-id="c7ad4-124">エントリ識別子は短い用語です。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-124">The entry identifier is short-term.</span></span> <span data-ttu-id="c7ad4-125">このバイトの他のすべての値は、エントリ識別子の他の使用法が有効になっていない限り、設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-125">All other values in this byte must be set unless other uses of the entry identifier are enabled.</span></span>
    
<span data-ttu-id="c7ad4-126">MAPI_THISSESSION</span><span class="sxs-lookup"><span data-stu-id="c7ad4-126">MAPI_THISSESSION</span></span> 
  
> <span data-ttu-id="c7ad4-127">他のセッションでは、エントリ識別子を使用できません。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-127">The entry identifier cannot be used on other sessions.</span></span>
    
 <span data-ttu-id="c7ad4-128">**l**</span><span class="sxs-lookup"><span data-stu-id="c7ad4-128">**ab**</span></span>
  
> <span data-ttu-id="c7ad4-129">サービスプロバイダーで使用されるバイナリデータの配列を示します。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-129">Indicates an array of binary data that is used by service providers.</span></span> <span data-ttu-id="c7ad4-130">クライアントアプリケーションは、この配列を使用できません。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-130">The client application cannot use this array.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c7ad4-131">注釈</span><span class="sxs-lookup"><span data-stu-id="c7ad4-131">Remarks</span></span>

<span data-ttu-id="c7ad4-132">**ENTRYID**構造体は、オブジェクトに一意の識別子を作成するために、メッセージストアとアドレス帳プロバイダーによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-132">The **ENTRYID** structure is used by message store and address book providers to construct unique identifiers for their objects.</span></span> <span data-ttu-id="c7ad4-133">エントリ識別子は、次の種類のオブジェクトを識別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-133">Entry identifiers are used to identify the following types of objects:</span></span> 
  
- <span data-ttu-id="c7ad4-134">メッセージストア</span><span class="sxs-lookup"><span data-stu-id="c7ad4-134">Message stores</span></span>
    
- <span data-ttu-id="c7ad4-135">Folders</span><span class="sxs-lookup"><span data-stu-id="c7ad4-135">Folders</span></span>
    
- <span data-ttu-id="c7ad4-136">メッセージ</span><span class="sxs-lookup"><span data-stu-id="c7ad4-136">Messages</span></span>
    
- <span data-ttu-id="c7ad4-137">アドレス帳のコンテナー</span><span class="sxs-lookup"><span data-stu-id="c7ad4-137">Address book containers</span></span>
    
- <span data-ttu-id="c7ad4-138">配布リスト</span><span class="sxs-lookup"><span data-stu-id="c7ad4-138">Distribution lists</span></span>
    
- <span data-ttu-id="c7ad4-139">メッセージングユーザー</span><span class="sxs-lookup"><span data-stu-id="c7ad4-139">Messaging users</span></span>
    
- <span data-ttu-id="c7ad4-140">状態オブジェクト</span><span class="sxs-lookup"><span data-stu-id="c7ad4-140">Status objects</span></span>
    
- <span data-ttu-id="c7ad4-141">プロファイルセクション</span><span class="sxs-lookup"><span data-stu-id="c7ad4-141">Profile sections</span></span>
    
<span data-ttu-id="c7ad4-142">各プロバイダーは、そのプロバイダーにとって意味のある**ENTRYID**構造の形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-142">Each provider uses a format for the **ENTRYID** structure that makes sense for that provider.</span></span> 
  
<span data-ttu-id="c7ad4-143">1 つのオブジェクトは、2 つの異なるバイナリ値で表すことができるため、エントリ ID を直接比較することはできません。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-143">Entry identifiers cannot be compared directly because one object can be represented by two different binary values.</span></span> <span data-ttu-id="c7ad4-144">2つのエントリ識別子が同じオブジェクトを表しているかどうかを判断するには、 [imapisession:: compareentryids](imapisession-compareentryids.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-144">To determine whether two entry identifiers represent the same object, call the [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) method.</span></span> 
  
<span data-ttu-id="c7ad4-145">クライアントがオブジェクトの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出してそのエントリ識別子を取得すると、オブジェクトは、エントリ識別子の最も永続的な形式を返します。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-145">When a client calls an object's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its entry identifier, the object returns the most permanent form of the entry identifier.</span></span> <span data-ttu-id="c7ad4-146">クライアントは、 **abflags**メンバの最初のバイトにフラグが設定されていないことを確認することによって、エントリ識別子が長期間であることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-146">A client can verify that an entry identifier is long-term by checking that none of the flags are set in the first byte of the **abFlags** member.</span></span> 
  
<span data-ttu-id="c7ad4-147">クライアントがテーブル内の列を使用してエントリ識別子にアクセスする場合、このエントリ識別子は長期間ではなく短期である可能性が高くなります。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-147">When a client accesses an entry identifier through a column in a table, most likely this entry identifier is short-term instead of long-term.</span></span> <span data-ttu-id="c7ad4-148">短期的なエントリ識別子を使用すると、現在の MAPI セッションでのみ、対応するオブジェクトを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-148">Short-term entry identifiers can be used to open their corresponding objects only in the current MAPI session.</span></span> <span data-ttu-id="c7ad4-149">クライアントは、すべてのフラグが**abflags**メンバーの最初のバイトに設定されていることを確認することによって、エントリ識別子が短縮されていることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-149">A client can verify that an entry identifier is short-term by checking that all of the flags are set in the first byte of the **abFlags** member.</span></span> 
  
<span data-ttu-id="c7ad4-150">一部のエントリ識別子は短期的ですが、長期間使用します。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-150">Some entry identifiers are short-term, but have long-term use.</span></span> <span data-ttu-id="c7ad4-151">このようなエントリ識別子には、 **abflags**メンバーの最初のバイトに1つ以上の適切なフラグが設定されています。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-151">Such an entry identifier will have one or more of the appropriate flags set in the first byte of its **abFlags** member.</span></span> 
  
<span data-ttu-id="c7ad4-152">**ENTRYID**構造体は、 [FLATENTRY](flatentry.md)構造体に似ています。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-152">An **ENTRYID** structure resembles a [FLATENTRY](flatentry.md) structure.</span></span> <span data-ttu-id="c7ad4-153">ただし、次のような違いがあります。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-153">However, there are some differences:</span></span> 
  
- <span data-ttu-id="c7ad4-154">**ENTRYID**構造体には、エントリ識別子のサイズは格納されません。**FLATENTRY**構造体があります。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-154">An **ENTRYID** structure does not store the size of the entry identifier; a **FLATENTRY** structure does.</span></span> 
    
- <span data-ttu-id="c7ad4-155">**ENTRYID**構造は、フラグデータとその他のエントリ識別子を個別に格納します。**FLATENTRY**構造体は、フラグデータをエントリ id の残りの部分と共に格納します。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-155">An **ENTRYID** structure stores the flag data and the rest of the entry identifier separately; a **FLATENTRY** structure stores the flag data with the rest of the entry identifier.</span></span> 
    
- <span data-ttu-id="c7ad4-156">**ENTRYID**構造体は、パラメーターとして[imapiprop](imapipropiunknown.md)インターフェイスのメソッドと、次の openentry \*\*\*\* メソッドに渡されます。 [IABLogon:: openentry](iablogon-openentry.md)、 [IAddrBook:: openentry](iaddrbook-openentry.md)、 [IMAPIContainer:: openentry](imapicontainer-openentry.md)、 [imapisession:: openentry](imapisession-openentry.md)、 [imapisession:: openentry](imapisupport-openentry.md)、 [IMsgStore:: openentry](imsgstore-openentry.md)、 [IMSLogon:: openentry](imslogon-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="c7ad4-156">An **ENTRYID** structure is passed as a parameter to the methods of the [IMAPIProp](imapipropiunknown.md) interface and to the following **OpenEntry** methods: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span></span>
    
- <span data-ttu-id="c7ad4-157">**ENTRYID**構造体は、ディスクにエントリ識別子を格納するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-157">An **ENTRYID** structure is used to store an entry identifier on disk.</span></span> <span data-ttu-id="c7ad4-158">**FLATENTRY**構造体は、エントリ id をファイルに格納したり、バイトのストリームに渡したりするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-158">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes.</span></span> 
    
<span data-ttu-id="c7ad4-159">クライアントは常に、自然に配置されたエントリ識別子を渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-159">Clients should always pass in naturally aligned entry identifiers.</span></span> <span data-ttu-id="c7ad4-160">プロバイダーは、任意に調整されたエントリ識別子を処理する必要がありますが、クライアントはこの動作を想定してはいけません。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-160">Although providers should handle arbitrarily aligned entry identifiers, clients should not expect this behavior.</span></span> <span data-ttu-id="c7ad4-161">適切なアライメントエントリ識別子をメソッドに渡さないと、RISC プロセッサでアライメントエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-161">Failure to pass a good aligned entry identifier to a method can cause an alignment fault on RISC processors.</span></span> 
  
<span data-ttu-id="c7ad4-162">自然なアラインメント要素 (通常は8バイト) は、CPU によってサポートされる最大のデータ型であり、通常はシステムメモリアロケーターによって使用される同じ配置要因です。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-162">The natural alignment factor, typically 8 bytes, is the largest data type supported by the CPU, and usually the same alignment factor used by the system memory allocator.</span></span> <span data-ttu-id="c7ad4-163">自然に配置されたメモリアドレスを使用すると、配置エラーが発生することなく、そのアドレスでサポートされているすべてのデータ型に CPU がアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-163">A naturally aligned memory address allows the CPU to access any data type it supports at that address without generating an alignment fault.</span></span> <span data-ttu-id="c7ad4-164">RISC cpu の場合、サイズ n バイトのデータ型は通常、n バイトの倍数になるように調整する必要があります。アドレスは n の偶数倍になります。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-164">For RISC CPUs, a data type of size N bytes must usually be aligned on an even multiple of N bytes, with the address being an even multiple of N.</span></span>
  
<span data-ttu-id="c7ad4-165">詳細については、「[エントリ識別子](mapi-entry-identifiers.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c7ad4-165">For more information, see [Entry Identifiers](mapi-entry-identifiers.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c7ad4-166">関連項目</span><span class="sxs-lookup"><span data-stu-id="c7ad4-166">See also</span></span>



[<span data-ttu-id="c7ad4-167">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="c7ad4-167">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="c7ad4-168">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="c7ad4-168">IMAPISupport::CompareEntryIDs</span></span>](imapisupport-compareentryids.md)
  
[<span data-ttu-id="c7ad4-169">PidTagRecordKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c7ad4-169">PidTagRecordKey Canonical Property</span></span>](pidtagrecordkey-canonical-property.md)


[<span data-ttu-id="c7ad4-170">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="c7ad4-170">MAPI Structures</span></span>](mapi-structures.md)

