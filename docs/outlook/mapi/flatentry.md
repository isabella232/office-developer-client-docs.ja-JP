---
title: FLATENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATENTRY
api_type:
- COM
ms.assetid: 03e53e08-9113-4101-84c9-ccf6d43127f6
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e47f4e0d1ab9ab3ecfd53932b8ef26440134c603
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407243"
---
# <a name="flatentry"></a><span data-ttu-id="8e93d-103">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="8e93d-103">FLATENTRY</span></span>

  
  
<span data-ttu-id="8e93d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e93d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e93d-105">entryid [](entryid.md)構造に加えて、 **entryid**構造体のサイズを指定するバイト数を指定します。</span><span class="sxs-lookup"><span data-stu-id="8e93d-105">An [ENTRYID](entryid.md) structure plus a byte count that specifies the size of the **ENTRYID** structure.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8e93d-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="8e93d-106">Header file:</span></span>  <br/> |<span data-ttu-id="8e93d-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8e93d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="8e93d-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="8e93d-108">Related macros:</span></span>  <br/> |<span data-ttu-id="8e93d-109">[cbFLATENTRY](cbflatentry.md)、 [CbNewFLATENTRY](cbnewflatentry.md)</span><span class="sxs-lookup"><span data-stu-id="8e93d-109">[cbFLATENTRY](cbflatentry.md), [CbNewFLATENTRY](cbnewflatentry.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} FLATENTRY, FAR *LPFLATENTRY;

```

## <a name="members"></a><span data-ttu-id="8e93d-110">メンバー</span><span class="sxs-lookup"><span data-stu-id="8e93d-110">Members</span></span>

 <span data-ttu-id="8e93d-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="8e93d-111">**cb**</span></span>
  
> <span data-ttu-id="8e93d-112">**abentry**メンバーのバイト数。</span><span class="sxs-lookup"><span data-stu-id="8e93d-112">Count of bytes in the **abEntry** member.</span></span> 
    
 <span data-ttu-id="8e93d-113">**abentry**</span><span class="sxs-lookup"><span data-stu-id="8e93d-113">**abEntry**</span></span>
  
> <span data-ttu-id="8e93d-114">フラグとバイナリデータの配列を含む完全なエントリ識別子。</span><span class="sxs-lookup"><span data-stu-id="8e93d-114">The complete entry identifier that includes the array of flags and binary data.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8e93d-115">注釈</span><span class="sxs-lookup"><span data-stu-id="8e93d-115">Remarks</span></span>

<span data-ttu-id="8e93d-116">**FLATENTRY**構造体は、 [ENTRYID](entryid.md)構造に似ています。</span><span class="sxs-lookup"><span data-stu-id="8e93d-116">A **FLATENTRY** structure resembles an [ENTRYID](entryid.md) structure.</span></span> <span data-ttu-id="8e93d-117">ただし、次のような違いがあります。</span><span class="sxs-lookup"><span data-stu-id="8e93d-117">However, there are some differences:</span></span> 
  
- <span data-ttu-id="8e93d-118">**FLATENTRY**構造体は、エントリ識別子のサイズを格納します。**ENTRYID**は無効です。</span><span class="sxs-lookup"><span data-stu-id="8e93d-118">A **FLATENTRY** structure stores the size of the entry identifier; **ENTRYID** does not.</span></span> 
    
- <span data-ttu-id="8e93d-119">**FLATENTRY**構造体は、フラグデータをエントリ id の残りの部分と一緒に格納します。**ENTRYID**は個別に格納します。</span><span class="sxs-lookup"><span data-stu-id="8e93d-119">A **FLATENTRY** structure stores the flag data together with the rest of the entry identifier; **ENTRYID** stores them separately.</span></span> 
    
- <span data-ttu-id="8e93d-120">**FLATENTRY**構造体は、エントリ id をファイルに格納したり、バイトのストリームに渡したりするために使用されます。 **ENTRYID**構造は、 [imapiprop](imapipropiunknown.md)のインターフェイスメソッドと、次の**openentry**メソッドで使用されます。 IABLogon は次のようになります。 [: openentry](iablogon-openentry.md)、 [IAddrBook:: openentry](iaddrbook-openentry.md)、 [IMAPIContainer:: openentry](imapicontainer-openentry.md)、 [imapisession:: openentry](imapisession-openentry.md)、 [imapisession:: openentry](imapisupport-openentry.md)、 [IMsgStore:: openentry](imsgstore-openentry.md)、 [IMSLogon:: openentry](imslogon-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="8e93d-120">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes whereas an **ENTRYID** structure is used by the [IMAPIProp](imapipropiunknown.md) interface methods and by the following **OpenEntry** methods: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span></span>
    
- <span data-ttu-id="8e93d-121">**FLATENTRY**構造体は、エントリ id をファイルに格納したり、バイトのストリームに渡したりするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8e93d-121">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes.</span></span> <span data-ttu-id="8e93d-122">**ENTRYID**構造体は、ディスクにエントリ識別子を格納するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8e93d-122">An **ENTRYID** structure is used to store an entry identifier on disk.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="8e93d-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="8e93d-123">See also</span></span>



[<span data-ttu-id="8e93d-124">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="8e93d-124">ENTRYID</span></span>](entryid.md)


[<span data-ttu-id="8e93d-125">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="8e93d-125">MAPI Structures</span></span>](mapi-structures.md)

