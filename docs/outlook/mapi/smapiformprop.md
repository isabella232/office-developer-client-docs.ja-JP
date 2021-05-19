---
title: SMAPIFormProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormProp
api_type:
- COM
ms.assetid: 80f1c2e0-3567-4b16-86cb-d5e6ac95c2ee
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 968f9e1dad3a233b31f0ce29d3ce935b1257948c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416700"
---
# <a name="smapiformprop"></a><span data-ttu-id="1a3b1-103">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="1a3b1-103">SMAPIFormProp</span></span>

  
  
<span data-ttu-id="1a3b1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a3b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a3b1-105">フォームで使用される名前付きプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="1a3b1-105">Describes a named property used with a form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1a3b1-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="1a3b1-106">Header file:</span></span>  <br/> |<span data-ttu-id="1a3b1-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="1a3b1-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct _SMAPIFormProp
{
  ULONG ulFlags;
  ULONG nPropType;
  MAPINAMEID nmid;
  LPSTR pszDisplayName;
  FORMPROPSPECIALTYPE nSpecialType;
  union
  {
    struct
    {
      MAPINAMEID nmidIdx;
      ULONG cfpevAvailable;
      LPMAPIFORMPROPENUMVAL pfpevAvailable;
    } s1;
  } u;
} SMAPIFormProp, FAR * LPMAPIFORMPROP;

```

## <a name="members"></a><span data-ttu-id="1a3b1-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="1a3b1-108">Members</span></span>

 <span data-ttu-id="1a3b1-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="1a3b1-109">**ulFlags**</span></span>
  
> <span data-ttu-id="1a3b1-110">**SMAPIFormProp** 構造体の文字列の形式を区別するために使用されるフラグ。</span><span class="sxs-lookup"><span data-stu-id="1a3b1-110">Flags used to distinguish the format of the strings in the **SMAPIFormProp** structure.</span></span> <span data-ttu-id="1a3b1-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="1a3b1-111">The following flag can be set:</span></span> 
    
<span data-ttu-id="1a3b1-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1a3b1-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1a3b1-113">返される文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="1a3b1-113">The strings returned are in Unicode format.</span></span> <span data-ttu-id="1a3b1-114">このMAPI_UNICODE設定されていない場合、文字列は ANSI 形式です。</span><span class="sxs-lookup"><span data-stu-id="1a3b1-114">If MAPI_UNICODE is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="1a3b1-115">**nPropType**</span><span class="sxs-lookup"><span data-stu-id="1a3b1-115">**nPropType**</span></span>
  
> <span data-ttu-id="1a3b1-116">最も重要な単語が 0 に設定された名前付きプロパティの種類。</span><span class="sxs-lookup"><span data-stu-id="1a3b1-116">Type of the named property, with the most significant word set to zero.</span></span> 
    
 <span data-ttu-id="1a3b1-117">**nmid**</span><span class="sxs-lookup"><span data-stu-id="1a3b1-117">**nmid**</span></span>
  
> <span data-ttu-id="1a3b1-118">プロパティ セットを識別する **GUID** 構造と、インターフェイス識別子とフォーム名を表す数値または文字列値を含む、名前付きプロパティの名前。</span><span class="sxs-lookup"><span data-stu-id="1a3b1-118">Name for the named property, which includes a **GUID** structure identifying the property set and either a numeric or string value that represents an interface identifier and form name.</span></span> 
    
 <span data-ttu-id="1a3b1-119">**pszDisplayName**</span><span class="sxs-lookup"><span data-stu-id="1a3b1-119">**pszDisplayName**</span></span>
  
> <span data-ttu-id="1a3b1-120">名前付きプロパティの表示名へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1a3b1-120">Pointer to the display name of the named property.</span></span>
    
 <span data-ttu-id="1a3b1-121">**nSpecialType**</span><span class="sxs-lookup"><span data-stu-id="1a3b1-121">**nSpecialType**</span></span>
  
> <span data-ttu-id="1a3b1-122">u メンバーに含まれるデータの種類を表す **値** 。</span><span class="sxs-lookup"><span data-stu-id="1a3b1-122">Value describing the type of data included in the **u** member.</span></span> <span data-ttu-id="1a3b1-123">指定できる値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="1a3b1-123">Possible values are as follows:</span></span> 
    
<span data-ttu-id="1a3b1-124">FPST_VANILLA</span><span class="sxs-lookup"><span data-stu-id="1a3b1-124">FPST_VANILLA</span></span> 
  
> <span data-ttu-id="1a3b1-125">**u メンバー** には列挙体が含めではありません。</span><span class="sxs-lookup"><span data-stu-id="1a3b1-125">The **u** member does not contain an enumeration.</span></span> 
    
<span data-ttu-id="1a3b1-126">FPST_ENUM_PROP</span><span class="sxs-lookup"><span data-stu-id="1a3b1-126">FPST_ENUM_PROP</span></span> 
  
> <span data-ttu-id="1a3b1-127">**u メンバー** には、列挙を記述する構造が含まれる。</span><span class="sxs-lookup"><span data-stu-id="1a3b1-127">The **u** member contains a structure that describes an enumeration.</span></span> 
    
 <span data-ttu-id="1a3b1-128">**u**</span><span class="sxs-lookup"><span data-stu-id="1a3b1-128">**u**</span></span>
  
> <span data-ttu-id="1a3b1-129">名前付きプロパティの名前と番号の関連付けを表す共用体。</span><span class="sxs-lookup"><span data-stu-id="1a3b1-129">Union describing the association between the name and number of the named property.</span></span> <span data-ttu-id="1a3b1-130">一部のプロパティを使用すると **、u** メンバーは空になります。</span><span class="sxs-lookup"><span data-stu-id="1a3b1-130">By using some properties, the **u** member is empty.</span></span> <span data-ttu-id="1a3b1-131">他のプロパティでは、次のメンバーで構成される構造で表されます。</span><span class="sxs-lookup"><span data-stu-id="1a3b1-131">With other properties, it is represented in a structure consisting of the following members:</span></span> 
    
 <span data-ttu-id="1a3b1-132">**nmidIdx**</span><span class="sxs-lookup"><span data-stu-id="1a3b1-132">**nmidIdx**</span></span>
  
> <span data-ttu-id="1a3b1-133">名前付 [きプロパティの](mapinameid.md) プロパティ セットと識別子を含む MAPINAMEID 構造体。</span><span class="sxs-lookup"><span data-stu-id="1a3b1-133">The [MAPINAMEID](mapinameid.md) structure that contains the property set and identifier for the named property.</span></span> 
    
 <span data-ttu-id="1a3b1-134">**cfpevAvailable**</span><span class="sxs-lookup"><span data-stu-id="1a3b1-134">**cfpevAvailable**</span></span>
  
> <span data-ttu-id="1a3b1-135">pfpevAvailable メンバーが指す配列内の [SMAPIFormPropEnumVal](smapiformpropenumval.md) **構造体の** 数。</span><span class="sxs-lookup"><span data-stu-id="1a3b1-135">Count of [SMAPIFormPropEnumVal](smapiformpropenumval.md) structures in the array pointed to by the **pfpevAvailable** member.</span></span> 
    
 <span data-ttu-id="1a3b1-136">**pfpevAvailable**</span><span class="sxs-lookup"><span data-stu-id="1a3b1-136">**pfpevAvailable**</span></span>
  
> <span data-ttu-id="1a3b1-137">**SMAPIFormPropEnumVal** 構造体の配列へのポインターで、それぞれ名前付きプロパティの値を保持します。</span><span class="sxs-lookup"><span data-stu-id="1a3b1-137">Pointer to an array of **SMAPIFormPropEnumVal** structures, each of which holds a value for the named property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1a3b1-138">注釈</span><span class="sxs-lookup"><span data-stu-id="1a3b1-138">Remarks</span></span>

<span data-ttu-id="1a3b1-139">**SMAPIFormProp** 構造体には [、IMAPIFormInfo](imapiforminfoimapiprop.md)インターフェイスの定義の一部として使用されるフォーム プロパティに関する情報が含まれる。**nSpecialType** には **、SMAPIFormProp** の一部である **u** 共用体に適用されるタグが含まれる。</span><span class="sxs-lookup"><span data-stu-id="1a3b1-139">The **SMAPIFormProp** structure contains information about a form property used as part of the definitions of the [IMAPIFormInfo](imapiforminfoimapiprop.md) interface; **nSpecialType** contains a tag that applies to the **u** union that is part of **SMAPIFormProp**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1a3b1-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="1a3b1-140">See also</span></span>



[<span data-ttu-id="1a3b1-141">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="1a3b1-141">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="1a3b1-142">SMAPIFormPropEnumVal</span><span class="sxs-lookup"><span data-stu-id="1a3b1-142">SMAPIFormPropEnumVal</span></span>](smapiformpropenumval.md)


[<span data-ttu-id="1a3b1-143">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="1a3b1-143">MAPI Structures</span></span>](mapi-structures.md)

