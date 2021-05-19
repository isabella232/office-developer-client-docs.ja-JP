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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7319f1abb4a74ee17b0a4a1220215c29434d256b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345508"
---
# <a name="imapipropcopyprops"></a><span data-ttu-id="66060-103">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="66060-103">IMAPIProp::CopyProps</span></span>

  
  
<span data-ttu-id="66060-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66060-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66060-105">選択したプロパティをコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="66060-105">Copies or moves selected properties.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="66060-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="66060-106">Parameters</span></span>

 <span data-ttu-id="66060-107">_lpIncludeProps_</span><span class="sxs-lookup"><span data-stu-id="66060-107">_lpIncludeProps_</span></span>
  
> <span data-ttu-id="66060-108">[in]コピーまたは移動するプロパティを指定するプロパティ タグ配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="66060-108">[in] A pointer to a property tag array that specifies the properties to copy or move.</span></span> <span data-ttu-id="66060-109">**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) を配列に含めません。</span><span class="sxs-lookup"><span data-stu-id="66060-109">**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) cannot be included in the array.</span></span> <span data-ttu-id="66060-110">_lpIncludeProps_ パラメーターを null に **することはできません**。</span><span class="sxs-lookup"><span data-stu-id="66060-110">The  _lpIncludeProps_ parameter cannot be **null**.</span></span>
    
 <span data-ttu-id="66060-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="66060-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="66060-112">[in]進行状況インジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="66060-112">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="66060-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="66060-113">_lpProgress_</span></span>
  
> <span data-ttu-id="66060-114">[in]進行状況インジケーターの実装へのポインター。</span><span class="sxs-lookup"><span data-stu-id="66060-114">[in] A pointer to an implementation of a progress indicator.</span></span> <span data-ttu-id="66060-115">_lpProgress_ パラメーターで null が渡された場合、MAPI 実装を使用して進行状況インジケーターが表示されます。 </span><span class="sxs-lookup"><span data-stu-id="66060-115">If **null** is passed in the  _lpProgress_ parameter, the progress indicator is displayed by using the MAPI implementation.</span></span> <span data-ttu-id="66060-116">_lpProgress パラメーター_ は _、ulFlags_ パラメーター MAPI_DIALOGフラグが設定されていない限り、無視されます。</span><span class="sxs-lookup"><span data-stu-id="66060-116">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="66060-117">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="66060-117">_lpInterface_</span></span>
  
> <span data-ttu-id="66060-118">[in]  _lpDestObj_ パラメーターが指すオブジェクトにアクセスするために使用する必要があるインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="66060-118">[in] A pointer to the interface identifier (IID) that represents the interface that must be used to access the object pointed to by the  _lpDestObj_ parameter.</span></span> <span data-ttu-id="66060-119">_lpInterface パラメーター_ は null に **することはできません**。</span><span class="sxs-lookup"><span data-stu-id="66060-119">The  _lpInterface_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="66060-120">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="66060-120">_lpDestObj_</span></span>
  
> <span data-ttu-id="66060-121">[in]コピーまたは移動されたプロパティを受け取るオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="66060-121">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="66060-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="66060-122">_ulFlags_</span></span>
  
> <span data-ttu-id="66060-123">[in]コピーまたは移動操作を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="66060-123">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="66060-124">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="66060-124">The following flags can be set:</span></span>
    
<span data-ttu-id="66060-125">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="66060-125">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="66060-126">**CopyProps** が [IMAPISupport::D oCopyProps](imapisupport-docopyprops.md)メソッドを呼び出してコピー操作または移動操作を処理する場合は、代わりにエラー値 MAPI_E_DECLINE_COPY を使用して直ちに返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="66060-126">If **CopyProps** calls the [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method to handle the copy or move operation, it should instead return immediately with the error value MAPI_E_DECLINE_COPY.</span></span> <span data-ttu-id="66060-127">再MAPI_DECLINE_OKを制限するために、MAPI によってこのフラグが設定されます。</span><span class="sxs-lookup"><span data-stu-id="66060-127">The MAPI_DECLINE_OK flag is set by MAPI to limit recursion.</span></span> <span data-ttu-id="66060-128">クライアントは、このフラグを設定しません。</span><span class="sxs-lookup"><span data-stu-id="66060-128">Clients do not set this flag.</span></span> 
    
<span data-ttu-id="66060-129">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="66060-129">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="66060-130">進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="66060-130">Displays a progress indicator.</span></span>
    
<span data-ttu-id="66060-131">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="66060-131">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="66060-132">**CopyProps は** 、コピー操作の代わりに移動操作を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="66060-132">**CopyProps** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="66060-133">このフラグを設定しない場合 **、CopyProps は** コピー操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="66060-133">When this flag is not set, **CopyProps** performs a copy operation.</span></span> 
    
<span data-ttu-id="66060-134">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="66060-134">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="66060-135">移動先オブジェクト内の既存のプロパティは上書きしないでください。</span><span class="sxs-lookup"><span data-stu-id="66060-135">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="66060-136">このフラグを設定しない場合 **、CopyProps は既存** のプロパティを上書きします。</span><span class="sxs-lookup"><span data-stu-id="66060-136">When this flag is not set, **CopyProps** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="66060-137">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="66060-137">_lppProblems_</span></span>
  
> <span data-ttu-id="66060-138">[in, out]入力時に [、SPropProblemArray](spropproblemarray.md) 構造体へのポインターを指すポインター。それ以外の **場合は、エラー** 情報が不要であることを示す null。</span><span class="sxs-lookup"><span data-stu-id="66060-138">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, **null**, indicating that there is no need for error information.</span></span> <span data-ttu-id="66060-139">_lppProblems が_ 入力の有効なポインターである場合 **、CopyProps** は 1 つ以上のプロパティをコピーするエラーに関する詳細情報を返します。</span><span class="sxs-lookup"><span data-stu-id="66060-139">If  _lppProblems_ is a valid pointer on input, **CopyProps** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="66060-140">戻り値</span><span class="sxs-lookup"><span data-stu-id="66060-140">Return value</span></span>

<span data-ttu-id="66060-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="66060-141">S_OK</span></span> 
  
> <span data-ttu-id="66060-142">プロパティが正常にコピーまたは移動されました。</span><span class="sxs-lookup"><span data-stu-id="66060-142">Properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="66060-143">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="66060-143">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="66060-144">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティで定義されている同じ表示名を持つサブオブジェクトが、コピー先オブジェクトに既に存在している場合、サブオブジェクトをコピーできません。</span><span class="sxs-lookup"><span data-stu-id="66060-144">A subobject cannot be copied because a subobject with the same display name, defined by the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, already exists in the destination object.</span></span> 
    
<span data-ttu-id="66060-145">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="66060-145">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="66060-146">サービス プロバイダーは、コピー操作を実装しない。</span><span class="sxs-lookup"><span data-stu-id="66060-146">The service provider does not implement the copy operation.</span></span>
    
<span data-ttu-id="66060-147">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="66060-147">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="66060-148">コピーまたは移動操作を直接または間接的に実行するソース オブジェクトには、移動先オブジェクトが含まれる。</span><span class="sxs-lookup"><span data-stu-id="66060-148">The source object performing the copy or move operation directly or indirectly contains the destination object.</span></span> <span data-ttu-id="66060-149">この条件が検出される前に重要な作業が実行された可能性があります。そのため、ソース オブジェクトと移動先オブジェクトが部分的に変更される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="66060-149">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="66060-150">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="66060-150">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="66060-151">_lpInterface_ パラメーターで識別されるインターフェイスは、移動先オブジェクトではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="66060-151">The interface identified by the  _lpInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="66060-152">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="66060-152">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="66060-153">呼び出し元のアクセス許可が不十分なオブジェクトにアクセスしようとした。</span><span class="sxs-lookup"><span data-stu-id="66060-153">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="66060-154">このエラーは、移動先オブジェクトがソース オブジェクトと同じ場合に返されます。</span><span class="sxs-lookup"><span data-stu-id="66060-154">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="66060-155">次の値は **、SPropProblemArray** 構造体で返されますが、CopyProps の戻り値として **返す値として返す必要があります**。</span><span class="sxs-lookup"><span data-stu-id="66060-155">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **CopyProps**.</span></span> <span data-ttu-id="66060-156">これらのエラーは、1 つのプロパティに適用されます。</span><span class="sxs-lookup"><span data-stu-id="66060-156">These errors apply to a single property.</span></span>
  
<span data-ttu-id="66060-157">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="66060-157">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="66060-158">このフラグMAPI_UNICODE設定され **、CopyProps** が Unicode をサポートしていないか、または設定されていない場合MAPI_UNICODE **CopyProps** は Unicode のみをサポートします。</span><span class="sxs-lookup"><span data-stu-id="66060-158">Either the MAPI_UNICODE flag was set and **CopyProps** does not support Unicode, or MAPI_UNICODE was not set and **CopyProps** supports only Unicode.</span></span> 
    
<span data-ttu-id="66060-159">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="66060-159">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="66060-160">プロパティは、読み取り専用プロパティなので、呼び出し元が変更することはできません。これは、移動先オブジェクトの所有者によって計算されます。</span><span class="sxs-lookup"><span data-stu-id="66060-160">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="66060-161">このエラーは重大ではありません。呼び出し元は、コピー操作の続行を許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="66060-161">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="66060-162">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="66060-162">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="66060-163">プロパティの種類が無効です。</span><span class="sxs-lookup"><span data-stu-id="66060-163">The property type is invalid.</span></span>
    
<span data-ttu-id="66060-164">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="66060-164">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="66060-165">プロパティの種類は、呼び出し元が予期する型ではありません。</span><span class="sxs-lookup"><span data-stu-id="66060-165">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="66060-166">注釈</span><span class="sxs-lookup"><span data-stu-id="66060-166">Remarks</span></span>

<span data-ttu-id="66060-167">**IMAPIProp::CopyProps** メソッドは、選択したプロパティを現在のオブジェクトから移動先オブジェクトにコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="66060-167">The **IMAPIProp::CopyProps** method copies or moves selected properties from the current object to a destination object.</span></span> <span data-ttu-id="66060-168">**CopyProps は** 主に、元のメッセージのプロパティの一部だけが返信または転送されたコピーと一緒に移動するメッセージへの返信と転送に使用されます。</span><span class="sxs-lookup"><span data-stu-id="66060-168">**CopyProps** is used mainly for replying to and forwarding messages, where only some of the properties from the original message travel with the reply or forwarded copy.</span></span> 
  
<span data-ttu-id="66060-169">[SPropTagArray](sproptagarray.md)構造体で示されるプロパティの使用に関係なく、ソース オブジェクト内のサブオブジェクトは自動的に操作に含まれてコピーまたは移動されます。</span><span class="sxs-lookup"><span data-stu-id="66060-169">Any subobjects in the source object are automatically included in the operation and copied or moved in their entirety, regardless of the use of properties indicated by the [SPropTagArray](sproptagarray.md) structure.</span></span> <span data-ttu-id="66060-170">既定では **、CopyProps は** 、ソース オブジェクトのプロパティに一致するコピー先オブジェクトのプロパティを上書きします。</span><span class="sxs-lookup"><span data-stu-id="66060-170">By default, **CopyProps** overwrites any properties in the destination object that match properties from the source object.</span></span> <span data-ttu-id="66060-171">コピーまたは移動されたプロパティがコピー先オブジェクトに既に存在する場合、MAPI_NOREPLACE フラグが  _ulFlags_ パラメーターに設定されていない限り、既存のプロパティは新しいプロパティによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="66060-171">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="66060-172">上書きされない移動先オブジェクト内の既存の情報はそのまま残ります。</span><span class="sxs-lookup"><span data-stu-id="66060-172">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="66060-173">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="66060-173">Notes to implementers</span></span>

<span data-ttu-id="66060-174">**CopyProps** の完全な実装を提供するか、MAPI がサポート オブジェクトで提供する実装に依存できます。</span><span class="sxs-lookup"><span data-stu-id="66060-174">You can provide a full implementation of **CopyProps** or rely on the implementation that MAPI provides in its support object.</span></span> <span data-ttu-id="66060-175">MAPI 実装を使用する場合は **、IMAPISupport::D oCopyProps メソッドを呼び出** します。</span><span class="sxs-lookup"><span data-stu-id="66060-175">If you want to use the MAPI implementation, call the **IMAPISupport::DoCopyProps** method.</span></span> <span data-ttu-id="66060-176">ただし **、DoCopyProps** に処理を委任し、MAPI_DECLINE_OK フラグを渡した場合は、サポート呼び出しを回避し、代わりにMAPI_E_DECLINE_COPY返します。</span><span class="sxs-lookup"><span data-stu-id="66060-176">However, if you do delegate processing to **DoCopyProps** and you are passed the MAPI_DECLINE_OK flag, avoid the support call and return MAPI_E_DECLINE_COPY instead.</span></span> <span data-ttu-id="66060-177">フォルダーをコピーするときに発生する可能性のある再帰を回避するために、MAPI によってこのフラグを使用して呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="66060-177">You will be called with this flag by MAPI to avoid the possible recursion that can occur when you copy folders.</span></span> 
  
<span data-ttu-id="66060-178">コピー操作は長い場合がありますから、進行状況インジケーターを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="66060-178">Because the copy operation can be lengthy, you should display a progress indicator.</span></span> <span data-ttu-id="66060-179">[lpProgress パラメーター](imapiprogressiunknown.md)に渡される _IMAPIProgress 実装_(ある場合) を使用します。</span><span class="sxs-lookup"><span data-stu-id="66060-179">Use the [IMAPIProgress](imapiprogressiunknown.md) implementation that is passed in the  _lpProgress_ parameter, if there is one.</span></span> <span data-ttu-id="66060-180">_lpProgress が_ **null** の場合は [、IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md)メソッドを呼び出して MAPI 実装を使用します。</span><span class="sxs-lookup"><span data-stu-id="66060-180">If  _lpProgress_ is **null**, call the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to use the MAPI implementation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="66060-181">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="66060-181">Notes to callers</span></span>

<span data-ttu-id="66060-182">このフラグを設定MAPI_DECLINE_OKしない。これは、メッセージ ストア プロバイダー **CopyProps** 実装への呼び出しで MAPI によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="66060-182">Do not set the MAPI_DECLINE_OK flag; it is used by MAPI in its calls to message store provider **CopyProps** implementations.</span></span> 
  
<span data-ttu-id="66060-183">コピー操作と移動操作には時間がかかる場合があります。このフラグを設定して進行状況インジケーターの表示を要求MAPI_DIALOGです。</span><span class="sxs-lookup"><span data-stu-id="66060-183">Because copy and move operations can take time, it is wise to request the display of a progress indicator by setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="66060-184">_lpProgress パラメーター_ を **IMAPIProgress** の実装 (ある場合)、または null に設定 **できます**。</span><span class="sxs-lookup"><span data-stu-id="66060-184">You can set the  _lpProgress_ parameter to your implementation of **IMAPIProgress**, if you have one, or to **null**.</span></span> <span data-ttu-id="66060-185">_lpProgress が_ null の **場合\*\*\*\*、CopyProps は MAPI** によって提供される既定の進行状況インジケーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="66060-185">If  _lpProgress_ is **null**, **CopyProps** will use the default progress indicator provided by MAPI.</span></span> 
  
<span data-ttu-id="66060-186">進行状況インジケーターの表示を抑制するには、進行状況フラグを設定MAPI_DIALOGできます。</span><span class="sxs-lookup"><span data-stu-id="66060-186">You can suppress the display of a progress indicator by not setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="66060-187">**CopyProps は**  _ulUIParam_ パラメーターと  _lpProgress_ パラメーターを無視し、インジケーターの表示を回避します。</span><span class="sxs-lookup"><span data-stu-id="66060-187">**CopyProps** will ignore the  _ulUIParam_ and  _lpProgress_ parameters and avoid displaying the indicator.</span></span> 
  
 <span data-ttu-id="66060-188">**CopyProps は** 、グローバル および個々のエラー、または 1 つ以上のプロパティで発生するエラーを報告できます。</span><span class="sxs-lookup"><span data-stu-id="66060-188">**CopyProps** can report global and individual errors, or errors that occur with one or more of the properties.</span></span> <span data-ttu-id="66060-189">これらの個々のエラーは **、SPropProblemArray 構造体に入** れ込まれています。</span><span class="sxs-lookup"><span data-stu-id="66060-189">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="66060-190">プロパティの問題配列構造パラメーターに対して、有効なポインターではなく **null** を渡して、プロパティ レベルでのエラー報告を抑制できます。</span><span class="sxs-lookup"><span data-stu-id="66060-190">You can suppress error reporting at the property level by passing **null**, instead of a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="66060-191">エラーに関する情報を受け取る場合は _、lppProblems_ パラメーターに有効な **SPropProblemArray** 構造体ポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="66060-191">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="66060-192">**CopyProps が** プロパティを返S_OK、構造内の個々のプロパティで発生する可能性のあるエラーを確認します。</span><span class="sxs-lookup"><span data-stu-id="66060-192">When **CopyProps** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="66060-193">**CopyProps がエラー** を返す場合 **、SPropProblemArray 構造体には情報は返** されません。</span><span class="sxs-lookup"><span data-stu-id="66060-193">When **CopyProps** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="66060-194">代わりに [、IMAPIProp::GetLastError](imapiprop-getlasterror.md) メソッドを呼び出して、詳細なエラー情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="66060-194">Instead, call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="66060-195">**CopyProps が** 関数を返S_OK [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、返される **SPropProblemArray** 構造体を解放します。</span><span class="sxs-lookup"><span data-stu-id="66060-195">If **CopyProps** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="66060-196">ソース オブジェクトの種類に固有のプロパティをコピーする場合は、コピー先のオブジェクトが同じ型である必要があります。</span><span class="sxs-lookup"><span data-stu-id="66060-196">If you are copying properties that are unique to the source object type, you must make sure that the destination object is of the same type.</span></span> <span data-ttu-id="66060-197">**CopyProps** では、通常、ある種類のオブジェクトに属するプロパティを別の種類のオブジェクトに関連付けできない場合があります。</span><span class="sxs-lookup"><span data-stu-id="66060-197">**CopyProps** does not prevent you from associating properties that typically belong to one type of object with another type of object.</span></span> <span data-ttu-id="66060-198">コピー先オブジェクトに合ったプロパティをコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="66060-198">It is up to you to copy properties that make sense for the destination object.</span></span> <span data-ttu-id="66060-199">たとえば、メッセージ のプロパティをアドレス帳コンテナーにコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="66060-199">For example, you should not copy message properties to an address book container.</span></span> 
  
<span data-ttu-id="66060-200">同じ型のオブジェクト間でコピーを行う場合は、オブジェクト ポインターを比較するか [、IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) メソッドを呼び出して、ソース オブジェクトとコピー先オブジェクトが同じ型である必要があります。</span><span class="sxs-lookup"><span data-stu-id="66060-200">To ensure that you are copying between objects of the same type, check that the source and destination object are the same type, either by comparing object pointers or calling the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) method.</span></span> <span data-ttu-id="66060-201">_lpInterface_ が指すインターフェイス識別子を、ソース オブジェクトの標準インターフェイスに設定します。</span><span class="sxs-lookup"><span data-stu-id="66060-201">Set the interface identifier pointed to by  _lpInterface_ to the standard interface for the source object.</span></span> <span data-ttu-id="66060-202">また、オブジェクトの種類またはプロパティ [(PidTagObjectType)](pidtagobjecttype-canonical-property.md)PR_OBJECT_TYPE **プロパティが** 2 つのオブジェクトで同じであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="66060-202">Also, ensure that the object type or **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property is the same for the two objects.</span></span> <span data-ttu-id="66060-203">たとえば、メッセージからコピーする場合は _、lpInterface_ を IID_IMessage に設定し、PR_OBJECT_TYPE両方のオブジェクトのMAPI_MESSAGE。</span><span class="sxs-lookup"><span data-stu-id="66060-203">For example, if you are copying from a message, set  _lpInterface_ to IID_IMessage and the **PR_OBJECT_TYPE** for both objects to MAPI_MESSAGE.</span></span> 
  
<span data-ttu-id="66060-204">_lpDestObj_ パラメーターに無効なポインターが渡された場合、結果は予測できません。</span><span class="sxs-lookup"><span data-stu-id="66060-204">If an invalid pointer is passed in the  _lpDestObj_ parameter, the results are unpredictable.</span></span> 
  
<span data-ttu-id="66060-205">メッセージの受信者リストをコピーするには、メッセージの **CopyProps** メソッドを呼び出し **、PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) プロパティをプロパティ タグ配列に含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="66060-205">To copy a message's recipient list, call the message's **CopyProps** method and include the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in the property tag array.</span></span> <span data-ttu-id="66060-206">メッセージの添付ファイルをコピーするには、PR_MESSAGE_ATTACHMENTS **(** [PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) プロパティを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="66060-206">To copy the message's attachments, include the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="66060-207">フォルダーまたはアドレス帳コンテナーの階層またはコンテンツ テーブルをコピーするには、プロパティ タグ配列に **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) プロパティまたは **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) プロパティを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="66060-207">To copy a folder or address book container's hierarchy or contents table, include the **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) properties in the property tag array.</span></span> <span data-ttu-id="66060-208">フォルダーに関連付けられているコンテンツ テーブルを含めるには、配列に PR_FOLDER_ASSOCIATED_CONTENTS **(** [PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) プロパティを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="66060-208">To include a folder's associated contents table, include the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property in the array.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="66060-209">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="66060-209">MFCMAPI reference</span></span>

<span data-ttu-id="66060-210">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="66060-210">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="66060-211">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="66060-211">**File**</span></span>|<span data-ttu-id="66060-212">**関数**</span><span class="sxs-lookup"><span data-stu-id="66060-212">**Function**</span></span>|<span data-ttu-id="66060-213">**コメント**</span><span class="sxs-lookup"><span data-stu-id="66060-213">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="66060-214">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="66060-214">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="66060-215">CopyNamedProps</span><span class="sxs-lookup"><span data-stu-id="66060-215">CopyNamedProps</span></span>  <br/> |<span data-ttu-id="66060-216">MFCMAPI は **IMAPIProp::CopyProps** メソッドを使用して、名前付きプロパティをメッセージ間でコピーします。</span><span class="sxs-lookup"><span data-stu-id="66060-216">MFCMAPI uses the **IMAPIProp::CopyProps** method to copy named properties from one message to another.</span></span>  <br/> |
|<span data-ttu-id="66060-217">SingleMAPIPropListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="66060-217">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="66060-218">CSingleMAPIPropListCtrl::OnPasteProperty</span><span class="sxs-lookup"><span data-stu-id="66060-218">CSingleMAPIPropListCtrl::OnPasteProperty</span></span>  <br/> |<span data-ttu-id="66060-219">MFCMAPI は **IMAPIProp::CopyProps** メソッドを使用して、別のオブジェクトからコピーされたプロパティを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="66060-219">MFCMAPI uses the **IMAPIProp::CopyProps** method to paste a property that has been copied from another object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="66060-220">関連項目</span><span class="sxs-lookup"><span data-stu-id="66060-220">See also</span></span>



[<span data-ttu-id="66060-221">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="66060-221">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="66060-222">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="66060-222">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="66060-223">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="66060-223">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="66060-224">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="66060-224">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="66060-225">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="66060-225">IMAPISupport::DoCopyProps</span></span>](imapisupport-docopyprops.md)
  
[<span data-ttu-id="66060-226">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="66060-226">IMAPISupport::DoProgressDialog</span></span>](imapisupport-doprogressdialog.md)
  
[<span data-ttu-id="66060-227">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="66060-227">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="66060-228">PidTagContainerContents 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="66060-228">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="66060-229">PidTagContainerHierarchy 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="66060-229">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="66060-230">PidTagDisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="66060-230">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="66060-231">PidTagFolderAssociatedContents 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="66060-231">PidTagFolderAssociatedContents Canonical Property</span></span>](pidtagfolderassociatedcontents-canonical-property.md)
  
[<span data-ttu-id="66060-232">PidTagMessageAttachments 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="66060-232">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="66060-233">PidTagMessageRecipients 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="66060-233">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="66060-234">PidTagObjectType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="66060-234">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="66060-235">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="66060-235">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="66060-236">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="66060-236">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="66060-237">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="66060-237">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


<span data-ttu-id="66060-238">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="66060-238">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

