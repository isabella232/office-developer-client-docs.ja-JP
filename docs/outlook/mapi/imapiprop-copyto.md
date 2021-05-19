---
title: IMAPIPropCopyTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.CopyTo
api_type:
- COM
ms.assetid: e56042e9-5bb7-4a99-b6de-1546d4ca07f0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f76b0a5482647fe3e181a36d7dcd8cb60ffc8985
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356393"
---
# <a name="imapipropcopyto"></a><span data-ttu-id="89bbd-103">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="89bbd-103">IMAPIProp::CopyTo</span></span>

  
  
<span data-ttu-id="89bbd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89bbd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89bbd-105">特定の除外プロパティを除くすべてのプロパティをコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="89bbd-105">Copies or moves all properties, except for specifically excluded properties.</span></span>
  
```cpp
HRESULT CopyTo(
 ULONG ciidExclude,
 LPCIID rgiidExclude,
 LPSPropTagArray lpExcludeProps,
 ULONG_PTR ulUIParam,
 LPMAPIPROGRESS lpProgress,
 LPCIID lpInterface,
 LPVOID lpDestObj,
 ULONG ulFlags,
 LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="89bbd-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89bbd-106">Parameters</span></span>

 <span data-ttu-id="89bbd-107">_ciidExclude_</span><span class="sxs-lookup"><span data-stu-id="89bbd-107">_ciidExclude_</span></span>
  
> <span data-ttu-id="89bbd-108">[in]プロパティをコピーまたは移動するときに除外するインターフェイスの数。</span><span class="sxs-lookup"><span data-stu-id="89bbd-108">[in] The count of interfaces to exclude when properties are copied or moved.</span></span>
    
 <span data-ttu-id="89bbd-109">_rgiidExclude_</span><span class="sxs-lookup"><span data-stu-id="89bbd-109">_rgiidExclude_</span></span>
  
> <span data-ttu-id="89bbd-110">[in]補足情報をコピーまたは移動先オブジェクトに移動するときに使用しないインターフェイスを指定するインターフェイス識別子 (IID) の配列。</span><span class="sxs-lookup"><span data-stu-id="89bbd-110">[in] An array of interface identifiers (IIDs) that specify interfaces that should not be used when supplemental information is copied or moved to the destination object.</span></span>
    
 <span data-ttu-id="89bbd-111">_lpExcludeProps_</span><span class="sxs-lookup"><span data-stu-id="89bbd-111">_lpExcludeProps_</span></span>
  
> <span data-ttu-id="89bbd-112">[in]コピーまたは移動操作から除外する必要があるプロパティ タグを識別するプロパティ タグ配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="89bbd-112">[in] A pointer to a property tag array that identifies the property tags that should be excluded from the copy or move operation.</span></span> <span data-ttu-id="89bbd-113">_lpExcludeProps_ パラメーターに null を渡す場合は、オブジェクトのすべてのプロパティをコピーまたは移動する必要があります。 </span><span class="sxs-lookup"><span data-stu-id="89bbd-113">Passing **null** in the  _lpExcludeProps_ parameter indicates that all of the object's properties should be copied or moved.</span></span> <span data-ttu-id="89bbd-114">**CopyTo** は _、lpExcludeProps_ MAPI_E_INVALID_PARAMETER示す [SPropProblemArray](spropproblemarray.md)構造体の **cValues** メンバーが 0 に設定されている場合に、この値を返します。</span><span class="sxs-lookup"><span data-stu-id="89bbd-114">**CopyTo** returns MAPI_E_INVALID_PARAMETER when the **cValues** member of the [SPropProblemArray](spropproblemarray.md) structure pointed to by  _lpExcludeProps_ is set to 0.</span></span> 
    
 <span data-ttu-id="89bbd-115">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="89bbd-115">_ulUIParam_</span></span>
  
> <span data-ttu-id="89bbd-116">[in]進行状況インジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="89bbd-116">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="89bbd-117">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="89bbd-117">_lpProgress_</span></span>
  
> <span data-ttu-id="89bbd-118">[in]進行状況インジケーターの実装へのポインター。</span><span class="sxs-lookup"><span data-stu-id="89bbd-118">[in] A pointer to a progress indicator implementation.</span></span> <span data-ttu-id="89bbd-119">_lpProgress_ パラメーターで null が渡された場合、MAPI は進行状況の実装を提供します。 </span><span class="sxs-lookup"><span data-stu-id="89bbd-119">If **null** is passed in the  _lpProgress_ parameter, MAPI provides the progress implementation.</span></span> <span data-ttu-id="89bbd-120">_lpProgress パラメーター_ は _、ulFlags_ パラメーター MAPI_DIALOGフラグが設定されていない限り、無視されます。</span><span class="sxs-lookup"><span data-stu-id="89bbd-120">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="89bbd-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="89bbd-121">_lpInterface_</span></span>
  
> <span data-ttu-id="89bbd-122">[in]  _lpDestObj_ パラメーターが指すオブジェクトにアクセスするために使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="89bbd-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object pointed to by the  _lpDestObj_ parameter.</span></span> <span data-ttu-id="89bbd-123">_lpInterface パラメーター_ は null に **することはできません**。</span><span class="sxs-lookup"><span data-stu-id="89bbd-123">The  _lpInterface_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="89bbd-124">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="89bbd-124">_lpDestObj_</span></span>
  
> <span data-ttu-id="89bbd-125">[in]コピーまたは移動されたプロパティを受け取るオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="89bbd-125">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="89bbd-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="89bbd-126">_ulFlags_</span></span>
  
> <span data-ttu-id="89bbd-127">[in]コピーまたは移動操作を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="89bbd-127">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="89bbd-128">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="89bbd-128">The following flags can be set:</span></span>
    
<span data-ttu-id="89bbd-129">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="89bbd-129">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="89bbd-130">**CopyTo が** [IMAPISupport::D oCopyTo](imapisupport-docopyto.md)メソッドを呼び出してコピー操作または移動操作を処理する場合は、代わりにエラー値 MAPI_E_DECLINE_COPY を使用して直ちに返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="89bbd-130">If **CopyTo** calls the [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) method to handle the copy or move operation, it should instead return immediately with the error value MAPI_E_DECLINE_COPY.</span></span> <span data-ttu-id="89bbd-131">再MAPI_DECLINE_OKを制限するために、MAPI によってこのフラグが設定されます。</span><span class="sxs-lookup"><span data-stu-id="89bbd-131">The MAPI_DECLINE_OK flag is set by MAPI to limit recursion.</span></span> <span data-ttu-id="89bbd-132">クライアントは、このフラグを設定しません。</span><span class="sxs-lookup"><span data-stu-id="89bbd-132">Clients do not set this flag.</span></span> 
    
<span data-ttu-id="89bbd-133">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="89bbd-133">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="89bbd-134">進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="89bbd-134">Displays a progress indicator.</span></span>
    
<span data-ttu-id="89bbd-135">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="89bbd-135">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="89bbd-136">**CopyTo** は、コピー操作の代わりに移動操作を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89bbd-136">**CopyTo** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="89bbd-137">このフラグが設定されていない場合 **、CopyTo は** コピー操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="89bbd-137">When this flag is not set, **CopyTo** performs a copy operation.</span></span> 
    
<span data-ttu-id="89bbd-138">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="89bbd-138">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="89bbd-139">移動先オブジェクト内の既存のプロパティは上書きしないでください。</span><span class="sxs-lookup"><span data-stu-id="89bbd-139">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="89bbd-140">このフラグを設定しない場合 **、CopyTo は** 既存のプロパティを上書きします。</span><span class="sxs-lookup"><span data-stu-id="89bbd-140">When this flag is not set, **CopyTo** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="89bbd-141">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="89bbd-141">_lppProblems_</span></span>
  
> <span data-ttu-id="89bbd-142">[in, out]入力時に **、SPropProblemArray** 構造体へのポインターを指すポインター。それ以外の場合 **は null**、エラー情報は不要であることを示します。</span><span class="sxs-lookup"><span data-stu-id="89bbd-142">[in, out] On input, a pointer to a pointer to an **SPropProblemArray** structure; otherwise, **null**, indicating no need for error information.</span></span> <span data-ttu-id="89bbd-143">_lppProblems が_ 入力の有効なポインターである場合 **、CopyTo** は 1 つ以上のプロパティをコピーするエラーに関する詳細情報を返します。</span><span class="sxs-lookup"><span data-stu-id="89bbd-143">If  _lppProblems_ is a valid pointer on input, **CopyTo** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="89bbd-144">戻り値</span><span class="sxs-lookup"><span data-stu-id="89bbd-144">Return value</span></span>

<span data-ttu-id="89bbd-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="89bbd-145">S_OK</span></span> 
  
> <span data-ttu-id="89bbd-146">プロパティが正常にコピーまたは移動されました。</span><span class="sxs-lookup"><span data-stu-id="89bbd-146">The properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="89bbd-147">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="89bbd-147">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="89bbd-148">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティで指定された同じ表示名を持つサブオブジェクトが、コピー先オブジェクトに既に存在する場合、サブオブジェクトをコピーできません。</span><span class="sxs-lookup"><span data-stu-id="89bbd-148">A subobject cannot be copied because a subobject with the same display name — specified by the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property — already exists in the destination object.</span></span> 
    
<span data-ttu-id="89bbd-149">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="89bbd-149">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="89bbd-150">サービス プロバイダーは、コピー操作を実装しない。</span><span class="sxs-lookup"><span data-stu-id="89bbd-150">The service provider does not implement the copy operation.</span></span>
    
<span data-ttu-id="89bbd-151">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="89bbd-151">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="89bbd-152">コピーまたは移動操作を直接または間接的に実行するソース オブジェクトには、移動先オブジェクトが含まれる。</span><span class="sxs-lookup"><span data-stu-id="89bbd-152">The source object performing the copy or move operation directly or indirectly contains the destination object.</span></span> <span data-ttu-id="89bbd-153">この条件が検出される前に重要な作業が実行された可能性があります。そのため、ソース オブジェクトと移動先オブジェクトが部分的に変更される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="89bbd-153">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="89bbd-154">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="89bbd-154">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="89bbd-155">_lpInterface_ パラメーターで識別されるインターフェイスは、移動先オブジェクトではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="89bbd-155">The interface identified by the  _lpInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="89bbd-156">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="89bbd-156">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="89bbd-157">呼び出し元のアクセス許可が不十分なオブジェクトにアクセスしようとした。</span><span class="sxs-lookup"><span data-stu-id="89bbd-157">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="89bbd-158">このエラーは、移動先オブジェクトがソース オブジェクトと同じ場合に返されます。</span><span class="sxs-lookup"><span data-stu-id="89bbd-158">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="89bbd-159">次の値は **、SPropProblemArray** 構造体で返されますが、CopyTo の戻り値として **返す値として返す必要があります**。</span><span class="sxs-lookup"><span data-stu-id="89bbd-159">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **CopyTo**.</span></span> <span data-ttu-id="89bbd-160">次のエラーは、1 つのプロパティに適用されます。</span><span class="sxs-lookup"><span data-stu-id="89bbd-160">The following errors apply to a single property:</span></span>
  
<span data-ttu-id="89bbd-161">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="89bbd-161">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="89bbd-162">このフラグMAPI_UNICODE設定され **、CopyTo** が Unicode をサポートしていないか、または設定されていない場合MAPI_UNICODE **CopyTo** は Unicode のみをサポートします。</span><span class="sxs-lookup"><span data-stu-id="89bbd-162">Either the MAPI_UNICODE flag was set and **CopyTo** does not support Unicode, or MAPI_UNICODE was not set and **CopyTo** supports only Unicode.</span></span> 
    
<span data-ttu-id="89bbd-163">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="89bbd-163">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="89bbd-164">プロパティは、読み取り専用プロパティなので、呼び出し元が変更することはできません。これは、移動先オブジェクトの所有者によって計算されます。</span><span class="sxs-lookup"><span data-stu-id="89bbd-164">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="89bbd-165">このエラーは重大ではありません。呼び出し元は、コピー操作の続行を許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89bbd-165">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="89bbd-166">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="89bbd-166">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="89bbd-167">プロパティの種類が無効です。</span><span class="sxs-lookup"><span data-stu-id="89bbd-167">The property type is invalid.</span></span>
    
<span data-ttu-id="89bbd-168">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="89bbd-168">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="89bbd-169">プロパティの種類は、呼び出し元が予期する型ではありません。</span><span class="sxs-lookup"><span data-stu-id="89bbd-169">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="89bbd-170">注釈</span><span class="sxs-lookup"><span data-stu-id="89bbd-170">Remarks</span></span>

<span data-ttu-id="89bbd-171">既定では **、IMAPIProp::CopyTo** メソッドは、現在のオブジェクトのすべてのプロパティをコピーまたは移動先オブジェクトに移動します。</span><span class="sxs-lookup"><span data-stu-id="89bbd-171">By default, the **IMAPIProp::CopyTo** method copies or moves all of the current object's properties to a destination object.</span></span> <span data-ttu-id="89bbd-172">**CopyTo** は、オブジェクトを正確にコピーまたは移動する必要がある場合に使用され、そのプロパティのすべてまたは大部分はそのまま使用されます。</span><span class="sxs-lookup"><span data-stu-id="89bbd-172">**CopyTo** is used when an object should be copied or moved exactly, with all or most of its properties intact.</span></span> 
  
<span data-ttu-id="89bbd-173">ソース オブジェクト内のサブオブジェクトは、自動的に操作に含まれてコピーまたは移動されます。</span><span class="sxs-lookup"><span data-stu-id="89bbd-173">Any subobjects in the source object are automatically included in the operation and are copied or moved in their entirety.</span></span> <span data-ttu-id="89bbd-174">既定では **、CopyTo** は、ソース オブジェクトのプロパティに一致するコピー先オブジェクトのプロパティを上書きします。</span><span class="sxs-lookup"><span data-stu-id="89bbd-174">By default, **CopyTo** overwrites any properties in the destination object that match properties from the source object.</span></span> <span data-ttu-id="89bbd-175">コピーまたは移動されたプロパティがコピー先オブジェクトに既に存在する場合、MAPI_NOREPLACE フラグが  _ulFlags_ パラメーターに設定されていない限り、既存のプロパティは新しいプロパティによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="89bbd-175">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="89bbd-176">上書きされない移動先オブジェクト内の既存の情報はそのまま残ります。</span><span class="sxs-lookup"><span data-stu-id="89bbd-176">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="89bbd-177">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="89bbd-177">Notes to implementers</span></span>

<span data-ttu-id="89bbd-178">CopyTo の完全な実装を提供するか **、MAPI** がサポート オブジェクトで提供する実装に依存できます。</span><span class="sxs-lookup"><span data-stu-id="89bbd-178">You can provide a full implementation of **CopyTo** or rely on the implementation that MAPI provides in its support object.</span></span> <span data-ttu-id="89bbd-179">MAPI 実装を使用する場合は **、IMAPISupport::D oCopyTo を呼び出します**。</span><span class="sxs-lookup"><span data-stu-id="89bbd-179">If you want to use the MAPI implementation, call **IMAPISupport::DoCopyTo**.</span></span> <span data-ttu-id="89bbd-180">ただし **、DoCopyTo** に処理を委任し、MAPI_DECLINE_OK フラグが渡された場合は、サポート呼び出しを回避し、代わりにMAPI_E_DECLINE_COPY返します。</span><span class="sxs-lookup"><span data-stu-id="89bbd-180">However, if you do delegate processing to **DoCopyTo** and you are passed the MAPI_DECLINE_OK flag, avoid the support call and return MAPI_E_DECLINE_COPY instead.</span></span> <span data-ttu-id="89bbd-181">MAPI は、フォルダーをコピーするときに発生する可能性のある再帰を回避するために、このフラグを使用して呼び出します。</span><span class="sxs-lookup"><span data-stu-id="89bbd-181">MAPI will call with this flag to avoid the possible recursion that can happen when folders are copied.</span></span> 
  
<span data-ttu-id="89bbd-182">コピー操作は長い場合がありますから、進行状況インジケーターを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89bbd-182">Because the copy operation can be lengthy, you should display a progress indicator.</span></span> <span data-ttu-id="89bbd-183">[lpProgress パラメーター](imapiprogressiunknown.md)に渡される _IMAPIProgress 実装_ がある場合は、その実装を使用します。</span><span class="sxs-lookup"><span data-stu-id="89bbd-183">Use the [IMAPIProgress](imapiprogressiunknown.md) implementation passed in the  _lpProgress_ parameter, if there is one.</span></span> <span data-ttu-id="89bbd-184">_lpProgress が_ **null** の場合は [、IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md)メソッドを呼び出して MAPI 実装を使用します。</span><span class="sxs-lookup"><span data-stu-id="89bbd-184">If  _lpProgress_ is **null**, call the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to use the MAPI implementation.</span></span> 
  
<span data-ttu-id="89bbd-185">宛先オブジェクトで既知の読み取り専用プロパティを設定しようとはしない。代わりにMAPI_E_NO_ACCESSを返します。</span><span class="sxs-lookup"><span data-stu-id="89bbd-185">Do not attempt to set any known read-only properties in the destination object; return MAPI_E_NO_ACCESS instead.</span></span>
  
<span data-ttu-id="89bbd-186">ソース オブジェクトと移動先オブジェクトは、同じインターフェイスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89bbd-186">The source and destination objects should use the same interfaces.</span></span> <span data-ttu-id="89bbd-187">_lpInterface MAPI_E_INVALID_PARAMETER設定されていない場合は、この値_ を返します。</span><span class="sxs-lookup"><span data-stu-id="89bbd-187">Return MAPI_E_INVALID_PARAMETER if  _lpInterface_ is not set.</span></span> 
  
<span data-ttu-id="89bbd-188">既知MAPI_E_INTERFACE_NOT_SUPPORTEDが除外されている場合は、この値を返します。</span><span class="sxs-lookup"><span data-stu-id="89bbd-188">Return MAPI_E_INTERFACE_NOT_SUPPORTED if all known interfaces are excluded.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="89bbd-189">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="89bbd-189">Notes to callers</span></span>

<span data-ttu-id="89bbd-190">このフラグを設定MAPI_DECLINE_OKしない。MAPI は、メッセージ ストア プロバイダーの CopyTo 実装への **呼び出しで** 使用します。</span><span class="sxs-lookup"><span data-stu-id="89bbd-190">Do not set the MAPI_DECLINE_OK flag; MAPI uses it in its calls to message store provider **CopyTo** implementations.</span></span> 
  
<span data-ttu-id="89bbd-191">コピー操作と移動操作には時間がかかる場合があります。このフラグを設定して進行状況インジケーターの表示をMAPI_DIALOGがあります。</span><span class="sxs-lookup"><span data-stu-id="89bbd-191">Because copy and move operations can take time, you should request the display of a progress indicator by setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="89bbd-192">_lpProgress パラメーター_ を **IMAPIProgress** の実装 (ある場合)、または null に設定 **できます**。</span><span class="sxs-lookup"><span data-stu-id="89bbd-192">You can set the  _lpProgress_ parameter to your implementation of **IMAPIProgress**, if you have one, or to **null**.</span></span> <span data-ttu-id="89bbd-193">_lpProgress が_ null の **場合\*\*\*\*、CopyTo は MAPI** が提供する既定の進行状況インジケーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="89bbd-193">If  _lpProgress_ is **null**, **CopyTo** will use the default progress indicator that MAPI provides.</span></span> 
  
<span data-ttu-id="89bbd-194">進行状況インジケーターの表示を抑制するには、進行状況フラグを設定MAPI_DIALOGできます。</span><span class="sxs-lookup"><span data-stu-id="89bbd-194">You can suppress the display of a progress indicator by not setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="89bbd-195">**CopyTo** は  _ulUIParam パラメーター_ と  _lpProgress_ パラメーターを無視し、インジケーターは表示されません。</span><span class="sxs-lookup"><span data-stu-id="89bbd-195">**CopyTo** will ignore the  _ulUIParam_ and  _lpProgress_ parameters and will not display the indicator.</span></span> 
  
 <span data-ttu-id="89bbd-196">**CopyTo** は、グローバルおよび個々のエラー、または 1 つ以上のプロパティで発生するエラーを報告できます。</span><span class="sxs-lookup"><span data-stu-id="89bbd-196">**CopyTo** can report global and individual errors, or errors that occur with one or more properties.</span></span> <span data-ttu-id="89bbd-197">これらの個々のエラーは **、SPropProblemArray 構造体に配置** されます。</span><span class="sxs-lookup"><span data-stu-id="89bbd-197">These individual errors are placed in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="89bbd-198">プロパティの問題配列構造パラメーターに対して、有効なポインターではなく **null** を渡して、プロパティ レベルでのエラー報告を抑制できます。</span><span class="sxs-lookup"><span data-stu-id="89bbd-198">You can suppress error reporting at the property level by passing **null**, instead of a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="89bbd-199">エラーに関する情報を受け取る場合は _、lppProblems_ パラメーターに有効な **SPropProblemArray** 構造体ポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="89bbd-199">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="89bbd-200">**CopyTo が** プロパティを返S_OK、構造内の個々のプロパティで発生する可能性のあるエラーを確認します。</span><span class="sxs-lookup"><span data-stu-id="89bbd-200">When **CopyTo** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="89bbd-201">**CopyTo が** エラーを返す場合 **、SPropProblemArray** 構造体に情報は返されません。</span><span class="sxs-lookup"><span data-stu-id="89bbd-201">When **CopyTo** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="89bbd-202">代わりに [、IMAPIProp::GetLastError](imapiprop-getlasterror.md) を呼び出して、詳細なエラー情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="89bbd-202">Instead, call [IMAPIProp::GetLastError](imapiprop-getlasterror.md) to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="89bbd-203">**CopyTo が** 関数を返S_OK [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、返される **SPropProblemArray** 構造体を解放します。</span><span class="sxs-lookup"><span data-stu-id="89bbd-203">If **CopyTo** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="89bbd-204">ソース オブジェクトの種類に固有のプロパティをコピーする場合は、コピー先オブジェクトの種類が同じことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89bbd-204">If you copy properties that are unique to the source object type, you must ensure that the destination object is of the same type.</span></span> <span data-ttu-id="89bbd-205">**CopyTo** を使用しても、通常、ある種類のオブジェクトに属するプロパティを別の種類のオブジェクトに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="89bbd-205">**CopyTo** does not prevent you from associating properties that typically belong to one type of object with another type of object.</span></span> <span data-ttu-id="89bbd-206">コピー先オブジェクトに合ったプロパティをコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="89bbd-206">It is up to you to copy properties that make sense for the destination object.</span></span> <span data-ttu-id="89bbd-207">たとえば、メッセージ のプロパティをアドレス帳コンテナーにコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="89bbd-207">For example, you should not copy message properties to an address book container.</span></span> 
  
<span data-ttu-id="89bbd-208">同じ型のオブジェクト間でコピーを行う場合は、オブジェクト ポインターを比較するか [、IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)を呼び出すことによって、ソース オブジェクトと移動先オブジェクトが同じ型である必要があります。</span><span class="sxs-lookup"><span data-stu-id="89bbd-208">To ensure that you copy between objects of the same type, check that the source and destination object are the same type, either by comparing object pointers or calling [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx).</span></span> <span data-ttu-id="89bbd-209">_lpInterface_ が指すインターフェイス識別子を、ソース オブジェクトの標準インターフェイスに設定します。</span><span class="sxs-lookup"><span data-stu-id="89bbd-209">Set the interface identifier pointed to by  _lpInterface_ to the standard interface for the source object.</span></span> <span data-ttu-id="89bbd-210">また、オブジェクトの種類またはプロパティ [(PidTagObjectType)](pidtagobjecttype-canonical-property.md)PR_OBJECT_TYPE **プロパティが** 2 つのオブジェクトで同じであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="89bbd-210">Also, be sure that the object type or **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property is the same for the two objects.</span></span> <span data-ttu-id="89bbd-211">たとえば、メッセージからコピーする場合は _、lpInterface_ を [IID_IMessage] に設定しPR_OBJECT_TYPE両方のオブジェクトMAPI_MESSAGE。</span><span class="sxs-lookup"><span data-stu-id="89bbd-211">For example, if you copy from a message, set  _lpInterface_ to IID_IMessage and the **PR_OBJECT_TYPE** for both objects to MAPI_MESSAGE.</span></span> 
  
<span data-ttu-id="89bbd-212">_lpDestObj_ パラメーターに無効なポインターが渡された場合、結果は予測できません。</span><span class="sxs-lookup"><span data-stu-id="89bbd-212">If an invalid pointer is passed in the  _lpDestObj_ parameter, the results are unpredictable.</span></span> 
  
<span data-ttu-id="89bbd-213">CopyTo 呼び出し **のプロパティを** 除外すると便利です。</span><span class="sxs-lookup"><span data-stu-id="89bbd-213">Excluding properties on a **CopyTo** call can be useful.</span></span> <span data-ttu-id="89bbd-214">たとえば、一部のオブジェクトには、メッセージ配信の日時など、オブジェクトの 1 つのインスタンスに固有のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="89bbd-214">For example, some objects have properties that are specific to a single instance of the object, such as the date and time of message delivery.</span></span> <span data-ttu-id="89bbd-215">メッセージを別のフォルダーにコピーするときにメッセージの配信時間をコピーしないようにするには、プロパティ タグ exclude 配列に **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) を指定します。</span><span class="sxs-lookup"><span data-stu-id="89bbd-215">To avoid copying a message's delivery time when you copy the message to a different folder, specify **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) in the property tag exclude array.</span></span> <span data-ttu-id="89bbd-216">メッセージの受信者リストを除外するには、PR_MESSAGE_RECIPIENTS **(** [PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) プロパティを exclude 配列に追加します。</span><span class="sxs-lookup"><span data-stu-id="89bbd-216">To exclude a message's recipient list, add the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property to the exclude array.</span></span> <span data-ttu-id="89bbd-217">メッセージの添付ファイルを除外するには、PR_MESSAGE_ATTACHMENTS **(** [PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) プロパティを配列に追加します。</span><span class="sxs-lookup"><span data-stu-id="89bbd-217">To exclude a message's attachments, add the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property to the array.</span></span>
  
<span data-ttu-id="89bbd-218">同様に、プロパティ タグの除外配列に **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) または **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) を含めて、フォルダーまたはアドレス帳コンテナーの階層またはコンテンツ テーブルのコピーまたは移動を防止します。</span><span class="sxs-lookup"><span data-stu-id="89bbd-218">Similarly, prevent the copying or moving of a folder or address book container's hierarchy or contents table by including **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag exclude array.</span></span>
  
<span data-ttu-id="89bbd-219">コピーまたは移動操作からプロパティを除外するには、プロパティ タグを  _lpExcludeProps パラメーターに含_ める必要があります。</span><span class="sxs-lookup"><span data-stu-id="89bbd-219">To exclude properties from the copy or move operation, include their property tags in the  _lpExcludeProps_ parameter.</span></span> <span data-ttu-id="89bbd-220">PROP_TAG マクロ **の結果** を渡して、プロパティ タグ配列内の特定の識別子からプロパティ タグを作成すると、その識別子を持つすべてのプロパティが除外されます。</span><span class="sxs-lookup"><span data-stu-id="89bbd-220">If you pass the results of the **PROP_TAG** macro to build a property tag from a specific identifier in the property tag array, all properties with that identifier will be excluded.</span></span> <span data-ttu-id="89bbd-221">たとえば、プロパティ タグ配列の次のエントリでは、型に関係なく、識別子を持つすべてのプロパティ0x8002除外されます。</span><span class="sxs-lookup"><span data-stu-id="89bbd-221">For example, the following entry in the property tag array causes all properties with an identifier of 0x8002 to be excluded, regardless of type:</span></span> 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
<span data-ttu-id="89bbd-222">プロパティ **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) プロパティ タグは  _、lpExcludeProps 配列に含_ めません。</span><span class="sxs-lookup"><span data-stu-id="89bbd-222">The **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) property tag cannot be included in the  _lpExcludeProps_ array.</span></span> 
  
<span data-ttu-id="89bbd-223">インターフェイスを除外する **CopyTo** 機能の使い方は、プロパティを除外する場合の便利さほど明らかではありません。</span><span class="sxs-lookup"><span data-stu-id="89bbd-223">The usefulness of the **CopyTo** feature for excluding interfaces is perhaps not as obvious as the usefulness of excluding properties.</span></span> <span data-ttu-id="89bbd-224">プロパティのグループに関する知識がないオブジェクトにコピーする場合は、インターフェイスを除外できます。</span><span class="sxs-lookup"><span data-stu-id="89bbd-224">You can exclude an interface when you copy to an object that has no knowledge of a group of properties.</span></span> <span data-ttu-id="89bbd-225">たとえば、フォルダーから添付ファイルにプロパティをコピーする場合、添付ファイルで使用できるプロパティは [、IMAPIProp](imapipropiunknown.md) 実装で使用できる汎用プロパティのみです。</span><span class="sxs-lookup"><span data-stu-id="89bbd-225">For example, if you copy properties from a folder to an attachment, the only properties that the attachment can work with are the generic properties available with any [IMAPIProp](imapipropiunknown.md) implementation.</span></span> <span data-ttu-id="89bbd-226">[IMAPIFolder をコピー](imapifolderimapicontainer.md)操作から除外すると、添付ファイルは、より具体的なフォルダー プロパティを受け取る必要がなされます。</span><span class="sxs-lookup"><span data-stu-id="89bbd-226">By excluding [IMAPIFolder](imapifolderimapicontainer.md) from the copy operation, the attachment will not receive any of the more specific folder properties.</span></span> 
  
<span data-ttu-id="89bbd-227">_rgiidExclude_ パラメーターを使用してインターフェイスを除外すると、そのインターフェイスから派生したインターフェイスもすべて除外されます。</span><span class="sxs-lookup"><span data-stu-id="89bbd-227">When you use the  _rgiidExclude_ parameter to exclude an interface, it also excludes all interfaces derived from that interface.</span></span> <span data-ttu-id="89bbd-228">たとえば [、IMAPIContainer を](imapicontainerimapiprop.md) 除外すると、プロバイダーの種類に応じてフォルダーまたはアドレス帳コンテナーが除外されます。</span><span class="sxs-lookup"><span data-stu-id="89bbd-228">For example, excluding [IMAPIContainer](imapicontainerimapiprop.md) causes folders or address book containers to be excluded, depending on the type of provider.</span></span> <span data-ttu-id="89bbd-229">**IMAPIProp** または [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)は、多くのインターフェイスから派生しますので、除外しません。</span><span class="sxs-lookup"><span data-stu-id="89bbd-229">Do not exclude **IMAPIProp** or [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) because so many interfaces derive from them.</span></span> 
  
<span data-ttu-id="89bbd-230">_lppProblems_ パラメーター MAPI_E_COMPUTED **SPropProblemArray** 構造体で返されるエラーを無視します。</span><span class="sxs-lookup"><span data-stu-id="89bbd-230">Ignore MAPI_E_COMPUTED errors returned in the **SPropProblemArray** structure in the  _lppProblems_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="89bbd-231">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="89bbd-231">MFCMAPI reference</span></span>

<span data-ttu-id="89bbd-232">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="89bbd-232">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="89bbd-233">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="89bbd-233">**File**</span></span>|<span data-ttu-id="89bbd-234">**関数**</span><span class="sxs-lookup"><span data-stu-id="89bbd-234">**Function**</span></span>|<span data-ttu-id="89bbd-235">**コメント**</span><span class="sxs-lookup"><span data-stu-id="89bbd-235">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="89bbd-236">File.cpp</span><span class="sxs-lookup"><span data-stu-id="89bbd-236">File.cpp</span></span>  <br/> |<span data-ttu-id="89bbd-237">LoadFromMSG</span><span class="sxs-lookup"><span data-stu-id="89bbd-237">LoadFromMSG</span></span>  <br/> |<span data-ttu-id="89bbd-238">MFCMAPI は **IMAPIProp::CopyTo** メソッドを使用して、.msg ファイルから [IMAPIMessageSite](imapimessagesiteiunknown.md) オブジェクトにプロパティをコピーします。</span><span class="sxs-lookup"><span data-stu-id="89bbd-238">MFCMAPI uses the **IMAPIProp::CopyTo** method to copy properties from a .msg file to an [IMAPIMessageSite](imapimessagesiteiunknown.md) object.</span></span>  <br/> |
|<span data-ttu-id="89bbd-239">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="89bbd-239">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="89bbd-240">CFolderDlg::HandlePaste</span><span class="sxs-lookup"><span data-stu-id="89bbd-240">CFolderDlg::HandlePaste</span></span>  <br/> |<span data-ttu-id="89bbd-241">MFCMAPI では **、IMAPIProp::CopyTo** メソッドを使用して、貼り付け操作中にソース メッセージからターゲット メッセージにプロパティをコピーします。</span><span class="sxs-lookup"><span data-stu-id="89bbd-241">MFCMAPI uses the **IMAPIProp::CopyTo** method to copy properties from a source message to a target message during a paste operation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="89bbd-242">関連項目</span><span class="sxs-lookup"><span data-stu-id="89bbd-242">See also</span></span>



[<span data-ttu-id="89bbd-243">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="89bbd-243">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="89bbd-244">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="89bbd-244">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="89bbd-245">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="89bbd-245">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)
  
[<span data-ttu-id="89bbd-246">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="89bbd-246">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="89bbd-247">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="89bbd-247">IMAPISupport::DoProgressDialog</span></span>](imapisupport-doprogressdialog.md)
  
[<span data-ttu-id="89bbd-248">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="89bbd-248">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
  
[<span data-ttu-id="89bbd-249">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="89bbd-249">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="89bbd-250">PidTagContainerContents 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="89bbd-250">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="89bbd-251">PidTagContainerHierarchy 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="89bbd-251">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="89bbd-252">PidTagMessageAttachments 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="89bbd-252">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="89bbd-253">PidTagMessageDeliveryTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="89bbd-253">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)
  
[<span data-ttu-id="89bbd-254">PidTagMessageRecipients 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="89bbd-254">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="89bbd-255">PidTagObjectType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="89bbd-255">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="89bbd-256">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="89bbd-256">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="89bbd-257">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="89bbd-257">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="89bbd-258">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="89bbd-258">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


<span data-ttu-id="89bbd-259">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="89bbd-259">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

