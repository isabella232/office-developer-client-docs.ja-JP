---
title: imapipropcopyprops
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345508"
---
# <a name="imapipropcopyprops"></a><span data-ttu-id="6b472-103">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="6b472-103">IMAPIProp::CopyProps</span></span>

  
  
<span data-ttu-id="6b472-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b472-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b472-105">選択されたプロパティをコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="6b472-105">Copies or moves selected properties.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="6b472-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6b472-106">Parameters</span></span>

 <span data-ttu-id="6b472-107">_lpincludeprops_</span><span class="sxs-lookup"><span data-stu-id="6b472-107">_lpIncludeProps_</span></span>
  
> <span data-ttu-id="6b472-108">順番コピーまたは移動するプロパティを指定するプロパティタグ配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6b472-108">[in] A pointer to a property tag array that specifies the properties to copy or move.</span></span> <span data-ttu-id="6b472-109">**PR_NULL**([PidTagNull](pidtagnull-canonical-property.md)) を配列に含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="6b472-109">**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) cannot be included in the array.</span></span> <span data-ttu-id="6b472-110">_lpincludeprops_パラメーターを**null**にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="6b472-110">The  _lpIncludeProps_ parameter cannot be **null**.</span></span>
    
 <span data-ttu-id="6b472-111">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="6b472-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="6b472-112">順番進行状況インジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="6b472-112">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="6b472-113">_lpprogress_</span><span class="sxs-lookup"><span data-stu-id="6b472-113">_lpProgress_</span></span>
  
> <span data-ttu-id="6b472-114">順番進行状況インジケーターの実装へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6b472-114">[in] A pointer to an implementation of a progress indicator.</span></span> <span data-ttu-id="6b472-115">_lpprogress_パラメーターで**null**が渡された場合は、MAPI 実装を使用して進行状況インジケーターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6b472-115">If **null** is passed in the  _lpProgress_ parameter, the progress indicator is displayed by using the MAPI implementation.</span></span> <span data-ttu-id="6b472-116">MAPI_DIALOG フラグが_ulflags_パラメーターで設定されていない場合、 _lpprogress_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="6b472-116">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="6b472-117">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="6b472-117">_lpInterface_</span></span>
  
> <span data-ttu-id="6b472-118">順番_lpdestobj_パラメーターによって指定されたオブジェクトへのアクセスに使用する必要があるインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6b472-118">[in] A pointer to the interface identifier (IID) that represents the interface that must be used to access the object pointed to by the  _lpDestObj_ parameter.</span></span> <span data-ttu-id="6b472-119">_lpinterface_パラメーターを**null**にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="6b472-119">The  _lpInterface_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="6b472-120">_lpdestobj_</span><span class="sxs-lookup"><span data-stu-id="6b472-120">_lpDestObj_</span></span>
  
> <span data-ttu-id="6b472-121">順番コピーまたは移動したプロパティを受け取るオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="6b472-121">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="6b472-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6b472-122">_ulFlags_</span></span>
  
> <span data-ttu-id="6b472-123">順番コピー操作または移動操作を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="6b472-123">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="6b472-124">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="6b472-124">The following flags can be set:</span></span>
    
<span data-ttu-id="6b472-125">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="6b472-125">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="6b472-126">**copyprops**が[imapisupport::D ocopyprops](imapisupport-docopyprops.md)メソッドを呼び出してコピー操作または移動操作を処理する場合は、エラー値 MAPI_E_DECLINE_COPY を使用して直ちに戻る必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b472-126">If **CopyProps** calls the [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method to handle the copy or move operation, it should instead return immediately with the error value MAPI_E_DECLINE_COPY.</span></span> <span data-ttu-id="6b472-127">MAPI_DECLINE_OK フラグは、再帰を制限するために MAPI によって設定されます。</span><span class="sxs-lookup"><span data-stu-id="6b472-127">The MAPI_DECLINE_OK flag is set by MAPI to limit recursion.</span></span> <span data-ttu-id="6b472-128">クライアントはこのフラグを設定しません。</span><span class="sxs-lookup"><span data-stu-id="6b472-128">Clients do not set this flag.</span></span> 
    
<span data-ttu-id="6b472-129">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="6b472-129">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="6b472-130">進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="6b472-130">Displays a progress indicator.</span></span>
    
<span data-ttu-id="6b472-131">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="6b472-131">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="6b472-132">**copyprops**はコピー操作ではなく、移動操作を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b472-132">**CopyProps** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="6b472-133">このフラグが設定されていない場合、 **copyprops**はコピー操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="6b472-133">When this flag is not set, **CopyProps** performs a copy operation.</span></span> 
    
<span data-ttu-id="6b472-134">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="6b472-134">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="6b472-135">対象のオブジェクト内の既存のプロパティは、上書きしないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="6b472-135">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="6b472-136">このフラグが設定されていない場合、 **copyprops**は既存のプロパティを上書きします。</span><span class="sxs-lookup"><span data-stu-id="6b472-136">When this flag is not set, **CopyProps** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="6b472-137">_lppproblems 問題_</span><span class="sxs-lookup"><span data-stu-id="6b472-137">_lppProblems_</span></span>
  
> <span data-ttu-id="6b472-138">[入力]input の場合は、 [spropの配列](spropproblemarray.md)構造体へのポインターへのポインターを返します。それ以外の場合は**null**。エラー情報を必要としないことを示します。</span><span class="sxs-lookup"><span data-stu-id="6b472-138">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, **null**, indicating that there is no need for error information.</span></span> <span data-ttu-id="6b472-139">_lppproblems_が入力の有効なポインターの場合、 **copyprops**は1つまたは複数のプロパティをコピーするときのエラーに関する詳細情報を返します。</span><span class="sxs-lookup"><span data-stu-id="6b472-139">If  _lppProblems_ is a valid pointer on input, **CopyProps** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6b472-140">戻り値</span><span class="sxs-lookup"><span data-stu-id="6b472-140">Return value</span></span>

<span data-ttu-id="6b472-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="6b472-141">S_OK</span></span> 
  
> <span data-ttu-id="6b472-142">プロパティが正常にコピーまたは移動されました。</span><span class="sxs-lookup"><span data-stu-id="6b472-142">Properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="6b472-143">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="6b472-143">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="6b472-144">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティで定義されているのと同じ表示名を持つサブオブジェクトが、対象オブジェクト内に既に存在するため、サブオブジェクトをコピーできません。</span><span class="sxs-lookup"><span data-stu-id="6b472-144">A subobject cannot be copied because a subobject with the same display name, defined by the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, already exists in the destination object.</span></span> 
    
<span data-ttu-id="6b472-145">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="6b472-145">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="6b472-146">サービスプロバイダーがコピー操作を実装していません。</span><span class="sxs-lookup"><span data-stu-id="6b472-146">The service provider does not implement the copy operation.</span></span>
    
<span data-ttu-id="6b472-147">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="6b472-147">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="6b472-148">コピーまたは移動操作を直接または間接的に実行しているソースオブジェクトは、目的のオブジェクトを直接または間接的に格納します。</span><span class="sxs-lookup"><span data-stu-id="6b472-148">The source object performing the copy or move operation directly or indirectly contains the destination object.</span></span> <span data-ttu-id="6b472-149">この条件が検出される前に、重要な作業が実行されている可能性があるので、移行元と移行先のオブジェクトの一部が変更されている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6b472-149">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="6b472-150">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="6b472-150">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="6b472-151">_lpinterface_パラメーターで指定されたインターフェイスは、destination オブジェクトではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6b472-151">The interface identified by the  _lpInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="6b472-152">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="6b472-152">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="6b472-153">発信者が十分なアクセス許可を持っていないオブジェクトにアクセスしようとしました。</span><span class="sxs-lookup"><span data-stu-id="6b472-153">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="6b472-154">destination オブジェクトがソースオブジェクトと同じ場合、このエラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="6b472-154">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="6b472-155">次の値は、 **spropの配列**構造で返すことができますが、 **copyprops**の戻り値として返すことはできません。</span><span class="sxs-lookup"><span data-stu-id="6b472-155">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **CopyProps**.</span></span> <span data-ttu-id="6b472-156">これらのエラーは、1つのプロパティに適用されます。</span><span class="sxs-lookup"><span data-stu-id="6b472-156">These errors apply to a single property.</span></span>
  
<span data-ttu-id="6b472-157">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="6b472-157">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="6b472-158">MAPI_UNICODE フラグが設定されていて、 **copyprops**が unicode をサポートしていないか、MAPI_UNICODE が設定されておらず、 **copyprops**は unicode のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="6b472-158">Either the MAPI_UNICODE flag was set and **CopyProps** does not support Unicode, or MAPI_UNICODE was not set and **CopyProps** supports only Unicode.</span></span> 
    
<span data-ttu-id="6b472-159">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="6b472-159">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="6b472-160">このプロパティは読み取り専用プロパティであるため、呼び出し元が変更することはできません。これは、対象オブジェクトの所有者によって計算されます。</span><span class="sxs-lookup"><span data-stu-id="6b472-160">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="6b472-161">このエラーは重大ではありません。呼び出し元がコピー操作を続行できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b472-161">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="6b472-162">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="6b472-162">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="6b472-163">プロパティの種類が無効です。</span><span class="sxs-lookup"><span data-stu-id="6b472-163">The property type is invalid.</span></span>
    
<span data-ttu-id="6b472-164">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="6b472-164">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="6b472-165">プロパティの型は、呼び出し元が想定した型ではありません。</span><span class="sxs-lookup"><span data-stu-id="6b472-165">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6b472-166">解説</span><span class="sxs-lookup"><span data-stu-id="6b472-166">Remarks</span></span>

<span data-ttu-id="6b472-167">**imapiprop:: copyprops**メソッドは、選択したプロパティを現在のオブジェクトから移動先のオブジェクトにコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="6b472-167">The **IMAPIProp::CopyProps** method copies or moves selected properties from the current object to a destination object.</span></span> <span data-ttu-id="6b472-168">**copyprops**は、主に、元のメッセージの一部のプロパティのみが返信または転送されたコピーで送信されるメッセージの返信と転送に使用します。</span><span class="sxs-lookup"><span data-stu-id="6b472-168">**CopyProps** is used mainly for replying to and forwarding messages, where only some of the properties from the original message travel with the reply or forwarded copy.</span></span> 
  
<span data-ttu-id="6b472-169">[SPropTagArray](sproptagarray.md)構造体で指定されたプロパティの使用に関係なく、ソースオブジェクト内のすべてのサブオブジェクトは、自動的に操作に含まれ、コピーまたは移動されます。</span><span class="sxs-lookup"><span data-stu-id="6b472-169">Any subobjects in the source object are automatically included in the operation and copied or moved in their entirety, regardless of the use of properties indicated by the [SPropTagArray](sproptagarray.md) structure.</span></span> <span data-ttu-id="6b472-170">既定では、 **copyprops**は、source オブジェクトのプロパティに一致する destination オブジェクト内のすべてのプロパティを上書きします。</span><span class="sxs-lookup"><span data-stu-id="6b472-170">By default, **CopyProps** overwrites any properties in the destination object that match properties from the source object.</span></span> <span data-ttu-id="6b472-171">コピーまたは移動されたプロパティのいずれかがコピー先オブジェクトに既に存在する場合、MAPI_NOREPLACE フラグが_ulflags_パラメーターで設定されていない限り、既存のプロパティは新しいプロパティによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="6b472-171">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="6b472-172">上書きされていない対象のオブジェクト内の既存の情報は、そのまま残ります。</span><span class="sxs-lookup"><span data-stu-id="6b472-172">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="6b472-173">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="6b472-173">Notes to implementers</span></span>

<span data-ttu-id="6b472-174">**copyprops**の完全な実装を提供することも、MAPI がサポートオブジェクトで提供する実装を利用することもできます。</span><span class="sxs-lookup"><span data-stu-id="6b472-174">You can provide a full implementation of **CopyProps** or rely on the implementation that MAPI provides in its support object.</span></span> <span data-ttu-id="6b472-175">MAPI 実装を使用する場合は、 **imapisupport::D ocopyprops**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6b472-175">If you want to use the MAPI implementation, call the **IMAPISupport::DoCopyProps** method.</span></span> <span data-ttu-id="6b472-176">ただし、 **docopyprops**に対して処理を委任し、MAPI_DECLINE_OK フラグが渡された場合は、サポートコールを避け、代わりに MAPI_E_DECLINE_COPY を返します。</span><span class="sxs-lookup"><span data-stu-id="6b472-176">However, if you do delegate processing to **DoCopyProps** and you are passed the MAPI_DECLINE_OK flag, avoid the support call and return MAPI_E_DECLINE_COPY instead.</span></span> <span data-ttu-id="6b472-177">フォルダーのコピー時に発生する可能性のある再帰を回避するために、このフラグを使用して MAPI によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6b472-177">You will be called with this flag by MAPI to avoid the possible recursion that can occur when you copy folders.</span></span> 
  
<span data-ttu-id="6b472-178">コピー操作に長い時間がかかる可能性があるため、進行状況インジケーターを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b472-178">Because the copy operation can be lengthy, you should display a progress indicator.</span></span> <span data-ttu-id="6b472-179">_lpprogress_パラメーターに渡された[imapiprogress](imapiprogressiunknown.md)実装を使用します (存在する場合)。</span><span class="sxs-lookup"><span data-stu-id="6b472-179">Use the [IMAPIProgress](imapiprogressiunknown.md) implementation that is passed in the  _lpProgress_ parameter, if there is one.</span></span> <span data-ttu-id="6b472-180">_lpprogress_が**null**の場合は、MAPI 実装を使用するために[imapisupport::D oprogress dialog](imapisupport-doprogressdialog.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6b472-180">If  _lpProgress_ is **null**, call the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to use the MAPI implementation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6b472-181">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="6b472-181">Notes to callers</span></span>

<span data-ttu-id="6b472-182">MAPI_DECLINE_OK フラグは設定しません。これは、メッセージストアプロバイダーの**copyprops**実装への呼び出しで MAPI によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="6b472-182">Do not set the MAPI_DECLINE_OK flag; it is used by MAPI in its calls to message store provider **CopyProps** implementations.</span></span> 
  
<span data-ttu-id="6b472-183">コピー操作および移動操作は時間がかかることがあるため、MAPI_DIALOG フラグを設定して進行状況インジケーターの表示を要求することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="6b472-183">Because copy and move operations can take time, it is wise to request the display of a progress indicator by setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="6b472-184">_lpprogress_パラメーターは、 **imapiprogress**の実装に設定できます (存在する場合)。それ以外の場合は**null**に設定できます。</span><span class="sxs-lookup"><span data-stu-id="6b472-184">You can set the  _lpProgress_ parameter to your implementation of **IMAPIProgress**, if you have one, or to **null**.</span></span> <span data-ttu-id="6b472-185">_lpprogress_が**null**の場合、 **copyprops**は MAPI によって提供される既定の進行状況インジケーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="6b472-185">If  _lpProgress_ is **null**, **CopyProps** will use the default progress indicator provided by MAPI.</span></span> 
  
<span data-ttu-id="6b472-186">MAPI_DIALOG フラグを設定しないと、進行状況インジケーターの表示を抑制することができます。</span><span class="sxs-lookup"><span data-stu-id="6b472-186">You can suppress the display of a progress indicator by not setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="6b472-187">**copyprops**は_uluiparam_パラメーターと_lpprogress_パラメーターを無視し、インジケーターを表示しないようにします。</span><span class="sxs-lookup"><span data-stu-id="6b472-187">**CopyProps** will ignore the  _ulUIParam_ and  _lpProgress_ parameters and avoid displaying the indicator.</span></span> 
  
 <span data-ttu-id="6b472-188">**copyprops**では、グローバルおよび個別のエラー、あるいは1つ以上のプロパティで発生するエラーを報告できます。</span><span class="sxs-lookup"><span data-stu-id="6b472-188">**CopyProps** can report global and individual errors, or errors that occur with one or more of the properties.</span></span> <span data-ttu-id="6b472-189">これらの個々のエラーは、 **sprop問題の配列**構造に配置されます。</span><span class="sxs-lookup"><span data-stu-id="6b472-189">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="6b472-190">プロパティ問題の array 構造パラメーターに対して、有効なポインターではなく**null**を渡すことにより、プロパティレベルでエラー報告を抑制することができます。</span><span class="sxs-lookup"><span data-stu-id="6b472-190">You can suppress error reporting at the property level by passing **null**, instead of a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="6b472-191">エラーに関する情報を受信する必要がある場合は、 _lppproblems_パラメーターに有効な**sprop問題の配列**構造ポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="6b472-191">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="6b472-192">**copyprops**が S_OK を返す場合は、構造内の各プロパティにエラーがあるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="6b472-192">When **CopyProps** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="6b472-193">**copyprops**がエラーを返す場合、 **sprop問題の配列**構造に情報は返されません。</span><span class="sxs-lookup"><span data-stu-id="6b472-193">When **CopyProps** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="6b472-194">代わりに、 [imapiprop:: GetLastError](imapiprop-getlasterror.md)メソッドを呼び出して詳細なエラー情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="6b472-194">Instead, call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="6b472-195">**copyprops**が S_OK を返す場合は、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによって返された**spropの配列**構造を解放します。</span><span class="sxs-lookup"><span data-stu-id="6b472-195">If **CopyProps** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="6b472-196">ソースオブジェクトの種類に固有のプロパティをコピーする場合は、対象のオブジェクトが同じ種類であることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b472-196">If you are copying properties that are unique to the source object type, you must make sure that the destination object is of the same type.</span></span> <span data-ttu-id="6b472-197">**copyprops**では、通常、ある種類のオブジェクトに属するプロパティを別の種類のオブジェクトに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="6b472-197">**CopyProps** does not prevent you from associating properties that typically belong to one type of object with another type of object.</span></span> <span data-ttu-id="6b472-198">目的のオブジェクトに適したプロパティをコピーするのは、自分のユーザーです。</span><span class="sxs-lookup"><span data-stu-id="6b472-198">It is up to you to copy properties that make sense for the destination object.</span></span> <span data-ttu-id="6b472-199">たとえば、メッセージのプロパティをアドレス帳のコンテナーにコピーしないでください。</span><span class="sxs-lookup"><span data-stu-id="6b472-199">For example, you should not copy message properties to an address book container.</span></span> 
  
<span data-ttu-id="6b472-200">同じ種類のオブジェクト間でコピーしていることを確認するには、オブジェクトポインターを比較するか、または[IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx)メソッドを呼び出して、コピー元とコピー先のオブジェクトが同じ種類であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6b472-200">To ensure that you are copying between objects of the same type, check that the source and destination object are the same type, either by comparing object pointers or calling the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) method.</span></span> <span data-ttu-id="6b472-201">_lpinterface_で示されるインターフェイス識別子を、source オブジェクトの標準インターフェイスに設定します。</span><span class="sxs-lookup"><span data-stu-id="6b472-201">Set the interface identifier pointed to by  _lpInterface_ to the standard interface for the source object.</span></span> <span data-ttu-id="6b472-202">また、オブジェクトの種類または**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) プロパティが、2つのオブジェクトに対して同じであることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="6b472-202">Also, ensure that the object type or **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property is the same for the two objects.</span></span> <span data-ttu-id="6b472-203">たとえば、メッセージからコピーする場合は、 _lpinterface_を IID_IMessage に、両方のオブジェクトの**PR_OBJECT_TYPE**を MAPI_MESSAGE に設定します。</span><span class="sxs-lookup"><span data-stu-id="6b472-203">For example, if you are copying from a message, set  _lpInterface_ to IID_IMessage and the **PR_OBJECT_TYPE** for both objects to MAPI_MESSAGE.</span></span> 
  
<span data-ttu-id="6b472-204">_lpdestobj_パラメーターに無効なポインターが渡された場合、結果は予測できません。</span><span class="sxs-lookup"><span data-stu-id="6b472-204">If an invalid pointer is passed in the  _lpDestObj_ parameter, the results are unpredictable.</span></span> 
  
<span data-ttu-id="6b472-205">メッセージの宛先リストをコピーするには、メッセージの**copyprops**メソッドを呼び出して、property タグ配列に**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) プロパティを含めます。</span><span class="sxs-lookup"><span data-stu-id="6b472-205">To copy a message's recipient list, call the message's **CopyProps** method and include the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in the property tag array.</span></span> <span data-ttu-id="6b472-206">メッセージの添付ファイルをコピーするには、 **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) プロパティを含めます。</span><span class="sxs-lookup"><span data-stu-id="6b472-206">To copy the message's attachments, include the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="6b472-207">フォルダーまたはアドレス帳のコンテナーの階層またはコンテンツテーブルをコピーするには、 **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) または**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) プロパティを追加します。プロパティタグ配列。</span><span class="sxs-lookup"><span data-stu-id="6b472-207">To copy a folder or address book container's hierarchy or contents table, include the **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) properties in the property tag array.</span></span> <span data-ttu-id="6b472-208">フォルダーに関連付けられたコンテンツテーブルを含めるには、 **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) プロパティを配列に含めます。</span><span class="sxs-lookup"><span data-stu-id="6b472-208">To include a folder's associated contents table, include the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property in the array.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6b472-209">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="6b472-209">MFCMAPI reference</span></span>

<span data-ttu-id="6b472-210">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b472-210">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6b472-211">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="6b472-211">**File**</span></span>|<span data-ttu-id="6b472-212">**関数**</span><span class="sxs-lookup"><span data-stu-id="6b472-212">**Function**</span></span>|<span data-ttu-id="6b472-213">**コメント**</span><span class="sxs-lookup"><span data-stu-id="6b472-213">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6b472-214">MAPIFunctions</span><span class="sxs-lookup"><span data-stu-id="6b472-214">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="6b472-215">copynamedprops</span><span class="sxs-lookup"><span data-stu-id="6b472-215">CopyNamedProps</span></span>  <br/> |<span data-ttu-id="6b472-216">mfcmapi は、 **imapiprop:: copyprops**メソッドを使用して、あるメッセージから別のメッセージに名前付きプロパティをコピーします。</span><span class="sxs-lookup"><span data-stu-id="6b472-216">MFCMAPI uses the **IMAPIProp::CopyProps** method to copy named properties from one message to another.</span></span>  <br/> |
|<span data-ttu-id="6b472-217">SingleMAPIPropListCtrl</span><span class="sxs-lookup"><span data-stu-id="6b472-217">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="6b472-218">CSingleMAPIPropListCtrl:: OnPasteProperty</span><span class="sxs-lookup"><span data-stu-id="6b472-218">CSingleMAPIPropListCtrl::OnPasteProperty</span></span>  <br/> |<span data-ttu-id="6b472-219">mfcmapi は、 **imapiprop:: copyprops**メソッドを使用して、別のオブジェクトからコピーされたプロパティを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="6b472-219">MFCMAPI uses the **IMAPIProp::CopyProps** method to paste a property that has been copied from another object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6b472-220">関連項目</span><span class="sxs-lookup"><span data-stu-id="6b472-220">See also</span></span>



[<span data-ttu-id="6b472-221">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="6b472-221">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="6b472-222">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6b472-222">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="6b472-223">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="6b472-223">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="6b472-224">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="6b472-224">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="6b472-225">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="6b472-225">IMAPISupport::DoCopyProps</span></span>](imapisupport-docopyprops.md)
  
[<span data-ttu-id="6b472-226">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="6b472-226">IMAPISupport::DoProgressDialog</span></span>](imapisupport-doprogressdialog.md)
  
[<span data-ttu-id="6b472-227">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="6b472-227">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="6b472-228">PidTagContainerContents 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6b472-228">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="6b472-229">PidTagContainerHierarchy 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6b472-229">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="6b472-230">PidTagDisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6b472-230">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="6b472-231">PidTagFolderAssociatedContents 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6b472-231">PidTagFolderAssociatedContents Canonical Property</span></span>](pidtagfolderassociatedcontents-canonical-property.md)
  
[<span data-ttu-id="6b472-232">PidTagMessageAttachments 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6b472-232">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="6b472-233">PidTagMessageRecipients 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6b472-233">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="6b472-234">PidTagObjectType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6b472-234">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="6b472-235">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="6b472-235">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="6b472-236">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="6b472-236">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="6b472-237">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6b472-237">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


<span data-ttu-id="6b472-238">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="6b472-238">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

