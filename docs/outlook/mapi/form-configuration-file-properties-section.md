---
title: フォーム構成ファイル [Properties] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f31a08ce-3a56-4c90-9502-5bcb09d8d80f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 86d2257b821622094ff8d5ad3a5d7b1bfc74942b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328106"
---
# <a name="form-configuration-file-properties-section"></a><span data-ttu-id="b4e26-103">フォーム構成ファイル [Properties] セクション</span><span class="sxs-lookup"><span data-stu-id="b4e26-103">Form Configuration File [Properties] Section</span></span>

  
  
<span data-ttu-id="b4e26-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4e26-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4e26-105">**[properties]** セクションには、フォームが使用および発行するプロパティの完全なセットがリストされています。これは、MAPI クライアントアプリケーションが列の表示、コンテンツテーブルのフィルター処理、検索結果フォルダーの設定を行うときに使用できる、カスタムメッセージ内に作成されるプロパティです。</span><span class="sxs-lookup"><span data-stu-id="b4e26-105">The **[Properties]** section lists the complete set of properties that the form uses and publishes; that is, the properties it creates in its custom messages that MAPI client applications can use when displaying columns, filtering contents tables, setting up search-results folders, and so on.</span></span> <span data-ttu-id="b4e26-106">このプロパティリストの各エントリは、後続の **[プロパティを参照します。**</span><span class="sxs-lookup"><span data-stu-id="b4e26-106">Each entry in this property list references a subsequent **[Property.**</span></span> <span data-ttu-id="b4e26-107">_文字列_**]** セクションは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="b4e26-107">_string_ **]** section as shown following.</span></span> 
  
 <span data-ttu-id="b4e26-108">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="b4e26-108">**[Properties]**</span></span>
  
 <span data-ttu-id="b4e26-109">**プロパティ.**</span><span class="sxs-lookup"><span data-stu-id="b4e26-109">**Property.**</span></span> <span data-ttu-id="b4e26-110">_文字列_ =  _文字列_</span><span class="sxs-lookup"><span data-stu-id="b4e26-110">_string_ =  _string_</span></span>
  
<span data-ttu-id="b4e26-111">[プロパティ] の形式 **。**</span><span class="sxs-lookup"><span data-stu-id="b4e26-111">The format of a [ **Property.**</span></span> <span data-ttu-id="b4e26-112">_string_]セクションは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b4e26-112">_string_] section is:</span></span> 
  
 <span data-ttu-id="b4e26-113">**プロパティ.**</span><span class="sxs-lookup"><span data-stu-id="b4e26-113">**[Property.**</span></span> <span data-ttu-id="b4e26-114">_文字列_**]**</span><span class="sxs-lookup"><span data-stu-id="b4e26-114">_string_ **]**</span></span>
  
 <span data-ttu-id="b4e26-115">\*\*\*\* =  _整数_型</span><span class="sxs-lookup"><span data-stu-id="b4e26-115">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="b4e26-116">**NmidPropset** =  _guid_</span><span class="sxs-lookup"><span data-stu-id="b4e26-116">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="b4e26-117">**nmidstring** =  _文字列_</span><span class="sxs-lookup"><span data-stu-id="b4e26-117">**NmidString** =  _string_</span></span>
  
 <span data-ttu-id="b4e26-118">**nmidinteger** =  _整数_</span><span class="sxs-lookup"><span data-stu-id="b4e26-118">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="b4e26-119">**DisplayName** =  _文字列_</span><span class="sxs-lookup"><span data-stu-id="b4e26-119">**DisplayName** =  _string_</span></span>
  
 <span data-ttu-id="b4e26-120">**Flags** =  _整数_</span><span class="sxs-lookup"><span data-stu-id="b4e26-120">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="b4e26-121">特別の**種類**= 0 | 1</span><span class="sxs-lookup"><span data-stu-id="b4e26-121">**SpecialType** = 0|1</span></span> 
  
 <span data-ttu-id="b4e26-122">**Enum1** =  _文字列_</span><span class="sxs-lookup"><span data-stu-id="b4e26-122">**Enum1** =  _string_</span></span>
  
<span data-ttu-id="b4e26-123">各 **[Property.**</span><span class="sxs-lookup"><span data-stu-id="b4e26-123">Each **[Property.**</span></span> <span data-ttu-id="b4e26-124">_文字列_**]** セクションでは、1つのプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="b4e26-124">_string_ **]** section describes a single property.</span></span> <span data-ttu-id="b4e26-125">**type**エントリは、プロパティの MAPI プロパティの種類 (例: 3 (PT_I4)) を指定します。</span><span class="sxs-lookup"><span data-stu-id="b4e26-125">The **Type** entry specifies the MAPI property type, for example 3 (PT_I4), of the property.</span></span> <span data-ttu-id="b4e26-126">**NmidPropset**エントリは省略可能です。**nmidstring**エントリまたは**nmidstring**エントリのいずれかと共に、 **NmidPropset**エントリはプロパティの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="b4e26-126">The **NmidPropset** entry is optional; together with either the **NmidString** entry or the **NmidInteger** entry, the **NmidPropset** entry gives the name of the property.</span></span> <span data-ttu-id="b4e26-127">**nmidstring**はプロパティの名前を指定し、 **nmidstring**はプロパティの識別子を示します。</span><span class="sxs-lookup"><span data-stu-id="b4e26-127">**NmidString** gives the name of the property, while **NmidInteger** gives the identifier of the property.</span></span> <span data-ttu-id="b4e26-128">**nmidstring**と**nmidstring**は相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="b4e26-128">**NmidString** and **NmidInteger** are mutually exclusive.</span></span> 
  
<span data-ttu-id="b4e26-129">設定されている場合、 **NmidPropset**にはプロパティセットの名前を指定する必要があります。存在しない場合、 **NmidPropset**は次のルールに基づいて既定値に設定されます。 **nmidinteger**が存在し、その値が0x8000 未満の場合、 **NmidPropset**は PS_MAPI に設定されます。</span><span class="sxs-lookup"><span data-stu-id="b4e26-129">If set, **NmidPropset** should contain the name of the property set; if absent, **NmidPropset** is set to a default based on the following rule: If **NmidInteger** is present and its value is less than 0x8000, **NmidPropset** is set to PS_MAPI.</span></span> <span data-ttu-id="b4e26-130">**nmidinteger**の値が0x8000 を超える整数に設定されている場合、または存在しない場合、 **NmidPropset**は PS_PUBLIC_STRINGS に設定されます。</span><span class="sxs-lookup"><span data-stu-id="b4e26-130">If the value of **NmidInteger** is set to an integer greater than 0x8000, or if it is absent, **NmidPropset** is set to PS_PUBLIC_STRINGS.</span></span> 
  
<span data-ttu-id="b4e26-131">**DisplayName**エントリには、プロパティのラベルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b4e26-131">The **DisplayName** entry contains the label for the property.</span></span> <span data-ttu-id="b4e26-132">特別な**種類**のエントリ (存在する場合)、非ゼロの場合は、このプロパティが特別なプロパティであることを示します。</span><span class="sxs-lookup"><span data-stu-id="b4e26-132">The **SpecialType** entry, if present and nonzero indicates that this property is a special property.</span></span> <span data-ttu-id="b4e26-133">現時点では、唯一定義されている\*\*\*\* 特別なプロパティの型は、文字列列挙型のプロパティを示す、指定された特別なプロパティの種類です。</span><span class="sxs-lookup"><span data-stu-id="b4e26-133">At present, the only special property type defined is **SpecialType** = 1, which indicates string enumerated properties.</span></span> <span data-ttu-id="b4e26-134">特別な**type**が1に設定されている場合、 **Enum1**エントリは [Enum1] を参照し**ます。**</span><span class="sxs-lookup"><span data-stu-id="b4e26-134">If **SpecialType** is set to 1, the **Enum1** entry references the **[Enum1.**</span></span> <span data-ttu-id="b4e26-135">_文字列_**]** セクション</span><span class="sxs-lookup"><span data-stu-id="b4e26-135">_string_ **]** section.</span></span> 
  
<span data-ttu-id="b4e26-136">**[properties]** セクションと [properties] の例を次に示し**ます。**</span><span class="sxs-lookup"><span data-stu-id="b4e26-136">Following is an example of a **[Properties]** section and a **[Properties.**</span></span> <span data-ttu-id="b4e26-137">_文字列_**]** セクション</span><span class="sxs-lookup"><span data-stu-id="b4e26-137">_string_ **]** section.</span></span> 
  
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

<span data-ttu-id="b4e26-138">前の例の**Enum1**エントリは、以降の [Enum1 を参照し**ます。**</span><span class="sxs-lookup"><span data-stu-id="b4e26-138">The **Enum1** entry in the preceeding example references to a subsequent **[Enum1.**</span></span> <span data-ttu-id="b4e26-139">_文字列_**]** を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b4e26-139">_string_ **]** section describing an enumeration of a particular type.</span></span> <span data-ttu-id="b4e26-140">このような列挙は、[property の最初のプロパティを関連付け**ます。**</span><span class="sxs-lookup"><span data-stu-id="b4e26-140">Such an enumeration associates the first property in the **[Property.**</span></span> <span data-ttu-id="b4e26-141">_文字列_**]** セクションで、インデックスと呼ばれる整数のプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="b4e26-141">_string_ **]** section with an integer property, called the index.</span></span> <span data-ttu-id="b4e26-142">この列挙型には、表示インデックスのペアが想定できる値の一覧も含まれています。</span><span class="sxs-lookup"><span data-stu-id="b4e26-142">Such an enumeration also contains a list of the possible values that the display-index pair can assume.</span></span> <span data-ttu-id="b4e26-143">**Enum1**エントリには常に PT_I4 型が指定されているため、列挙のプロパティの種類を指定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="b4e26-143">Specifying a property type for the enumeration is unnecessary because by definition an **Enum1** entry always has the PT_I4 type.</span></span> <span data-ttu-id="b4e26-144">**[Enum1**の形式。</span><span class="sxs-lookup"><span data-stu-id="b4e26-144">The format for the **[Enum1.**</span></span> <span data-ttu-id="b4e26-145">_文字列_**]** セクションは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b4e26-145">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="b4e26-146">**[Enum1**</span><span class="sxs-lookup"><span data-stu-id="b4e26-146">**[Enum1.**</span></span> <span data-ttu-id="b4e26-147">_文字列_**]**</span><span class="sxs-lookup"><span data-stu-id="b4e26-147">_string_ **]**</span></span>
  
 <span data-ttu-id="b4e26-148">**NmidPropset** =  _guid_</span><span class="sxs-lookup"><span data-stu-id="b4e26-148">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="b4e26-149">**nmidstring** =  _文字列_</span><span class="sxs-lookup"><span data-stu-id="b4e26-149">**NmidString** =  _string_</span></span>
  
 <span data-ttu-id="b4e26-150">**nmidinteger** =  _整数_</span><span class="sxs-lookup"><span data-stu-id="b4e26-150">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="b4e26-151">**enumcount** =  _整数_</span><span class="sxs-lookup"><span data-stu-id="b4e26-151">**EnumCount** =  _integer_</span></span>
  
 <span data-ttu-id="b4e26-152">**long.**</span><span class="sxs-lookup"><span data-stu-id="b4e26-152">**Val.**</span></span> <span data-ttu-id="b4e26-153">_整数型_**.表示** =  _文字列_</span><span class="sxs-lookup"><span data-stu-id="b4e26-153">_integer_ **.Display** =  _string_</span></span>
  
 <span data-ttu-id="b4e26-154">**long.**</span><span class="sxs-lookup"><span data-stu-id="b4e26-154">**Val.**</span></span> <span data-ttu-id="b4e26-155">_整数型_**.インデックス** =  _整数_</span><span class="sxs-lookup"><span data-stu-id="b4e26-155">_integer_ **.Index** =  _integer_</span></span>
  
<span data-ttu-id="b4e26-156">次に示すのは、低、中、高の可能な値を持つ、"Fire 危険" という名前の列挙プロパティのプロパティ定義の例です。</span><span class="sxs-lookup"><span data-stu-id="b4e26-156">The following is an example property definition for an enumerated property named Fire Hazard with possible values of Low, Medium, and High.</span></span>
  
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

 <span data-ttu-id="b4e26-157">**[Enum1**</span><span class="sxs-lookup"><span data-stu-id="b4e26-157">**[Enum1.**</span></span> <span data-ttu-id="b4e26-158">_文字列_**]** セクションは、次の2つの目的でアプリケーションによって使用されます。プロパティのフィルター処理を高速化するには、文字列の代わりにインデックスを使用し、文字列値のアルファベット順とは異なる順序で並べ替えます。</span><span class="sxs-lookup"><span data-stu-id="b4e26-158">_string_ **]** sections can be used by applications for two purposes: to speed up the filtering of properties by using the index instead of the string and to sort by a different order than the alphanumeric order of the string values.</span></span> <span data-ttu-id="b4e26-159">たとえば、高-中-低の順序ではなく、低中-高の順序に基づいて並べ替えを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="b4e26-159">For example, sorting could be done based on Low-Medium-High order instead of High-Medium-Low order.</span></span> 
  

