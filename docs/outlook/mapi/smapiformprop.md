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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4e8e2474d2adb882dd0ba43aeb0d8b05044a6ce6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592060"
---
# <a name="smapiformprop"></a><span data-ttu-id="f1ef1-103">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="f1ef1-103">SMAPIFormProp</span></span>

  
  
<span data-ttu-id="f1ef1-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1ef1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1ef1-105">フォームで使用される名前付きプロパティをについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f1ef1-105">Describes a named property used with a form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f1ef1-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="f1ef1-106">Header file:</span></span>  <br/> |<span data-ttu-id="f1ef1-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="f1ef1-107">Mapiform.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="f1ef1-108">Members</span><span class="sxs-lookup"><span data-stu-id="f1ef1-108">Members</span></span>

 <span data-ttu-id="f1ef1-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="f1ef1-109">**ulFlags**</span></span>
  
> <span data-ttu-id="f1ef1-110">**SMAPIFormProp**構造体の文字列の形式を識別するために使用するフラグ。</span><span class="sxs-lookup"><span data-stu-id="f1ef1-110">Flags used to distinguish the format of the strings in the **SMAPIFormProp** structure.</span></span> <span data-ttu-id="f1ef1-111">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="f1ef1-111">The following flag can be set:</span></span> 
    
<span data-ttu-id="f1ef1-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f1ef1-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f1ef1-113">返される文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="f1ef1-113">The strings returned are in Unicode format.</span></span> <span data-ttu-id="f1ef1-114">MAPI_UNICODE が設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="f1ef1-114">If MAPI_UNICODE is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="f1ef1-115">**nPropType**</span><span class="sxs-lookup"><span data-stu-id="f1ef1-115">**nPropType**</span></span>
  
> <span data-ttu-id="f1ef1-116">0 に設定する最も重要な単語を名前付きプロパティの型。</span><span class="sxs-lookup"><span data-stu-id="f1ef1-116">Type of the named property, with the most significant word set to zero.</span></span> 
    
 <span data-ttu-id="f1ef1-117">**nmid**</span><span class="sxs-lookup"><span data-stu-id="f1ef1-117">**nmid**</span></span>
  
> <span data-ttu-id="f1ef1-118">インターフェイス識別子およびフォーム名を表すプロパティ セットが、数値または文字列の値を識別する**GUID**構造体を含む名前付きプロパティの名前です。</span><span class="sxs-lookup"><span data-stu-id="f1ef1-118">Name for the named property, which includes a **GUID** structure identifying the property set and either a numeric or string value that represents an interface identifier and form name.</span></span> 
    
 <span data-ttu-id="f1ef1-119">**pszDisplayName**</span><span class="sxs-lookup"><span data-stu-id="f1ef1-119">**pszDisplayName**</span></span>
  
> <span data-ttu-id="f1ef1-120">名前付きプロパティの表示名へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f1ef1-120">Pointer to the display name of the named property.</span></span>
    
 <span data-ttu-id="f1ef1-121">**nSpecialType**</span><span class="sxs-lookup"><span data-stu-id="f1ef1-121">**nSpecialType**</span></span>
  
> <span data-ttu-id="f1ef1-122">**U**メンバーに含まれるデータの種類を示す数値です。</span><span class="sxs-lookup"><span data-stu-id="f1ef1-122">Value describing the type of data included in the **u** member.</span></span> <span data-ttu-id="f1ef1-123">使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f1ef1-123">Possible values are as follows:</span></span> 
    
<span data-ttu-id="f1ef1-124">FPST_VANILLA</span><span class="sxs-lookup"><span data-stu-id="f1ef1-124">FPST_VANILLA</span></span> 
  
> <span data-ttu-id="f1ef1-125">**U**のメンバーは、列挙体には含まれません。</span><span class="sxs-lookup"><span data-stu-id="f1ef1-125">The **u** member does not contain an enumeration.</span></span> 
    
<span data-ttu-id="f1ef1-126">FPST_ENUM_PROP</span><span class="sxs-lookup"><span data-stu-id="f1ef1-126">FPST_ENUM_PROP</span></span> 
  
> <span data-ttu-id="f1ef1-127">**U**のメンバーには、列挙体を記述する構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f1ef1-127">The **u** member contains a structure that describes an enumeration.</span></span> 
    
 <span data-ttu-id="f1ef1-128">**u**</span><span class="sxs-lookup"><span data-stu-id="f1ef1-128">**u**</span></span>
  
> <span data-ttu-id="f1ef1-129">共用体の名前と、名前付きプロパティの数の間の関連付けを記述します。</span><span class="sxs-lookup"><span data-stu-id="f1ef1-129">Union describing the association between the name and number of the named property.</span></span> <span data-ttu-id="f1ef1-130">いくつかのプロパティを使用すると、空では、 **u**のメンバーです。</span><span class="sxs-lookup"><span data-stu-id="f1ef1-130">By using some properties, the **u** member is empty.</span></span> <span data-ttu-id="f1ef1-131">他のプロパティでは、次のメンバーで構成される構造体で表されます。</span><span class="sxs-lookup"><span data-stu-id="f1ef1-131">With other properties, it is represented in a structure consisting of the following members:</span></span> 
    
 <span data-ttu-id="f1ef1-132">**nmidIdx**</span><span class="sxs-lookup"><span data-stu-id="f1ef1-132">**nmidIdx**</span></span>
  
> <span data-ttu-id="f1ef1-133">プロパティ セットと名前付きプロパティの識別子を含む[MAPINAMEID](mapinameid.md)構造体です。</span><span class="sxs-lookup"><span data-stu-id="f1ef1-133">The [MAPINAMEID](mapinameid.md) structure that contains the property set and identifier for the named property.</span></span> 
    
 <span data-ttu-id="f1ef1-134">**cfpevAvailable**</span><span class="sxs-lookup"><span data-stu-id="f1ef1-134">**cfpevAvailable**</span></span>
  
> <span data-ttu-id="f1ef1-135">**PfpevAvailable**メンバーが指す配列内の[SMAPIFormPropEnumVal](smapiformpropenumval.md)構造体の数です。</span><span class="sxs-lookup"><span data-stu-id="f1ef1-135">Count of [SMAPIFormPropEnumVal](smapiformpropenumval.md) structures in the array pointed to by the **pfpevAvailable** member.</span></span> 
    
 <span data-ttu-id="f1ef1-136">**pfpevAvailable**</span><span class="sxs-lookup"><span data-stu-id="f1ef1-136">**pfpevAvailable**</span></span>
  
> <span data-ttu-id="f1ef1-137">それぞれの名前付きプロパティの値を保持する**SMAPIFormPropEnumVal**構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f1ef1-137">Pointer to an array of **SMAPIFormPropEnumVal** structures, each of which holds a value for the named property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f1ef1-138">注釈</span><span class="sxs-lookup"><span data-stu-id="f1ef1-138">Remarks</span></span>

<span data-ttu-id="f1ef1-139">**SMAPIFormProp**構造体には、 [IMAPIFormInfo](imapiforminfoimapiprop.md)インターフェイスの定義の一部として使用されるフォームのプロパティに関する情報が含まれています。**nSpecialType**には、 **SMAPIFormProp**の一部である**u**の和集合に適用されるタグが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f1ef1-139">The **SMAPIFormProp** structure contains information about a form property used as part of the definitions of the [IMAPIFormInfo](imapiforminfoimapiprop.md) interface; **nSpecialType** contains a tag that applies to the **u** union that is part of **SMAPIFormProp**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f1ef1-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="f1ef1-140">See also</span></span>



[<span data-ttu-id="f1ef1-141">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="f1ef1-141">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="f1ef1-142">SMAPIFormPropEnumVal</span><span class="sxs-lookup"><span data-stu-id="f1ef1-142">SMAPIFormPropEnumVal</span></span>](smapiformpropenumval.md)


[<span data-ttu-id="f1ef1-143">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="f1ef1-143">MAPI Structures</span></span>](mapi-structures.md)

