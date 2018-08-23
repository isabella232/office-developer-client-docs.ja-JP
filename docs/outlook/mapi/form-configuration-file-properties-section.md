---
title: フォーム構成ファイル [Properties] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f31a08ce-3a56-4c90-9502-5bcb09d8d80f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f25d6b2db00f5629a9bf88499f9f4e080422ac29
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585648"
---
# <a name="form-configuration-file-properties-section"></a><span data-ttu-id="1c68c-103">フォーム構成ファイル [Properties] セクション</span><span class="sxs-lookup"><span data-stu-id="1c68c-103">Form Configuration File [Properties] Section</span></span>

  
  
<span data-ttu-id="1c68c-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c68c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c68c-105">**[プロパティ]** セクションでフォームを使用し、公開のプロパティの完全なセットを一覧表示します。作成し、そのカスタム メッセージを MAPI クライアント アプリケーションのプロパティは、検索結果フォルダーの設定、内容のテーブルのフィルター処理、列を表示するときに使用し、ためにできます。</span><span class="sxs-lookup"><span data-stu-id="1c68c-105">The **[Properties]** section lists the complete set of properties that the form uses and publishes; that is, the properties it creates in its custom messages that MAPI client applications can use when displaying columns, filtering contents tables, setting up search-results folders, and so on.</span></span> <span data-ttu-id="1c68c-106">このプロパティ リスト内の各エントリを参照して、その後 **[プロパティ**。</span><span class="sxs-lookup"><span data-stu-id="1c68c-106">Each entry in this property list references a subsequent **[Property.**</span></span> <span data-ttu-id="1c68c-107">_文字列_**]** のセクションに示すように次のようです。</span><span class="sxs-lookup"><span data-stu-id="1c68c-107">_string_ **]** section as shown following.</span></span> 
  
 <span data-ttu-id="1c68c-108">**[のプロパティ]**</span><span class="sxs-lookup"><span data-stu-id="1c68c-108">**[Properties]**</span></span>
  
 <span data-ttu-id="1c68c-109">**プロパティです。**</span><span class="sxs-lookup"><span data-stu-id="1c68c-109">**Property.**</span></span> <span data-ttu-id="1c68c-110">_文字列_ =  _の文字列_</span><span class="sxs-lookup"><span data-stu-id="1c68c-110">_string_ =  _string_</span></span>
  
<span data-ttu-id="1c68c-111">形式を [**プロパティ**。</span><span class="sxs-lookup"><span data-stu-id="1c68c-111">The format of a [ **Property.**</span></span> <span data-ttu-id="1c68c-112">_文字列_]セクションは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="1c68c-112">_string_] section is:</span></span> 
  
 <span data-ttu-id="1c68c-113">**[プロパティです。**</span><span class="sxs-lookup"><span data-stu-id="1c68c-113">**[Property.**</span></span> <span data-ttu-id="1c68c-114">_文字列_**]**</span><span class="sxs-lookup"><span data-stu-id="1c68c-114">_string_ **]**</span></span>
  
 <span data-ttu-id="1c68c-115">**タイプ** =  _の整数_</span><span class="sxs-lookup"><span data-stu-id="1c68c-115">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="1c68c-116">**NmidPropset** =  _guid_</span><span class="sxs-lookup"><span data-stu-id="1c68c-116">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="1c68c-117">**NmidString** =  _の文字列_</span><span class="sxs-lookup"><span data-stu-id="1c68c-117">**NmidString** =  _string_</span></span>
  
 <span data-ttu-id="1c68c-118">**NmidInteger** =  _の整数_</span><span class="sxs-lookup"><span data-stu-id="1c68c-118">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="1c68c-119">**表示名** =  _の文字列_</span><span class="sxs-lookup"><span data-stu-id="1c68c-119">**DisplayName** =  _string_</span></span>
  
 <span data-ttu-id="1c68c-120">**フラグ** =  _の整数_</span><span class="sxs-lookup"><span data-stu-id="1c68c-120">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="1c68c-121">**SpecialType** = 0 | 1</span><span class="sxs-lookup"><span data-stu-id="1c68c-121">**SpecialType** = 0|1</span></span> 
  
 <span data-ttu-id="1c68c-122">**Enum1** =  _の文字列_</span><span class="sxs-lookup"><span data-stu-id="1c68c-122">**Enum1** =  _string_</span></span>
  
<span data-ttu-id="1c68c-123">各 **[プロパティ**。</span><span class="sxs-lookup"><span data-stu-id="1c68c-123">Each **[Property.**</span></span> <span data-ttu-id="1c68c-124">_文字列_**]** では、1 つのプロパティをについて説明します。</span><span class="sxs-lookup"><span data-stu-id="1c68c-124">_string_ **]** section describes a single property.</span></span> <span data-ttu-id="1c68c-125">**型**指定では、MAPI プロパティの種類、たとえば 3 (PT_I4)、プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="1c68c-125">The **Type** entry specifies the MAPI property type, for example 3 (PT_I4), of the property.</span></span> <span data-ttu-id="1c68c-126">**NmidPropset**エントリは省略可能です。**NmidString**エントリまたは**NmidInteger**エントリのいずれかとは、 **NmidPropset**のエントリは、プロパティの名前を示します。</span><span class="sxs-lookup"><span data-stu-id="1c68c-126">The **NmidPropset** entry is optional; together with either the **NmidString** entry or the **NmidInteger** entry, the **NmidPropset** entry gives the name of the property.</span></span> <span data-ttu-id="1c68c-127">**NmidInteger**プロパティの識別子を使用するときに、 **NmidString**は、プロパティの名前を示します。</span><span class="sxs-lookup"><span data-stu-id="1c68c-127">**NmidString** gives the name of the property, while **NmidInteger** gives the identifier of the property.</span></span> <span data-ttu-id="1c68c-128">**NmidString**と**NmidInteger**は、相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="1c68c-128">**NmidString** and **NmidInteger** are mutually exclusive.</span></span> 
  
<span data-ttu-id="1c68c-129">セット、 **NmidPropset**には、プロパティ セットの名前が含まれている必要がある場合省略すると、 **NmidPropset**は、次のルールに基づいて既定値に設定されている場合: **NmidInteger**が存在し、その値が 0x8000 未満である場合**NmidPropset**が PS_MAPI に設定されています。</span><span class="sxs-lookup"><span data-stu-id="1c68c-129">If set, **NmidPropset** should contain the name of the property set; if absent, **NmidPropset** is set to a default based on the following rule: If **NmidInteger** is present and its value is less than 0x8000, **NmidPropset** is set to PS_MAPI.</span></span> <span data-ttu-id="1c68c-130">**NmidInteger**の値が整数値 0x8000 に割り当てより大きい値に設定されている場合、またはそれが存在しない場合は、 **NmidPropset**が PS_PUBLIC_STRINGS に設定されています。</span><span class="sxs-lookup"><span data-stu-id="1c68c-130">If the value of **NmidInteger** is set to an integer greater than 0x8000, or if it is absent, **NmidPropset** is set to PS_PUBLIC_STRINGS.</span></span> 
  
<span data-ttu-id="1c68c-131">**表示名**のエントリには、プロパティのラベルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="1c68c-131">The **DisplayName** entry contains the label for the property.</span></span> <span data-ttu-id="1c68c-132">**SpecialType**エントリが存在し、0 以外の場合は、このプロパティは、特殊なプロパティであることを示します。</span><span class="sxs-lookup"><span data-stu-id="1c68c-132">The **SpecialType** entry, if present and nonzero indicates that this property is a special property.</span></span> <span data-ttu-id="1c68c-133">現時点で定義されている唯一の特別なプロパティの型は、 **SpecialType** = 1 は、列挙された文字列のプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="1c68c-133">At present, the only special property type defined is **SpecialType** = 1, which indicates string enumerated properties.</span></span> <span data-ttu-id="1c68c-134">**Enum1**エントリを参照して**SpecialType**は、1 に設定されている場合、 **[Enum1 です**。</span><span class="sxs-lookup"><span data-stu-id="1c68c-134">If **SpecialType** is set to 1, the **Enum1** entry references the **[Enum1.**</span></span> <span data-ttu-id="1c68c-135">_文字列_**]** のセクションです。</span><span class="sxs-lookup"><span data-stu-id="1c68c-135">_string_ **]** section.</span></span> 
  
<span data-ttu-id="1c68c-136">以下は、 **[プロパティ]** セクションの例と、 **[のプロパティ**。</span><span class="sxs-lookup"><span data-stu-id="1c68c-136">Following is an example of a **[Properties]** section and a **[Properties.**</span></span> <span data-ttu-id="1c68c-137">_文字列_**]** のセクションです。</span><span class="sxs-lookup"><span data-stu-id="1c68c-137">_string_ **]** section.</span></span> 
  
```cpp
[Properties]
Property.1 = Fire Hazard
Property.2 = Safe
[Property.Fire Hazard]
Type = 1
NmidPropSet = {E47F4480-8400-101B-934D-04021C007002]
NmidString = FireHazard
DisplayName = Fire Hazard
SpecialType = 1
Enum1 = HazardEnum

```

<span data-ttu-id="1c68c-138">上記の例への参照、それ以降の**Enum1**エントリ **[Enum1 です**。</span><span class="sxs-lookup"><span data-stu-id="1c68c-138">The **Enum1** entry in the preceeding example references to a subsequent **[Enum1.**</span></span> <span data-ttu-id="1c68c-139">_文字列_**]** セクションの特定の種類の列挙体を記述します。</span><span class="sxs-lookup"><span data-stu-id="1c68c-139">_string_ **]** section describing an enumeration of a particular type.</span></span> <span data-ttu-id="1c68c-140">このような列挙体の最初のプロパティに関連付ける、 **[プロパティ**。</span><span class="sxs-lookup"><span data-stu-id="1c68c-140">Such an enumeration associates the first property in the **[Property.**</span></span> <span data-ttu-id="1c68c-141">_文字列_**]** のセクションでは、整数型のプロパティにインデックスが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="1c68c-141">_string_ **]** section with an integer property, called the index.</span></span> <span data-ttu-id="1c68c-142">このような列挙体には、表示インデックスのペアを引き受けることが可能な値の一覧も含まれています。</span><span class="sxs-lookup"><span data-stu-id="1c68c-142">Such an enumeration also contains a list of the possible values that the display-index pair can assume.</span></span> <span data-ttu-id="1c68c-143">定義によって**Enum1**エントリは、常に PT_I4 種類がいるために、列挙型のプロパティの種類を指定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="1c68c-143">Specifying a property type for the enumeration is unnecessary because by definition an **Enum1** entry always has the PT_I4 type.</span></span> <span data-ttu-id="1c68c-144">形式、 **[Enum1 です**。</span><span class="sxs-lookup"><span data-stu-id="1c68c-144">The format for the **[Enum1.**</span></span> <span data-ttu-id="1c68c-145">_文字列_**]** のセクションでは。</span><span class="sxs-lookup"><span data-stu-id="1c68c-145">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="1c68c-146">**[Enum1。**</span><span class="sxs-lookup"><span data-stu-id="1c68c-146">**[Enum1.**</span></span> <span data-ttu-id="1c68c-147">_文字列_**]**</span><span class="sxs-lookup"><span data-stu-id="1c68c-147">_string_ **]**</span></span>
  
 <span data-ttu-id="1c68c-148">**NmidPropset** =  _guid_</span><span class="sxs-lookup"><span data-stu-id="1c68c-148">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="1c68c-149">**NmidString** =  _の文字列_</span><span class="sxs-lookup"><span data-stu-id="1c68c-149">**NmidString** =  _string_</span></span>
  
 <span data-ttu-id="1c68c-150">**NmidInteger** =  _の整数_</span><span class="sxs-lookup"><span data-stu-id="1c68c-150">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="1c68c-151">**EnumCount** =  _の整数_</span><span class="sxs-lookup"><span data-stu-id="1c68c-151">**EnumCount** =  _integer_</span></span>
  
 <span data-ttu-id="1c68c-152">**Val 関数です。**</span><span class="sxs-lookup"><span data-stu-id="1c68c-152">**Val.**</span></span> <span data-ttu-id="1c68c-153">_整数_**.表示** =  _の文字列_</span><span class="sxs-lookup"><span data-stu-id="1c68c-153">_integer_ **.Display** =  _string_</span></span>
  
 <span data-ttu-id="1c68c-154">**Val 関数です。**</span><span class="sxs-lookup"><span data-stu-id="1c68c-154">**Val.**</span></span> <span data-ttu-id="1c68c-155">_整数_**.インデックス** =  _の整数_</span><span class="sxs-lookup"><span data-stu-id="1c68c-155">_integer_ **.Index** =  _integer_</span></span>
  
<span data-ttu-id="1c68c-156">火災の危険を低、中、高の値を持つ名前付き列挙型のプロパティのプロパティの定義例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="1c68c-156">The following is an example property definition for an enumerated property named Fire Hazard with possible values of Low, Medium, and High.</span></span>
  
```cpp
[Properties]
Property1 = Fire Hazard
[Enum1.HazardEnum]
IdxNmidPropset={E47F4480-8400-101B-934D-04021C007002]
IdxNmidString=FireHazardEnum
EnumCount = 3
Val.1.Display = Low
Val.1.Index = 1
Val.2.Display = Medium
Val.2.Index = 2
Val.3.Display = High
Val.3.Index = 3

```

 <span data-ttu-id="1c68c-157">**[Enum1。**</span><span class="sxs-lookup"><span data-stu-id="1c68c-157">**[Enum1.**</span></span> <span data-ttu-id="1c68c-158">_文字列_**]** のセクションでは、2 つの目的のアプリケーションで使用することができます: 文字列の代わりに、インデックスを使用して、プロパティのフィルター処理を高速化し、文字列値のアルファベット順とは異なる順序で並べ替えるには。</span><span class="sxs-lookup"><span data-stu-id="1c68c-158">_string_ **]** sections can be used by applications for two purposes: to speed up the filtering of properties by using the index instead of the string and to sort by a different order than the alphanumeric order of the string values.</span></span> <span data-ttu-id="1c68c-159">たとえば、並べ替え行います高-低の順序ではなく、低、中、高順に基づいて。</span><span class="sxs-lookup"><span data-stu-id="1c68c-159">For example, sorting could be done based on Low-Medium-High order instead of High-Medium-Low order.</span></span> 
  

