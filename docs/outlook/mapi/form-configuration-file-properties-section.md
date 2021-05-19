---
title: フォーム構成ファイル [プロパティ] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f31a08ce-3a56-4c90-9502-5bcb09d8d80f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 86d2257b821622094ff8d5ad3a5d7b1bfc74942b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421292"
---
# <a name="form-configuration-file-properties-section"></a><span data-ttu-id="0d198-103">フォーム構成ファイル [プロパティ] セクション</span><span class="sxs-lookup"><span data-stu-id="0d198-103">Form Configuration File [Properties] Section</span></span>

  
  
<span data-ttu-id="0d198-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d198-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d198-105">[ **プロパティ] セクションには** 、フォームが使用して発行するプロパティの完全なセットが一覧表示されます。つまり、MAPI クライアント アプリケーションが列の表示、コンテンツ テーブルのフィルター処理、検索結果フォルダーの設定時に使用できるカスタム メッセージで作成するプロパティです。</span><span class="sxs-lookup"><span data-stu-id="0d198-105">The **[Properties]** section lists the complete set of properties that the form uses and publishes; that is, the properties it creates in its custom messages that MAPI client applications can use when displaying columns, filtering contents tables, setting up search-results folders, and so on.</span></span> <span data-ttu-id="0d198-106">このプロパティ リスト内の各エントリは、後続の **[プロパティ] を参照します。**</span><span class="sxs-lookup"><span data-stu-id="0d198-106">Each entry in this property list references a subsequent **[Property.**</span></span> <span data-ttu-id="0d198-107">_次に_**示すように**、string ] セクションを使用します。</span><span class="sxs-lookup"><span data-stu-id="0d198-107">_string_ **]** section as shown following.</span></span> 
  
 <span data-ttu-id="0d198-108">**[プロパティ]**</span><span class="sxs-lookup"><span data-stu-id="0d198-108">**[Properties]**</span></span>
  
 <span data-ttu-id="0d198-109">**プロパティ。**</span><span class="sxs-lookup"><span data-stu-id="0d198-109">**Property.**</span></span> <span data-ttu-id="0d198-110">_string_  =  _string_</span><span class="sxs-lookup"><span data-stu-id="0d198-110">_string_ =  _string_</span></span>
  
<span data-ttu-id="0d198-111">[ プロパティ] の **形式を指定します。**</span><span class="sxs-lookup"><span data-stu-id="0d198-111">The format of a [ **Property.**</span></span> <span data-ttu-id="0d198-112">_string_]セクションは次の場合です。</span><span class="sxs-lookup"><span data-stu-id="0d198-112">_string_] section is:</span></span> 
  
 <span data-ttu-id="0d198-113">**[プロパティ]**</span><span class="sxs-lookup"><span data-stu-id="0d198-113">**[Property.**</span></span> <span data-ttu-id="0d198-114">_string_ **]**</span><span class="sxs-lookup"><span data-stu-id="0d198-114">_string_ **]**</span></span>
  
 <span data-ttu-id="0d198-115">**型**  =  _integer_</span><span class="sxs-lookup"><span data-stu-id="0d198-115">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="0d198-116">**NmidPropset**  =  _guid_</span><span class="sxs-lookup"><span data-stu-id="0d198-116">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="0d198-117">**NmidString**  =  _string_</span><span class="sxs-lookup"><span data-stu-id="0d198-117">**NmidString** =  _string_</span></span>
  
 <span data-ttu-id="0d198-118">**NmidInteger**  =  _integer_</span><span class="sxs-lookup"><span data-stu-id="0d198-118">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="0d198-119">**DisplayName**  =  _string_</span><span class="sxs-lookup"><span data-stu-id="0d198-119">**DisplayName** =  _string_</span></span>
  
 <span data-ttu-id="0d198-120">**フラグ**  =  _integer_</span><span class="sxs-lookup"><span data-stu-id="0d198-120">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="0d198-121">**SpecialType** = 0|1</span><span class="sxs-lookup"><span data-stu-id="0d198-121">**SpecialType** = 0|1</span></span> 
  
 <span data-ttu-id="0d198-122">**Enum1**  =  _string_</span><span class="sxs-lookup"><span data-stu-id="0d198-122">**Enum1** =  _string_</span></span>
  
<span data-ttu-id="0d198-123">各 **[プロパティ]**</span><span class="sxs-lookup"><span data-stu-id="0d198-123">Each **[Property.**</span></span> <span data-ttu-id="0d198-124">_string_ **] セクション** では、1 つのプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="0d198-124">_string_ **]** section describes a single property.</span></span> <span data-ttu-id="0d198-125">Type **エントリ** は、プロパティの MAPI プロパティの種類 (たとえば、3 (PT_I4) を指定します。</span><span class="sxs-lookup"><span data-stu-id="0d198-125">The **Type** entry specifies the MAPI property type, for example 3 (PT_I4), of the property.</span></span> <span data-ttu-id="0d198-126">**NmidPropset エントリ** はオプションです。NmidString エントリまたは **NmidInteger** エントリと共に **、NmidPropset** エントリはプロパティの名前を指定します。 </span><span class="sxs-lookup"><span data-stu-id="0d198-126">The **NmidPropset** entry is optional; together with either the **NmidString** entry or the **NmidInteger** entry, the **NmidPropset** entry gives the name of the property.</span></span> <span data-ttu-id="0d198-127">**NmidString** はプロパティの名前を指定し **、NmidInteger はプロパティ** の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="0d198-127">**NmidString** gives the name of the property, while **NmidInteger** gives the identifier of the property.</span></span> <span data-ttu-id="0d198-128">**NmidString と** **NmidInteger は** 相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="0d198-128">**NmidString** and **NmidInteger** are mutually exclusive.</span></span> 
  
<span data-ttu-id="0d198-129">設定されている場合 **、NmidPropset には** プロパティ セットの名前が含まれている必要があります。指定しない場合 **、NmidPropset** は次のルールに基づいて既定値に設定されます **。NmidInteger** が存在し、その値が 0x8000 未満の場合 **、NmidPropset** は PS_MAPI に設定されます。</span><span class="sxs-lookup"><span data-stu-id="0d198-129">If set, **NmidPropset** should contain the name of the property set; if absent, **NmidPropset** is set to a default based on the following rule: If **NmidInteger** is present and its value is less than 0x8000, **NmidPropset** is set to PS_MAPI.</span></span> <span data-ttu-id="0d198-130">**NmidInteger** の値が 0x8000 より大きい整数に設定されている場合、または指定しない場合 **、NmidPropset** は PS_PUBLIC_STRINGS に設定されます。</span><span class="sxs-lookup"><span data-stu-id="0d198-130">If the value of **NmidInteger** is set to an integer greater than 0x8000, or if it is absent, **NmidPropset** is set to PS_PUBLIC_STRINGS.</span></span> 
  
<span data-ttu-id="0d198-131">**DisplayName エントリ** には、プロパティのラベルが含まれる。</span><span class="sxs-lookup"><span data-stu-id="0d198-131">The **DisplayName** entry contains the label for the property.</span></span> <span data-ttu-id="0d198-132">**SpecialType エントリ**(存在する場合と 0 以外の場合) は、このプロパティが特別なプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="0d198-132">The **SpecialType** entry, if present and nonzero indicates that this property is a special property.</span></span> <span data-ttu-id="0d198-133">現在、定義されている特殊なプロパティの種類は **SpecialType** = 1 のみです。これは文字列列挙プロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="0d198-133">At present, the only special property type defined is **SpecialType** = 1, which indicates string enumerated properties.</span></span> <span data-ttu-id="0d198-134">**SpecialType が** 1 に設定されている場合 **、Enum1** エントリは **[Enum1] を参照します。**</span><span class="sxs-lookup"><span data-stu-id="0d198-134">If **SpecialType** is set to 1, the **Enum1** entry references the **[Enum1.**</span></span> <span data-ttu-id="0d198-135">_string_ **]** セクション。</span><span class="sxs-lookup"><span data-stu-id="0d198-135">_string_ **]** section.</span></span> 
  
<span data-ttu-id="0d198-136">[プロパティ] セクションと **[プロパティ]** の例を **次に示します。**</span><span class="sxs-lookup"><span data-stu-id="0d198-136">Following is an example of a **[Properties]** section and a **[Properties.**</span></span> <span data-ttu-id="0d198-137">_string_ **]** セクション。</span><span class="sxs-lookup"><span data-stu-id="0d198-137">_string_ **]** section.</span></span> 
  
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

<span data-ttu-id="0d198-138">前 **出の例の Enum1** エントリは、後続の **[Enum1] を参照します。**</span><span class="sxs-lookup"><span data-stu-id="0d198-138">The **Enum1** entry in the preceeding example references to a subsequent **[Enum1.**</span></span> <span data-ttu-id="0d198-139">_string_ **] セクション** で、特定の型の列挙を説明します。</span><span class="sxs-lookup"><span data-stu-id="0d198-139">_string_ **]** section describing an enumeration of a particular type.</span></span> <span data-ttu-id="0d198-140">このような列挙体は、[プロパティ] の最初のプロパティ **を関連付けます。**</span><span class="sxs-lookup"><span data-stu-id="0d198-140">Such an enumeration associates the first property in the **[Property.**</span></span> <span data-ttu-id="0d198-141">_string_ **]** セクションに、インデックスと呼ばれる整数プロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="0d198-141">_string_ **]** section with an integer property, called the index.</span></span> <span data-ttu-id="0d198-142">このような列挙には、表示インデックスペアが想定できる値の一覧も含まれます。</span><span class="sxs-lookup"><span data-stu-id="0d198-142">Such an enumeration also contains a list of the possible values that the display-index pair can assume.</span></span> <span data-ttu-id="0d198-143">列挙体のプロパティの種類を指定する必要は不要です。定義上 **、Enum1** エントリには常に列挙型PT_I4があります。</span><span class="sxs-lookup"><span data-stu-id="0d198-143">Specifying a property type for the enumeration is unnecessary because by definition an **Enum1** entry always has the PT_I4 type.</span></span> <span data-ttu-id="0d198-144">**[Enum1] の形式を指定します。**</span><span class="sxs-lookup"><span data-stu-id="0d198-144">The format for the **[Enum1.**</span></span> <span data-ttu-id="0d198-145">_string_ **] セクション** は次の場合です。</span><span class="sxs-lookup"><span data-stu-id="0d198-145">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="0d198-146">**[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="0d198-146">**[Enum1.**</span></span> <span data-ttu-id="0d198-147">_string_ **]**</span><span class="sxs-lookup"><span data-stu-id="0d198-147">_string_ **]**</span></span>
  
 <span data-ttu-id="0d198-148">**NmidPropset**  =  _guid_</span><span class="sxs-lookup"><span data-stu-id="0d198-148">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="0d198-149">**NmidString**  =  _string_</span><span class="sxs-lookup"><span data-stu-id="0d198-149">**NmidString** =  _string_</span></span>
  
 <span data-ttu-id="0d198-150">**NmidInteger**  =  _integer_</span><span class="sxs-lookup"><span data-stu-id="0d198-150">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="0d198-151">**EnumCount**  =  _integer_</span><span class="sxs-lookup"><span data-stu-id="0d198-151">**EnumCount** =  _integer_</span></span>
  
 <span data-ttu-id="0d198-152">**Val。**</span><span class="sxs-lookup"><span data-stu-id="0d198-152">**Val.**</span></span> <span data-ttu-id="0d198-153">_integer_ **.表示**  =   _文字列_</span><span class="sxs-lookup"><span data-stu-id="0d198-153">_integer_ **.Display** =  _string_</span></span>
  
 <span data-ttu-id="0d198-154">**Val。**</span><span class="sxs-lookup"><span data-stu-id="0d198-154">**Val.**</span></span> <span data-ttu-id="0d198-155">_integer_ **.インデックス**  =   _の整数_</span><span class="sxs-lookup"><span data-stu-id="0d198-155">_integer_ **.Index** =  _integer_</span></span>
  
<span data-ttu-id="0d198-156">次に示すのは、低、中、高の値を指定できる Fire Hazard という名前の列挙プロパティのプロパティ定義の例です。</span><span class="sxs-lookup"><span data-stu-id="0d198-156">The following is an example property definition for an enumerated property named Fire Hazard with possible values of Low, Medium, and High.</span></span>
  
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

 <span data-ttu-id="0d198-157">**[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="0d198-157">**[Enum1.**</span></span> <span data-ttu-id="0d198-158">_string_ **] セクション** は、アプリケーションで、文字列の代わりにインデックスを使用してプロパティのフィルター処理を高速化し、文字列値の英数字の順序とは異なる順序で並べ替えるという 2 つの目的で使用できます。</span><span class="sxs-lookup"><span data-stu-id="0d198-158">_string_ **]** sections can be used by applications for two purposes: to speed up the filtering of properties by using the index instead of the string and to sort by a different order than the alphanumeric order of the string values.</span></span> <span data-ttu-id="0d198-159">たとえば、並べ替えは、高中低の順序ではなく、低中高の順序に基づいて実行できます。</span><span class="sxs-lookup"><span data-stu-id="0d198-159">For example, sorting could be done based on Low-Medium-High order instead of High-Medium-Low order.</span></span> 
  

