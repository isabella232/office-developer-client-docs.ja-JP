---
title: IMAPIPropCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.CopyProps
api_type:
- COM
ms.assetid: f65da1c8-d49b-44e8-8c66-9c53d088d334
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7319f1abb4a74ee17b0a4a1220215c29434d256b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398403"
---
# <a name="imapipropcopyprops"></a><span data-ttu-id="13d76-103">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="13d76-103">IMAPIProp::CopyProps</span></span>

  
  
<span data-ttu-id="13d76-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13d76-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13d76-105">選択したプロパティのコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="13d76-105">Copies or moves selected properties.</span></span> 
  
```cpp
HRESULT CopyProps(
  LPSPropTagArray lpIncludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="13d76-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="13d76-106">Parameters</span></span>

 <span data-ttu-id="13d76-107">_lpIncludeProps_</span><span class="sxs-lookup"><span data-stu-id="13d76-107">_lpIncludeProps_</span></span>
  
> <span data-ttu-id="13d76-108">[in]コピーまたは移動するにはプロパティを指定するプロパティ タグ配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="13d76-108">[in] A pointer to a property tag array that specifies the properties to copy or move.</span></span> <span data-ttu-id="13d76-109">**PR_NULL**([PidTagNull](pidtagnull-canonical-property.md)) は、配列に含めることができません。</span><span class="sxs-lookup"><span data-stu-id="13d76-109">**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) cannot be included in the array.</span></span> <span data-ttu-id="13d76-110">_LpIncludeProps_パラメーターを**null**にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="13d76-110">The  _lpIncludeProps_ parameter cannot be **null**.</span></span>
    
 <span data-ttu-id="13d76-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="13d76-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="13d76-112">[in]進行状況インジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="13d76-112">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="13d76-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="13d76-113">_lpProgress_</span></span>
  
> <span data-ttu-id="13d76-114">[in]進行状況のインジケーターの実装へのポインター。</span><span class="sxs-lookup"><span data-stu-id="13d76-114">[in] A pointer to an implementation of a progress indicator.</span></span> <span data-ttu-id="13d76-115">**Null**が渡された場合、 _lpProgress_パラメーターで、MAPI 実装を使用して進行状況のインジケーターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="13d76-115">If **null** is passed in the  _lpProgress_ parameter, the progress indicator is displayed by using the MAPI implementation.</span></span> <span data-ttu-id="13d76-116">_UlFlags_パラメーターで MAPI_DIALOG フラグが設定されていない場合、 _lpProgress_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="13d76-116">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="13d76-117">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="13d76-117">_lpInterface_</span></span>
  
> <span data-ttu-id="13d76-118">[in]_LpDestObj_パラメーターが指すオブジェクトにアクセスするために使用する必要がありますインターフェイスを表すインターフェイス識別子 (IID) へのポインターです。</span><span class="sxs-lookup"><span data-stu-id="13d76-118">[in] A pointer to the interface identifier (IID) that represents the interface that must be used to access the object pointed to by the  _lpDestObj_ parameter.</span></span> <span data-ttu-id="13d76-119">_LpInterface_パラメーターを**null**にするにはできません。</span><span class="sxs-lookup"><span data-stu-id="13d76-119">The  _lpInterface_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="13d76-120">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="13d76-120">_lpDestObj_</span></span>
  
> <span data-ttu-id="13d76-121">[in]コピーまたは移動先のプロパティを表示するオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="13d76-121">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="13d76-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="13d76-122">_ulFlags_</span></span>
  
> <span data-ttu-id="13d76-123">[in]コピーまたは移動操作を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="13d76-123">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="13d76-124">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="13d76-124">The following flags can be set:</span></span>
    
<span data-ttu-id="13d76-125">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="13d76-125">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="13d76-126">**CopyProps**は、処理、コピーまたは移動の操作をするには、 [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md)メソッドを呼び出して場合、代わりにすぐに MAPI_E_DECLINE_COPY のエラー値を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="13d76-126">If **CopyProps** calls the [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method to handle the copy or move operation, it should instead return immediately with the error value MAPI_E_DECLINE_COPY.</span></span> <span data-ttu-id="13d76-127">MAPI_DECLINE_OK フラグは、再帰を制限するのには MAPI によって設定されています。</span><span class="sxs-lookup"><span data-stu-id="13d76-127">The MAPI_DECLINE_OK flag is set by MAPI to limit recursion.</span></span> <span data-ttu-id="13d76-128">クライアントでは、このフラグは設定されません。</span><span class="sxs-lookup"><span data-stu-id="13d76-128">Clients do not set this flag.</span></span> 
    
<span data-ttu-id="13d76-129">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="13d76-129">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="13d76-130">進行状況のインジケーターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="13d76-130">Displays a progress indicator.</span></span>
    
<span data-ttu-id="13d76-131">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="13d76-131">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="13d76-132">**CopyProps**は、コピー操作ではなく移動操作を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13d76-132">**CopyProps** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="13d76-133">このフラグが設定されていない場合、 **CopyProps**は、コピー操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="13d76-133">When this flag is not set, **CopyProps** performs a copy operation.</span></span> 
    
<span data-ttu-id="13d76-134">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="13d76-134">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="13d76-135">コピー先オブジェクトの既存のプロパティを上書きしてはなりません。</span><span class="sxs-lookup"><span data-stu-id="13d76-135">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="13d76-136">このフラグが設定されていない場合、 **CopyProps**には、既存のプロパティが上書きされます。</span><span class="sxs-lookup"><span data-stu-id="13d76-136">When this flag is not set, **CopyProps** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="13d76-137">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="13d76-137">_lppProblems_</span></span>
  
> <span data-ttu-id="13d76-138">[で [チェック アウト][SPropProblemArray](spropproblemarray.md)構造体へのポインターへのポインターの入力でそれ以外の場合、 **null**、エラー情報の必要性がないことを示します。</span><span class="sxs-lookup"><span data-stu-id="13d76-138">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, **null**, indicating that there is no need for error information.</span></span> <span data-ttu-id="13d76-139">_LppProblems_が入力時に有効なポインターである場合は、 **CopyProps**は、1 つまたは複数のプロパティのコピーでエラーに関する詳細な情報を返します。</span><span class="sxs-lookup"><span data-stu-id="13d76-139">If  _lppProblems_ is a valid pointer on input, **CopyProps** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="13d76-140">戻り値</span><span class="sxs-lookup"><span data-stu-id="13d76-140">Return value</span></span>

<span data-ttu-id="13d76-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="13d76-141">S_OK</span></span> 
  
> <span data-ttu-id="13d76-142">プロパティは、正常にコピーまたは移動されています。</span><span class="sxs-lookup"><span data-stu-id="13d76-142">Properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="13d76-143">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="13d76-143">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="13d76-144">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティで定義されている、同じ表示名のサブオブジェクトは、目的のオブジェクトに既に存在するため、サブオブジェクトをコピーできません。</span><span class="sxs-lookup"><span data-stu-id="13d76-144">A subobject cannot be copied because a subobject with the same display name, defined by the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, already exists in the destination object.</span></span> 
    
<span data-ttu-id="13d76-145">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="13d76-145">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="13d76-146">サービス プロバイダーは、コピー操作を実装していません。</span><span class="sxs-lookup"><span data-stu-id="13d76-146">The service provider does not implement the copy operation.</span></span>
    
<span data-ttu-id="13d76-147">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="13d76-147">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="13d76-148">ソース オブジェクトが直接的または間接的にコピーまたは移動操作を実行するには、目的のオブジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="13d76-148">The source object performing the copy or move operation directly or indirectly contains the destination object.</span></span> <span data-ttu-id="13d76-149">重要な作業が実行された前に、この条件が検出された元とコピー先のオブジェクトを部分的に変更された可能性がありますので。</span><span class="sxs-lookup"><span data-stu-id="13d76-149">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="13d76-150">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="13d76-150">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="13d76-151">先のオブジェクトでは、 _lpInterface_パラメーターで指定されたインターフェイスはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="13d76-151">The interface identified by the  _lpInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="13d76-152">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="13d76-152">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="13d76-153">呼び出し元が十分なアクセス許可を持っているオブジェクトにアクセスしようとしました。</span><span class="sxs-lookup"><span data-stu-id="13d76-153">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="13d76-154">目的のオブジェクトは、ソース オブジェクトと同じ場合、このエラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="13d76-154">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="13d76-155">次の値が返される、 **SPropProblemArray**構造体には戻り値としてではなく**CopyProps**。</span><span class="sxs-lookup"><span data-stu-id="13d76-155">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **CopyProps**.</span></span> <span data-ttu-id="13d76-156">これらのエラーは、1 つのプロパティに適用されます。</span><span class="sxs-lookup"><span data-stu-id="13d76-156">These errors apply to a single property.</span></span>
  
<span data-ttu-id="13d76-157">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="13d76-157">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="13d76-158">か、MAPI_UNICODE フラグが設定された**CopyProps**は、Unicode をサポートしていませんまたは MAPI_UNICODE が設定されていないと**CopyProps**は、Unicode だけをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="13d76-158">Either the MAPI_UNICODE flag was set and **CopyProps** does not support Unicode, or MAPI_UNICODE was not set and **CopyProps** supports only Unicode.</span></span> 
    
<span data-ttu-id="13d76-159">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="13d76-159">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="13d76-160">コピー先オブジェクトの所有者によって計算される、読み取り専用プロパティであるために、呼び出し元がプロパティを変更できません。</span><span class="sxs-lookup"><span data-stu-id="13d76-160">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="13d76-161">このエラーは重大です。呼び出し元は、コピー操作を続行を許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13d76-161">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="13d76-162">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="13d76-162">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="13d76-163">プロパティの型が正しくありません。</span><span class="sxs-lookup"><span data-stu-id="13d76-163">The property type is invalid.</span></span>
    
<span data-ttu-id="13d76-164">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="13d76-164">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="13d76-165">プロパティの型は、呼び出し元の型ではありません。</span><span class="sxs-lookup"><span data-stu-id="13d76-165">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="13d76-166">備考</span><span class="sxs-lookup"><span data-stu-id="13d76-166">Remarks</span></span>

<span data-ttu-id="13d76-167">**IMAPIProp::CopyProps**メソッドは、コピーまたは、選択したプロパティを現在のオブジェクトからコピー先のオブジェクトに移動します。</span><span class="sxs-lookup"><span data-stu-id="13d76-167">The **IMAPIProp::CopyProps** method copies or moves selected properties from the current object to a destination object.</span></span> <span data-ttu-id="13d76-168">**CopyProps**は、返信または転送するメッセージ、返信を移動またはコピーを転送元のメッセージからのプロパティの一部のみ、主に使用されます。</span><span class="sxs-lookup"><span data-stu-id="13d76-168">**CopyProps** is used mainly for replying to and forwarding messages, where only some of the properties from the original message travel with the reply or forwarded copy.</span></span> 
  
<span data-ttu-id="13d76-169">ソース オブジェクトのサブオブジェクトは、自動的に操作に含まれているとコピーまたは移動した[SPropTagArray](sproptagarray.md)構造体で示されているプロパティの使用に関係なく、完全に。</span><span class="sxs-lookup"><span data-stu-id="13d76-169">Any subobjects in the source object are automatically included in the operation and copied or moved in their entirety, regardless of the use of properties indicated by the [SPropTagArray](sproptagarray.md) structure.</span></span> <span data-ttu-id="13d76-170">既定では、 **CopyProps**には、ソース オブジェクトからプロパティに一致する対象のオブジェクトのプロパティが上書きされます。</span><span class="sxs-lookup"><span data-stu-id="13d76-170">By default, **CopyProps** overwrites any properties in the destination object that match properties from the source object.</span></span> <span data-ttu-id="13d76-171">コピー先オブジェクトにコピーまたは移動先のプロパティのいずれかの場合、 _ulFlags_パラメーターに MAPI_NOREPLACE フラグが設定されていない限り、既存のプロパティが新しいプロパティによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="13d76-171">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="13d76-172">変更は上書きされず、変換先オブジェクトの既存の情報は行われないです。</span><span class="sxs-lookup"><span data-stu-id="13d76-172">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="13d76-173">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="13d76-173">Notes to implementers</span></span>

<span data-ttu-id="13d76-174">**CopyProps**の完全な実装を提供するか、サポート オブジェクトは、MAPI が提供する実装に依存します。</span><span class="sxs-lookup"><span data-stu-id="13d76-174">You can provide a full implementation of **CopyProps** or rely on the implementation that MAPI provides in its support object.</span></span> <span data-ttu-id="13d76-175">MAPI 実装を使用する場合は、 **IMAPISupport::DoCopyProps**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="13d76-175">If you want to use the MAPI implementation, call the **IMAPISupport::DoCopyProps** method.</span></span> <span data-ttu-id="13d76-176">ただし、 **DoCopyProps**に処理を委任する操作を行います、MAPI_DECLINE_OK フラグが渡されますが、サポートの呼び出しを避けるため、代わりに MAPI_E_DECLINE_COPY を返します。</span><span class="sxs-lookup"><span data-stu-id="13d76-176">However, if you do delegate processing to **DoCopyProps** and you are passed the MAPI_DECLINE_OK flag, avoid the support call and return MAPI_E_DECLINE_COPY instead.</span></span> <span data-ttu-id="13d76-177">呼び出されますこのフラグを持つフォルダーをコピーする場合に発生する可能性のある再帰を回避するのには MAPI によって。</span><span class="sxs-lookup"><span data-stu-id="13d76-177">You will be called with this flag by MAPI to avoid the possible recursion that can occur when you copy folders.</span></span> 
  
<span data-ttu-id="13d76-178">コピー操作できますが、時間がかかるため、進行状況インジケーターを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13d76-178">Because the copy operation can be lengthy, you should display a progress indicator.</span></span> <span data-ttu-id="13d76-179">いずれかを使用する必要がある場合は、 _lpProgress_パラメーターに渡される[IMAPIProgress](imapiprogressiunknown.md)の実装を使用します。</span><span class="sxs-lookup"><span data-stu-id="13d76-179">Use the [IMAPIProgress](imapiprogressiunknown.md) implementation that is passed in the  _lpProgress_ parameter, if there is one.</span></span> <span data-ttu-id="13d76-180">_LpProgress_が**null**の場合は、MAPI 実装を使用する[IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="13d76-180">If  _lpProgress_ is **null**, call the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to use the MAPI implementation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="13d76-181">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="13d76-181">Notes to callers</span></span>

<span data-ttu-id="13d76-182">MAPI_DECLINE_OK フラグを設定しません。メッセージ ストア プロバイダーの**CopyProps**の実装への呼び出しで MAPI によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="13d76-182">Do not set the MAPI_DECLINE_OK flag; it is used by MAPI in its calls to message store provider **CopyProps** implementations.</span></span> 
  
<span data-ttu-id="13d76-183">のコピーと移動の操作に時間がかかる場合、MAPI_DIALOG フラグを設定することにより、進行状況インジケーターの表示を要求することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="13d76-183">Because copy and move operations can take time, it is wise to request the display of a progress indicator by setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="13d76-184">**IMAPIProgress**で、いずれかの操作をした場合の実装に、または**null**には、 _lpProgress_パラメーターを設定できます。</span><span class="sxs-lookup"><span data-stu-id="13d76-184">You can set the  _lpProgress_ parameter to your implementation of **IMAPIProgress**, if you have one, or to **null**.</span></span> <span data-ttu-id="13d76-185">_LpProgress_が**null**の場合は、 **CopyProps**は MAPI によって提供される既定の進行状況のインジケーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="13d76-185">If  _lpProgress_ is **null**, **CopyProps** will use the default progress indicator provided by MAPI.</span></span> 
  
<span data-ttu-id="13d76-186">MAPI_DIALOG フラグを設定しない、進行状況インジケーターの表示を抑制できます。</span><span class="sxs-lookup"><span data-stu-id="13d76-186">You can suppress the display of a progress indicator by not setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="13d76-187">**CopyProps**は、 _ulUIParam_および_lpProgress_パラメーターを無視して、インジケーターが表示されないようにします。</span><span class="sxs-lookup"><span data-stu-id="13d76-187">**CopyProps** will ignore the  _ulUIParam_ and  _lpProgress_ parameters and avoid displaying the indicator.</span></span> 
  
 <span data-ttu-id="13d76-188">**CopyProps**には、グローバルおよび個々 のエラーの場合、またはプロパティのいずれかで発生するエラーを報告できます。</span><span class="sxs-lookup"><span data-stu-id="13d76-188">**CopyProps** can report global and individual errors, or errors that occur with one or more of the properties.</span></span> <span data-ttu-id="13d76-189">これらの個々 のエラーは、 **SPropProblemArray**構造体に配置されます。</span><span class="sxs-lookup"><span data-stu-id="13d76-189">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="13d76-190">**Null**、代わりに、プロパティの問題の配列構造体のパラメーターの有効なポインターを渡すことにより、プロパティ レベルでレポートのエラーを抑制できます。</span><span class="sxs-lookup"><span data-stu-id="13d76-190">You can suppress error reporting at the property level by passing **null**, instead of a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="13d76-191">エラーに関する情報を受信する場合は、 _lppProblems_パラメーターに有効な**SPropProblemArray**構造体のポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="13d76-191">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="13d76-192">**CopyProps**に S_OK が返されるときは、構造内の個々 のプロパティを持つ可能性のあるエラーを確認します。</span><span class="sxs-lookup"><span data-stu-id="13d76-192">When **CopyProps** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="13d76-193">**CopyProps**にエラーが返されるとき、 **SPropProblemArray**構造体の情報は返されません。</span><span class="sxs-lookup"><span data-stu-id="13d76-193">When **CopyProps** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="13d76-194">代わりに、詳細なエラー情報を取得するために[IMAPIProp::GetLastError](imapiprop-getlasterror.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="13d76-194">Instead, call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="13d76-195">**CopyProps**では、S_OK が返された場合は、 [MAPIFreeBuffer](mapifreebuffer.md)関数の呼び出しによって返された**SPropProblemArray**構造体を解放します。</span><span class="sxs-lookup"><span data-stu-id="13d76-195">If **CopyProps** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="13d76-196">ソース オブジェクトの種類に固有のプロパティをコピーする場合は、目的のオブジェクトが同じ型のあることを確認の操作を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="13d76-196">If you are copying properties that are unique to the source object type, you must make sure that the destination object is of the same type.</span></span> <span data-ttu-id="13d76-197">**CopyProps**ができないから、通常、1 種類のオブジェクトの別の種類のオブジェクトに属するプロパティを関連付けることです。</span><span class="sxs-lookup"><span data-stu-id="13d76-197">**CopyProps** does not prevent you from associating properties that typically belong to one type of object with another type of object.</span></span> <span data-ttu-id="13d76-198">変換先オブジェクトのプロパティをコピーすることの責任です。</span><span class="sxs-lookup"><span data-stu-id="13d76-198">It is up to you to copy properties that make sense for the destination object.</span></span> <span data-ttu-id="13d76-199">などのアドレス帳コンテナーにメッセージのプロパティをコピーする必要がありますされません。</span><span class="sxs-lookup"><span data-stu-id="13d76-199">For example, you should not copy message properties to an address book container.</span></span> 
  
<span data-ttu-id="13d76-200">同じ種類のオブジェクト間でコピーしていることを確認するには、元とコピー先のオブジェクトが同じ型、オブジェクトのポインターを比較するか、 [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx)メソッドを呼び出すことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="13d76-200">To ensure that you are copying between objects of the same type, check that the source and destination object are the same type, either by comparing object pointers or calling the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) method.</span></span> <span data-ttu-id="13d76-201">ソース オブジェクトの標準的なインタ フェースを_lpInterface_が指すインターフェイスの識別子を設定します。</span><span class="sxs-lookup"><span data-stu-id="13d76-201">Set the interface identifier pointed to by  _lpInterface_ to the standard interface for the source object.</span></span> <span data-ttu-id="13d76-202">オブジェクト タイプまたは**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) のプロパティは、2 つのオブジェクトに対して同じであることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="13d76-202">Also, ensure that the object type or **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property is the same for the two objects.</span></span> <span data-ttu-id="13d76-203">たとえば、メッセージからコピーする場合は、IID_IMessage と MAPI_MESSAGE を両方のオブジェクトの**PR_OBJECT_TYPE**に_lpInterface_を設定します。</span><span class="sxs-lookup"><span data-stu-id="13d76-203">For example, if you are copying from a message, set  _lpInterface_ to IID_IMessage and the **PR_OBJECT_TYPE** for both objects to MAPI_MESSAGE.</span></span> 
  
<span data-ttu-id="13d76-204">場合は、 _lpDestObj_パラメーターに無効なポインターが渡されると、結果は予測できません。</span><span class="sxs-lookup"><span data-stu-id="13d76-204">If an invalid pointer is passed in the  _lpDestObj_ parameter, the results are unpredictable.</span></span> 
  
<span data-ttu-id="13d76-205">メッセージの受信者のリストをコピーするには、メッセージの**CopyProps**メソッドを呼び出すし、プロパティ タグ配列の**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) のプロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="13d76-205">To copy a message's recipient list, call the message's **CopyProps** method and include the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in the property tag array.</span></span> <span data-ttu-id="13d76-206">メッセージの添付ファイルをコピーするには、 **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) のプロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="13d76-206">To copy the message's attachments, include the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="13d76-207">フォルダーまたはアドレス帳コンテナーの階層構造または内容のテーブルをコピーするには、 **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) または**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) のプロパティで、プロパティ タグの配列です。</span><span class="sxs-lookup"><span data-stu-id="13d76-207">To copy a folder or address book container's hierarchy or contents table, include the **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) properties in the property tag array.</span></span> <span data-ttu-id="13d76-208">フォルダーの内容を関連するテーブルを含めるには、 **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) のプロパティを配列に指定します。</span><span class="sxs-lookup"><span data-stu-id="13d76-208">To include a folder's associated contents table, include the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property in the array.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="13d76-209">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="13d76-209">MFCMAPI reference</span></span>

<span data-ttu-id="13d76-210">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="13d76-210">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="13d76-211">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="13d76-211">**File**</span></span>|<span data-ttu-id="13d76-212">**関数**</span><span class="sxs-lookup"><span data-stu-id="13d76-212">**Function**</span></span>|<span data-ttu-id="13d76-213">**コメント**</span><span class="sxs-lookup"><span data-stu-id="13d76-213">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="13d76-214">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="13d76-214">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="13d76-215">CopyNamedProps</span><span class="sxs-lookup"><span data-stu-id="13d76-215">CopyNamedProps</span></span>  <br/> |<span data-ttu-id="13d76-216">MFCMAPI では、1 つのメッセージから名前付きプロパティをコピーするのにには、 **IMAPIProp::CopyProps**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="13d76-216">MFCMAPI uses the **IMAPIProp::CopyProps** method to copy named properties from one message to another.</span></span>  <br/> |
|<span data-ttu-id="13d76-217">SingleMAPIPropListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="13d76-217">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="13d76-218">CSingleMAPIPropListCtrl::OnPasteProperty</span><span class="sxs-lookup"><span data-stu-id="13d76-218">CSingleMAPIPropListCtrl::OnPasteProperty</span></span>  <br/> |<span data-ttu-id="13d76-219">MFCMAPI では、 **IMAPIProp::CopyProps**メソッドを使用して、別のオブジェクトからコピーされたプロパティを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="13d76-219">MFCMAPI uses the **IMAPIProp::CopyProps** method to paste a property that has been copied from another object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="13d76-220">関連項目</span><span class="sxs-lookup"><span data-stu-id="13d76-220">See also</span></span>



[<span data-ttu-id="13d76-221">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="13d76-221">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="13d76-222">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="13d76-222">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="13d76-223">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="13d76-223">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="13d76-224">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="13d76-224">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="13d76-225">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="13d76-225">IMAPISupport::DoCopyProps</span></span>](imapisupport-docopyprops.md)
  
[<span data-ttu-id="13d76-226">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="13d76-226">IMAPISupport::DoProgressDialog</span></span>](imapisupport-doprogressdialog.md)
  
[<span data-ttu-id="13d76-227">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="13d76-227">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="13d76-228">PidTagContainerContents 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="13d76-228">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="13d76-229">PidTagContainerHierarchy 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="13d76-229">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="13d76-230">PidTagDisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="13d76-230">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="13d76-231">PidTagFolderAssociatedContents 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="13d76-231">PidTagFolderAssociatedContents Canonical Property</span></span>](pidtagfolderassociatedcontents-canonical-property.md)
  
[<span data-ttu-id="13d76-232">PidTagMessageAttachments 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="13d76-232">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="13d76-233">PidTagMessageRecipients 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="13d76-233">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="13d76-234">PidTagObjectType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="13d76-234">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="13d76-235">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="13d76-235">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="13d76-236">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="13d76-236">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="13d76-237">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="13d76-237">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


<span data-ttu-id="13d76-238">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="13d76-238">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

