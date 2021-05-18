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
# <a name="mapinameid"></a><span data-ttu-id="4b045-103">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="4b045-103">MAPINAMEID</span></span>

  
  
<span data-ttu-id="4b045-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b045-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b045-105">名前付きプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="4b045-105">Describes a named property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4b045-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="4b045-106">Header file:</span></span>  <br/> |<span data-ttu-id="4b045-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4b045-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="4b045-108">Members</span><span class="sxs-lookup"><span data-stu-id="4b045-108">Members</span></span>

 <span data-ttu-id="4b045-109">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="4b045-109">**lpguid**</span></span>
  
> <span data-ttu-id="4b045-110">特定のプロパティ セットを定義する [GUID](guid.md) 構造へのポインター。このメンバーを NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="4b045-110">Pointer to a [GUID](guid.md) structure defining a particular property set; this member cannot be NULL.</span></span> <span data-ttu-id="4b045-111">有効な値は以下のとおりです。</span><span class="sxs-lookup"><span data-stu-id="4b045-111">Valid values are as follows:</span></span> 
    
<span data-ttu-id="4b045-112">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="4b045-112">PS_PUBLIC_STRINGS</span></span>
  
> 
    
<span data-ttu-id="4b045-113">PS_MAPI</span><span class="sxs-lookup"><span data-stu-id="4b045-113">PS_MAPI</span></span>
  
> 
    
<span data-ttu-id="4b045-114">クライアント定義の値</span><span class="sxs-lookup"><span data-stu-id="4b045-114">A client-defined value</span></span>
  
> 
    
 <span data-ttu-id="4b045-115">**ulKind**</span><span class="sxs-lookup"><span data-stu-id="4b045-115">**ulKind**</span></span>
  
> <span data-ttu-id="4b045-116">Kind メンバーの値の種類を表 **す** 値。</span><span class="sxs-lookup"><span data-stu-id="4b045-116">Value describing the type of value in the **Kind** member.</span></span> <span data-ttu-id="4b045-117">有効な値は以下のとおりです。</span><span class="sxs-lookup"><span data-stu-id="4b045-117">Valid values are as follows:</span></span> 
    
<span data-ttu-id="4b045-118">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="4b045-118">MNID_ID</span></span> 
  
> <span data-ttu-id="4b045-119">**Kind メンバー** には、プロパティ名を表す整数値が含まれる。</span><span class="sxs-lookup"><span data-stu-id="4b045-119">The **Kind** member contains an integer value that represents the property name.</span></span> 
    
<span data-ttu-id="4b045-120">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="4b045-120">MNID_STRING</span></span> 
  
> <span data-ttu-id="4b045-121">**Kind メンバーには**、プロパティ名を表す Unicode 文字文字列が含まれます。</span><span class="sxs-lookup"><span data-stu-id="4b045-121">The **Kind** member contains a Unicode character string representing the property name.</span></span> 
    
 <span data-ttu-id="4b045-122">**Kind**</span><span class="sxs-lookup"><span data-stu-id="4b045-122">**Kind**</span></span>
  
> <span data-ttu-id="4b045-123">名前付きプロパティの名前を表す共用体。</span><span class="sxs-lookup"><span data-stu-id="4b045-123">Union describing the name of the named property.</span></span> <span data-ttu-id="4b045-124">名前には **、lID** に格納された整数値、または **lpwstrName** に格納された Unicode 文字文字列のいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="4b045-124">The name can be either an integer value, stored in **lID**, or a Unicode character string, stored in **lpwstrName**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4b045-125">注釈</span><span class="sxs-lookup"><span data-stu-id="4b045-125">Remarks</span></span>

<span data-ttu-id="4b045-126">**MAPINAMEID 構造体は**、名前の付いたプロパティを記述するために使用されます。このプロパティの識別子は、0x8000。</span><span class="sxs-lookup"><span data-stu-id="4b045-126">The **MAPINAMEID** structure is used to describe named properties properties that have identifiers over 0x8000.</span></span> <span data-ttu-id="4b045-127">プロパティ セットは、名前付きプロパティの重要な部分です。</span><span class="sxs-lookup"><span data-stu-id="4b045-127">A property set is an important part a named property.</span></span> <span data-ttu-id="4b045-128">たとえば、mapi PS_PUBLIC_STRINGSまたはPS_ROUTING_ADDRTYPEプロパティ セットを指定します。</span><span class="sxs-lookup"><span data-stu-id="4b045-128">For example PS_PUBLIC_STRINGS or PS_ROUTING_ADDRTYPE are property sets defined by MAPI.</span></span> 
  
<span data-ttu-id="4b045-129">名前付きプロパティを使用すると、MAPI で定義されたプロパティ識別子の範囲よりも大きな名前空間でカスタム プロパティを定義できます。</span><span class="sxs-lookup"><span data-stu-id="4b045-129">Named properties enable clients to define custom properties in a larger namespace than is available in the MAPI-defined property identifier range.</span></span> <span data-ttu-id="4b045-130">プロパティ名を使用してプロパティ値を直接取得することはできません。まず [、IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) メソッドを使用してプロパティ識別子にマップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4b045-130">Property names cannot be used to obtain property values directly; they must first be mapped to property identifiers through the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> <span data-ttu-id="4b045-131">メッセージなどの特定のオブジェクトに対して、MAPI はカスタム プロパティのプロパティ識別子の範囲を予約します。</span><span class="sxs-lookup"><span data-stu-id="4b045-131">For particular objects such as messages, MAPI reserves a range of property identifiers for custom properties.</span></span> <span data-ttu-id="4b045-132">したがって、これらのオブジェクトの場合、クライアントは名前付きプロパティを使用する必要はありません。関連するオーバーヘッドを保存できます。</span><span class="sxs-lookup"><span data-stu-id="4b045-132">Therefore, for these objects, clients do not have to use named properties and can save the associated overhead.</span></span> 
  
<span data-ttu-id="4b045-133">名前付きプロパティの詳細については、「名前付きプロパティ [」を参照してください](mapi-named-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="4b045-133">For more information about named properties, see [Named Properties](mapi-named-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4b045-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="4b045-134">See also</span></span>



[<span data-ttu-id="4b045-135">GUID</span><span class="sxs-lookup"><span data-stu-id="4b045-135">GUID</span></span>](guid.md)
  
[<span data-ttu-id="4b045-136">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="4b045-136">IMAPIProp::GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md)


[<span data-ttu-id="4b045-137">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="4b045-137">MAPI Structures</span></span>](mapi-structures.md)

