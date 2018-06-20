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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: f378bdd473410b846328cbe1f911eba9401f88cf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804003"
---
# <a name="spropvalue"></a><span data-ttu-id="d86d3-103">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d86d3-103">SPropValue</span></span>

  
  
<span data-ttu-id="d86d3-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d86d3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d86d3-105">MAPI プロパティをについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d86d3-105">Describes a MAPI property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d86d3-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="d86d3-106">Header file:</span></span>  <br/> |<span data-ttu-id="d86d3-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d86d3-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="d86d3-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="d86d3-108">Related macros:</span></span>  <br/> |<span data-ttu-id="d86d3-109">[CHANGE_PROP_TYPE](change_prop_type.md)、 [MVI_PROP](mvi_prop.md)、 [PROP_ID](prop_id.md)、 [PROP_TAG](prop_tag.md)、 [PROP_TYPE](prop_type.md)</span><span class="sxs-lookup"><span data-stu-id="d86d3-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span></span> <br/> |
   
```cpp
typedef struct _SPropValue
{
  ULONG ulPropTag;
  ULONG dwAlignPad;
  union _PV Value;
} SPropValue, FAR *LPSPropValue;

```

## <a name="members"></a><span data-ttu-id="d86d3-110">メンバー</span><span class="sxs-lookup"><span data-stu-id="d86d3-110">Members</span></span>

 <span data-ttu-id="d86d3-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="d86d3-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="d86d3-112">プロパティのプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="d86d3-112">Property tag for the property.</span></span> <span data-ttu-id="d86d3-113">プロパティ タグは、プロパティの一意の識別子の上位 16 ビットと下位の 16 ビットのプロパティの型で構成される 32 ビットの符号なし整数です。</span><span class="sxs-lookup"><span data-stu-id="d86d3-113">Property tags are 32-bit unsigned integers consisting of the property's unique identifier in the high-order 16 bits and the property's type in the low-order 16 bits.</span></span>
    
 <span data-ttu-id="d86d3-114">**dwAlignPad**</span><span class="sxs-lookup"><span data-stu-id="d86d3-114">**dwAlignPad**</span></span>
  
> <span data-ttu-id="d86d3-115">MAPI のために予約使用しません。</span><span class="sxs-lookup"><span data-stu-id="d86d3-115">Reserved for MAPI; do not use.</span></span> 
    
 <span data-ttu-id="d86d3-116">**値**</span><span class="sxs-lookup"><span data-stu-id="d86d3-116">**Value**</span></span>
  
> <span data-ttu-id="d86d3-117">共用体データの値の特定の値をプロパティの型によって決まります。</span><span class="sxs-lookup"><span data-stu-id="d86d3-117">Union of data values, the specific value dictated by the property type.</span></span> <span data-ttu-id="d86d3-118">次の表は、各プロパティの種類、使用する共用体のメンバーとその関連するデータ型の一覧です。</span><span class="sxs-lookup"><span data-stu-id="d86d3-118">The following table lists for each property type, the member of the union that should be used and its associated data type.</span></span>
    
|<span data-ttu-id="d86d3-119">**プロパティの種類**</span><span class="sxs-lookup"><span data-stu-id="d86d3-119">**Property type**</span></span>|<span data-ttu-id="d86d3-120">**値**</span><span class="sxs-lookup"><span data-stu-id="d86d3-120">**Value**</span></span>|<span data-ttu-id="d86d3-121">**値のデータ型**</span><span class="sxs-lookup"><span data-stu-id="d86d3-121">**Data type of Value**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d86d3-122">PT_I2 または PT_SHORT</span><span class="sxs-lookup"><span data-stu-id="d86d3-122">PT_I2 or PT_SHORT</span></span>  <br/> |<span data-ttu-id="d86d3-123">**i**</span><span class="sxs-lookup"><span data-stu-id="d86d3-123">**i**</span></span> <br/> |<span data-ttu-id="d86d3-124">短い int</span><span class="sxs-lookup"><span data-stu-id="d86d3-124">short int</span></span>  <br/> |
|<span data-ttu-id="d86d3-125">PT_I4 または PT_LONG を (符号付き)</span><span class="sxs-lookup"><span data-stu-id="d86d3-125">PT_I4 or PT_LONG (signed)</span></span>  <br/> |<span data-ttu-id="d86d3-126">**l**</span><span class="sxs-lookup"><span data-stu-id="d86d3-126">**l**</span></span> <br/> |<span data-ttu-id="d86d3-127">長</span><span class="sxs-lookup"><span data-stu-id="d86d3-127">LONG</span></span>  <br/> |
|<span data-ttu-id="d86d3-128">PT_I4 または PT_LONG の (符号なし)</span><span class="sxs-lookup"><span data-stu-id="d86d3-128">PT_I4 or PT_LONG (unsigned)</span></span>  <br/> |<span data-ttu-id="d86d3-129">**ul**</span><span class="sxs-lookup"><span data-stu-id="d86d3-129">**ul**</span></span> <br/> |<span data-ttu-id="d86d3-130">ULONG</span><span class="sxs-lookup"><span data-stu-id="d86d3-130">ULONG</span></span>  <br/> |
|<span data-ttu-id="d86d3-131">PT_R4 または PT_FLOAT</span><span class="sxs-lookup"><span data-stu-id="d86d3-131">PT_R4 or PT_FLOAT</span></span>  <br/> |<span data-ttu-id="d86d3-132">**flt**</span><span class="sxs-lookup"><span data-stu-id="d86d3-132">**flt**</span></span> <br/> |<span data-ttu-id="d86d3-133">浮動小数点数</span><span class="sxs-lookup"><span data-stu-id="d86d3-133">float</span></span>  <br/> |
|<span data-ttu-id="d86d3-134">PT_R8 または PT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="d86d3-134">PT_R8 or PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="d86d3-135">**複列**</span><span class="sxs-lookup"><span data-stu-id="d86d3-135">**dbl**</span></span> <br/> |<span data-ttu-id="d86d3-136">double</span><span class="sxs-lookup"><span data-stu-id="d86d3-136">double</span></span>  <br/> |
|<span data-ttu-id="d86d3-137">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="d86d3-137">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="d86d3-138">**b**</span><span class="sxs-lookup"><span data-stu-id="d86d3-138">**b**</span></span> <br/> |<span data-ttu-id="d86d3-139">符号なし短整数</span><span class="sxs-lookup"><span data-stu-id="d86d3-139">unsigned short int</span></span>  <br/> |
|<span data-ttu-id="d86d3-140">PT_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="d86d3-140">PT_CURRENCY</span></span>  <br/> |<span data-ttu-id="d86d3-141">**cur**</span><span class="sxs-lookup"><span data-stu-id="d86d3-141">**cur**</span></span> <br/> |[<span data-ttu-id="d86d3-142">通貨</span><span class="sxs-lookup"><span data-stu-id="d86d3-142">CURRENCY</span></span>](currency.md) <br/> |
|<span data-ttu-id="d86d3-143">PT_APPTIME</span><span class="sxs-lookup"><span data-stu-id="d86d3-143">PT_APPTIME</span></span>  <br/> |<span data-ttu-id="d86d3-144">**で**</span><span class="sxs-lookup"><span data-stu-id="d86d3-144">**at**</span></span> <br/> |<span data-ttu-id="d86d3-145">double</span><span class="sxs-lookup"><span data-stu-id="d86d3-145">double</span></span>  <br/> |
|<span data-ttu-id="d86d3-146">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="d86d3-146">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="d86d3-147">**ft**</span><span class="sxs-lookup"><span data-stu-id="d86d3-147">**ft**</span></span> <br/> |[<span data-ttu-id="d86d3-148">FILETIME</span><span class="sxs-lookup"><span data-stu-id="d86d3-148">FILETIME</span></span>](filetime.md) <br/> |
|<span data-ttu-id="d86d3-149">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="d86d3-149">PT_STRING8</span></span>  <br/> |<span data-ttu-id="d86d3-150">**lpszA**</span><span class="sxs-lookup"><span data-stu-id="d86d3-150">**lpszA**</span></span> <br/> |<span data-ttu-id="d86d3-151">LPSTR</span><span class="sxs-lookup"><span data-stu-id="d86d3-151">LPSTR</span></span>  <br/> |
|<span data-ttu-id="d86d3-152">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d86d3-152">PT_BINARY</span></span>  <br/> |<span data-ttu-id="d86d3-153">**箱**</span><span class="sxs-lookup"><span data-stu-id="d86d3-153">**bin**</span></span> <br/> |<span data-ttu-id="d86d3-154">バイト [配列]</span><span class="sxs-lookup"><span data-stu-id="d86d3-154">BYTE [array]</span></span>  <br/> |
|<span data-ttu-id="d86d3-155">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d86d3-155">PT_UNICODE</span></span>  <br/> |<span data-ttu-id="d86d3-156">**lpszW**</span><span class="sxs-lookup"><span data-stu-id="d86d3-156">**lpszW**</span></span> <br/> |<span data-ttu-id="d86d3-157">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="d86d3-157">LPWSTR</span></span>  <br/> |
|<span data-ttu-id="d86d3-158">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="d86d3-158">PT_CLSID</span></span>  <br/> |<span data-ttu-id="d86d3-159">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="d86d3-159">**lpguid**</span></span> <br/> |<span data-ttu-id="d86d3-160">LPGUID</span><span class="sxs-lookup"><span data-stu-id="d86d3-160">LPGUID</span></span>  <br/> |
|<span data-ttu-id="d86d3-161">PT_I8 または PT_LONGLONG</span><span class="sxs-lookup"><span data-stu-id="d86d3-161">PT_I8 or PT_LONGLONG</span></span>  <br/> |<span data-ttu-id="d86d3-162">**li**</span><span class="sxs-lookup"><span data-stu-id="d86d3-162">**li**</span></span> <br/> |<span data-ttu-id="d86d3-163">**LARGE_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="d86d3-163">**LARGE_INTEGER**</span></span> <br/> |
|<span data-ttu-id="d86d3-164">PT_MV_I2</span><span class="sxs-lookup"><span data-stu-id="d86d3-164">PT_MV_I2</span></span>  <br/> |<span data-ttu-id="d86d3-165">**MVi**</span><span class="sxs-lookup"><span data-stu-id="d86d3-165">**MVi**</span></span> <br/> |[<span data-ttu-id="d86d3-166">SShortArray</span><span class="sxs-lookup"><span data-stu-id="d86d3-166">SShortArray</span></span>](sshortarray.md) <br/> |
|<span data-ttu-id="d86d3-167">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="d86d3-167">PT_MV_LONG</span></span>  <br/> |<span data-ttu-id="d86d3-168">**MVI**</span><span class="sxs-lookup"><span data-stu-id="d86d3-168">**MVI**</span></span> <br/> |[<span data-ttu-id="d86d3-169">SLongArray</span><span class="sxs-lookup"><span data-stu-id="d86d3-169">SLongArray</span></span>](slongarray.md) <br/> |
|<span data-ttu-id="d86d3-170">PT_MV_R4</span><span class="sxs-lookup"><span data-stu-id="d86d3-170">PT_MV_R4</span></span>  <br/> |<span data-ttu-id="d86d3-171">**MVflt**</span><span class="sxs-lookup"><span data-stu-id="d86d3-171">**MVflt**</span></span> <br/> |[<span data-ttu-id="d86d3-172">SRealArray</span><span class="sxs-lookup"><span data-stu-id="d86d3-172">SRealArray</span></span>](srealarray.md) <br/> |
|<span data-ttu-id="d86d3-173">PT_MV_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="d86d3-173">PT_MV_DOUBLE</span></span>  <br/> |<span data-ttu-id="d86d3-174">**MVdbl**</span><span class="sxs-lookup"><span data-stu-id="d86d3-174">**MVdbl**</span></span> <br/> |[<span data-ttu-id="d86d3-175">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="d86d3-175">SDoubleArray</span></span>](sdoublearray.md) <br/> |
|<span data-ttu-id="d86d3-176">PT_MV_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="d86d3-176">PT_MV_CURRENCY</span></span>  <br/> |<span data-ttu-id="d86d3-177">**MVcur**</span><span class="sxs-lookup"><span data-stu-id="d86d3-177">**MVcur**</span></span> <br/> |[<span data-ttu-id="d86d3-178">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="d86d3-178">SCurrencyArray</span></span>](scurrencyarray.md) <br/> |
|<span data-ttu-id="d86d3-179">PT_MV_APPTIME</span><span class="sxs-lookup"><span data-stu-id="d86d3-179">PT_MV_APPTIME</span></span>  <br/> |<span data-ttu-id="d86d3-180">**MVat**</span><span class="sxs-lookup"><span data-stu-id="d86d3-180">**MVat**</span></span> <br/> |[<span data-ttu-id="d86d3-181">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="d86d3-181">SAppTimeArray</span></span>](sapptimearray.md) <br/> |
|<span data-ttu-id="d86d3-182">PT_MV_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="d86d3-182">PT_MV_SYSTIME</span></span>  <br/> |<span data-ttu-id="d86d3-183">**MVft**</span><span class="sxs-lookup"><span data-stu-id="d86d3-183">**MVft**</span></span> <br/> |[<span data-ttu-id="d86d3-184">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="d86d3-184">SDateTimeArray</span></span>](sdatetimearray.md) <br/> |
|<span data-ttu-id="d86d3-185">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="d86d3-185">PT_MV_BINARY</span></span>  <br/> |<span data-ttu-id="d86d3-186">**MVbin**</span><span class="sxs-lookup"><span data-stu-id="d86d3-186">**MVbin**</span></span> <br/> |[<span data-ttu-id="d86d3-187">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="d86d3-187">SBinaryArray</span></span>](sbinaryarray.md) <br/> |
|<span data-ttu-id="d86d3-188">PT_MV_STRING8</span><span class="sxs-lookup"><span data-stu-id="d86d3-188">PT_MV_STRING8</span></span>  <br/> |<span data-ttu-id="d86d3-189">**MVszA**</span><span class="sxs-lookup"><span data-stu-id="d86d3-189">**MVszA**</span></span> <br/> |[<span data-ttu-id="d86d3-190">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="d86d3-190">SLPSTRArray</span></span>](slpstrarray.md) <br/> |
|<span data-ttu-id="d86d3-191">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d86d3-191">PT_MV_UNICODE</span></span>  <br/> |<span data-ttu-id="d86d3-192">**MVszW**</span><span class="sxs-lookup"><span data-stu-id="d86d3-192">**MVszW**</span></span> <br/> |[<span data-ttu-id="d86d3-193">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="d86d3-193">SWStringArray</span></span>](swstringarray.md) <br/> |
|<span data-ttu-id="d86d3-194">PT_MV_CLSID</span><span class="sxs-lookup"><span data-stu-id="d86d3-194">PT_MV_CLSID</span></span>  <br/> |<span data-ttu-id="d86d3-195">**MVguid**</span><span class="sxs-lookup"><span data-stu-id="d86d3-195">**MVguid**</span></span> <br/> |[<span data-ttu-id="d86d3-196">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="d86d3-196">SGuidArray</span></span>](sguidarray.md) <br/> |
|<span data-ttu-id="d86d3-197">PT_MV_I8</span><span class="sxs-lookup"><span data-stu-id="d86d3-197">PT_MV_I8</span></span>  <br/> |<span data-ttu-id="d86d3-198">**MVli**</span><span class="sxs-lookup"><span data-stu-id="d86d3-198">**MVli**</span></span> <br/> |[<span data-ttu-id="d86d3-199">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="d86d3-199">SLargeIntegerArray</span></span>](slargeintegerarray.md) <br/> |
|<span data-ttu-id="d86d3-200">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="d86d3-200">PT_ERROR</span></span>  <br/> |<span data-ttu-id="d86d3-201">**err**</span><span class="sxs-lookup"><span data-stu-id="d86d3-201">**err**</span></span> <br/> |[<span data-ttu-id="d86d3-202">SCODE</span><span class="sxs-lookup"><span data-stu-id="d86d3-202">SCODE</span></span>](scode.md) <br/> |
|<span data-ttu-id="d86d3-203">PT_NULL または PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="d86d3-203">PT_NULL or PT_OBJECT</span></span>  <br/> |<span data-ttu-id="d86d3-204">**x**</span><span class="sxs-lookup"><span data-stu-id="d86d3-204">**x**</span></span> <br/> |<span data-ttu-id="d86d3-205">長</span><span class="sxs-lookup"><span data-stu-id="d86d3-205">LONG</span></span>  <br/> |
|<span data-ttu-id="d86d3-206">PT_PTR</span><span class="sxs-lookup"><span data-stu-id="d86d3-206">PT_PTR</span></span>  <br/> |<span data-ttu-id="d86d3-207">**lpv**</span><span class="sxs-lookup"><span data-stu-id="d86d3-207">**lpv**</span></span> <br/> |<span data-ttu-id="d86d3-208">VOID\*</span><span class="sxs-lookup"><span data-stu-id="d86d3-208">VOID \*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d86d3-209">備考</span><span class="sxs-lookup"><span data-stu-id="d86d3-209">Remarks</span></span>

<span data-ttu-id="d86d3-210">**UlPropTag**メンバーは、2 つの部分で構成されています。</span><span class="sxs-lookup"><span data-stu-id="d86d3-210">The **ulPropTag** member is made up of two parts:</span></span> 
  
- <span data-ttu-id="d86d3-211">上位 16 ビットの識別子です。</span><span class="sxs-lookup"><span data-stu-id="d86d3-211">An identifier in the high-order 16 bits.</span></span>
    
- <span data-ttu-id="d86d3-212">下位 16 ビットのタイプです。</span><span class="sxs-lookup"><span data-stu-id="d86d3-212">A type in the low-order 16 bits.</span></span>
    
<span data-ttu-id="d86d3-213">識別子は、特定の範囲内の数値です。</span><span class="sxs-lookup"><span data-stu-id="d86d3-213">The identifier is a numeric value within a particular range.</span></span> <span data-ttu-id="d86d3-214">MAPI は、プロパティの使用および保守の責任者を記述する識別子の範囲を定義します。</span><span class="sxs-lookup"><span data-stu-id="d86d3-214">MAPI defines ranges for identifiers to describe what the property is used for and who is responsible for maintaining it.</span></span> <span data-ttu-id="d86d3-215">MAPI では、Mapitags.h ヘッダー ファイルでサポートされているプロパティ タグのそれぞれの制約を定義します。</span><span class="sxs-lookup"><span data-stu-id="d86d3-215">MAPI defines constraints for each of the property tags that it supports in the Mapitags.h header file.</span></span>
  
<span data-ttu-id="d86d3-216">型は、プロパティの値の形式を示します。</span><span class="sxs-lookup"><span data-stu-id="d86d3-216">The type indicates the format for the property's value.</span></span> <span data-ttu-id="d86d3-217">MAPI では、Mapidefs.h ヘッダー ファイルでサポートされているプロパティの型のそれぞれの定数を定義します。</span><span class="sxs-lookup"><span data-stu-id="d86d3-217">MAPI defines constants for each of the property types that it supports in the Mapidefs.h header file.</span></span> 
  
<span data-ttu-id="d86d3-218">識別子とプロパティの型のプロパティの有効な範囲の一覧については、[プロパティの識別子と型](property-identifiers-and-types.md)の付録を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d86d3-218">For a complete list of the valid property ranges for identifiers and property types, see the [Property Identifiers and Types](property-identifiers-and-types.md) appendix.</span></span> 
  
<span data-ttu-id="d86d3-219">**DwAlignPad**メンバーは、8 バイトの値を 8 バイトのアライメントが必要なコンピューターに確実に適切なアライメントを作成する、スペースとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="d86d3-219">The **dwAlignPad** member is used as padding to make sure proper alignment on computers that require 8-byte alignment for 8-byte values.</span></span> <span data-ttu-id="d86d3-220">このようなコンピューター上のコードを記述する開発者は、8 バイト境界に**SPropValue**の配列を割り当てるメモリ割り当てルーチンを使用してください。</span><span class="sxs-lookup"><span data-stu-id="d86d3-220">Developers who write code on such computers should use memory allocation routines that allocate the **SPropValue** arrays on 8-byte boundaries.</span></span> 
  
<span data-ttu-id="d86d3-221">詳細については、 [MAPI プロパティの種類の概要](mapi-property-type-overview.md)と、 [MAPI プロパティの更新](updating-mapi-properties.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d86d3-221">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md) and [Updating MAPI Properties](updating-mapi-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d86d3-222">関連項目</span><span class="sxs-lookup"><span data-stu-id="d86d3-222">See also</span></span>



[<span data-ttu-id="d86d3-223">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="d86d3-223">MAPI Structures</span></span>](mapi-structures.md)

