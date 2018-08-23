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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8540176b7675917dde7c618c40142605e9622282
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586222"
---
# <a name="entryid"></a><span data-ttu-id="38a5a-103">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="38a5a-103">ENTRYID</span></span>

  
  
<span data-ttu-id="38a5a-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38a5a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38a5a-105">MAPI オブジェクトのエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="38a5a-105">Contains an entry identifier for a MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="38a5a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="38a5a-106">Header file:</span></span>  <br/> |<span data-ttu-id="38a5a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="38a5a-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="38a5a-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="38a5a-108">Related macros:</span></span>  <br/> |<span data-ttu-id="38a5a-109">[CbNewENTRYID](cbnewentryid.md)、 [SizedENTRYID](sizedentryid.md)</span><span class="sxs-lookup"><span data-stu-id="38a5a-109">[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  BYTE abFlags[4];
  BYTE ab[MAPI_DIM];
} ENTRYID, FAR *LPENTRYID;

```

## <a name="members"></a><span data-ttu-id="38a5a-110">Members</span><span class="sxs-lookup"><span data-stu-id="38a5a-110">Members</span></span>

 <span data-ttu-id="38a5a-111">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="38a5a-111">**abFlags**</span></span>
  
> <span data-ttu-id="38a5a-112">オブジェクトを説明する情報を提供するためのフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="38a5a-112">Bitmask of flags that provide information that describes the object.</span></span> <span data-ttu-id="38a5a-113">フラグ、 **abFlags [0]** の最初のバイトのみが、プロバイダーによって設定することが他の 3 つが予約されています。</span><span class="sxs-lookup"><span data-stu-id="38a5a-113">Only the first byte of the flags, **abFlags[0]**, may be set by the provider; the other three are reserved.</span></span> <span data-ttu-id="38a5a-114">永続的なエントリの識別子は、これらのフラグを設定しないでください。短期的なエントリの識別子にのみ設定されます。</span><span class="sxs-lookup"><span data-stu-id="38a5a-114">These flags must not be set for permanent entry identifiers; they are only set for short-term entry identifiers.</span></span> <span data-ttu-id="38a5a-115">クライアントにこの構造体は、読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="38a5a-115">To clients, this structure is read-only.</span></span> <span data-ttu-id="38a5a-116">**AbFlags [0]** では、次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="38a5a-116">The following flags can be set in **abFlags[0]**:</span></span>
    
<span data-ttu-id="38a5a-117">MAPI_NOTRECIP</span><span class="sxs-lookup"><span data-stu-id="38a5a-117">MAPI_NOTRECIP</span></span> 
  
> <span data-ttu-id="38a5a-118">エントリの識別子は、メッセージの受信者として使用できません。</span><span class="sxs-lookup"><span data-stu-id="38a5a-118">The entry identifier cannot be used as a recipient on a message.</span></span>
    
<span data-ttu-id="38a5a-119">MAPI_NOTRESERVED</span><span class="sxs-lookup"><span data-stu-id="38a5a-119">MAPI_NOTRESERVED</span></span> 
  
> <span data-ttu-id="38a5a-120">他のユーザーは、エントリの識別子にアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="38a5a-120">Other users cannot access the entry identifier.</span></span>
    
<span data-ttu-id="38a5a-121">MAPI_NOW</span><span class="sxs-lookup"><span data-stu-id="38a5a-121">MAPI_NOW</span></span> 
  
> <span data-ttu-id="38a5a-122">それ以外の場合は、エントリの識別子を使用できません。</span><span class="sxs-lookup"><span data-stu-id="38a5a-122">The entry identifier cannot be used at other times.</span></span>
    
<span data-ttu-id="38a5a-123">MAPI_SHORTTERM</span><span class="sxs-lookup"><span data-stu-id="38a5a-123">MAPI_SHORTTERM</span></span> 
  
> <span data-ttu-id="38a5a-124">エントリの識別子は、短期的です。</span><span class="sxs-lookup"><span data-stu-id="38a5a-124">The entry identifier is short-term.</span></span> <span data-ttu-id="38a5a-125">エントリの識別子の他の使用が有効でない場合、このバイトで他のすべての値を設定しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="38a5a-125">All other values in this byte must be set unless other uses of the entry identifier are enabled.</span></span>
    
<span data-ttu-id="38a5a-126">MAPI_THISSESSION</span><span class="sxs-lookup"><span data-stu-id="38a5a-126">MAPI_THISSESSION</span></span> 
  
> <span data-ttu-id="38a5a-127">エントリの識別子は、他のセッションでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="38a5a-127">The entry identifier cannot be used on other sessions.</span></span>
    
 <span data-ttu-id="38a5a-128">**ab**</span><span class="sxs-lookup"><span data-stu-id="38a5a-128">**ab**</span></span>
  
> <span data-ttu-id="38a5a-129">サービス プロバイダーによって使用されるバイナリ データの配列を示します。</span><span class="sxs-lookup"><span data-stu-id="38a5a-129">Indicates an array of binary data that is used by service providers.</span></span> <span data-ttu-id="38a5a-130">クライアント アプリケーションは、この配列を使用できません。</span><span class="sxs-lookup"><span data-stu-id="38a5a-130">The client application cannot use this array.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="38a5a-131">注釈</span><span class="sxs-lookup"><span data-stu-id="38a5a-131">Remarks</span></span>

<span data-ttu-id="38a5a-132">**エントリ ID**の構造を使用してメッセージを格納し、アドレス帳プロバイダーは、オブジェクトの一意の識別子を作成します。</span><span class="sxs-lookup"><span data-stu-id="38a5a-132">The **ENTRYID** structure is used by message store and address book providers to construct unique identifiers for their objects.</span></span> <span data-ttu-id="38a5a-133">次の種類のオブジェクトを識別するエントリの識別子が使用されます。</span><span class="sxs-lookup"><span data-stu-id="38a5a-133">Entry identifiers are used to identify the following types of objects:</span></span> 
  
- <span data-ttu-id="38a5a-134">メッセージ ・ ストア</span><span class="sxs-lookup"><span data-stu-id="38a5a-134">Message stores</span></span>
    
- <span data-ttu-id="38a5a-135">フォルダー</span><span class="sxs-lookup"><span data-stu-id="38a5a-135">Folders</span></span>
    
- <span data-ttu-id="38a5a-136">メッセージ</span><span class="sxs-lookup"><span data-stu-id="38a5a-136">Messages</span></span>
    
- <span data-ttu-id="38a5a-137">アドレス帳コンテナー</span><span class="sxs-lookup"><span data-stu-id="38a5a-137">Address book containers</span></span>
    
- <span data-ttu-id="38a5a-138">配布リスト</span><span class="sxs-lookup"><span data-stu-id="38a5a-138">Distribution lists</span></span>
    
- <span data-ttu-id="38a5a-139">ユーザーのメッセージング</span><span class="sxs-lookup"><span data-stu-id="38a5a-139">Messaging users</span></span>
    
- <span data-ttu-id="38a5a-140">ステータス オブジェクト</span><span class="sxs-lookup"><span data-stu-id="38a5a-140">Status objects</span></span>
    
- <span data-ttu-id="38a5a-141">プロファイル セクション</span><span class="sxs-lookup"><span data-stu-id="38a5a-141">Profile sections</span></span>
    
<span data-ttu-id="38a5a-142">各プロバイダーでは、そのプロバイダーに適した**エントリ ID**の構造体の形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="38a5a-142">Each provider uses a format for the **ENTRYID** structure that makes sense for that provider.</span></span> 
  
<span data-ttu-id="38a5a-143">1 つのオブジェクトは、2 つの異なるバイナリ値で表すことができるため、エントリ ID を直接比較することはできません。</span><span class="sxs-lookup"><span data-stu-id="38a5a-143">Entry identifiers cannot be compared directly because one object can be represented by two different binary values.</span></span> <span data-ttu-id="38a5a-144">2 つのエントリ id が同じオブジェクトを表しているかどうかを確認するのには、 [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="38a5a-144">To determine whether two entry identifiers represent the same object, call the [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) method.</span></span> 
  
<span data-ttu-id="38a5a-145">クライアントは、そのエントリの識別子を取得するオブジェクトの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出す、ときにオブジェクトのエントリ id の最も永続的な形式を返します。</span><span class="sxs-lookup"><span data-stu-id="38a5a-145">When a client calls an object's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its entry identifier, the object returns the most permanent form of the entry identifier.</span></span> <span data-ttu-id="38a5a-146">エントリ識別子は、 **abFlags**メンバーの最初のバイトに設定されているフラグのいずれかを確認することで長期的なクライアントを確認できます。</span><span class="sxs-lookup"><span data-stu-id="38a5a-146">A client can verify that an entry identifier is long-term by checking that none of the flags are set in the first byte of the **abFlags** member.</span></span> 
  
<span data-ttu-id="38a5a-147">クライアントには、このエントリの識別子は、長期的なのではなく短期的な多くの場合、テーブル内の列をエントリ id がアクセスするとします。</span><span class="sxs-lookup"><span data-stu-id="38a5a-147">When a client accesses an entry identifier through a column in a table, most likely this entry identifier is short-term instead of long-term.</span></span> <span data-ttu-id="38a5a-148">現在の MAPI セッションでのみ、対応するオブジェクトを開くには、短期的なエントリの識別子を使用できます。</span><span class="sxs-lookup"><span data-stu-id="38a5a-148">Short-term entry identifiers can be used to open their corresponding objects only in the current MAPI session.</span></span> <span data-ttu-id="38a5a-149">クライアントは、エントリ識別子は、 **abFlags**メンバーの最初のバイトに設定されているすべてのフラグを確認することで短期的なことを確認できます。</span><span class="sxs-lookup"><span data-stu-id="38a5a-149">A client can verify that an entry identifier is short-term by checking that all of the flags are set in the first byte of the **abFlags** member.</span></span> 
  
<span data-ttu-id="38a5a-150">いくつかのエントリ id は短期的なが、長期的に使用されています。</span><span class="sxs-lookup"><span data-stu-id="38a5a-150">Some entry identifiers are short-term, but have long-term use.</span></span> <span data-ttu-id="38a5a-151">このようなエントリ id は、 **abFlags**メンバーの最初のバイトに設定する適切なフラグの 1 つ以上があります。</span><span class="sxs-lookup"><span data-stu-id="38a5a-151">Such an entry identifier will have one or more of the appropriate flags set in the first byte of its **abFlags** member.</span></span> 
  
<span data-ttu-id="38a5a-152">**エントリ ID**の構造体には、 [FLATENTRY](flatentry.md)構造体に似ています。</span><span class="sxs-lookup"><span data-stu-id="38a5a-152">An **ENTRYID** structure resembles a [FLATENTRY](flatentry.md) structure.</span></span> <span data-ttu-id="38a5a-153">ただし、これにはいくつか相違点があります。</span><span class="sxs-lookup"><span data-stu-id="38a5a-153">However, there are some differences:</span></span> 
  
- <span data-ttu-id="38a5a-154">**エントリ ID**の構造体は、エントリ識別子のサイズを格納しません。**FLATENTRY**構造体は次のとおり行われます。</span><span class="sxs-lookup"><span data-stu-id="38a5a-154">An **ENTRYID** structure does not store the size of the entry identifier; a **FLATENTRY** structure does.</span></span> 
    
- <span data-ttu-id="38a5a-155">フラグ データおよびエントリの識別子の残りの部分に個別に格納**エントリ ID**の構造体**FLATENTRY**構造体は、フラグとデータ エントリの識別子の残りの部分を格納します。</span><span class="sxs-lookup"><span data-stu-id="38a5a-155">An **ENTRYID** structure stores the flag data and the rest of the entry identifier separately; a **FLATENTRY** structure stores the flag data with the rest of the entry identifier.</span></span> 
    
- <span data-ttu-id="38a5a-156">[IMAPIProp](imapipropiunknown.md)インターフェイスのメソッドに、次の**OpenEntry**メソッドを**エントリ ID**の構造体がパラメーターとして渡された: [IABLogon::OpenEntry](iablogon-openentry.md)、[アドレス帳コンテナー](iaddrbook-openentry.md)、 [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)、 [IMAPISession::OpenEntry](imapisession-openentry.md)、 [IMAPISupport::OpenEntry](imapisupport-openentry.md)、 [IMsgStore::OpenEntry](imsgstore-openentry.md)、 [IMSLogon::OpenEntry](imslogon-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="38a5a-156">An **ENTRYID** structure is passed as a parameter to the methods of the [IMAPIProp](imapipropiunknown.md) interface and to the following **OpenEntry** methods: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span></span>
    
- <span data-ttu-id="38a5a-157">**エントリ ID**の構造体を使用すると、ディスク上のエントリ id を格納します。</span><span class="sxs-lookup"><span data-stu-id="38a5a-157">An **ENTRYID** structure is used to store an entry identifier on disk.</span></span> <span data-ttu-id="38a5a-158">エントリ識別子をファイルに格納するバイトのストリームに渡すことは、 **FLATENTRY**構造体が使用されます。</span><span class="sxs-lookup"><span data-stu-id="38a5a-158">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes.</span></span> 
    
<span data-ttu-id="38a5a-159">クライアントは、必然的に配置されたエントリの識別子で常に渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="38a5a-159">Clients should always pass in naturally aligned entry identifiers.</span></span> <span data-ttu-id="38a5a-160">プロバイダーでは、任意に配置されたエントリの識別子を処理する必要がありますがクライアントにはこの現象は限りません。</span><span class="sxs-lookup"><span data-stu-id="38a5a-160">Although providers should handle arbitrarily aligned entry identifiers, clients should not expect this behavior.</span></span> <span data-ttu-id="38a5a-161">適切なアライメントされたエントリの識別子をメソッドに渡すと可能性が整列エラー RISC プロセッサにします。</span><span class="sxs-lookup"><span data-stu-id="38a5a-161">Failure to pass a good aligned entry identifier to a method can cause an alignment fault on RISC processors.</span></span> 
  
<span data-ttu-id="38a5a-162">自然な配置、8 バイト、通常は、CPU でサポートされる最大のデータ型と通常のシステム メモリ アロケーターによって使用される同じ配置係数。</span><span class="sxs-lookup"><span data-stu-id="38a5a-162">The natural alignment factor, typically 8 bytes, is the largest data type supported by the CPU, and usually the same alignment factor used by the system memory allocator.</span></span> <span data-ttu-id="38a5a-163">自然にアラインメントされたメモリ アドレスでは、整列エラーを生成することがなくそのアドレスをサポートしている任意のデータ型にアクセスするために CPU を使用できます。</span><span class="sxs-lookup"><span data-stu-id="38a5a-163">A naturally aligned memory address allows the CPU to access any data type it supports at that address without generating an alignment fault.</span></span> <span data-ttu-id="38a5a-164">RISC cpu、サイズ N バイトのデータ型する必要があります通常に配置する、N バイトの倍数 N. の偶数の倍数の中のアドレスを持つ</span><span class="sxs-lookup"><span data-stu-id="38a5a-164">For RISC CPUs, a data type of size N bytes must usually be aligned on an even multiple of N bytes, with the address being an even multiple of N.</span></span>
  
<span data-ttu-id="38a5a-165">詳細については、[エントリの識別子](mapi-entry-identifiers.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="38a5a-165">For more information, see [Entry Identifiers](mapi-entry-identifiers.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="38a5a-166">関連項目</span><span class="sxs-lookup"><span data-stu-id="38a5a-166">See also</span></span>



[<span data-ttu-id="38a5a-167">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="38a5a-167">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="38a5a-168">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="38a5a-168">IMAPISupport::CompareEntryIDs</span></span>](imapisupport-compareentryids.md)
  
[<span data-ttu-id="38a5a-169">PidTagRecordKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="38a5a-169">PidTagRecordKey Canonical Property</span></span>](pidtagrecordkey-canonical-property.md)


[<span data-ttu-id="38a5a-170">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="38a5a-170">MAPI Structures</span></span>](mapi-structures.md)

