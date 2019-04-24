---
title: SPropValue
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropValue
api_type:
- COM
ms.assetid: faf795a2-84db-432d-a05f-082f25a5cab5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c7f4e8835831af6277cef134bf3961e9928cba33
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326587"
---
# <a name="spropvalue"></a><span data-ttu-id="0947a-103">SPropValue</span><span class="sxs-lookup"><span data-stu-id="0947a-103">SPropValue</span></span>

  
  
<span data-ttu-id="0947a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0947a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0947a-105">MAPI プロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="0947a-105">Describes a MAPI property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0947a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0947a-106">Header file:</span></span>  <br/> |<span data-ttu-id="0947a-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0947a-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0947a-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="0947a-108">Related macros:</span></span>  <br/> |<span data-ttu-id="0947a-109">[CHANGE_PROP_TYPE](change_prop_type.md)、 [MVI_PROP](mvi_prop.md)、 [PROP_ID](prop_id.md)、 [PROP_TAG](prop_tag.md)、 [PROP_TYPE](prop_type.md)</span><span class="sxs-lookup"><span data-stu-id="0947a-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span></span> <br/> |
   
```cpp
typedef struct _SPropValue
{
  ULONG ulPropTag;
  ULONG dwAlignPad;
  union _PV Value;
} SPropValue, FAR *LPSPropValue;

```

## <a name="members"></a><span data-ttu-id="0947a-110">Members</span><span class="sxs-lookup"><span data-stu-id="0947a-110">Members</span></span>

 <span data-ttu-id="0947a-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="0947a-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="0947a-112">プロパティのプロパティタグ。</span><span class="sxs-lookup"><span data-stu-id="0947a-112">Property tag for the property.</span></span> <span data-ttu-id="0947a-113">property タグは、上位16ビットのプロパティの一意の識別子と、下位16ビットのプロパティの型で構成される、32ビットの符号なし整数です。</span><span class="sxs-lookup"><span data-stu-id="0947a-113">Property tags are 32-bit unsigned integers consisting of the property's unique identifier in the high-order 16 bits and the property's type in the low-order 16 bits.</span></span>
    
 <span data-ttu-id="0947a-114">**dwAlignPad**</span><span class="sxs-lookup"><span data-stu-id="0947a-114">**dwAlignPad**</span></span>
  
> <span data-ttu-id="0947a-115">MAPI 用に予約済み。を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="0947a-115">Reserved for MAPI; do not use.</span></span> 
    
 <span data-ttu-id="0947a-116">**値**</span><span class="sxs-lookup"><span data-stu-id="0947a-116">**Value**</span></span>
  
> <span data-ttu-id="0947a-117">データ値の和集合。プロパティの型によって指定される特定の値。</span><span class="sxs-lookup"><span data-stu-id="0947a-117">Union of data values, the specific value dictated by the property type.</span></span> <span data-ttu-id="0947a-118">次の表に、使用する必要がある結合のメンバーと、関連付けられたデータ型について、各プロパティの種類の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="0947a-118">The following table lists for each property type, the member of the union that should be used and its associated data type.</span></span>
    
|<span data-ttu-id="0947a-119">**プロパティの種類**</span><span class="sxs-lookup"><span data-stu-id="0947a-119">**Property type**</span></span>|<span data-ttu-id="0947a-120">**値**</span><span class="sxs-lookup"><span data-stu-id="0947a-120">**Value**</span></span>|<span data-ttu-id="0947a-121">**値のデータ型**</span><span class="sxs-lookup"><span data-stu-id="0947a-121">**Data type of Value**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0947a-122">PT_I2 または PT_SHORT</span><span class="sxs-lookup"><span data-stu-id="0947a-122">PT_I2 or PT_SHORT</span></span>  <br/> |<span data-ttu-id="0947a-123">**i**</span><span class="sxs-lookup"><span data-stu-id="0947a-123">**i**</span></span> <br/> |<span data-ttu-id="0947a-124">short int</span><span class="sxs-lookup"><span data-stu-id="0947a-124">short int</span></span>  <br/> |
|<span data-ttu-id="0947a-125">PT_I4 または PT_LONG (署名済み)</span><span class="sxs-lookup"><span data-stu-id="0947a-125">PT_I4 or PT_LONG (signed)</span></span>  <br/> |<span data-ttu-id="0947a-126">**l**</span><span class="sxs-lookup"><span data-stu-id="0947a-126">**l**</span></span> <br/> |<span data-ttu-id="0947a-127">l</span><span class="sxs-lookup"><span data-stu-id="0947a-127">LONG</span></span>  <br/> |
|<span data-ttu-id="0947a-128">PT_I4 または PT_LONG (署名なし)</span><span class="sxs-lookup"><span data-stu-id="0947a-128">PT_I4 or PT_LONG (unsigned)</span></span>  <br/> |<span data-ttu-id="0947a-129">**ul**</span><span class="sxs-lookup"><span data-stu-id="0947a-129">**ul**</span></span> <br/> |<span data-ttu-id="0947a-130">ULONG</span><span class="sxs-lookup"><span data-stu-id="0947a-130">ULONG</span></span>  <br/> |
|<span data-ttu-id="0947a-131">PT_R4 または PT_FLOAT</span><span class="sxs-lookup"><span data-stu-id="0947a-131">PT_R4 or PT_FLOAT</span></span>  <br/> |<span data-ttu-id="0947a-132">**flt**</span><span class="sxs-lookup"><span data-stu-id="0947a-132">**flt**</span></span> <br/> |<span data-ttu-id="0947a-133">浮動小数点数</span><span class="sxs-lookup"><span data-stu-id="0947a-133">float</span></span>  <br/> |
|<span data-ttu-id="0947a-134">PT_R8 または PT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="0947a-134">PT_R8 or PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="0947a-135">**click**</span><span class="sxs-lookup"><span data-stu-id="0947a-135">**dbl**</span></span> <br/> |<span data-ttu-id="0947a-136">double</span><span class="sxs-lookup"><span data-stu-id="0947a-136">double</span></span>  <br/> |
|<span data-ttu-id="0947a-137">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="0947a-137">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="0947a-138">**b**</span><span class="sxs-lookup"><span data-stu-id="0947a-138">**b**</span></span> <br/> |<span data-ttu-id="0947a-139">符号なし short int</span><span class="sxs-lookup"><span data-stu-id="0947a-139">unsigned short int</span></span>  <br/> |
|<span data-ttu-id="0947a-140">PT_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="0947a-140">PT_CURRENCY</span></span>  <br/> |<span data-ttu-id="0947a-141">**.cur**</span><span class="sxs-lookup"><span data-stu-id="0947a-141">**cur**</span></span> <br/> |[<span data-ttu-id="0947a-142">単位</span><span class="sxs-lookup"><span data-stu-id="0947a-142">CURRENCY</span></span>](currency.md) <br/> |
|<span data-ttu-id="0947a-143">PT_APPTIME</span><span class="sxs-lookup"><span data-stu-id="0947a-143">PT_APPTIME</span></span>  <br/> |<span data-ttu-id="0947a-144">**下部**</span><span class="sxs-lookup"><span data-stu-id="0947a-144">**at**</span></span> <br/> |<span data-ttu-id="0947a-145">double</span><span class="sxs-lookup"><span data-stu-id="0947a-145">double</span></span>  <br/> |
|<span data-ttu-id="0947a-146">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="0947a-146">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="0947a-147">**cm**</span><span class="sxs-lookup"><span data-stu-id="0947a-147">**ft**</span></span> <br/> |[<span data-ttu-id="0947a-148">FILETIME</span><span class="sxs-lookup"><span data-stu-id="0947a-148">FILETIME</span></span>](filetime.md) <br/> |
|<span data-ttu-id="0947a-149">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="0947a-149">PT_STRING8</span></span>  <br/> |<span data-ttu-id="0947a-150">**lpszA**</span><span class="sxs-lookup"><span data-stu-id="0947a-150">**lpszA**</span></span> <br/> |<span data-ttu-id="0947a-151">LPSTR</span><span class="sxs-lookup"><span data-stu-id="0947a-151">LPSTR</span></span>  <br/> |
|<span data-ttu-id="0947a-152">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0947a-152">PT_BINARY</span></span>  <br/> |<span data-ttu-id="0947a-153">**在庫**</span><span class="sxs-lookup"><span data-stu-id="0947a-153">**bin**</span></span> <br/> |<span data-ttu-id="0947a-154">BYTE [配列]</span><span class="sxs-lookup"><span data-stu-id="0947a-154">BYTE [array]</span></span>  <br/> |
|<span data-ttu-id="0947a-155">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0947a-155">PT_UNICODE</span></span>  <br/> |<span data-ttu-id="0947a-156">**lpszw**</span><span class="sxs-lookup"><span data-stu-id="0947a-156">**lpszW**</span></span> <br/> |<span data-ttu-id="0947a-157">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="0947a-157">LPWSTR</span></span>  <br/> |
|<span data-ttu-id="0947a-158">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="0947a-158">PT_CLSID</span></span>  <br/> |<span data-ttu-id="0947a-159">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="0947a-159">**lpguid**</span></span> <br/> |<span data-ttu-id="0947a-160">lpguid</span><span class="sxs-lookup"><span data-stu-id="0947a-160">LPGUID</span></span>  <br/> |
|<span data-ttu-id="0947a-161">PT_I8 または PT_LONGLONG</span><span class="sxs-lookup"><span data-stu-id="0947a-161">PT_I8 or PT_LONGLONG</span></span>  <br/> |<span data-ttu-id="0947a-162">**&**</span><span class="sxs-lookup"><span data-stu-id="0947a-162">**li**</span></span> <br/> |<span data-ttu-id="0947a-163">**LARGE_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="0947a-163">**LARGE_INTEGER**</span></span> <br/> |
|<span data-ttu-id="0947a-164">PT_MV_I2</span><span class="sxs-lookup"><span data-stu-id="0947a-164">PT_MV_I2</span></span>  <br/> |<span data-ttu-id="0947a-165">**mvi**</span><span class="sxs-lookup"><span data-stu-id="0947a-165">**MVi**</span></span> <br/> |[<span data-ttu-id="0947a-166">SShortArray</span><span class="sxs-lookup"><span data-stu-id="0947a-166">SShortArray</span></span>](sshortarray.md) <br/> |
|<span data-ttu-id="0947a-167">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="0947a-167">PT_MV_LONG</span></span>  <br/> |<span data-ttu-id="0947a-168">**mvi**</span><span class="sxs-lookup"><span data-stu-id="0947a-168">**MVI**</span></span> <br/> |[<span data-ttu-id="0947a-169">SLongArray</span><span class="sxs-lookup"><span data-stu-id="0947a-169">SLongArray</span></span>](slongarray.md) <br/> |
|<span data-ttu-id="0947a-170">PT_MV_R4</span><span class="sxs-lookup"><span data-stu-id="0947a-170">PT_MV_R4</span></span>  <br/> |<span data-ttu-id="0947a-171">**MVflt**</span><span class="sxs-lookup"><span data-stu-id="0947a-171">**MVflt**</span></span> <br/> |[<span data-ttu-id="0947a-172">SRealArray</span><span class="sxs-lookup"><span data-stu-id="0947a-172">SRealArray</span></span>](srealarray.md) <br/> |
|<span data-ttu-id="0947a-173">PT_MV_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="0947a-173">PT_MV_DOUBLE</span></span>  <br/> |<span data-ttu-id="0947a-174">**MVdbl**</span><span class="sxs-lookup"><span data-stu-id="0947a-174">**MVdbl**</span></span> <br/> |[<span data-ttu-id="0947a-175">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="0947a-175">SDoubleArray</span></span>](sdoublearray.md) <br/> |
|<span data-ttu-id="0947a-176">PT_MV_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="0947a-176">PT_MV_CURRENCY</span></span>  <br/> |<span data-ttu-id="0947a-177">**MVcur**</span><span class="sxs-lookup"><span data-stu-id="0947a-177">**MVcur**</span></span> <br/> |[<span data-ttu-id="0947a-178">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="0947a-178">SCurrencyArray</span></span>](scurrencyarray.md) <br/> |
|<span data-ttu-id="0947a-179">PT_MV_APPTIME</span><span class="sxs-lookup"><span data-stu-id="0947a-179">PT_MV_APPTIME</span></span>  <br/> |<span data-ttu-id="0947a-180">**mvat**</span><span class="sxs-lookup"><span data-stu-id="0947a-180">**MVat**</span></span> <br/> |[<span data-ttu-id="0947a-181">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="0947a-181">SAppTimeArray</span></span>](sapptimearray.md) <br/> |
|<span data-ttu-id="0947a-182">PT_MV_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="0947a-182">PT_MV_SYSTIME</span></span>  <br/> |<span data-ttu-id="0947a-183">**MVft**</span><span class="sxs-lookup"><span data-stu-id="0947a-183">**MVft**</span></span> <br/> |[<span data-ttu-id="0947a-184">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="0947a-184">SDateTimeArray</span></span>](sdatetimearray.md) <br/> |
|<span data-ttu-id="0947a-185">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="0947a-185">PT_MV_BINARY</span></span>  <br/> |<span data-ttu-id="0947a-186">**mvbin**</span><span class="sxs-lookup"><span data-stu-id="0947a-186">**MVbin**</span></span> <br/> |[<span data-ttu-id="0947a-187">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="0947a-187">SBinaryArray</span></span>](sbinaryarray.md) <br/> |
|<span data-ttu-id="0947a-188">PT_MV_STRING8</span><span class="sxs-lookup"><span data-stu-id="0947a-188">PT_MV_STRING8</span></span>  <br/> |<span data-ttu-id="0947a-189">**MVszA**</span><span class="sxs-lookup"><span data-stu-id="0947a-189">**MVszA**</span></span> <br/> |[<span data-ttu-id="0947a-190">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="0947a-190">SLPSTRArray</span></span>](slpstrarray.md) <br/> |
|<span data-ttu-id="0947a-191">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0947a-191">PT_MV_UNICODE</span></span>  <br/> |<span data-ttu-id="0947a-192">**MVszW**</span><span class="sxs-lookup"><span data-stu-id="0947a-192">**MVszW**</span></span> <br/> |[<span data-ttu-id="0947a-193">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="0947a-193">SWStringArray</span></span>](swstringarray.md) <br/> |
|<span data-ttu-id="0947a-194">PT_MV_CLSID</span><span class="sxs-lookup"><span data-stu-id="0947a-194">PT_MV_CLSID</span></span>  <br/> |<span data-ttu-id="0947a-195">**MVguid**</span><span class="sxs-lookup"><span data-stu-id="0947a-195">**MVguid**</span></span> <br/> |[<span data-ttu-id="0947a-196">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="0947a-196">SGuidArray</span></span>](sguidarray.md) <br/> |
|<span data-ttu-id="0947a-197">PT_MV_I8</span><span class="sxs-lookup"><span data-stu-id="0947a-197">PT_MV_I8</span></span>  <br/> |<span data-ttu-id="0947a-198">**MVli**</span><span class="sxs-lookup"><span data-stu-id="0947a-198">**MVli**</span></span> <br/> |[<span data-ttu-id="0947a-199">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="0947a-199">SLargeIntegerArray</span></span>](slargeintegerarray.md) <br/> |
|<span data-ttu-id="0947a-200">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="0947a-200">PT_ERROR</span></span>  <br/> |<span data-ttu-id="0947a-201">**err**</span><span class="sxs-lookup"><span data-stu-id="0947a-201">**err**</span></span> <br/> |[<span data-ttu-id="0947a-202">SCODE</span><span class="sxs-lookup"><span data-stu-id="0947a-202">SCODE</span></span>](scode.md) <br/> |
|<span data-ttu-id="0947a-203">PT_NULL または PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="0947a-203">PT_NULL or PT_OBJECT</span></span>  <br/> |<span data-ttu-id="0947a-204">**x**</span><span class="sxs-lookup"><span data-stu-id="0947a-204">**x**</span></span> <br/> |<span data-ttu-id="0947a-205">l</span><span class="sxs-lookup"><span data-stu-id="0947a-205">LONG</span></span>  <br/> |
|<span data-ttu-id="0947a-206">PT_PTR</span><span class="sxs-lookup"><span data-stu-id="0947a-206">PT_PTR</span></span>  <br/> |<span data-ttu-id="0947a-207">**lpv**</span><span class="sxs-lookup"><span data-stu-id="0947a-207">**lpv**</span></span> <br/> |<span data-ttu-id="0947a-208">VOID\*</span><span class="sxs-lookup"><span data-stu-id="0947a-208">VOID \*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0947a-209">解説</span><span class="sxs-lookup"><span data-stu-id="0947a-209">Remarks</span></span>

<span data-ttu-id="0947a-210">**ulPropTag**メンバーは、次の2つの部分で構成されます。</span><span class="sxs-lookup"><span data-stu-id="0947a-210">The **ulPropTag** member is made up of two parts:</span></span> 
  
- <span data-ttu-id="0947a-211">上位16ビットの識別子。</span><span class="sxs-lookup"><span data-stu-id="0947a-211">An identifier in the high-order 16 bits.</span></span>
    
- <span data-ttu-id="0947a-212">ローオーダー16ビットの型。</span><span class="sxs-lookup"><span data-stu-id="0947a-212">A type in the low-order 16 bits.</span></span>
    
<span data-ttu-id="0947a-213">識別子は、特定の範囲内の数値です。</span><span class="sxs-lookup"><span data-stu-id="0947a-213">The identifier is a numeric value within a particular range.</span></span> <span data-ttu-id="0947a-214">MAPI は、識別子の範囲を定義して、プロパティがどのように使用され、保持する責任者を示します。</span><span class="sxs-lookup"><span data-stu-id="0947a-214">MAPI defines ranges for identifiers to describe what the property is used for and who is responsible for maintaining it.</span></span> <span data-ttu-id="0947a-215">MAPI は、Mapitags ヘッダーファイルでサポートされている各プロパティタグに対する制約を定義します。</span><span class="sxs-lookup"><span data-stu-id="0947a-215">MAPI defines constraints for each of the property tags that it supports in the Mapitags.h header file.</span></span>
  
<span data-ttu-id="0947a-216">この型は、プロパティの値の形式を示します。</span><span class="sxs-lookup"><span data-stu-id="0947a-216">The type indicates the format for the property's value.</span></span> <span data-ttu-id="0947a-217">MAPI は、mapidefs.h ヘッダーファイルでサポートされている各プロパティの種類に対して定数を定義します。</span><span class="sxs-lookup"><span data-stu-id="0947a-217">MAPI defines constants for each of the property types that it supports in the Mapidefs.h header file.</span></span> 
  
<span data-ttu-id="0947a-218">識別子およびプロパティの種類の有効なプロパティ範囲の完全な一覧については、「付録」の「[プロパティの識別子と種類](property-identifiers-and-types.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0947a-218">For a complete list of the valid property ranges for identifiers and property types, see the [Property Identifiers and Types](property-identifiers-and-types.md) appendix.</span></span> 
  
<span data-ttu-id="0947a-219">**dwAlignPad**メンバーは、8バイト値の8バイト配置を必要とするコンピューターで適切に配置されるように、パディングとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="0947a-219">The **dwAlignPad** member is used as padding to make sure proper alignment on computers that require 8-byte alignment for 8-byte values.</span></span> <span data-ttu-id="0947a-220">このようなコンピューターでコードを記述する開発者は、8バイト境界に**spropvalue**配列を割り当てるメモリ割り当てルーチンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0947a-220">Developers who write code on such computers should use memory allocation routines that allocate the **SPropValue** arrays on 8-byte boundaries.</span></span> 
  
<span data-ttu-id="0947a-221">詳細については、「 [mapi プロパティの種類の概要](mapi-property-type-overview.md)」および「 [mapi プロパティの更新](updating-mapi-properties.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0947a-221">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md) and [Updating MAPI Properties](updating-mapi-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0947a-222">関連項目</span><span class="sxs-lookup"><span data-stu-id="0947a-222">See also</span></span>



[<span data-ttu-id="0947a-223">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="0947a-223">MAPI Structures</span></span>](mapi-structures.md)

