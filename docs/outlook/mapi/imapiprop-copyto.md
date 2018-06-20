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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: aa2869b1e3495bfb8a431e79a55d11a1ee1c5ca6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800649"
---
# <a name="imapipropcopyto"></a><span data-ttu-id="35cf1-103">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="35cf1-103">IMAPIProp::CopyTo</span></span>

  
  
<span data-ttu-id="35cf1-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="35cf1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="35cf1-105">明確に除外されたプロパティ以外のすべてのプロパティを移動またはコピーします。</span><span class="sxs-lookup"><span data-stu-id="35cf1-105">Copies or moves all properties, except for specifically excluded properties.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="35cf1-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="35cf1-106">Parameters</span></span>

 <span data-ttu-id="35cf1-107">_ciidExclude_</span><span class="sxs-lookup"><span data-stu-id="35cf1-107">_ciidExclude_</span></span>
  
> <span data-ttu-id="35cf1-108">[in]プロパティをコピーまたは移動した場合を除外するのにはインターフェイスの数。</span><span class="sxs-lookup"><span data-stu-id="35cf1-108">[in] The count of interfaces to exclude when properties are copied or moved.</span></span>
    
 <span data-ttu-id="35cf1-109">_rgiidExclude_</span><span class="sxs-lookup"><span data-stu-id="35cf1-109">_rgiidExclude_</span></span>
  
> <span data-ttu-id="35cf1-110">[in]補足情報をコピーまたは移動先のオブジェクトに移動するとき使用しないインターフェイスを指定するインターフェイス id (Iid) の配列です。</span><span class="sxs-lookup"><span data-stu-id="35cf1-110">[in] An array of interface identifiers (IIDs) that specify interfaces that should not be used when supplemental information is copied or moved to the destination object.</span></span>
    
 <span data-ttu-id="35cf1-111">_lpExcludeProps_</span><span class="sxs-lookup"><span data-stu-id="35cf1-111">_lpExcludeProps_</span></span>
  
> <span data-ttu-id="35cf1-112">[in]コピーから除外する必要がありますまたは移動操作のプロパティ タグを識別するプロパティ タグ配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="35cf1-112">[in] A pointer to a property tag array that identifies the property tags that should be excluded from the copy or move operation.</span></span> <span data-ttu-id="35cf1-113">_LpExcludeProps_パラメーターに**null**を渡す場合に、されるすべてのオブジェクトのプロパティがコピーまたは移動することを示します。</span><span class="sxs-lookup"><span data-stu-id="35cf1-113">Passing **null** in the  _lpExcludeProps_ parameter indicates that all of the object's properties should be copied or moved.</span></span> <span data-ttu-id="35cf1-114">**CopyTo**は、MAPI_E_INVALID_PARAMETER、**あう**、 [SPropProblemArray](spropproblemarray.md)構造体のメンバーが_lpExcludeProps_で示される場合は 0 に設定を取得します。</span><span class="sxs-lookup"><span data-stu-id="35cf1-114">**CopyTo** returns MAPI_E_INVALID_PARAMETER when the **cValues** member of the [SPropProblemArray](spropproblemarray.md) structure pointed to by  _lpExcludeProps_ is set to 0.</span></span> 
    
 <span data-ttu-id="35cf1-115">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="35cf1-115">_ulUIParam_</span></span>
  
> <span data-ttu-id="35cf1-116">[in]進行状況インジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="35cf1-116">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="35cf1-117">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="35cf1-117">_lpProgress_</span></span>
  
> <span data-ttu-id="35cf1-118">[in]進行状況インジケーターの実装へのポインター。</span><span class="sxs-lookup"><span data-stu-id="35cf1-118">[in] A pointer to a progress indicator implementation.</span></span> <span data-ttu-id="35cf1-119">**Null**が渡された場合、 _lpProgress_パラメーターで、MAPI は、進行状況の実装を提供します。</span><span class="sxs-lookup"><span data-stu-id="35cf1-119">If **null** is passed in the  _lpProgress_ parameter, MAPI provides the progress implementation.</span></span> <span data-ttu-id="35cf1-120">_UlFlags_パラメーターで MAPI_DIALOG フラグが設定されていない場合、 _lpProgress_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="35cf1-120">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="35cf1-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="35cf1-121">_lpInterface_</span></span>
  
> <span data-ttu-id="35cf1-122">[in]_LpDestObj_パラメーターが指すオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインターです。</span><span class="sxs-lookup"><span data-stu-id="35cf1-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object pointed to by the  _lpDestObj_ parameter.</span></span> <span data-ttu-id="35cf1-123">_LpInterface_パラメーターを**null**にするにはできません。</span><span class="sxs-lookup"><span data-stu-id="35cf1-123">The  _lpInterface_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="35cf1-124">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="35cf1-124">_lpDestObj_</span></span>
  
> <span data-ttu-id="35cf1-125">[in]コピーまたは移動先のプロパティを表示するオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="35cf1-125">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="35cf1-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="35cf1-126">_ulFlags_</span></span>
  
> <span data-ttu-id="35cf1-127">[in]コピーまたは移動操作を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="35cf1-127">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="35cf1-128">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="35cf1-128">The following flags can be set:</span></span>
    
<span data-ttu-id="35cf1-129">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="35cf1-129">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="35cf1-130">場合は、 **CopyTo**メソッドを呼び出して、 [IMAPISupport::DoCopyTo](imapisupport-docopyto.md)処理、コピーまたは移動操作は、代わりにすぐに MAPI_E_DECLINE_COPY のエラー値を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="35cf1-130">If **CopyTo** calls the [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) method to handle the copy or move operation, it should instead return immediately with the error value MAPI_E_DECLINE_COPY.</span></span> <span data-ttu-id="35cf1-131">MAPI_DECLINE_OK フラグは、再帰を制限するのには MAPI によって設定されています。</span><span class="sxs-lookup"><span data-stu-id="35cf1-131">The MAPI_DECLINE_OK flag is set by MAPI to limit recursion.</span></span> <span data-ttu-id="35cf1-132">クライアントでは、このフラグは設定されません。</span><span class="sxs-lookup"><span data-stu-id="35cf1-132">Clients do not set this flag.</span></span> 
    
<span data-ttu-id="35cf1-133">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="35cf1-133">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="35cf1-134">進行状況のインジケーターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="35cf1-134">Displays a progress indicator.</span></span>
    
<span data-ttu-id="35cf1-135">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="35cf1-135">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="35cf1-136">**CopyTo**は、コピー操作ではなく移動操作を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="35cf1-136">**CopyTo** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="35cf1-137">このフラグが設定されていない、 **CopyTo**は、コピー操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="35cf1-137">When this flag is not set, **CopyTo** performs a copy operation.</span></span> 
    
<span data-ttu-id="35cf1-138">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="35cf1-138">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="35cf1-139">コピー先オブジェクトの既存のプロパティを上書きしてはなりません。</span><span class="sxs-lookup"><span data-stu-id="35cf1-139">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="35cf1-140">このフラグが設定されていない、 **CopyTo**によって既存のプロパティが上書きされます。</span><span class="sxs-lookup"><span data-stu-id="35cf1-140">When this flag is not set, **CopyTo** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="35cf1-141">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="35cf1-141">_lppProblems_</span></span>
  
> <span data-ttu-id="35cf1-142">[で [チェック アウト]**SPropProblemArray**構造体へのポインターへのポインターの入力でそれ以外の場合、 **null**、エラー情報の必要性がないことを示します。</span><span class="sxs-lookup"><span data-stu-id="35cf1-142">[in, out] On input, a pointer to a pointer to an **SPropProblemArray** structure; otherwise, **null**, indicating no need for error information.</span></span> <span data-ttu-id="35cf1-143">_LppProblems_が入力時に有効なポインターである場合は、 **CopyTo**は、1 つまたは複数のプロパティのコピーでエラーに関する詳細な情報を返します。</span><span class="sxs-lookup"><span data-stu-id="35cf1-143">If  _lppProblems_ is a valid pointer on input, **CopyTo** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="35cf1-144">�߂�l</span><span class="sxs-lookup"><span data-stu-id="35cf1-144">Return value</span></span>

<span data-ttu-id="35cf1-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="35cf1-145">S_OK</span></span> 
  
> <span data-ttu-id="35cf1-146">プロパティは、正常にコピーまたは移動されています。</span><span class="sxs-lookup"><span data-stu-id="35cf1-146">The properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="35cf1-147">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="35cf1-147">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="35cf1-148">サブオブジェクトと同じ名前を表示するためにサブオブジェクトをコピーすることはできません- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) のプロパティで指定された、目的のオブジェクトに既に存在します。</span><span class="sxs-lookup"><span data-stu-id="35cf1-148">A subobject cannot be copied because a subobject with the same display name — specified by the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property — already exists in the destination object.</span></span> 
    
<span data-ttu-id="35cf1-149">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="35cf1-149">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="35cf1-150">サービス プロバイダーは、コピー操作を実装していません。</span><span class="sxs-lookup"><span data-stu-id="35cf1-150">The service provider does not implement the copy operation.</span></span>
    
<span data-ttu-id="35cf1-151">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="35cf1-151">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="35cf1-152">ソース オブジェクトが直接的または間接的にコピーまたは移動操作を実行するには、目的のオブジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="35cf1-152">The source object performing the copy or move operation directly or indirectly contains the destination object.</span></span> <span data-ttu-id="35cf1-153">重要な作業が実行された前に、この条件が検出された元とコピー先のオブジェクトを部分的に変更された可能性がありますので。</span><span class="sxs-lookup"><span data-stu-id="35cf1-153">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="35cf1-154">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="35cf1-154">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="35cf1-155">先のオブジェクトでは、 _lpInterface_パラメーターで指定されたインターフェイスはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="35cf1-155">The interface identified by the  _lpInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="35cf1-156">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="35cf1-156">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="35cf1-157">呼び出し元が十分なアクセス許可を持っているオブジェクトにアクセスしようとしました。</span><span class="sxs-lookup"><span data-stu-id="35cf1-157">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="35cf1-158">目的のオブジェクトは、ソース オブジェクトと同じ場合、このエラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="35cf1-158">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="35cf1-159">次の値が返される、 **SPropProblemArray**構造体には戻り値としてではなく**CopyTo**です。</span><span class="sxs-lookup"><span data-stu-id="35cf1-159">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **CopyTo**.</span></span> <span data-ttu-id="35cf1-160">次のエラーは、1 つのプロパティに適用されます。</span><span class="sxs-lookup"><span data-stu-id="35cf1-160">The following errors apply to a single property:</span></span>
  
<span data-ttu-id="35cf1-161">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="35cf1-161">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="35cf1-162">か、MAPI_UNICODE フラグが設定された**CopyTo**は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、 **CopyTo**は、Unicode だけをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="35cf1-162">Either the MAPI_UNICODE flag was set and **CopyTo** does not support Unicode, or MAPI_UNICODE was not set and **CopyTo** supports only Unicode.</span></span> 
    
<span data-ttu-id="35cf1-163">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="35cf1-163">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="35cf1-164">コピー先オブジェクトの所有者によって計算される、読み取り専用プロパティであるために、呼び出し元がプロパティを変更できません。</span><span class="sxs-lookup"><span data-stu-id="35cf1-164">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="35cf1-165">このエラーは重大です。呼び出し元は、コピー操作を続行を許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="35cf1-165">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="35cf1-166">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="35cf1-166">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="35cf1-167">プロパティの型が正しくありません。</span><span class="sxs-lookup"><span data-stu-id="35cf1-167">The property type is invalid.</span></span>
    
<span data-ttu-id="35cf1-168">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="35cf1-168">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="35cf1-169">プロパティの型は、呼び出し元の型ではありません。</span><span class="sxs-lookup"><span data-stu-id="35cf1-169">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="35cf1-170">備考</span><span class="sxs-lookup"><span data-stu-id="35cf1-170">Remarks</span></span>

<span data-ttu-id="35cf1-171">既定では、 **IMAPIProp::CopyTo**メソッドは、コピーまたは、すべての現在のオブジェクトのプロパティをコピー先のオブジェクトに移動します。</span><span class="sxs-lookup"><span data-stu-id="35cf1-171">By default, the **IMAPIProp::CopyTo** method copies or moves all of the current object's properties to a destination object.</span></span> <span data-ttu-id="35cf1-172">**CopyTo**は、オブジェクトをコピーまたはすべてまたはほとんどのプロパティをそのままの状態を正確に移動する必要があるときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="35cf1-172">**CopyTo** is used when an object should be copied or moved exactly, with all or most of its properties intact.</span></span> 
  
<span data-ttu-id="35cf1-173">ソース オブジェクトのサブオブジェクト操作に自動的に含まれ、コピーまたは移動の全体。</span><span class="sxs-lookup"><span data-stu-id="35cf1-173">Any subobjects in the source object are automatically included in the operation and are copied or moved in their entirety.</span></span> <span data-ttu-id="35cf1-174">**CopyTo**は既定では、ソース オブジェクトからプロパティに一致する対象のオブジェクトのプロパティを上書きします。</span><span class="sxs-lookup"><span data-stu-id="35cf1-174">By default, **CopyTo** overwrites any properties in the destination object that match properties from the source object.</span></span> <span data-ttu-id="35cf1-175">コピー先オブジェクトにコピーまたは移動先のプロパティのいずれかの場合、 _ulFlags_パラメーターに MAPI_NOREPLACE フラグが設定されていない限り、既存のプロパティが新しいプロパティによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="35cf1-175">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="35cf1-176">変更は上書きされず、変換先オブジェクトの既存の情報は行われないです。</span><span class="sxs-lookup"><span data-stu-id="35cf1-176">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="35cf1-177">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="35cf1-177">Notes to implementers</span></span>

<span data-ttu-id="35cf1-178">**CopyTo**の完全な実装を提供するか、サポート オブジェクトは、MAPI が提供する実装に依存します。</span><span class="sxs-lookup"><span data-stu-id="35cf1-178">You can provide a full implementation of **CopyTo** or rely on the implementation that MAPI provides in its support object.</span></span> <span data-ttu-id="35cf1-179">MAPI 実装を使用する場合は、 **IMAPISupport::DoCopyTo**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="35cf1-179">If you want to use the MAPI implementation, call **IMAPISupport::DoCopyTo**.</span></span> <span data-ttu-id="35cf1-180">ただし、 **DoCopyTo**に処理を委任する操作を行います、MAPI_DECLINE_OK フラグが渡されますが、サポートの呼び出しを避けるため、代わりに MAPI_E_DECLINE_COPY を返します。</span><span class="sxs-lookup"><span data-stu-id="35cf1-180">However, if you do delegate processing to **DoCopyTo** and you are passed the MAPI_DECLINE_OK flag, avoid the support call and return MAPI_E_DECLINE_COPY instead.</span></span> <span data-ttu-id="35cf1-181">MAPI は、フォルダーがコピーされるときに発生する可能性のある再帰を回避するには、このフラグを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="35cf1-181">MAPI will call with this flag to avoid the possible recursion that can happen when folders are copied.</span></span> 
  
<span data-ttu-id="35cf1-182">コピー操作できますが、時間がかかるため、進行状況インジケーターを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="35cf1-182">Because the copy operation can be lengthy, you should display a progress indicator.</span></span> <span data-ttu-id="35cf1-183">いずれかを使用する必要がある場合は、 _lpProgress_パラメーターに渡された[IMAPIProgress](imapiprogressiunknown.md)の実装を使用します。</span><span class="sxs-lookup"><span data-stu-id="35cf1-183">Use the [IMAPIProgress](imapiprogressiunknown.md) implementation passed in the  _lpProgress_ parameter, if there is one.</span></span> <span data-ttu-id="35cf1-184">_LpProgress_が**null**の場合は、MAPI 実装を使用する[IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="35cf1-184">If  _lpProgress_ is **null**, call the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to use the MAPI implementation.</span></span> 
  
<span data-ttu-id="35cf1-185">目的のオブジェクトのすべての既知の読み取り専用プロパティを設定しようとはしないで代わりに MAPI_E_NO_ACCESS を返します。</span><span class="sxs-lookup"><span data-stu-id="35cf1-185">Do not attempt to set any known read-only properties in the destination object; return MAPI_E_NO_ACCESS instead.</span></span>
  
<span data-ttu-id="35cf1-186">元とコピー先のオブジェクトは、同じインターフェイスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="35cf1-186">The source and destination objects should use the same interfaces.</span></span> <span data-ttu-id="35cf1-187">_LpInterface_が設定されていない場合は、MAPI_E_INVALID_PARAMETER を返します。</span><span class="sxs-lookup"><span data-stu-id="35cf1-187">Return MAPI_E_INVALID_PARAMETER if  _lpInterface_ is not set.</span></span> 
  
<span data-ttu-id="35cf1-188">既知のすべてのインタ フェースが除外されている場合は、MAPI_E_INTERFACE_NOT_SUPPORTED を返します。</span><span class="sxs-lookup"><span data-stu-id="35cf1-188">Return MAPI_E_INTERFACE_NOT_SUPPORTED if all known interfaces are excluded.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="35cf1-189">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="35cf1-189">Notes to callers</span></span>

<span data-ttu-id="35cf1-190">MAPI_DECLINE_OK フラグを設定しません。MAPI の呼び出しでメッセージのストア プロバイダーの**CopyTo**の実装に使用します。</span><span class="sxs-lookup"><span data-stu-id="35cf1-190">Do not set the MAPI_DECLINE_OK flag; MAPI uses it in its calls to message store provider **CopyTo** implementations.</span></span> 
  
<span data-ttu-id="35cf1-191">のコピーと移動の操作に時間がかかる場合、MAPI_DIALOG フラグを設定することにより、進行状況インジケーターの表示を要求する必要があります。</span><span class="sxs-lookup"><span data-stu-id="35cf1-191">Because copy and move operations can take time, you should request the display of a progress indicator by setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="35cf1-192">**IMAPIProgress**で、いずれかの操作をした場合の実装に、または**null**には、 _lpProgress_パラメーターを設定できます。</span><span class="sxs-lookup"><span data-stu-id="35cf1-192">You can set the  _lpProgress_ parameter to your implementation of **IMAPIProgress**, if you have one, or to **null**.</span></span> <span data-ttu-id="35cf1-193">_LpProgress_が**null**の場合は、 **CopyTo**は MAPI が提供する既定の進行状況のインジケーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="35cf1-193">If  _lpProgress_ is **null**, **CopyTo** will use the default progress indicator that MAPI provides.</span></span> 
  
<span data-ttu-id="35cf1-194">MAPI_DIALOG フラグを設定しない、進行状況インジケーターの表示を抑制できます。</span><span class="sxs-lookup"><span data-stu-id="35cf1-194">You can suppress the display of a progress indicator by not setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="35cf1-195">**CopyTo**は、 _ulUIParam_と_lpProgress_のパラメーターは無視され、インジケーターは表示されません。</span><span class="sxs-lookup"><span data-stu-id="35cf1-195">**CopyTo** will ignore the  _ulUIParam_ and  _lpProgress_ parameters and will not display the indicator.</span></span> 
  
 <span data-ttu-id="35cf1-196">**CopyTo**は、グローバルおよび個々 のエラーの場合、または 1 つまたは複数のプロパティを使用して発生したエラーを報告できます。</span><span class="sxs-lookup"><span data-stu-id="35cf1-196">**CopyTo** can report global and individual errors, or errors that occur with one or more properties.</span></span> <span data-ttu-id="35cf1-197">これらの個々 のエラーは、 **SPropProblemArray**構造体に格納されます。</span><span class="sxs-lookup"><span data-stu-id="35cf1-197">These individual errors are placed in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="35cf1-198">**Null**、代わりに、プロパティの問題の配列構造体のパラメーターの有効なポインターを渡すことにより、プロパティ レベルでレポートのエラーを抑制できます。</span><span class="sxs-lookup"><span data-stu-id="35cf1-198">You can suppress error reporting at the property level by passing **null**, instead of a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="35cf1-199">エラーに関する情報を受信する場合は、 _lppProblems_パラメーターに有効な**SPropProblemArray**構造体のポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="35cf1-199">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="35cf1-200">**CopyTo**に S_OK が返されるときは、構造内の個々 のプロパティを持つ可能性のあるエラーを確認します。</span><span class="sxs-lookup"><span data-stu-id="35cf1-200">When **CopyTo** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="35cf1-201">**CopyTo**にエラーが返されるとき、 **SPropProblemArray**構造体の情報は返されません。</span><span class="sxs-lookup"><span data-stu-id="35cf1-201">When **CopyTo** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="35cf1-202">代わりに、詳細なエラー情報を取得するために[IMAPIProp::GetLastError](imapiprop-getlasterror.md) 。</span><span class="sxs-lookup"><span data-stu-id="35cf1-202">Instead, call [IMAPIProp::GetLastError](imapiprop-getlasterror.md) to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="35cf1-203">**CopyTo**には、S_OK が返された場合は、 [MAPIFreeBuffer](mapifreebuffer.md)関数の呼び出しによって返された**SPropProblemArray**構造体を解放します。</span><span class="sxs-lookup"><span data-stu-id="35cf1-203">If **CopyTo** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="35cf1-204">ソース オブジェクトの種類に固有のプロパティをコピーする場合、同じ種類の対象になるオブジェクトであるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="35cf1-204">If you copy properties that are unique to the source object type, you must ensure that the destination object is of the same type.</span></span> <span data-ttu-id="35cf1-205">**CopyTo**ができないから、通常、1 種類のオブジェクトの別の種類のオブジェクトに属するプロパティを関連付けることです。</span><span class="sxs-lookup"><span data-stu-id="35cf1-205">**CopyTo** does not prevent you from associating properties that typically belong to one type of object with another type of object.</span></span> <span data-ttu-id="35cf1-206">変換先オブジェクトのプロパティをコピーすることの責任です。</span><span class="sxs-lookup"><span data-stu-id="35cf1-206">It is up to you to copy properties that make sense for the destination object.</span></span> <span data-ttu-id="35cf1-207">などのアドレス帳コンテナーにメッセージのプロパティをコピーする必要がありますされません。</span><span class="sxs-lookup"><span data-stu-id="35cf1-207">For example, you should not copy message properties to an address book container.</span></span> 
  
<span data-ttu-id="35cf1-208">同じ種類のオブジェクト間でコピーすることを確認するには、元とコピー先のオブジェクトが同じ型、オブジェクトのポインターを比較するか、 [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx)を呼び出すことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="35cf1-208">To ensure that you copy between objects of the same type, check that the source and destination object are the same type, either by comparing object pointers or calling [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx).</span></span> <span data-ttu-id="35cf1-209">ソース オブジェクトの標準的なインタ フェースを_lpInterface_が指すインターフェイスの識別子を設定します。</span><span class="sxs-lookup"><span data-stu-id="35cf1-209">Set the interface identifier pointed to by  _lpInterface_ to the standard interface for the source object.</span></span> <span data-ttu-id="35cf1-210">また、オブジェクト タイプまたは**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) のプロパティは、2 つのオブジェクトに対して同じであることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="35cf1-210">Also, be sure that the object type or **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property is the same for the two objects.</span></span> <span data-ttu-id="35cf1-211">たとえば、メッセージからコピーする場合は、IID_IMessage と MAPI_MESSAGE を両方のオブジェクトの**PR_OBJECT_TYPE**に_lpInterface_を設定します。</span><span class="sxs-lookup"><span data-stu-id="35cf1-211">For example, if you copy from a message, set  _lpInterface_ to IID_IMessage and the **PR_OBJECT_TYPE** for both objects to MAPI_MESSAGE.</span></span> 
  
<span data-ttu-id="35cf1-212">場合は、 _lpDestObj_パラメーターに無効なポインターが渡されると、結果は予測できません。</span><span class="sxs-lookup"><span data-stu-id="35cf1-212">If an invalid pointer is passed in the  _lpDestObj_ parameter, the results are unpredictable.</span></span> 
  
<span data-ttu-id="35cf1-213">**CopyTo**の呼び出しでプロパティを除外できます。</span><span class="sxs-lookup"><span data-stu-id="35cf1-213">Excluding properties on a **CopyTo** call can be useful.</span></span> <span data-ttu-id="35cf1-214">などのいくつかのオブジェクトには、日付と時刻のメッセージの配信など、オブジェクトの単一のインスタンスに固有のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="35cf1-214">For example, some objects have properties that are specific to a single instance of the object, such as the date and time of message delivery.</span></span> <span data-ttu-id="35cf1-215">プロパティをコピーすると、メッセージを別のフォルダーに**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) を指定するメッセージの配信時刻をコピーしないようにするのには、タグは、配列を除外します。</span><span class="sxs-lookup"><span data-stu-id="35cf1-215">To avoid copying a message's delivery time when you copy the message to a different folder, specify **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) in the property tag exclude array.</span></span> <span data-ttu-id="35cf1-216">メッセージの受信者の一覧を除外するには、除外アレイに**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) のプロパティを追加します。</span><span class="sxs-lookup"><span data-stu-id="35cf1-216">To exclude a message's recipient list, add the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property to the exclude array.</span></span> <span data-ttu-id="35cf1-217">メッセージの添付ファイルを除外するには、配列に**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) のプロパティを追加します。</span><span class="sxs-lookup"><span data-stu-id="35cf1-217">To exclude a message's attachments, add the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property to the array.</span></span>
  
<span data-ttu-id="35cf1-218">同様に、コピーまたは移動するフォルダーまたはアドレス帳コンテナーの階層構造または内容のテーブルを防ぐため、 **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) または**PR_CONTAINER_CONTENTS** ([を含めることで、PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) プロパティのタグは配列を除外します。</span><span class="sxs-lookup"><span data-stu-id="35cf1-218">Similarly, prevent the copying or moving of a folder or address book container's hierarchy or contents table by including **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag exclude array.</span></span>
  
<span data-ttu-id="35cf1-219">除外するプロパティのコピーか移動の操作を_lpExcludeProps_パラメーターで、プロパティ タグが含まれます。</span><span class="sxs-lookup"><span data-stu-id="35cf1-219">To exclude properties from the copy or move operation, include their property tags in the  _lpExcludeProps_ parameter.</span></span> <span data-ttu-id="35cf1-220">プロパティ タグ プロパティ タグ配列内の特定の識別子からを構築する**PROP_TAG**マクロの結果を渡すと、その識別子を持つすべてのプロパティは除外されます。</span><span class="sxs-lookup"><span data-stu-id="35cf1-220">If you pass the results of the **PROP_TAG** macro to build a property tag from a specific identifier in the property tag array, all properties with that identifier will be excluded.</span></span> <span data-ttu-id="35cf1-221">たとえば、プロパティ タグ配列内の次のエントリでは、種類に関係なく、除外する 0x8002 の識別子を持つすべてのプロパティが発生します。</span><span class="sxs-lookup"><span data-stu-id="35cf1-221">For example, the following entry in the property tag array causes all properties with an identifier of 0x8002 to be excluded, regardless of type:</span></span> 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
<span data-ttu-id="35cf1-222">_LpExcludeProps_アレイでは、 **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) のプロパティ タグを含めることができません。</span><span class="sxs-lookup"><span data-stu-id="35cf1-222">The **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) property tag cannot be included in the  _lpExcludeProps_ array.</span></span> 
  
<span data-ttu-id="35cf1-223">インタ フェースを除外するための**CopyTo**機能の有用性はおそらくプロパティを除外することの有用性としては明らかにします。</span><span class="sxs-lookup"><span data-stu-id="35cf1-223">The usefulness of the **CopyTo** feature for excluding interfaces is perhaps not as obvious as the usefulness of excluding properties.</span></span> <span data-ttu-id="35cf1-224">プロパティのグループの知識を持たないオブジェクトにコピーするときは、インタ フェースを除外できます。</span><span class="sxs-lookup"><span data-stu-id="35cf1-224">You can exclude an interface when you copy to an object that has no knowledge of a group of properties.</span></span> <span data-ttu-id="35cf1-225">などのプロパティをフォルダーから添付ファイルをコピーする場合、添付ファイルが使用できる唯一のプロパティ、 [IMAPIProp](imapipropiunknown.md)実装で利用可能な汎用的なプロパティです。</span><span class="sxs-lookup"><span data-stu-id="35cf1-225">For example, if you copy properties from a folder to an attachment, the only properties that the attachment can work with are the generic properties available with any [IMAPIProp](imapipropiunknown.md) implementation.</span></span> <span data-ttu-id="35cf1-226">コピー操作から[IMAPIFolder](imapifolderimapicontainer.md)を除外することで添付ファイルを受信しません、特定のフォルダーのプロパティのいずれか。</span><span class="sxs-lookup"><span data-stu-id="35cf1-226">By excluding [IMAPIFolder](imapifolderimapicontainer.md) from the copy operation, the attachment will not receive any of the more specific folder properties.</span></span> 
  
<span data-ttu-id="35cf1-227">インタ フェースを除外するのには、 _rgiidExclude_パラメーターを使用する場合も、そのインターフェイスから派生するすべてのインタ フェースを除外します。</span><span class="sxs-lookup"><span data-stu-id="35cf1-227">When you use the  _rgiidExclude_ parameter to exclude an interface, it also excludes all interfaces derived from that interface.</span></span> <span data-ttu-id="35cf1-228">たとえば、 [IMAPIContainer](imapicontainerimapiprop.md)を除外すると、フォルダーまたはプロバイダーの種類によって、除外するアドレス帳のコンテナー。</span><span class="sxs-lookup"><span data-stu-id="35cf1-228">For example, excluding [IMAPIContainer](imapicontainerimapiprop.md) causes folders or address book containers to be excluded, depending on the type of provider.</span></span> <span data-ttu-id="35cf1-229">非常に多くのインターフェイスは、それらから派生するために**IMAPIProp**または[IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx)を除外しません。</span><span class="sxs-lookup"><span data-stu-id="35cf1-229">Do not exclude **IMAPIProp** or [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) because so many interfaces derive from them.</span></span> 
  
<span data-ttu-id="35cf1-230">MAPI_E_COMPUTED を無視して、 **SPropProblemArray**パラメーターに構造体の_lppProblems_でエラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="35cf1-230">Ignore MAPI_E_COMPUTED errors returned in the **SPropProblemArray** structure in the  _lppProblems_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="35cf1-231">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="35cf1-231">MFCMAPI reference</span></span>

<span data-ttu-id="35cf1-232">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="35cf1-232">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="35cf1-233">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="35cf1-233">**File**</span></span>|<span data-ttu-id="35cf1-234">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="35cf1-234">**Function**</span></span>|<span data-ttu-id="35cf1-235">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="35cf1-235">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="35cf1-236">File.cpp</span><span class="sxs-lookup"><span data-stu-id="35cf1-236">File.cpp</span></span>  <br/> |<span data-ttu-id="35cf1-237">LoadFromMSG</span><span class="sxs-lookup"><span data-stu-id="35cf1-237">LoadFromMSG</span></span>  <br/> |<span data-ttu-id="35cf1-238">MFCMAPI では、 [IMAPIMessageSite](imapimessagesiteiunknown.md)オブジェクトに .msg ファイルからプロパティをコピーするのには、 **IMAPIProp::CopyTo**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="35cf1-238">MFCMAPI uses the **IMAPIProp::CopyTo** method to copy properties from a .msg file to an [IMAPIMessageSite](imapimessagesiteiunknown.md) object.</span></span>  <br/> |
|<span data-ttu-id="35cf1-239">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="35cf1-239">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="35cf1-240">CFolderDlg::HandlePaste</span><span class="sxs-lookup"><span data-stu-id="35cf1-240">CFolderDlg::HandlePaste</span></span>  <br/> |<span data-ttu-id="35cf1-241">MFCMAPI では、 **IMAPIProp::CopyTo**メソッドを使用して、貼り付けの操作中に、対象のメッセージを送信元のメッセージからプロパティをコピーします。</span><span class="sxs-lookup"><span data-stu-id="35cf1-241">MFCMAPI uses the **IMAPIProp::CopyTo** method to copy properties from a source message to a target message during a paste operation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="35cf1-242">関連項目</span><span class="sxs-lookup"><span data-stu-id="35cf1-242">See also</span></span>



[<span data-ttu-id="35cf1-243">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="35cf1-243">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="35cf1-244">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="35cf1-244">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="35cf1-245">IMAPIMessageSite: IUnknown</span><span class="sxs-lookup"><span data-stu-id="35cf1-245">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)
  
[<span data-ttu-id="35cf1-246">IMAPIProgress: IUnknown</span><span class="sxs-lookup"><span data-stu-id="35cf1-246">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="35cf1-247">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="35cf1-247">IMAPISupport::DoProgressDialog</span></span>](imapisupport-doprogressdialog.md)
  
[<span data-ttu-id="35cf1-248">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="35cf1-248">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
  
[<span data-ttu-id="35cf1-249">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="35cf1-249">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="35cf1-250">PidTagContainerContents の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="35cf1-250">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="35cf1-251">PidTagContainerHierarchy の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="35cf1-251">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="35cf1-252">PidTagMessageAttachments の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="35cf1-252">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="35cf1-253">PidTagMessageDeliveryTime の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="35cf1-253">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)
  
[<span data-ttu-id="35cf1-254">PidTagMessageRecipients の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="35cf1-254">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="35cf1-255">PidTagObjectType の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="35cf1-255">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="35cf1-256">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="35cf1-256">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="35cf1-257">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="35cf1-257">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="35cf1-258">IMAPIProp: IUnknown</span><span class="sxs-lookup"><span data-stu-id="35cf1-258">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


<span data-ttu-id="35cf1-259">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="35cf1-259">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

