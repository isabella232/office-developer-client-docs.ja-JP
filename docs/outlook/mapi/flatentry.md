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
# <a name="flatentry"></a><span data-ttu-id="2738b-103">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="2738b-103">FLATENTRY</span></span>

  
  
<span data-ttu-id="2738b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2738b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2738b-105">[ENTRYID 構造体に、ENTRYID](entryid.md)構造体のサイズを指定するバイト数 **を加えた値を指定** します。</span><span class="sxs-lookup"><span data-stu-id="2738b-105">An [ENTRYID](entryid.md) structure plus a byte count that specifies the size of the **ENTRYID** structure.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2738b-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2738b-106">Header file:</span></span>  <br/> |<span data-ttu-id="2738b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2738b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2738b-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="2738b-108">Related macros:</span></span>  <br/> |<span data-ttu-id="2738b-109">[cbFLATENTRY](cbflatentry.md)、 [CbNewFLATENTRY](cbnewflatentry.md)</span><span class="sxs-lookup"><span data-stu-id="2738b-109">[cbFLATENTRY](cbflatentry.md), [CbNewFLATENTRY](cbnewflatentry.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} FLATENTRY, FAR *LPFLATENTRY;

```

## <a name="members"></a><span data-ttu-id="2738b-110">Members</span><span class="sxs-lookup"><span data-stu-id="2738b-110">Members</span></span>

 <span data-ttu-id="2738b-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="2738b-111">**cb**</span></span>
  
> <span data-ttu-id="2738b-112">**abEntry メンバーのバイト数**。</span><span class="sxs-lookup"><span data-stu-id="2738b-112">Count of bytes in the **abEntry** member.</span></span> 
    
 <span data-ttu-id="2738b-113">**abEntry**</span><span class="sxs-lookup"><span data-stu-id="2738b-113">**abEntry**</span></span>
  
> <span data-ttu-id="2738b-114">フラグとバイナリ データの配列を含む完全なエントリ識別子。</span><span class="sxs-lookup"><span data-stu-id="2738b-114">The complete entry identifier that includes the array of flags and binary data.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2738b-115">注釈</span><span class="sxs-lookup"><span data-stu-id="2738b-115">Remarks</span></span>

<span data-ttu-id="2738b-116">**FLATENTRY 構造体は** [ENTRYID 構造に似](entryid.md)ている。</span><span class="sxs-lookup"><span data-stu-id="2738b-116">A **FLATENTRY** structure resembles an [ENTRYID](entryid.md) structure.</span></span> <span data-ttu-id="2738b-117">ただし、いくつかの違いがあります。</span><span class="sxs-lookup"><span data-stu-id="2738b-117">However, there are some differences:</span></span> 
  
- <span data-ttu-id="2738b-118">**FLATENTRY 構造体** は、エントリ識別子のサイズを格納します。**ENTRYID** は使用しない。</span><span class="sxs-lookup"><span data-stu-id="2738b-118">A **FLATENTRY** structure stores the size of the entry identifier; **ENTRYID** does not.</span></span> 
    
- <span data-ttu-id="2738b-119">**FLATENTRY 構造体は**、残りのエントリ識別子と共にフラグ データを格納します。**ENTRYID は** それらを個別に格納します。</span><span class="sxs-lookup"><span data-stu-id="2738b-119">A **FLATENTRY** structure stores the flag data together with the rest of the entry identifier; **ENTRYID** stores them separately.</span></span> 
    
- <span data-ttu-id="2738b-120">**FLATENTRY** 構造体は、エントリ識別子をファイルに格納したり、バイト ストリームで渡したりするために使用しますが **、ENTRYID** 構造体は [IMAPIProp](imapipropiunknown.md)インターフェイス メソッドと次の **OpenEntry** メソッドによって使用されます [。IABLogon::OpenEntry](iablogon-openentry.md) [、IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="2738b-120">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes whereas an **ENTRYID** structure is used by the [IMAPIProp](imapipropiunknown.md) interface methods and by the following **OpenEntry** methods: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span></span>
    
- <span data-ttu-id="2738b-121">**FLATENTRY 構造体は**、エントリ識別子をファイルに格納したり、バイト ストリームで渡したりするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2738b-121">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes.</span></span> <span data-ttu-id="2738b-122">ENTRYID **構造体は** 、エントリ識別子をディスクに格納するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2738b-122">An **ENTRYID** structure is used to store an entry identifier on disk.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="2738b-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="2738b-123">See also</span></span>



[<span data-ttu-id="2738b-124">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="2738b-124">ENTRYID</span></span>](entryid.md)


[<span data-ttu-id="2738b-125">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="2738b-125">MAPI Structures</span></span>](mapi-structures.md)

