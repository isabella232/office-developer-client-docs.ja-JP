---
title: MAPINAMEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPINAMEID
api_type:
- COM
ms.assetid: 9a92e9cd-8282-4cf0-93af-4089b3763594
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: baec750a460b3ba9becd2e1dddf967705424ac4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411681"
---
# <a name="mapinameid"></a><span data-ttu-id="74648-103">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="74648-103">MAPINAMEID</span></span>

  
  
<span data-ttu-id="74648-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74648-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74648-105">名前付きプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="74648-105">Describes a named property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="74648-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="74648-106">Header file:</span></span>  <br/> |<span data-ttu-id="74648-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="74648-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _MAPINAMEID
{
  LPGUID lpguid;
  ULONG ulKind;
  union
  {
    LONG lID;
    LPWSTR lpwstrName;
  } Kind;
} MAPINAMEID, FAR *LPMAPINAMEID;

```

## <a name="members"></a><span data-ttu-id="74648-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="74648-108">Members</span></span>

 <span data-ttu-id="74648-109">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="74648-109">**lpguid**</span></span>
  
> <span data-ttu-id="74648-110">特定のプロパティセットを定義する[GUID](guid.md)構造体へのポインター。このメンバーを NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="74648-110">Pointer to a [GUID](guid.md) structure defining a particular property set; this member cannot be NULL.</span></span> <span data-ttu-id="74648-111">有効な値は以下のとおりです。</span><span class="sxs-lookup"><span data-stu-id="74648-111">Valid values are as follows:</span></span> 
    
<span data-ttu-id="74648-112">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="74648-112">PS_PUBLIC_STRINGS</span></span>
  
> 
    
<span data-ttu-id="74648-113">PS_MAPI</span><span class="sxs-lookup"><span data-stu-id="74648-113">PS_MAPI</span></span>
  
> 
    
<span data-ttu-id="74648-114">クライアント定義の値</span><span class="sxs-lookup"><span data-stu-id="74648-114">A client-defined value</span></span>
  
> 
    
 <span data-ttu-id="74648-115">**ulkind**</span><span class="sxs-lookup"><span data-stu-id="74648-115">**ulKind**</span></span>
  
> <span data-ttu-id="74648-116">**Kind**メンバー内の値の種類を説明する値。</span><span class="sxs-lookup"><span data-stu-id="74648-116">Value describing the type of value in the **Kind** member.</span></span> <span data-ttu-id="74648-117">有効な値は以下のとおりです。</span><span class="sxs-lookup"><span data-stu-id="74648-117">Valid values are as follows:</span></span> 
    
<span data-ttu-id="74648-118">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="74648-118">MNID_ID</span></span> 
  
> <span data-ttu-id="74648-119">**Kind**メンバーには、プロパティ名を表す整数値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="74648-119">The **Kind** member contains an integer value that represents the property name.</span></span> 
    
<span data-ttu-id="74648-120">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="74648-120">MNID_STRING</span></span> 
  
> <span data-ttu-id="74648-121">**Kind**メンバーには、プロパティ名を表す Unicode 文字の文字列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="74648-121">The **Kind** member contains a Unicode character string representing the property name.</span></span> 
    
 <span data-ttu-id="74648-122">**Kind**</span><span class="sxs-lookup"><span data-stu-id="74648-122">**Kind**</span></span>
  
> <span data-ttu-id="74648-123">名前付きプロパティの名前を説明する共用体。</span><span class="sxs-lookup"><span data-stu-id="74648-123">Union describing the name of the named property.</span></span> <span data-ttu-id="74648-124">この名前は、 **lID**に格納された整数値、または**lpwstrname**に格納されている Unicode 文字列のいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="74648-124">The name can be either an integer value, stored in **lID**, or a Unicode character string, stored in **lpwstrName**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="74648-125">注釈</span><span class="sxs-lookup"><span data-stu-id="74648-125">Remarks</span></span>

<span data-ttu-id="74648-126">**mapinameid**構造は、0x8000 を超える識別子を持つ名前付きプロパティのプロパティを記述するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="74648-126">The **MAPINAMEID** structure is used to describe named properties properties that have identifiers over 0x8000.</span></span> <span data-ttu-id="74648-127">プロパティセットは、名前付きプロパティという重要な部分です。</span><span class="sxs-lookup"><span data-stu-id="74648-127">A property set is an important part a named property.</span></span> <span data-ttu-id="74648-128">たとえば、PS_PUBLIC_STRINGS や PS_ROUTING_ADDRTYPE は、MAPI によって定義されたプロパティセットです。</span><span class="sxs-lookup"><span data-stu-id="74648-128">For example PS_PUBLIC_STRINGS or PS_ROUTING_ADDRTYPE are property sets defined by MAPI.</span></span> 
  
<span data-ttu-id="74648-129">名前付きプロパティを使用すると、クライアントは、MAPI で定義されたプロパティ識別子の範囲で利用できない、より大きな名前空間でカスタムプロパティを定義できます。</span><span class="sxs-lookup"><span data-stu-id="74648-129">Named properties enable clients to define custom properties in a larger namespace than is available in the MAPI-defined property identifier range.</span></span> <span data-ttu-id="74648-130">プロパティの名前を使用してプロパティの値を直接取得することはできません。最初に、 [imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)メソッドを使用して、プロパティ識別子にマップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="74648-130">Property names cannot be used to obtain property values directly; they must first be mapped to property identifiers through the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> <span data-ttu-id="74648-131">メッセージなどの特定のオブジェクトの場合、MAPI はカスタムプロパティの一連のプロパティ識別子を予約します。</span><span class="sxs-lookup"><span data-stu-id="74648-131">For particular objects such as messages, MAPI reserves a range of property identifiers for custom properties.</span></span> <span data-ttu-id="74648-132">そのため、これらのオブジェクトの場合、クライアントは名前付きプロパティを使用する必要がなく、関連するオーバーヘッドを保存できます。</span><span class="sxs-lookup"><span data-stu-id="74648-132">Therefore, for these objects, clients do not have to use named properties and can save the associated overhead.</span></span> 
  
<span data-ttu-id="74648-133">名前付きプロパティの詳細については、「[名前付きプロパティ](mapi-named-properties.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="74648-133">For more information about named properties, see [Named Properties](mapi-named-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="74648-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="74648-134">See also</span></span>



[<span data-ttu-id="74648-135">GUID</span><span class="sxs-lookup"><span data-stu-id="74648-135">GUID</span></span>](guid.md)
  
[<span data-ttu-id="74648-136">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="74648-136">IMAPIProp::GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md)


[<span data-ttu-id="74648-137">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="74648-137">MAPI Structures</span></span>](mapi-structures.md)

