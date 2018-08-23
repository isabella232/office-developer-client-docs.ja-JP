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
ms.openlocfilehash: c3a21e8a6e69cae9d8b757a60fe56d63e079b3ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801498"
---
# <a name="mapinameid"></a><span data-ttu-id="99dad-103">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="99dad-103">MAPINAMEID</span></span>

  
  
<span data-ttu-id="99dad-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="99dad-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="99dad-105">名前付きプロパティをについて説明します。</span><span class="sxs-lookup"><span data-stu-id="99dad-105">Describes a named property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="99dad-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="99dad-106">Header file:</span></span>  <br/> |<span data-ttu-id="99dad-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="99dad-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="99dad-108">Members</span><span class="sxs-lookup"><span data-stu-id="99dad-108">Members</span></span>

 <span data-ttu-id="99dad-109">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="99dad-109">**lpguid**</span></span>
  
> <span data-ttu-id="99dad-110">特定のプロパティを定義する[GUID](guid.md)構造体へのポインターを設定します。このメンバーは NULL にできません。</span><span class="sxs-lookup"><span data-stu-id="99dad-110">Pointer to a [GUID](guid.md) structure defining a particular property set; this member cannot be NULL.</span></span> <span data-ttu-id="99dad-111">有効な値は以下のとおりです。</span><span class="sxs-lookup"><span data-stu-id="99dad-111">Valid values are as follows:</span></span> 
    
<span data-ttu-id="99dad-112">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="99dad-112">PS_PUBLIC_STRINGS</span></span>
  
> 
    
<span data-ttu-id="99dad-113">PS_MAPI</span><span class="sxs-lookup"><span data-stu-id="99dad-113">PS_MAPI</span></span>
  
> 
    
<span data-ttu-id="99dad-114">クライアント定義の値</span><span class="sxs-lookup"><span data-stu-id="99dad-114">A client-defined value</span></span>
  
> 
    
 <span data-ttu-id="99dad-115">**ulKind**</span><span class="sxs-lookup"><span data-stu-id="99dad-115">**ulKind**</span></span>
  
> <span data-ttu-id="99dad-116">**種類**のメンバーの値の種類を示す数値です。</span><span class="sxs-lookup"><span data-stu-id="99dad-116">Value describing the type of value in the **Kind** member.</span></span> <span data-ttu-id="99dad-117">有効な値は以下のとおりです。</span><span class="sxs-lookup"><span data-stu-id="99dad-117">Valid values are as follows:</span></span> 
    
<span data-ttu-id="99dad-118">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="99dad-118">MNID_ID</span></span> 
  
> <span data-ttu-id="99dad-119">**種類**のメンバーには、プロパティ名を表す整数値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="99dad-119">The **Kind** member contains an integer value that represents the property name.</span></span> 
    
<span data-ttu-id="99dad-120">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="99dad-120">MNID_STRING</span></span> 
  
> <span data-ttu-id="99dad-121">**種類**のメンバーには、プロパティ名を表す Unicode 文字の文字列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="99dad-121">The **Kind** member contains a Unicode character string representing the property name.</span></span> 
    
 <span data-ttu-id="99dad-122">**種類**</span><span class="sxs-lookup"><span data-stu-id="99dad-122">**Kind**</span></span>
  
> <span data-ttu-id="99dad-123">共用体の名前付きプロパティの名前を記述します。</span><span class="sxs-lookup"><span data-stu-id="99dad-123">Union describing the name of the named property.</span></span> <span data-ttu-id="99dad-124">名前は**カバー**に格納されている整数値、または**lpwstrName**に格納されている Unicode 文字の文字列のいずれかにできます。</span><span class="sxs-lookup"><span data-stu-id="99dad-124">The name can be either an integer value, stored in **lID**, or a Unicode character string, stored in **lpwstrName**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="99dad-125">注釈</span><span class="sxs-lookup"><span data-stu-id="99dad-125">Remarks</span></span>

<span data-ttu-id="99dad-126">**MAPINAMEID**構造体を使用して、0x8000 以上の識別子を持つ名前付きプロパティのプロパティを記述します。</span><span class="sxs-lookup"><span data-stu-id="99dad-126">The **MAPINAMEID** structure is used to describe named properties properties that have identifiers over 0x8000.</span></span> <span data-ttu-id="99dad-127">プロパティ セットは、重要な部分の名前付きプロパティです。</span><span class="sxs-lookup"><span data-stu-id="99dad-127">A property set is an important part a named property.</span></span> <span data-ttu-id="99dad-128">たとえば PS_PUBLIC_STRINGS または PS_ROUTING_ADDRTYPE は、MAPI によって定義されているプロパティのセットです。</span><span class="sxs-lookup"><span data-stu-id="99dad-128">For example PS_PUBLIC_STRINGS or PS_ROUTING_ADDRTYPE are property sets defined by MAPI.</span></span> 
  
<span data-ttu-id="99dad-129">名前付きプロパティは、MAPI 定義のプロパティの識別子の範囲で利用できるよりも大規模な名前空間のカスタム プロパティを定義するのにはクライアントを有効にします。</span><span class="sxs-lookup"><span data-stu-id="99dad-129">Named properties enable clients to define custom properties in a larger namespace than is available in the MAPI-defined property identifier range.</span></span> <span data-ttu-id="99dad-130">プロパティの値を直接取得するプロパティ名を使用することはできません。最初にマップされるプロパティ識別子[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="99dad-130">Property names cannot be used to obtain property values directly; they must first be mapped to property identifiers through the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> <span data-ttu-id="99dad-131">メッセージなど、特定のオブジェクトには、MAPI は、カスタム プロパティのプロパティ id の範囲を予約します。</span><span class="sxs-lookup"><span data-stu-id="99dad-131">For particular objects such as messages, MAPI reserves a range of property identifiers for custom properties.</span></span> <span data-ttu-id="99dad-132">したがって、これらのオブジェクトのクライアント名前付きプロパティを使用することはありません、できれば、それに関連付けられたオーバーヘッドです。</span><span class="sxs-lookup"><span data-stu-id="99dad-132">Therefore, for these objects, clients do not have to use named properties and can save the associated overhead.</span></span> 
  
<span data-ttu-id="99dad-133">名前付きプロパティの詳細については、[名前付きプロパティ](mapi-named-properties.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="99dad-133">For more information about named properties, see [Named Properties](mapi-named-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="99dad-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="99dad-134">See also</span></span>



[<span data-ttu-id="99dad-135">GUID</span><span class="sxs-lookup"><span data-stu-id="99dad-135">GUID</span></span>](guid.md)
  
[<span data-ttu-id="99dad-136">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="99dad-136">IMAPIProp::GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md)


[<span data-ttu-id="99dad-137">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="99dad-137">MAPI Structures</span></span>](mapi-structures.md)

