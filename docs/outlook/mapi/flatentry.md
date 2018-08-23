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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cf84c7d94e67da0ce7453829042e7be0d4e313f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585550"
---
# <a name="flatentry"></a><span data-ttu-id="0d59c-103">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="0d59c-103">FLATENTRY</span></span>

  
  
<span data-ttu-id="0d59c-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d59c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d59c-105">[エントリ ID](entryid.md)の構造体と構造体**エントリ ID**のサイズを指定するバイト数です。</span><span class="sxs-lookup"><span data-stu-id="0d59c-105">An [ENTRYID](entryid.md) structure plus a byte count that specifies the size of the **ENTRYID** structure.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0d59c-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0d59c-106">Header file:</span></span>  <br/> |<span data-ttu-id="0d59c-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0d59c-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0d59c-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="0d59c-108">Related macros:</span></span>  <br/> |<span data-ttu-id="0d59c-109">[cbFLATENTRY](cbflatentry.md)、 [CbNewFLATENTRY](cbnewflatentry.md)</span><span class="sxs-lookup"><span data-stu-id="0d59c-109">[cbFLATENTRY](cbflatentry.md), [CbNewFLATENTRY](cbnewflatentry.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} FLATENTRY, FAR *LPFLATENTRY;

```

## <a name="members"></a><span data-ttu-id="0d59c-110">Members</span><span class="sxs-lookup"><span data-stu-id="0d59c-110">Members</span></span>

 <span data-ttu-id="0d59c-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="0d59c-111">**cb**</span></span>
  
> <span data-ttu-id="0d59c-112">**AbEntry**メンバーのバイト数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="0d59c-112">Count of bytes in the **abEntry** member.</span></span> 
    
 <span data-ttu-id="0d59c-113">**abEntry**</span><span class="sxs-lookup"><span data-stu-id="0d59c-113">**abEntry**</span></span>
  
> <span data-ttu-id="0d59c-114">フラグ、およびバイナリ データの配列を含む完全なエントリの識別子です。</span><span class="sxs-lookup"><span data-stu-id="0d59c-114">The complete entry identifier that includes the array of flags and binary data.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0d59c-115">注釈</span><span class="sxs-lookup"><span data-stu-id="0d59c-115">Remarks</span></span>

<span data-ttu-id="0d59c-116">**FLATENTRY**構造体では、[エントリ ID](entryid.md)の構造が似ています。</span><span class="sxs-lookup"><span data-stu-id="0d59c-116">A **FLATENTRY** structure resembles an [ENTRYID](entryid.md) structure.</span></span> <span data-ttu-id="0d59c-117">ただし、これにはいくつか相違点があります。</span><span class="sxs-lookup"><span data-stu-id="0d59c-117">However, there are some differences:</span></span> 
  
- <span data-ttu-id="0d59c-118">エントリ識別子のサイズを格納する**FLATENTRY**構造体**エントリ ID**はありません。</span><span class="sxs-lookup"><span data-stu-id="0d59c-118">A **FLATENTRY** structure stores the size of the entry identifier; **ENTRYID** does not.</span></span> 
    
- <span data-ttu-id="0d59c-119">**FLATENTRY**構造体は、エントリの識別子の残りの部分と一緒にフラグ データを格納します。**エントリ ID**を格納するとは別にします。</span><span class="sxs-lookup"><span data-stu-id="0d59c-119">A **FLATENTRY** structure stores the flag data together with the rest of the entry identifier; **ENTRYID** stores them separately.</span></span> 
    
- <span data-ttu-id="0d59c-120">エントリ識別子をファイルに保存またはバイトのストリームに渡すことが、**エントリ ID**の構造体は、 [IMAPIProp](imapipropiunknown.md)インターフェイスのメソッドと次の**OpenEntry**メソッドで使用する**FLATENTRY**構造体が使用される: [IABLogon:: OpenEntry](iablogon-openentry.md)、[アドレス帳コンテナー](iaddrbook-openentry.md)、 [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)、 [IMAPISession::OpenEntry](imapisession-openentry.md)、 [IMAPISupport::OpenEntry](imapisupport-openentry.md)、 [IMsgStore::OpenEntry](imsgstore-openentry.md)、 [IMSLogon::OpenEntry](imslogon-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="0d59c-120">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes whereas an **ENTRYID** structure is used by the [IMAPIProp](imapipropiunknown.md) interface methods and by the following **OpenEntry** methods: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span></span>
    
- <span data-ttu-id="0d59c-121">エントリ識別子をファイルに格納するバイトのストリームに渡すことは、 **FLATENTRY**構造体が使用されます。</span><span class="sxs-lookup"><span data-stu-id="0d59c-121">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes.</span></span> <span data-ttu-id="0d59c-122">**エントリ ID**の構造体を使用すると、ディスク上のエントリ id を格納します。</span><span class="sxs-lookup"><span data-stu-id="0d59c-122">An **ENTRYID** structure is used to store an entry identifier on disk.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="0d59c-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="0d59c-123">See also</span></span>



[<span data-ttu-id="0d59c-124">エントリ ID</span><span class="sxs-lookup"><span data-stu-id="0d59c-124">ENTRYID</span></span>](entryid.md)


[<span data-ttu-id="0d59c-125">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="0d59c-125">MAPI Structures</span></span>](mapi-structures.md)

