---
title: imapipropcopyto
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f76b0a5482647fe3e181a36d7dcd8cb60ffc8985
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356393"
---
# <a name="imapipropcopyto"></a><span data-ttu-id="a0540-103">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="a0540-103">IMAPIProp::CopyTo</span></span>

  
  
<span data-ttu-id="a0540-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0540-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0540-105">明示的に除外されているプロパティ以外のすべてのプロパティをコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="a0540-105">Copies or moves all properties, except for specifically excluded properties.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="a0540-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a0540-106">Parameters</span></span>

 <span data-ttu-id="a0540-107">_ciidExclude_</span><span class="sxs-lookup"><span data-stu-id="a0540-107">_ciidExclude_</span></span>
  
> <span data-ttu-id="a0540-108">順番プロパティがコピーまたは移動されたときに除外するインターフェイスの数。</span><span class="sxs-lookup"><span data-stu-id="a0540-108">[in] The count of interfaces to exclude when properties are copied or moved.</span></span>
    
 <span data-ttu-id="a0540-109">_rgiidExclude_</span><span class="sxs-lookup"><span data-stu-id="a0540-109">_rgiidExclude_</span></span>
  
> <span data-ttu-id="a0540-110">順番追加情報をコピーまたは移動先オブジェクトに移動するときに使用しないインターフェイスを指定するインターフェイス識別子 (IIDs) の配列。</span><span class="sxs-lookup"><span data-stu-id="a0540-110">[in] An array of interface identifiers (IIDs) that specify interfaces that should not be used when supplemental information is copied or moved to the destination object.</span></span>
    
 <span data-ttu-id="a0540-111">_lpexcludeprops_</span><span class="sxs-lookup"><span data-stu-id="a0540-111">_lpExcludeProps_</span></span>
  
> <span data-ttu-id="a0540-112">順番コピー操作または移動操作から除外する必要があるプロパティタグを識別するプロパティタグ配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a0540-112">[in] A pointer to a property tag array that identifies the property tags that should be excluded from the copy or move operation.</span></span> <span data-ttu-id="a0540-113">_lpexcludeprops_パラメーターで**null**を渡すことは、オブジェクトのすべてのプロパティをコピーまたは移動する必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="a0540-113">Passing **null** in the  _lpExcludeProps_ parameter indicates that all of the object's properties should be copied or moved.</span></span> <span data-ttu-id="a0540-114">_lpexcludeprops_によって指定される[spropprops 配列](spropproblemarray.md)構造の**cvalues**メンバが0に設定されている場合、 **CopyTo**は MAPI_E_INVALID_PARAMETER を返します。</span><span class="sxs-lookup"><span data-stu-id="a0540-114">**CopyTo** returns MAPI_E_INVALID_PARAMETER when the **cValues** member of the [SPropProblemArray](spropproblemarray.md) structure pointed to by  _lpExcludeProps_ is set to 0.</span></span> 
    
 <span data-ttu-id="a0540-115">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="a0540-115">_ulUIParam_</span></span>
  
> <span data-ttu-id="a0540-116">順番進行状況インジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="a0540-116">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="a0540-117">_lpprogress_</span><span class="sxs-lookup"><span data-stu-id="a0540-117">_lpProgress_</span></span>
  
> <span data-ttu-id="a0540-118">順番進行状況インジケーターの実装へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a0540-118">[in] A pointer to a progress indicator implementation.</span></span> <span data-ttu-id="a0540-119">_lpprogress_パラメーターで**null**が渡された場合、MAPI は進行状況の実装を提供します。</span><span class="sxs-lookup"><span data-stu-id="a0540-119">If **null** is passed in the  _lpProgress_ parameter, MAPI provides the progress implementation.</span></span> <span data-ttu-id="a0540-120">MAPI_DIALOG フラグが_ulflags_パラメーターで設定されていない場合、 _lpprogress_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="a0540-120">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="a0540-121">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="a0540-121">_lpInterface_</span></span>
  
> <span data-ttu-id="a0540-122">順番_lpdestobj_パラメーターによって指定されたオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a0540-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object pointed to by the  _lpDestObj_ parameter.</span></span> <span data-ttu-id="a0540-123">_lpinterface_パラメーターを**null**にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="a0540-123">The  _lpInterface_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="a0540-124">_lpdestobj_</span><span class="sxs-lookup"><span data-stu-id="a0540-124">_lpDestObj_</span></span>
  
> <span data-ttu-id="a0540-125">順番コピーまたは移動したプロパティを受け取るオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a0540-125">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="a0540-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a0540-126">_ulFlags_</span></span>
  
> <span data-ttu-id="a0540-127">順番コピー操作または移動操作を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="a0540-127">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="a0540-128">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a0540-128">The following flags can be set:</span></span>
    
<span data-ttu-id="a0540-129">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="a0540-129">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="a0540-130">**CopyTo**が[imapisupport::D ocopyto](imapisupport-docopyto.md)メソッドを呼び出してコピー操作または移動操作を処理する場合は、エラー値 MAPI_E_DECLINE_COPY を使用して直ちに戻る必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0540-130">If **CopyTo** calls the [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) method to handle the copy or move operation, it should instead return immediately with the error value MAPI_E_DECLINE_COPY.</span></span> <span data-ttu-id="a0540-131">MAPI_DECLINE_OK フラグは、再帰を制限するために MAPI によって設定されます。</span><span class="sxs-lookup"><span data-stu-id="a0540-131">The MAPI_DECLINE_OK flag is set by MAPI to limit recursion.</span></span> <span data-ttu-id="a0540-132">クライアントはこのフラグを設定しません。</span><span class="sxs-lookup"><span data-stu-id="a0540-132">Clients do not set this flag.</span></span> 
    
<span data-ttu-id="a0540-133">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="a0540-133">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="a0540-134">進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="a0540-134">Displays a progress indicator.</span></span>
    
<span data-ttu-id="a0540-135">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="a0540-135">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="a0540-136">**CopyTo**では、コピー操作の代わりに移動操作を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0540-136">**CopyTo** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="a0540-137">このフラグが設定されていない場合、 **CopyTo**はコピー操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="a0540-137">When this flag is not set, **CopyTo** performs a copy operation.</span></span> 
    
<span data-ttu-id="a0540-138">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="a0540-138">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="a0540-139">対象のオブジェクト内の既存のプロパティは、上書きしないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="a0540-139">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="a0540-140">このフラグが設定されていない場合、 **CopyTo**は既存のプロパティを上書きします。</span><span class="sxs-lookup"><span data-stu-id="a0540-140">When this flag is not set, **CopyTo** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="a0540-141">_lppproblems 問題_</span><span class="sxs-lookup"><span data-stu-id="a0540-141">_lppProblems_</span></span>
  
> <span data-ttu-id="a0540-142">[入力]input の場合は、 **spropの配列**構造体へのポインターへのポインターを返します。それ以外の場合、エラー情報を必要としないことを示す**null**。</span><span class="sxs-lookup"><span data-stu-id="a0540-142">[in, out] On input, a pointer to a pointer to an **SPropProblemArray** structure; otherwise, **null**, indicating no need for error information.</span></span> <span data-ttu-id="a0540-143">_lppproblems_が入力の有効なポインターである場合、 **CopyTo**は1つ以上のプロパティをコピーする際のエラーに関する詳細情報を返します。</span><span class="sxs-lookup"><span data-stu-id="a0540-143">If  _lppProblems_ is a valid pointer on input, **CopyTo** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a0540-144">戻り値</span><span class="sxs-lookup"><span data-stu-id="a0540-144">Return value</span></span>

<span data-ttu-id="a0540-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="a0540-145">S_OK</span></span> 
  
> <span data-ttu-id="a0540-146">プロパティが正常にコピーまたは移動されました。</span><span class="sxs-lookup"><span data-stu-id="a0540-146">The properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="a0540-147">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="a0540-147">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="a0540-148">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティによって指定された同じ表示名のサブオブジェクトが対象オブジェクトに既に存在しているため、サブオブジェクトをコピーできません。</span><span class="sxs-lookup"><span data-stu-id="a0540-148">A subobject cannot be copied because a subobject with the same display name — specified by the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property — already exists in the destination object.</span></span> 
    
<span data-ttu-id="a0540-149">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="a0540-149">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="a0540-150">サービスプロバイダーがコピー操作を実装していません。</span><span class="sxs-lookup"><span data-stu-id="a0540-150">The service provider does not implement the copy operation.</span></span>
    
<span data-ttu-id="a0540-151">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="a0540-151">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="a0540-152">コピーまたは移動操作を直接または間接的に実行しているソースオブジェクトは、目的のオブジェクトを直接または間接的に格納します。</span><span class="sxs-lookup"><span data-stu-id="a0540-152">The source object performing the copy or move operation directly or indirectly contains the destination object.</span></span> <span data-ttu-id="a0540-153">この条件が検出される前に、重要な作業が実行されている可能性があるので、移行元と移行先のオブジェクトの一部が変更されている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a0540-153">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="a0540-154">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="a0540-154">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="a0540-155">_lpinterface_パラメーターで指定されたインターフェイスは、destination オブジェクトではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="a0540-155">The interface identified by the  _lpInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="a0540-156">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="a0540-156">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="a0540-157">発信者が十分なアクセス許可を持っていないオブジェクトにアクセスしようとしました。</span><span class="sxs-lookup"><span data-stu-id="a0540-157">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="a0540-158">destination オブジェクトがソースオブジェクトと同じ場合、このエラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="a0540-158">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="a0540-159">次の値は、 **spropの配列**構造で返すことができますが、 **CopyTo**の戻り値としては返されません。</span><span class="sxs-lookup"><span data-stu-id="a0540-159">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **CopyTo**.</span></span> <span data-ttu-id="a0540-160">次のエラーが1つのプロパティに適用されます。</span><span class="sxs-lookup"><span data-stu-id="a0540-160">The following errors apply to a single property:</span></span>
  
<span data-ttu-id="a0540-161">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="a0540-161">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="a0540-162">MAPI_UNICODE フラグが設定されており、 **copyto**が unicode をサポートしていないか、MAPI_UNICODE が設定されておらず、 **copyto**は unicode のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="a0540-162">Either the MAPI_UNICODE flag was set and **CopyTo** does not support Unicode, or MAPI_UNICODE was not set and **CopyTo** supports only Unicode.</span></span> 
    
<span data-ttu-id="a0540-163">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="a0540-163">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="a0540-164">このプロパティは読み取り専用プロパティであるため、呼び出し元が変更することはできません。これは、対象オブジェクトの所有者によって計算されます。</span><span class="sxs-lookup"><span data-stu-id="a0540-164">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="a0540-165">このエラーは重大ではありません。呼び出し元がコピー操作を続行できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0540-165">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="a0540-166">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="a0540-166">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="a0540-167">プロパティの種類が無効です。</span><span class="sxs-lookup"><span data-stu-id="a0540-167">The property type is invalid.</span></span>
    
<span data-ttu-id="a0540-168">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="a0540-168">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="a0540-169">プロパティの型は、呼び出し元が想定した型ではありません。</span><span class="sxs-lookup"><span data-stu-id="a0540-169">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a0540-170">解説</span><span class="sxs-lookup"><span data-stu-id="a0540-170">Remarks</span></span>

<span data-ttu-id="a0540-171">既定では、 **imapiprop:: CopyTo**メソッドは、現在のオブジェクトのすべてのプロパティを対象のオブジェクトにコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="a0540-171">By default, the **IMAPIProp::CopyTo** method copies or moves all of the current object's properties to a destination object.</span></span> <span data-ttu-id="a0540-172">**CopyTo**は、オブジェクトが正確にコピーまたは移動されるときに使用されます。プロパティのすべてまたはほとんどはそのままです。</span><span class="sxs-lookup"><span data-stu-id="a0540-172">**CopyTo** is used when an object should be copied or moved exactly, with all or most of its properties intact.</span></span> 
  
<span data-ttu-id="a0540-173">source オブジェクト内のすべてのサブオブジェクトは、自動的に操作に含まれ、全体でコピーまたは移動されます。</span><span class="sxs-lookup"><span data-stu-id="a0540-173">Any subobjects in the source object are automatically included in the operation and are copied or moved in their entirety.</span></span> <span data-ttu-id="a0540-174">既定では、 **CopyTo**はコピー先オブジェクトのプロパティに一致するすべてのプロパティをソースオブジェクトから上書きします。</span><span class="sxs-lookup"><span data-stu-id="a0540-174">By default, **CopyTo** overwrites any properties in the destination object that match properties from the source object.</span></span> <span data-ttu-id="a0540-175">コピーまたは移動されたプロパティのいずれかがコピー先オブジェクトに既に存在する場合、MAPI_NOREPLACE フラグが_ulflags_パラメーターで設定されていない限り、既存のプロパティは新しいプロパティによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="a0540-175">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="a0540-176">上書きされていない対象のオブジェクト内の既存の情報は、そのまま残ります。</span><span class="sxs-lookup"><span data-stu-id="a0540-176">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a0540-177">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="a0540-177">Notes to implementers</span></span>

<span data-ttu-id="a0540-178">**CopyTo**の完全な実装を提供することも、MAPI がサポートオブジェクトで提供する実装に依存することもできます。</span><span class="sxs-lookup"><span data-stu-id="a0540-178">You can provide a full implementation of **CopyTo** or rely on the implementation that MAPI provides in its support object.</span></span> <span data-ttu-id="a0540-179">MAPI 実装を使用する場合は、 **imapisupport::D ocopyto**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a0540-179">If you want to use the MAPI implementation, call **IMAPISupport::DoCopyTo**.</span></span> <span data-ttu-id="a0540-180">ただし、MAPI_DECLINE_OK フラグが渡された\*\*\*\* 場合に、委任処理を実行すると、サポートコールを避け、代わりに MAPI_E_DECLINE_COPY を返します。</span><span class="sxs-lookup"><span data-stu-id="a0540-180">However, if you do delegate processing to **DoCopyTo** and you are passed the MAPI_DECLINE_OK flag, avoid the support call and return MAPI_E_DECLINE_COPY instead.</span></span> <span data-ttu-id="a0540-181">MAPI は、フォルダーがコピーされたときに発生する可能性のある再帰を回避するために、このフラグを使用して呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a0540-181">MAPI will call with this flag to avoid the possible recursion that can happen when folders are copied.</span></span> 
  
<span data-ttu-id="a0540-182">コピー操作に長い時間がかかる可能性があるため、進行状況インジケーターを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0540-182">Because the copy operation can be lengthy, you should display a progress indicator.</span></span> <span data-ttu-id="a0540-183">_lpprogress_パラメーターに渡された[imapiprogress](imapiprogressiunknown.md)実装を使用します (存在する場合)。</span><span class="sxs-lookup"><span data-stu-id="a0540-183">Use the [IMAPIProgress](imapiprogressiunknown.md) implementation passed in the  _lpProgress_ parameter, if there is one.</span></span> <span data-ttu-id="a0540-184">_lpprogress_が**null**の場合は、MAPI 実装を使用するために[imapisupport::D oprogress dialog](imapisupport-doprogressdialog.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a0540-184">If  _lpProgress_ is **null**, call the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to use the MAPI implementation.</span></span> 
  
<span data-ttu-id="a0540-185">対象のオブジェクトで読み取り専用プロパティを設定しようとしないでください。代わりに MAPI_E_NO_ACCESS を返します。</span><span class="sxs-lookup"><span data-stu-id="a0540-185">Do not attempt to set any known read-only properties in the destination object; return MAPI_E_NO_ACCESS instead.</span></span>
  
<span data-ttu-id="a0540-186">コピー元とコピー先のオブジェクトは、同じインターフェイスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0540-186">The source and destination objects should use the same interfaces.</span></span> <span data-ttu-id="a0540-187">_lpinterface_が設定されていない場合は、MAPI_E_INVALID_PARAMETER を返します。</span><span class="sxs-lookup"><span data-stu-id="a0540-187">Return MAPI_E_INVALID_PARAMETER if  _lpInterface_ is not set.</span></span> 
  
<span data-ttu-id="a0540-188">既知のすべてのインターフェイスが除外されている場合は、MAPI_E_INTERFACE_NOT_SUPPORTED を返します。</span><span class="sxs-lookup"><span data-stu-id="a0540-188">Return MAPI_E_INTERFACE_NOT_SUPPORTED if all known interfaces are excluded.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="a0540-189">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="a0540-189">Notes to callers</span></span>

<span data-ttu-id="a0540-190">MAPI_DECLINE_OK フラグは設定しません。MAPI では、メッセージストアプロバイダーの**CopyTo**実装への呼び出しでそれが使用されます。</span><span class="sxs-lookup"><span data-stu-id="a0540-190">Do not set the MAPI_DECLINE_OK flag; MAPI uses it in its calls to message store provider **CopyTo** implementations.</span></span> 
  
<span data-ttu-id="a0540-191">コピー操作および移動操作は時間がかかることがあるため、MAPI_DIALOG フラグを設定して進行状況インジケーターの表示を要求する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0540-191">Because copy and move operations can take time, you should request the display of a progress indicator by setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="a0540-192">_lpprogress_パラメーターは、 **imapiprogress**の実装に設定できます (存在する場合)。それ以外の場合は**null**に設定できます。</span><span class="sxs-lookup"><span data-stu-id="a0540-192">You can set the  _lpProgress_ parameter to your implementation of **IMAPIProgress**, if you have one, or to **null**.</span></span> <span data-ttu-id="a0540-193">_lpprogress_が**null**の場合、 **CopyTo**は MAPI が提供する既定の進行状況インジケーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="a0540-193">If  _lpProgress_ is **null**, **CopyTo** will use the default progress indicator that MAPI provides.</span></span> 
  
<span data-ttu-id="a0540-194">MAPI_DIALOG フラグを設定しないと、進行状況インジケーターの表示を抑制することができます。</span><span class="sxs-lookup"><span data-stu-id="a0540-194">You can suppress the display of a progress indicator by not setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="a0540-195">**CopyTo**では_uluiparam_パラメーターと_lpprogress_パラメーターは無視され、インジケーターは表示されません。</span><span class="sxs-lookup"><span data-stu-id="a0540-195">**CopyTo** will ignore the  _ulUIParam_ and  _lpProgress_ parameters and will not display the indicator.</span></span> 
  
 <span data-ttu-id="a0540-196">**CopyTo**では、グローバルおよび個別のエラー、あるいは1つ以上のプロパティで発生するエラーを報告できます。</span><span class="sxs-lookup"><span data-stu-id="a0540-196">**CopyTo** can report global and individual errors, or errors that occur with one or more properties.</span></span> <span data-ttu-id="a0540-197">これらの個々のエラーは、 **sprop問題の配列**構造に配置されます。</span><span class="sxs-lookup"><span data-stu-id="a0540-197">These individual errors are placed in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="a0540-198">プロパティ問題の array 構造パラメーターに対して、有効なポインターではなく**null**を渡すことにより、プロパティレベルでエラー報告を抑制することができます。</span><span class="sxs-lookup"><span data-stu-id="a0540-198">You can suppress error reporting at the property level by passing **null**, instead of a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="a0540-199">エラーに関する情報を受信する必要がある場合は、 _lppproblems_パラメーターに有効な**sprop問題の配列**構造ポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="a0540-199">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="a0540-200">**CopyTo**が S_OK を返す場合は、構造内の個々のプロパティに関するエラーがあるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0540-200">When **CopyTo** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="a0540-201">**CopyTo**がエラーを返す場合、 **sprop問題の配列**構造に情報は返されません。</span><span class="sxs-lookup"><span data-stu-id="a0540-201">When **CopyTo** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="a0540-202">代わりに、 [imapiprop:: GetLastError](imapiprop-getlasterror.md)を呼び出して詳細なエラー情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="a0540-202">Instead, call [IMAPIProp::GetLastError](imapiprop-getlasterror.md) to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="a0540-203">**CopyTo**が S_OK を返す場合は、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによって返された**spropの配列**構造を解放します。</span><span class="sxs-lookup"><span data-stu-id="a0540-203">If **CopyTo** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="a0540-204">ソースオブジェクトの種類に固有のプロパティをコピーする場合は、対象のオブジェクトが同じ種類であることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0540-204">If you copy properties that are unique to the source object type, you must ensure that the destination object is of the same type.</span></span> <span data-ttu-id="a0540-205">**CopyTo**では、通常、ある種類のオブジェクトに属するプロパティを別の種類のオブジェクトに関連付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="a0540-205">**CopyTo** does not prevent you from associating properties that typically belong to one type of object with another type of object.</span></span> <span data-ttu-id="a0540-206">目的のオブジェクトに適したプロパティをコピーするのは、自分のユーザーです。</span><span class="sxs-lookup"><span data-stu-id="a0540-206">It is up to you to copy properties that make sense for the destination object.</span></span> <span data-ttu-id="a0540-207">たとえば、メッセージのプロパティをアドレス帳のコンテナーにコピーしないでください。</span><span class="sxs-lookup"><span data-stu-id="a0540-207">For example, you should not copy message properties to an address book container.</span></span> 
  
<span data-ttu-id="a0540-208">同じ種類のオブジェクト間でコピーされるようにするには、オブジェクトポインターを比較するか、 [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)を呼び出して、コピー元とコピー先のオブジェクトが同じ種類であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0540-208">To ensure that you copy between objects of the same type, check that the source and destination object are the same type, either by comparing object pointers or calling [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx).</span></span> <span data-ttu-id="a0540-209">_lpinterface_で示されるインターフェイス識別子を、source オブジェクトの標準インターフェイスに設定します。</span><span class="sxs-lookup"><span data-stu-id="a0540-209">Set the interface identifier pointed to by  _lpInterface_ to the standard interface for the source object.</span></span> <span data-ttu-id="a0540-210">また、オブジェクトの種類または**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) プロパティが、2つのオブジェクトに対して同じであることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a0540-210">Also, be sure that the object type or **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property is the same for the two objects.</span></span> <span data-ttu-id="a0540-211">たとえば、メッセージからコピーする場合は、 _lpinterface_を IID_IMessage に、両方のオブジェクトの**PR_OBJECT_TYPE**を MAPI_MESSAGE に設定します。</span><span class="sxs-lookup"><span data-stu-id="a0540-211">For example, if you copy from a message, set  _lpInterface_ to IID_IMessage and the **PR_OBJECT_TYPE** for both objects to MAPI_MESSAGE.</span></span> 
  
<span data-ttu-id="a0540-212">_lpdestobj_パラメーターに無効なポインターが渡された場合、結果は予測できません。</span><span class="sxs-lookup"><span data-stu-id="a0540-212">If an invalid pointer is passed in the  _lpDestObj_ parameter, the results are unpredictable.</span></span> 
  
<span data-ttu-id="a0540-213">**CopyTo**呼び出しでプロパティを除外することが有用な場合があります。</span><span class="sxs-lookup"><span data-stu-id="a0540-213">Excluding properties on a **CopyTo** call can be useful.</span></span> <span data-ttu-id="a0540-214">たとえば、一部のオブジェクトには、オブジェクトの1つのインスタンスに固有のプロパティがあります (メッセージ配信の日時など)。</span><span class="sxs-lookup"><span data-stu-id="a0540-214">For example, some objects have properties that are specific to a single instance of the object, such as the date and time of message delivery.</span></span> <span data-ttu-id="a0540-215">メッセージを別のフォルダーにコピーしたときにメッセージの配信時刻がコピーされないようにするには、property タグの除外配列で**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) を指定します。</span><span class="sxs-lookup"><span data-stu-id="a0540-215">To avoid copying a message's delivery time when you copy the message to a different folder, specify **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) in the property tag exclude array.</span></span> <span data-ttu-id="a0540-216">メッセージの宛先リストを除外するには、 **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) プロパティを exclude 配列に追加します。</span><span class="sxs-lookup"><span data-stu-id="a0540-216">To exclude a message's recipient list, add the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property to the exclude array.</span></span> <span data-ttu-id="a0540-217">メッセージの添付ファイルを除外するには、 **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) プロパティを配列に追加します。</span><span class="sxs-lookup"><span data-stu-id="a0540-217">To exclude a message's attachments, add the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property to the array.</span></span>
  
<span data-ttu-id="a0540-218">同様に、 **PR_CONTAINER_HIERARCHY** (PidTagContainerHierarchy) または PR_CONTAINER_CONTENTS ([](pidtagcontainerhierarchy-canonical-property.md)) または\*\*\*\* を含めることによって、フォルダーまたはアドレス帳コンテナーの階層またはコンテンツテーブルをコピーまたは移動できないようにします ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) プロパティタグの除外配列。</span><span class="sxs-lookup"><span data-stu-id="a0540-218">Similarly, prevent the copying or moving of a folder or address book container's hierarchy or contents table by including **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag exclude array.</span></span>
  
<span data-ttu-id="a0540-219">コピー操作または移動操作からプロパティを除外するには、そのプロパティタグを_lpexcludeprops_パラメーターに含めます。</span><span class="sxs-lookup"><span data-stu-id="a0540-219">To exclude properties from the copy or move operation, include their property tags in the  _lpExcludeProps_ parameter.</span></span> <span data-ttu-id="a0540-220">**PROP_TAG**マクロの結果を渡して、プロパティタグ配列の特定の識別子からプロパティタグを作成すると、その識別子を持つすべてのプロパティが除外されます。</span><span class="sxs-lookup"><span data-stu-id="a0540-220">If you pass the results of the **PROP_TAG** macro to build a property tag from a specific identifier in the property tag array, all properties with that identifier will be excluded.</span></span> <span data-ttu-id="a0540-221">たとえば、次のエントリをプロパティタグ配列に配置すると、型に関係なく、0x8002 の識別子が含まれるすべてのプロパティが除外されます。</span><span class="sxs-lookup"><span data-stu-id="a0540-221">For example, the following entry in the property tag array causes all properties with an identifier of 0x8002 to be excluded, regardless of type:</span></span> 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
<span data-ttu-id="a0540-222">**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) プロパティタグを_lpexcludeprops_配列に含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="a0540-222">The **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) property tag cannot be included in the  _lpExcludeProps_ array.</span></span> 
  
<span data-ttu-id="a0540-223">インターフェイスを除外するための**CopyTo**機能の有用性は、プロパティを除外することほど明確ではありません。</span><span class="sxs-lookup"><span data-stu-id="a0540-223">The usefulness of the **CopyTo** feature for excluding interfaces is perhaps not as obvious as the usefulness of excluding properties.</span></span> <span data-ttu-id="a0540-224">プロパティのグループについての知識がないオブジェクトにコピーするときに、インターフェイスを除外することができます。</span><span class="sxs-lookup"><span data-stu-id="a0540-224">You can exclude an interface when you copy to an object that has no knowledge of a group of properties.</span></span> <span data-ttu-id="a0540-225">たとえば、プロパティをフォルダーから添付ファイルにコピーした場合、添付ファイルで使用できるプロパティは、任意の[imapiprop](imapipropiunknown.md)実装で使用できる汎用プロパティだけです。</span><span class="sxs-lookup"><span data-stu-id="a0540-225">For example, if you copy properties from a folder to an attachment, the only properties that the attachment can work with are the generic properties available with any [IMAPIProp](imapipropiunknown.md) implementation.</span></span> <span data-ttu-id="a0540-226">[imapifolder](imapifolderimapicontainer.md)をコピー操作から除外すると、添付ファイルは、より具体的なフォルダープロパティを受け取ることはありません。</span><span class="sxs-lookup"><span data-stu-id="a0540-226">By excluding [IMAPIFolder](imapifolderimapicontainer.md) from the copy operation, the attachment will not receive any of the more specific folder properties.</span></span> 
  
<span data-ttu-id="a0540-227">_rgiidExclude_パラメーターを使用してインターフェイスを除外すると、そのインターフェイスから派生したすべてのインターフェイスも除外されます。</span><span class="sxs-lookup"><span data-stu-id="a0540-227">When you use the  _rgiidExclude_ parameter to exclude an interface, it also excludes all interfaces derived from that interface.</span></span> <span data-ttu-id="a0540-228">たとえば、 [IMAPIContainer](imapicontainerimapiprop.md)を除外すると、プロバイダーの種類に応じてフォルダーまたはアドレス帳コンテナーが除外されます。</span><span class="sxs-lookup"><span data-stu-id="a0540-228">For example, excluding [IMAPIContainer](imapicontainerimapiprop.md) causes folders or address book containers to be excluded, depending on the type of provider.</span></span> <span data-ttu-id="a0540-229">**imapiprop**または[IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)から派生しているインターフェイスが多いため、これを除外しないでください。</span><span class="sxs-lookup"><span data-stu-id="a0540-229">Do not exclude **IMAPIProp** or [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) because so many interfaces derive from them.</span></span> 
  
<span data-ttu-id="a0540-230">_lppproblems_パラメーターの**sprop問題の配列**構造で返された MAPI_E_COMPUTED エラーを無視します。</span><span class="sxs-lookup"><span data-stu-id="a0540-230">Ignore MAPI_E_COMPUTED errors returned in the **SPropProblemArray** structure in the  _lppProblems_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a0540-231">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="a0540-231">MFCMAPI reference</span></span>

<span data-ttu-id="a0540-232">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0540-232">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a0540-233">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="a0540-233">**File**</span></span>|<span data-ttu-id="a0540-234">**関数**</span><span class="sxs-lookup"><span data-stu-id="a0540-234">**Function**</span></span>|<span data-ttu-id="a0540-235">**コメント**</span><span class="sxs-lookup"><span data-stu-id="a0540-235">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a0540-236">ファイル .cpp</span><span class="sxs-lookup"><span data-stu-id="a0540-236">File.cpp</span></span>  <br/> |<span data-ttu-id="a0540-237">LoadFromMSG</span><span class="sxs-lookup"><span data-stu-id="a0540-237">LoadFromMSG</span></span>  <br/> |<span data-ttu-id="a0540-238">mfcmapi は、 **imapiprop:: CopyTo**メソッドを使用して、.msg ファイルのプロパティを[IMAPIMessageSite](imapimessagesiteiunknown.md)オブジェクトにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0540-238">MFCMAPI uses the **IMAPIProp::CopyTo** method to copy properties from a .msg file to an [IMAPIMessageSite](imapimessagesiteiunknown.md) object.</span></span>  <br/> |
|<span data-ttu-id="a0540-239">folderdlg</span><span class="sxs-lookup"><span data-stu-id="a0540-239">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="a0540-240">cfolderdlg:: handlepaste</span><span class="sxs-lookup"><span data-stu-id="a0540-240">CFolderDlg::HandlePaste</span></span>  <br/> |<span data-ttu-id="a0540-241">mfcmapi は、 **imapiprop:: CopyTo**メソッドを使用して、貼り付け操作中にソースメッセージからターゲットメッセージにプロパティをコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0540-241">MFCMAPI uses the **IMAPIProp::CopyTo** method to copy properties from a source message to a target message during a paste operation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a0540-242">関連項目</span><span class="sxs-lookup"><span data-stu-id="a0540-242">See also</span></span>



[<span data-ttu-id="a0540-243">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="a0540-243">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="a0540-244">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="a0540-244">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="a0540-245">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a0540-245">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)
  
[<span data-ttu-id="a0540-246">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a0540-246">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="a0540-247">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="a0540-247">IMAPISupport::DoProgressDialog</span></span>](imapisupport-doprogressdialog.md)
  
[<span data-ttu-id="a0540-248">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="a0540-248">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
  
[<span data-ttu-id="a0540-249">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="a0540-249">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="a0540-250">PidTagContainerContents 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a0540-250">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="a0540-251">PidTagContainerHierarchy 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a0540-251">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="a0540-252">PidTagMessageAttachments 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a0540-252">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="a0540-253">PidTagMessageDeliveryTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a0540-253">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)
  
[<span data-ttu-id="a0540-254">PidTagMessageRecipients 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a0540-254">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="a0540-255">PidTagObjectType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a0540-255">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="a0540-256">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="a0540-256">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="a0540-257">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="a0540-257">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="a0540-258">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a0540-258">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


<span data-ttu-id="a0540-259">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="a0540-259">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

