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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c7f4e8835831af6277cef134bf3961e9928cba33
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433529"
---
# <a name="spropvalue"></a><span data-ttu-id="76ad1-103">SPropValue</span><span class="sxs-lookup"><span data-stu-id="76ad1-103">SPropValue</span></span>

  
  
<span data-ttu-id="76ad1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76ad1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76ad1-105">MAPI プロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="76ad1-105">Describes a MAPI property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="76ad1-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="76ad1-106">Header file:</span></span>  <br/> |<span data-ttu-id="76ad1-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="76ad1-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="76ad1-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="76ad1-108">Related macros:</span></span>  <br/> |<span data-ttu-id="76ad1-109">[CHANGE_PROP_TYPE](change_prop_type.md)、 [MVI_PROP](mvi_prop.md) [、](prop_id.md)PROP_ID [、](prop_tag.md)PROP_TAG [、](prop_type.md) PROP_TYPE</span><span class="sxs-lookup"><span data-stu-id="76ad1-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span></span> <br/> |
   
```cpp
typedef struct _SPropValue
{
  ULONG ulPropTag;
  ULONG dwAlignPad;
  union _PV Value;
} SPropValue, FAR *LPSPropValue;

```

## <a name="members"></a><span data-ttu-id="76ad1-110">Members</span><span class="sxs-lookup"><span data-stu-id="76ad1-110">Members</span></span>

 <span data-ttu-id="76ad1-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="76ad1-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="76ad1-112">プロパティのプロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="76ad1-112">Property tag for the property.</span></span> <span data-ttu-id="76ad1-113">プロパティ タグは、高次 16 ビットのプロパティの一意識別子と、低次 16 ビットのプロパティの型で構成される 32 ビットの符号なし整数です。</span><span class="sxs-lookup"><span data-stu-id="76ad1-113">Property tags are 32-bit unsigned integers consisting of the property's unique identifier in the high-order 16 bits and the property's type in the low-order 16 bits.</span></span>
    
 <span data-ttu-id="76ad1-114">**dwAlignPad**</span><span class="sxs-lookup"><span data-stu-id="76ad1-114">**dwAlignPad**</span></span>
  
> <span data-ttu-id="76ad1-115">MAPI 用に予約されています。使用しない。</span><span class="sxs-lookup"><span data-stu-id="76ad1-115">Reserved for MAPI; do not use.</span></span> 
    
 <span data-ttu-id="76ad1-116">**値**</span><span class="sxs-lookup"><span data-stu-id="76ad1-116">**Value**</span></span>
  
> <span data-ttu-id="76ad1-117">データ値の共用体、プロパティの種類によって決まる特定の値。</span><span class="sxs-lookup"><span data-stu-id="76ad1-117">Union of data values, the specific value dictated by the property type.</span></span> <span data-ttu-id="76ad1-118">次の表に、各プロパティの種類、使用する共用体のメンバー、および関連するデータ型を示します。</span><span class="sxs-lookup"><span data-stu-id="76ad1-118">The following table lists for each property type, the member of the union that should be used and its associated data type.</span></span>
    
|<span data-ttu-id="76ad1-119">**プロパティの種類**</span><span class="sxs-lookup"><span data-stu-id="76ad1-119">**Property type**</span></span>|<span data-ttu-id="76ad1-120">**値**</span><span class="sxs-lookup"><span data-stu-id="76ad1-120">**Value**</span></span>|<span data-ttu-id="76ad1-121">**Value のデータ型**</span><span class="sxs-lookup"><span data-stu-id="76ad1-121">**Data type of Value**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="76ad1-122">PT_I2またはPT_SHORT</span><span class="sxs-lookup"><span data-stu-id="76ad1-122">PT_I2 or PT_SHORT</span></span>  <br/> |<span data-ttu-id="76ad1-123">**i**</span><span class="sxs-lookup"><span data-stu-id="76ad1-123">**i**</span></span> <br/> |<span data-ttu-id="76ad1-124">short int</span><span class="sxs-lookup"><span data-stu-id="76ad1-124">short int</span></span>  <br/> |
|<span data-ttu-id="76ad1-125">PT_I4またはPT_LONG (署名済み)</span><span class="sxs-lookup"><span data-stu-id="76ad1-125">PT_I4 or PT_LONG (signed)</span></span>  <br/> |<span data-ttu-id="76ad1-126">**l**</span><span class="sxs-lookup"><span data-stu-id="76ad1-126">**l**</span></span> <br/> |<span data-ttu-id="76ad1-127">LONG</span><span class="sxs-lookup"><span data-stu-id="76ad1-127">LONG</span></span>  <br/> |
|<span data-ttu-id="76ad1-128">PT_I4またはPT_LONG (符号なし)</span><span class="sxs-lookup"><span data-stu-id="76ad1-128">PT_I4 or PT_LONG (unsigned)</span></span>  <br/> |<span data-ttu-id="76ad1-129">**ul**</span><span class="sxs-lookup"><span data-stu-id="76ad1-129">**ul**</span></span> <br/> |<span data-ttu-id="76ad1-130">ULONG</span><span class="sxs-lookup"><span data-stu-id="76ad1-130">ULONG</span></span>  <br/> |
|<span data-ttu-id="76ad1-131">PT_R4またはPT_FLOAT</span><span class="sxs-lookup"><span data-stu-id="76ad1-131">PT_R4 or PT_FLOAT</span></span>  <br/> |<span data-ttu-id="76ad1-132">**flt**</span><span class="sxs-lookup"><span data-stu-id="76ad1-132">**flt**</span></span> <br/> |<span data-ttu-id="76ad1-133">浮動小数点数</span><span class="sxs-lookup"><span data-stu-id="76ad1-133">float</span></span>  <br/> |
|<span data-ttu-id="76ad1-134">PT_R8またはPT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="76ad1-134">PT_R8 or PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="76ad1-135">**dbl**</span><span class="sxs-lookup"><span data-stu-id="76ad1-135">**dbl**</span></span> <br/> |<span data-ttu-id="76ad1-136">double</span><span class="sxs-lookup"><span data-stu-id="76ad1-136">double</span></span>  <br/> |
|<span data-ttu-id="76ad1-137">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="76ad1-137">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="76ad1-138">**b**</span><span class="sxs-lookup"><span data-stu-id="76ad1-138">**b**</span></span> <br/> |<span data-ttu-id="76ad1-139">符号なし short int</span><span class="sxs-lookup"><span data-stu-id="76ad1-139">unsigned short int</span></span>  <br/> |
|<span data-ttu-id="76ad1-140">PT_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="76ad1-140">PT_CURRENCY</span></span>  <br/> |<span data-ttu-id="76ad1-141">**cur**</span><span class="sxs-lookup"><span data-stu-id="76ad1-141">**cur**</span></span> <br/> |[<span data-ttu-id="76ad1-142">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="76ad1-142">CURRENCY</span></span>](currency.md) <br/> |
|<span data-ttu-id="76ad1-143">PT_APPTIME</span><span class="sxs-lookup"><span data-stu-id="76ad1-143">PT_APPTIME</span></span>  <br/> |<span data-ttu-id="76ad1-144">**at**</span><span class="sxs-lookup"><span data-stu-id="76ad1-144">**at**</span></span> <br/> |<span data-ttu-id="76ad1-145">double</span><span class="sxs-lookup"><span data-stu-id="76ad1-145">double</span></span>  <br/> |
|<span data-ttu-id="76ad1-146">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="76ad1-146">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="76ad1-147">**ft**</span><span class="sxs-lookup"><span data-stu-id="76ad1-147">**ft**</span></span> <br/> |[<span data-ttu-id="76ad1-148">FILETIME</span><span class="sxs-lookup"><span data-stu-id="76ad1-148">FILETIME</span></span>](filetime.md) <br/> |
|<span data-ttu-id="76ad1-149">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="76ad1-149">PT_STRING8</span></span>  <br/> |<span data-ttu-id="76ad1-150">**lpszA**</span><span class="sxs-lookup"><span data-stu-id="76ad1-150">**lpszA**</span></span> <br/> |<span data-ttu-id="76ad1-151">LPSTR</span><span class="sxs-lookup"><span data-stu-id="76ad1-151">LPSTR</span></span>  <br/> |
|<span data-ttu-id="76ad1-152">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="76ad1-152">PT_BINARY</span></span>  <br/> |<span data-ttu-id="76ad1-153">**bin**</span><span class="sxs-lookup"><span data-stu-id="76ad1-153">**bin**</span></span> <br/> |<span data-ttu-id="76ad1-154">BYTE [配列]</span><span class="sxs-lookup"><span data-stu-id="76ad1-154">BYTE [array]</span></span>  <br/> |
|<span data-ttu-id="76ad1-155">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="76ad1-155">PT_UNICODE</span></span>  <br/> |<span data-ttu-id="76ad1-156">**lpszW**</span><span class="sxs-lookup"><span data-stu-id="76ad1-156">**lpszW**</span></span> <br/> |<span data-ttu-id="76ad1-157">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="76ad1-157">LPWSTR</span></span>  <br/> |
|<span data-ttu-id="76ad1-158">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="76ad1-158">PT_CLSID</span></span>  <br/> |<span data-ttu-id="76ad1-159">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="76ad1-159">**lpguid**</span></span> <br/> |<span data-ttu-id="76ad1-160">LPGUID</span><span class="sxs-lookup"><span data-stu-id="76ad1-160">LPGUID</span></span>  <br/> |
|<span data-ttu-id="76ad1-161">PT_I8またはPT_LONGLONG</span><span class="sxs-lookup"><span data-stu-id="76ad1-161">PT_I8 or PT_LONGLONG</span></span>  <br/> |<span data-ttu-id="76ad1-162">**li**</span><span class="sxs-lookup"><span data-stu-id="76ad1-162">**li**</span></span> <br/> |<span data-ttu-id="76ad1-163">**LARGE_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="76ad1-163">**LARGE_INTEGER**</span></span> <br/> |
|<span data-ttu-id="76ad1-164">PT_MV_I2</span><span class="sxs-lookup"><span data-stu-id="76ad1-164">PT_MV_I2</span></span>  <br/> |<span data-ttu-id="76ad1-165">**MVi**</span><span class="sxs-lookup"><span data-stu-id="76ad1-165">**MVi**</span></span> <br/> |[<span data-ttu-id="76ad1-166">SShortArray</span><span class="sxs-lookup"><span data-stu-id="76ad1-166">SShortArray</span></span>](sshortarray.md) <br/> |
|<span data-ttu-id="76ad1-167">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="76ad1-167">PT_MV_LONG</span></span>  <br/> |<span data-ttu-id="76ad1-168">**MVI**</span><span class="sxs-lookup"><span data-stu-id="76ad1-168">**MVI**</span></span> <br/> |[<span data-ttu-id="76ad1-169">SLongArray</span><span class="sxs-lookup"><span data-stu-id="76ad1-169">SLongArray</span></span>](slongarray.md) <br/> |
|<span data-ttu-id="76ad1-170">PT_MV_R4</span><span class="sxs-lookup"><span data-stu-id="76ad1-170">PT_MV_R4</span></span>  <br/> |<span data-ttu-id="76ad1-171">**MVflt**</span><span class="sxs-lookup"><span data-stu-id="76ad1-171">**MVflt**</span></span> <br/> |[<span data-ttu-id="76ad1-172">SRealArray</span><span class="sxs-lookup"><span data-stu-id="76ad1-172">SRealArray</span></span>](srealarray.md) <br/> |
|<span data-ttu-id="76ad1-173">PT_MV_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="76ad1-173">PT_MV_DOUBLE</span></span>  <br/> |<span data-ttu-id="76ad1-174">**MVdbl**</span><span class="sxs-lookup"><span data-stu-id="76ad1-174">**MVdbl**</span></span> <br/> |[<span data-ttu-id="76ad1-175">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="76ad1-175">SDoubleArray</span></span>](sdoublearray.md) <br/> |
|<span data-ttu-id="76ad1-176">PT_MV_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="76ad1-176">PT_MV_CURRENCY</span></span>  <br/> |<span data-ttu-id="76ad1-177">**MVcur**</span><span class="sxs-lookup"><span data-stu-id="76ad1-177">**MVcur**</span></span> <br/> |[<span data-ttu-id="76ad1-178">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="76ad1-178">SCurrencyArray</span></span>](scurrencyarray.md) <br/> |
|<span data-ttu-id="76ad1-179">PT_MV_APPTIME</span><span class="sxs-lookup"><span data-stu-id="76ad1-179">PT_MV_APPTIME</span></span>  <br/> |<span data-ttu-id="76ad1-180">**MVat**</span><span class="sxs-lookup"><span data-stu-id="76ad1-180">**MVat**</span></span> <br/> |[<span data-ttu-id="76ad1-181">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="76ad1-181">SAppTimeArray</span></span>](sapptimearray.md) <br/> |
|<span data-ttu-id="76ad1-182">PT_MV_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="76ad1-182">PT_MV_SYSTIME</span></span>  <br/> |<span data-ttu-id="76ad1-183">**MVft**</span><span class="sxs-lookup"><span data-stu-id="76ad1-183">**MVft**</span></span> <br/> |[<span data-ttu-id="76ad1-184">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="76ad1-184">SDateTimeArray</span></span>](sdatetimearray.md) <br/> |
|<span data-ttu-id="76ad1-185">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="76ad1-185">PT_MV_BINARY</span></span>  <br/> |<span data-ttu-id="76ad1-186">**MVbin**</span><span class="sxs-lookup"><span data-stu-id="76ad1-186">**MVbin**</span></span> <br/> |[<span data-ttu-id="76ad1-187">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="76ad1-187">SBinaryArray</span></span>](sbinaryarray.md) <br/> |
|<span data-ttu-id="76ad1-188">PT_MV_STRING8</span><span class="sxs-lookup"><span data-stu-id="76ad1-188">PT_MV_STRING8</span></span>  <br/> |<span data-ttu-id="76ad1-189">**MVszA**</span><span class="sxs-lookup"><span data-stu-id="76ad1-189">**MVszA**</span></span> <br/> |[<span data-ttu-id="76ad1-190">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="76ad1-190">SLPSTRArray</span></span>](slpstrarray.md) <br/> |
|<span data-ttu-id="76ad1-191">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="76ad1-191">PT_MV_UNICODE</span></span>  <br/> |<span data-ttu-id="76ad1-192">**MVszW**</span><span class="sxs-lookup"><span data-stu-id="76ad1-192">**MVszW**</span></span> <br/> |[<span data-ttu-id="76ad1-193">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="76ad1-193">SWStringArray</span></span>](swstringarray.md) <br/> |
|<span data-ttu-id="76ad1-194">PT_MV_CLSID</span><span class="sxs-lookup"><span data-stu-id="76ad1-194">PT_MV_CLSID</span></span>  <br/> |<span data-ttu-id="76ad1-195">**MVguid**</span><span class="sxs-lookup"><span data-stu-id="76ad1-195">**MVguid**</span></span> <br/> |[<span data-ttu-id="76ad1-196">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="76ad1-196">SGuidArray</span></span>](sguidarray.md) <br/> |
|<span data-ttu-id="76ad1-197">PT_MV_I8</span><span class="sxs-lookup"><span data-stu-id="76ad1-197">PT_MV_I8</span></span>  <br/> |<span data-ttu-id="76ad1-198">**MVli**</span><span class="sxs-lookup"><span data-stu-id="76ad1-198">**MVli**</span></span> <br/> |[<span data-ttu-id="76ad1-199">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="76ad1-199">SLargeIntegerArray</span></span>](slargeintegerarray.md) <br/> |
|<span data-ttu-id="76ad1-200">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="76ad1-200">PT_ERROR</span></span>  <br/> |<span data-ttu-id="76ad1-201">**err**</span><span class="sxs-lookup"><span data-stu-id="76ad1-201">**err**</span></span> <br/> |[<span data-ttu-id="76ad1-202">SCODE</span><span class="sxs-lookup"><span data-stu-id="76ad1-202">SCODE</span></span>](scode.md) <br/> |
|<span data-ttu-id="76ad1-203">PT_NULLまたはPT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="76ad1-203">PT_NULL or PT_OBJECT</span></span>  <br/> |<span data-ttu-id="76ad1-204">**x**</span><span class="sxs-lookup"><span data-stu-id="76ad1-204">**x**</span></span> <br/> |<span data-ttu-id="76ad1-205">LONG</span><span class="sxs-lookup"><span data-stu-id="76ad1-205">LONG</span></span>  <br/> |
|<span data-ttu-id="76ad1-206">PT_PTR</span><span class="sxs-lookup"><span data-stu-id="76ad1-206">PT_PTR</span></span>  <br/> |<span data-ttu-id="76ad1-207">**lpv**</span><span class="sxs-lookup"><span data-stu-id="76ad1-207">**lpv**</span></span> <br/> |<span data-ttu-id="76ad1-208">VOID \*</span><span class="sxs-lookup"><span data-stu-id="76ad1-208">VOID \*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76ad1-209">注釈</span><span class="sxs-lookup"><span data-stu-id="76ad1-209">Remarks</span></span>

<span data-ttu-id="76ad1-210">**ulPropTag メンバー** は、次の 2 つの部分で構成されます。</span><span class="sxs-lookup"><span data-stu-id="76ad1-210">The **ulPropTag** member is made up of two parts:</span></span> 
  
- <span data-ttu-id="76ad1-211">高次 16 ビットの識別子。</span><span class="sxs-lookup"><span data-stu-id="76ad1-211">An identifier in the high-order 16 bits.</span></span>
    
- <span data-ttu-id="76ad1-212">低次 16 ビットの型。</span><span class="sxs-lookup"><span data-stu-id="76ad1-212">A type in the low-order 16 bits.</span></span>
    
<span data-ttu-id="76ad1-213">識別子は、特定の範囲内の数値です。</span><span class="sxs-lookup"><span data-stu-id="76ad1-213">The identifier is a numeric value within a particular range.</span></span> <span data-ttu-id="76ad1-214">MAPI では、プロパティの使用および管理の責任者を示す識別子の範囲を定義します。</span><span class="sxs-lookup"><span data-stu-id="76ad1-214">MAPI defines ranges for identifiers to describe what the property is used for and who is responsible for maintaining it.</span></span> <span data-ttu-id="76ad1-215">MAPI は、Mapitags.h ヘッダー ファイルでサポートする各プロパティ タグの制約を定義します。</span><span class="sxs-lookup"><span data-stu-id="76ad1-215">MAPI defines constraints for each of the property tags that it supports in the Mapitags.h header file.</span></span>
  
<span data-ttu-id="76ad1-216">型は、プロパティの値の形式を示します。</span><span class="sxs-lookup"><span data-stu-id="76ad1-216">The type indicates the format for the property's value.</span></span> <span data-ttu-id="76ad1-217">MAPI は、Mapidefs.h ヘッダー ファイルでサポートする各プロパティの種類の定数を定義します。</span><span class="sxs-lookup"><span data-stu-id="76ad1-217">MAPI defines constants for each of the property types that it supports in the Mapidefs.h header file.</span></span> 
  
<span data-ttu-id="76ad1-218">識別子とプロパティ型の有効なプロパティ範囲の完全な一覧については、付録「プロパティ識別子と型」 [を参照](property-identifiers-and-types.md) してください。</span><span class="sxs-lookup"><span data-stu-id="76ad1-218">For a complete list of the valid property ranges for identifiers and property types, see the [Property Identifiers and Types](property-identifiers-and-types.md) appendix.</span></span> 
  
<span data-ttu-id="76ad1-219">**dwAlignPad メンバー** は、8 バイト値に対して 8 バイトの配置を必要とするコンピューター上で適切な配置を行うパディングとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="76ad1-219">The **dwAlignPad** member is used as padding to make sure proper alignment on computers that require 8-byte alignment for 8-byte values.</span></span> <span data-ttu-id="76ad1-220">このようなコンピューターでコードを記述する開発者は、8 バイト境界に **SPropValue** 配列を割り当てるメモリ割り当てルーチンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="76ad1-220">Developers who write code on such computers should use memory allocation routines that allocate the **SPropValue** arrays on 8-byte boundaries.</span></span> 
  
<span data-ttu-id="76ad1-221">詳細については、「MAPI プロパティの [種類の概要」および「MAPI](mapi-property-type-overview.md) [プロパティの更新」を参照してください](updating-mapi-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="76ad1-221">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md) and [Updating MAPI Properties](updating-mapi-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="76ad1-222">関連項目</span><span class="sxs-lookup"><span data-stu-id="76ad1-222">See also</span></span>



[<span data-ttu-id="76ad1-223">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="76ad1-223">MAPI Structures</span></span>](mapi-structures.md)

