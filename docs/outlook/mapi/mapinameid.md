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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f0ff4d8beb9c9d82d685630a35aefebaf7de71fc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570829"
---
# <a name="mapinameid"></a><span data-ttu-id="e28dc-103">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="e28dc-103">MAPINAMEID</span></span>

  
  
<span data-ttu-id="e28dc-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e28dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e28dc-105">名前付きプロパティをについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e28dc-105">Describes a named property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e28dc-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e28dc-106">Header file:</span></span>  <br/> |<span data-ttu-id="e28dc-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e28dc-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="e28dc-108">Members</span><span class="sxs-lookup"><span data-stu-id="e28dc-108">Members</span></span>

 <span data-ttu-id="e28dc-109">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="e28dc-109">**lpguid**</span></span>
  
> <span data-ttu-id="e28dc-110">特定のプロパティを定義する[GUID](guid.md)構造体へのポインターを設定します。このメンバーは NULL にできません。</span><span class="sxs-lookup"><span data-stu-id="e28dc-110">Pointer to a [GUID](guid.md) structure defining a particular property set; this member cannot be NULL.</span></span> <span data-ttu-id="e28dc-111">有効な値は以下のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e28dc-111">Valid values are as follows:</span></span> 
    
<span data-ttu-id="e28dc-112">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="e28dc-112">PS_PUBLIC_STRINGS</span></span>
  
> 
    
<span data-ttu-id="e28dc-113">PS_MAPI</span><span class="sxs-lookup"><span data-stu-id="e28dc-113">PS_MAPI</span></span>
  
> 
    
<span data-ttu-id="e28dc-114">クライアント定義の値</span><span class="sxs-lookup"><span data-stu-id="e28dc-114">A client-defined value</span></span>
  
> 
    
 <span data-ttu-id="e28dc-115">**ulKind**</span><span class="sxs-lookup"><span data-stu-id="e28dc-115">**ulKind**</span></span>
  
> <span data-ttu-id="e28dc-116">**種類**のメンバーの値の種類を示す数値です。</span><span class="sxs-lookup"><span data-stu-id="e28dc-116">Value describing the type of value in the **Kind** member.</span></span> <span data-ttu-id="e28dc-117">有効な値は以下のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e28dc-117">Valid values are as follows:</span></span> 
    
<span data-ttu-id="e28dc-118">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="e28dc-118">MNID_ID</span></span> 
  
> <span data-ttu-id="e28dc-119">**種類**のメンバーには、プロパティ名を表す整数値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e28dc-119">The **Kind** member contains an integer value that represents the property name.</span></span> 
    
<span data-ttu-id="e28dc-120">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="e28dc-120">MNID_STRING</span></span> 
  
> <span data-ttu-id="e28dc-121">**種類**のメンバーには、プロパティ名を表す Unicode 文字の文字列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e28dc-121">The **Kind** member contains a Unicode character string representing the property name.</span></span> 
    
 <span data-ttu-id="e28dc-122">**種類**</span><span class="sxs-lookup"><span data-stu-id="e28dc-122">**Kind**</span></span>
  
> <span data-ttu-id="e28dc-123">共用体の名前付きプロパティの名前を記述します。</span><span class="sxs-lookup"><span data-stu-id="e28dc-123">Union describing the name of the named property.</span></span> <span data-ttu-id="e28dc-124">名前は**カバー**に格納されている整数値、または**lpwstrName**に格納されている Unicode 文字の文字列のいずれかにできます。</span><span class="sxs-lookup"><span data-stu-id="e28dc-124">The name can be either an integer value, stored in **lID**, or a Unicode character string, stored in **lpwstrName**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e28dc-125">注釈</span><span class="sxs-lookup"><span data-stu-id="e28dc-125">Remarks</span></span>

<span data-ttu-id="e28dc-126">**MAPINAMEID**構造体を使用して、0x8000 以上の識別子を持つ名前付きプロパティのプロパティを記述します。</span><span class="sxs-lookup"><span data-stu-id="e28dc-126">The **MAPINAMEID** structure is used to describe named properties properties that have identifiers over 0x8000.</span></span> <span data-ttu-id="e28dc-127">プロパティ セットは、重要な部分の名前付きプロパティです。</span><span class="sxs-lookup"><span data-stu-id="e28dc-127">A property set is an important part a named property.</span></span> <span data-ttu-id="e28dc-128">たとえば PS_PUBLIC_STRINGS または PS_ROUTING_ADDRTYPE は、MAPI によって定義されているプロパティのセットです。</span><span class="sxs-lookup"><span data-stu-id="e28dc-128">For example PS_PUBLIC_STRINGS or PS_ROUTING_ADDRTYPE are property sets defined by MAPI.</span></span> 
  
<span data-ttu-id="e28dc-129">名前付きプロパティは、MAPI 定義のプロパティの識別子の範囲で利用できるよりも大規模な名前空間のカスタム プロパティを定義するのにはクライアントを有効にします。</span><span class="sxs-lookup"><span data-stu-id="e28dc-129">Named properties enable clients to define custom properties in a larger namespace than is available in the MAPI-defined property identifier range.</span></span> <span data-ttu-id="e28dc-130">プロパティの値を直接取得するプロパティ名を使用することはできません。最初にマップされるプロパティ識別子[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="e28dc-130">Property names cannot be used to obtain property values directly; they must first be mapped to property identifiers through the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> <span data-ttu-id="e28dc-131">メッセージなど、特定のオブジェクトには、MAPI は、カスタム プロパティのプロパティ id の範囲を予約します。</span><span class="sxs-lookup"><span data-stu-id="e28dc-131">For particular objects such as messages, MAPI reserves a range of property identifiers for custom properties.</span></span> <span data-ttu-id="e28dc-132">したがって、これらのオブジェクトのクライアント名前付きプロパティを使用することはありません、できれば、それに関連付けられたオーバーヘッドです。</span><span class="sxs-lookup"><span data-stu-id="e28dc-132">Therefore, for these objects, clients do not have to use named properties and can save the associated overhead.</span></span> 
  
<span data-ttu-id="e28dc-133">名前付きプロパティの詳細については、[名前付きプロパティ](mapi-named-properties.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e28dc-133">For more information about named properties, see [Named Properties](mapi-named-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e28dc-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="e28dc-134">See also</span></span>



[<span data-ttu-id="e28dc-135">GUID</span><span class="sxs-lookup"><span data-stu-id="e28dc-135">GUID</span></span>](guid.md)
  
[<span data-ttu-id="e28dc-136">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="e28dc-136">IMAPIProp::GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md)


[<span data-ttu-id="e28dc-137">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="e28dc-137">MAPI Structures</span></span>](mapi-structures.md)

