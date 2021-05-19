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
# <a name="entryid"></a><span data-ttu-id="9152a-103">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="9152a-103">ENTRYID</span></span>

  
  
<span data-ttu-id="9152a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9152a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9152a-105">MAPI オブジェクトのエントリ識別子が含まれる。</span><span class="sxs-lookup"><span data-stu-id="9152a-105">Contains an entry identifier for a MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9152a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="9152a-106">Header file:</span></span>  <br/> |<span data-ttu-id="9152a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9152a-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9152a-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="9152a-108">Related macros:</span></span>  <br/> |<span data-ttu-id="9152a-109">[CbNewENTRYID](cbnewentryid.md) [、SizedENTRYID](sizedentryid.md)</span><span class="sxs-lookup"><span data-stu-id="9152a-109">[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  BYTE abFlags[4];
  BYTE ab[MAPI_DIM];
} ENTRYID, FAR *LPENTRYID;

```

## <a name="members"></a><span data-ttu-id="9152a-110">Members</span><span class="sxs-lookup"><span data-stu-id="9152a-110">Members</span></span>

 <span data-ttu-id="9152a-111">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="9152a-111">**abFlags**</span></span>
  
> <span data-ttu-id="9152a-112">オブジェクトを説明する情報を提供するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="9152a-112">Bitmask of flags that provide information that describes the object.</span></span> <span data-ttu-id="9152a-113">フラグの最初のバイト **abFlags[0]** だけがプロバイダーによって設定できます。他の 3 つは予約済みです。</span><span class="sxs-lookup"><span data-stu-id="9152a-113">Only the first byte of the flags, **abFlags[0]**, may be set by the provider; the other three are reserved.</span></span> <span data-ttu-id="9152a-114">これらのフラグは、永続的なエントリ識別子に対して設定する必要があります。これらは、短期エントリ識別子にのみ設定されます。</span><span class="sxs-lookup"><span data-stu-id="9152a-114">These flags must not be set for permanent entry identifiers; they are only set for short-term entry identifiers.</span></span> <span data-ttu-id="9152a-115">クライアントの場合、この構造は読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="9152a-115">To clients, this structure is read-only.</span></span> <span data-ttu-id="9152a-116">**abFlags[0] では、次のフラグを設定できます**。</span><span class="sxs-lookup"><span data-stu-id="9152a-116">The following flags can be set in **abFlags[0]**:</span></span>
    
<span data-ttu-id="9152a-117">MAPI_NOTRECIP</span><span class="sxs-lookup"><span data-stu-id="9152a-117">MAPI_NOTRECIP</span></span> 
  
> <span data-ttu-id="9152a-118">エントリ識別子をメッセージの受信者として使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="9152a-118">The entry identifier cannot be used as a recipient on a message.</span></span>
    
<span data-ttu-id="9152a-119">MAPI_NOTRESERVED</span><span class="sxs-lookup"><span data-stu-id="9152a-119">MAPI_NOTRESERVED</span></span> 
  
> <span data-ttu-id="9152a-120">他のユーザーは、エントリ識別子にアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="9152a-120">Other users cannot access the entry identifier.</span></span>
    
<span data-ttu-id="9152a-121">MAPI_NOW</span><span class="sxs-lookup"><span data-stu-id="9152a-121">MAPI_NOW</span></span> 
  
> <span data-ttu-id="9152a-122">エントリ識別子は、他の時点では使用できません。</span><span class="sxs-lookup"><span data-stu-id="9152a-122">The entry identifier cannot be used at other times.</span></span>
    
<span data-ttu-id="9152a-123">MAPI_SHORTTERM</span><span class="sxs-lookup"><span data-stu-id="9152a-123">MAPI_SHORTTERM</span></span> 
  
> <span data-ttu-id="9152a-124">エントリ識別子は短期的です。</span><span class="sxs-lookup"><span data-stu-id="9152a-124">The entry identifier is short-term.</span></span> <span data-ttu-id="9152a-125">エントリ識別子の他の使用が有効になっていない限り、このバイト内の他のすべての値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9152a-125">All other values in this byte must be set unless other uses of the entry identifier are enabled.</span></span>
    
<span data-ttu-id="9152a-126">MAPI_THISSESSION</span><span class="sxs-lookup"><span data-stu-id="9152a-126">MAPI_THISSESSION</span></span> 
  
> <span data-ttu-id="9152a-127">エントリ識別子は、他のセッションでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="9152a-127">The entry identifier cannot be used on other sessions.</span></span>
    
 <span data-ttu-id="9152a-128">**ab**</span><span class="sxs-lookup"><span data-stu-id="9152a-128">**ab**</span></span>
  
> <span data-ttu-id="9152a-129">サービス プロバイダーによって使用されるバイナリ データの配列を示します。</span><span class="sxs-lookup"><span data-stu-id="9152a-129">Indicates an array of binary data that is used by service providers.</span></span> <span data-ttu-id="9152a-130">クライアント アプリケーションでは、この配列を使用できません。</span><span class="sxs-lookup"><span data-stu-id="9152a-130">The client application cannot use this array.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9152a-131">注釈</span><span class="sxs-lookup"><span data-stu-id="9152a-131">Remarks</span></span>

<span data-ttu-id="9152a-132">**ENTRYID 構造体は**、メッセージ ストアとアドレス帳プロバイダーがオブジェクトの一意の識別子を作成するために使用します。</span><span class="sxs-lookup"><span data-stu-id="9152a-132">The **ENTRYID** structure is used by message store and address book providers to construct unique identifiers for their objects.</span></span> <span data-ttu-id="9152a-133">エントリ識別子は、次の種類のオブジェクトを識別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="9152a-133">Entry identifiers are used to identify the following types of objects:</span></span> 
  
- <span data-ttu-id="9152a-134">メッセージ ストア</span><span class="sxs-lookup"><span data-stu-id="9152a-134">Message stores</span></span>
    
- <span data-ttu-id="9152a-135">Folders</span><span class="sxs-lookup"><span data-stu-id="9152a-135">Folders</span></span>
    
- <span data-ttu-id="9152a-136">メッセージ</span><span class="sxs-lookup"><span data-stu-id="9152a-136">Messages</span></span>
    
- <span data-ttu-id="9152a-137">アドレス帳コンテナー</span><span class="sxs-lookup"><span data-stu-id="9152a-137">Address book containers</span></span>
    
- <span data-ttu-id="9152a-138">配布リスト</span><span class="sxs-lookup"><span data-stu-id="9152a-138">Distribution lists</span></span>
    
- <span data-ttu-id="9152a-139">メッセージング ユーザー</span><span class="sxs-lookup"><span data-stu-id="9152a-139">Messaging users</span></span>
    
- <span data-ttu-id="9152a-140">状態オブジェクト</span><span class="sxs-lookup"><span data-stu-id="9152a-140">Status objects</span></span>
    
- <span data-ttu-id="9152a-141">プロファイル セクション</span><span class="sxs-lookup"><span data-stu-id="9152a-141">Profile sections</span></span>
    
<span data-ttu-id="9152a-142">各プロバイダーは、そのプロバイダーに合った **ENTRYID** 構造の形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="9152a-142">Each provider uses a format for the **ENTRYID** structure that makes sense for that provider.</span></span> 
  
<span data-ttu-id="9152a-143">1 つのオブジェクトは、2 つの異なるバイナリ値で表すことができるため、エントリ ID を直接比較することはできません。</span><span class="sxs-lookup"><span data-stu-id="9152a-143">Entry identifiers cannot be compared directly because one object can be represented by two different binary values.</span></span> <span data-ttu-id="9152a-144">2 つのエントリ識別子が同じオブジェクトを表すかどうかを確認するには [、IMAPISession::CompareEntryIDs メソッドを呼び出](imapisession-compareentryids.md) します。</span><span class="sxs-lookup"><span data-stu-id="9152a-144">To determine whether two entry identifiers represent the same object, call the [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) method.</span></span> 
  
<span data-ttu-id="9152a-145">クライアントがオブジェクトの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出してエントリ識別子を取得すると、オブジェクトはエントリ識別子の最も永続的な形式を返します。</span><span class="sxs-lookup"><span data-stu-id="9152a-145">When a client calls an object's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its entry identifier, the object returns the most permanent form of the entry identifier.</span></span> <span data-ttu-id="9152a-146">クライアントは **、abFlags** メンバーの最初のバイトにどのフラグも設定されなかから、エントリ識別子が長期に設定されているのを確認できます。</span><span class="sxs-lookup"><span data-stu-id="9152a-146">A client can verify that an entry identifier is long-term by checking that none of the flags are set in the first byte of the **abFlags** member.</span></span> 
  
<span data-ttu-id="9152a-147">クライアントがテーブル内の列を通じてエントリ識別子にアクセスする場合、ほとんどの場合、このエントリ識別子は長期ではなく短期的です。</span><span class="sxs-lookup"><span data-stu-id="9152a-147">When a client accesses an entry identifier through a column in a table, most likely this entry identifier is short-term instead of long-term.</span></span> <span data-ttu-id="9152a-148">短期エントリ識別子を使用すると、現在の MAPI セッションでのみ対応するオブジェクトを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="9152a-148">Short-term entry identifiers can be used to open their corresponding objects only in the current MAPI session.</span></span> <span data-ttu-id="9152a-149">クライアントは **、abFlags** メンバーの最初のバイトにすべてのフラグが設定されているのを確認することで、エントリ識別子が短期的な状態を確認できます。</span><span class="sxs-lookup"><span data-stu-id="9152a-149">A client can verify that an entry identifier is short-term by checking that all of the flags are set in the first byte of the **abFlags** member.</span></span> 
  
<span data-ttu-id="9152a-150">一部のエントリ識別子は短期的ですが、長期的な使用があります。</span><span class="sxs-lookup"><span data-stu-id="9152a-150">Some entry identifiers are short-term, but have long-term use.</span></span> <span data-ttu-id="9152a-151">このようなエントリ識別子には **、abFlags** メンバーの最初のバイトに 1 つ以上の適切なフラグが設定されます。</span><span class="sxs-lookup"><span data-stu-id="9152a-151">Such an entry identifier will have one or more of the appropriate flags set in the first byte of its **abFlags** member.</span></span> 
  
<span data-ttu-id="9152a-152">**ENTRYID 構造体は** [FLATENTRY 構造に似](flatentry.md)ている。</span><span class="sxs-lookup"><span data-stu-id="9152a-152">An **ENTRYID** structure resembles a [FLATENTRY](flatentry.md) structure.</span></span> <span data-ttu-id="9152a-153">ただし、いくつかの違いがあります。</span><span class="sxs-lookup"><span data-stu-id="9152a-153">However, there are some differences:</span></span> 
  
- <span data-ttu-id="9152a-154">**ENTRYID 構造体** は、エントリ識別子のサイズを格納しない。**FLATENTRY 構造体** は、次の動作を行います。</span><span class="sxs-lookup"><span data-stu-id="9152a-154">An **ENTRYID** structure does not store the size of the entry identifier; a **FLATENTRY** structure does.</span></span> 
    
- <span data-ttu-id="9152a-155">**ENTRYID 構造体は**、フラグ データとエントリ識別子の残りの部分を個別に格納します。**FLATENTRY 構造体は**、残りのエントリ識別子を持つフラグ データを格納します。</span><span class="sxs-lookup"><span data-stu-id="9152a-155">An **ENTRYID** structure stores the flag data and the rest of the entry identifier separately; a **FLATENTRY** structure stores the flag data with the rest of the entry identifier.</span></span> 
    
- <span data-ttu-id="9152a-156">**ENTRYID** 構造体は [、IMAPIProp](imapipropiunknown.md)インターフェイスのメソッドおよび次の OpenEntry メソッドにパラメーターとして渡されます [。IABLogon::OpenEntry](iablogon-openentry.md)、 [IAddrBook::OpenEntry](iaddrbook-openentry.md)、 [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)  、 [IMAPISession::OpenEntry](imapisession-openentry.md)、 [IMAPISupport::OpenEntry](imapisupport-openentry.md)、 [IMsgStore::OpenEntry](imsgstore-openentry.md)、 [IMSLogon::OpenEntry](imslogon-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="9152a-156">An **ENTRYID** structure is passed as a parameter to the methods of the [IMAPIProp](imapipropiunknown.md) interface and to the following **OpenEntry** methods: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span></span>
    
- <span data-ttu-id="9152a-157">ENTRYID **構造体は** 、エントリ識別子をディスクに格納するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="9152a-157">An **ENTRYID** structure is used to store an entry identifier on disk.</span></span> <span data-ttu-id="9152a-158">**FLATENTRY 構造体は**、エントリ識別子をファイルに格納したり、バイト ストリームで渡したりするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="9152a-158">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes.</span></span> 
    
<span data-ttu-id="9152a-159">クライアントは、常に自然に配置されたエントリ識別子を渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="9152a-159">Clients should always pass in naturally aligned entry identifiers.</span></span> <span data-ttu-id="9152a-160">プロバイダーは任意に配置されたエントリ識別子を処理する必要があります。ただし、クライアントは、この動作を期待しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="9152a-160">Although providers should handle arbitrarily aligned entry identifiers, clients should not expect this behavior.</span></span> <span data-ttu-id="9152a-161">位置合わせされたエントリ識別子をメソッドに渡さない場合、RISC プロセッサで配置エラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9152a-161">Failure to pass a good aligned entry identifier to a method can cause an alignment fault on RISC processors.</span></span> 
  
<span data-ttu-id="9152a-162">自然な配置係数 (通常は 8 バイト) は、CPU でサポートされる最大のデータ型であり、通常はシステム メモリ アロケーターで使用されるのと同じ配置係数です。</span><span class="sxs-lookup"><span data-stu-id="9152a-162">The natural alignment factor, typically 8 bytes, is the largest data type supported by the CPU, and usually the same alignment factor used by the system memory allocator.</span></span> <span data-ttu-id="9152a-163">自然に配置されたメモリ アドレスを使用すると、CPU は、そのアドレスでサポートしている任意のデータ型に、配置エラーを生成せずにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="9152a-163">A naturally aligned memory address allows the CPU to access any data type it supports at that address without generating an alignment fault.</span></span> <span data-ttu-id="9152a-164">RISC CPU の場合、サイズ N バイトのデータ型は通常、N バイトの倍数で配置され、アドレスは N の倍数である必要があります。</span><span class="sxs-lookup"><span data-stu-id="9152a-164">For RISC CPUs, a data type of size N bytes must usually be aligned on an even multiple of N bytes, with the address being an even multiple of N.</span></span>
  
<span data-ttu-id="9152a-165">詳細については、「Entry [IDENTIFIERs」を参照してください](mapi-entry-identifiers.md)。</span><span class="sxs-lookup"><span data-stu-id="9152a-165">For more information, see [Entry Identifiers](mapi-entry-identifiers.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9152a-166">関連項目</span><span class="sxs-lookup"><span data-stu-id="9152a-166">See also</span></span>



[<span data-ttu-id="9152a-167">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="9152a-167">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="9152a-168">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="9152a-168">IMAPISupport::CompareEntryIDs</span></span>](imapisupport-compareentryids.md)
  
[<span data-ttu-id="9152a-169">PidTagRecordKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9152a-169">PidTagRecordKey Canonical Property</span></span>](pidtagrecordkey-canonical-property.md)


[<span data-ttu-id="9152a-170">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="9152a-170">MAPI Structures</span></span>](mapi-structures.md)

