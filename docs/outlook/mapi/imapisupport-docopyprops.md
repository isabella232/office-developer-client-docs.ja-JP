---
title: imapisupportdocopyprops
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoCopyProps
api_type:
- COM
ms.assetid: 2446ef52-578a-4004-9719-de9b0207ccad
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 24107ae1926c8590da6a823a354eeae72d72f248
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405584"
---
# <a name="imapisupportdocopyprops"></a><span data-ttu-id="901d8-103">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="901d8-103">IMAPISupport::DoCopyProps</span></span>

  
  
<span data-ttu-id="901d8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="901d8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="901d8-105">オブジェクトの1つまたは複数のプロパティを別のオブジェクトにコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="901d8-105">Copies or moves one or more properties of an object to another object.</span></span>
  
```cpp
HRESULT DoCopyProps(
  LPCIID lpSrcInterface,
  LPVOID lpSrcObj,
  LPSPropTagArray lpIncludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpDestInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="901d8-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="901d8-106">Parameters</span></span>

 <span data-ttu-id="901d8-107">_lpsrcinterface_</span><span class="sxs-lookup"><span data-stu-id="901d8-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="901d8-108">順番コピーまたは移動するプロパティを持つオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="901d8-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object with the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="901d8-109">_lpsrcobj_</span><span class="sxs-lookup"><span data-stu-id="901d8-109">_lpSrcObj_</span></span>
  
> <span data-ttu-id="901d8-110">順番コピーまたは移動するプロパティを含むオブジェクトへのポインターを指定します。</span><span class="sxs-lookup"><span data-stu-id="901d8-110">[in] A pointer to the object that contains the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="901d8-111">_lpincludeprops_</span><span class="sxs-lookup"><span data-stu-id="901d8-111">_lpIncludeProps_</span></span>
  
> <span data-ttu-id="901d8-112">順番コピーまたは移動するプロパティを示す、カウントされたプロパティタグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="901d8-112">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains a counted array of property tags that indicate the properties to copy or move.</span></span> <span data-ttu-id="901d8-113">_lpincludeprops_パラメーターを NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="901d8-113">The  _lpIncludeProps_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="901d8-114">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="901d8-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="901d8-115">順番進行状況インジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="901d8-115">[in] A handle to the parent window of the progress indicator.</span></span>
    
 <span data-ttu-id="901d8-116">_lpprogress_</span><span class="sxs-lookup"><span data-stu-id="901d8-116">_lpProgress_</span></span>
  
> <span data-ttu-id="901d8-117">順番進行状況インジケーターの実装へのポインター。</span><span class="sxs-lookup"><span data-stu-id="901d8-117">[in] A pointer to an implementation of a progress indicator.</span></span> <span data-ttu-id="901d8-118">_lpprogress_パラメーターで NULL が渡された場合は、MAPI 実装を使用して進行状況インジケーターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="901d8-118">If NULL is passed in the  _lpProgress_ parameter, the progress indicator is displayed by using the MAPI implementation.</span></span> <span data-ttu-id="901d8-119">MAPI_DIALOG フラグが_ulflags_パラメーターで設定されていない場合、 _lpprogress_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="901d8-119">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="901d8-120">_lpdestinterface_</span><span class="sxs-lookup"><span data-stu-id="901d8-120">_lpDestInterface_</span></span>
  
> <span data-ttu-id="901d8-121">順番コピーまたは移動されるプロパティを受け取るためのオブジェクトへのアクセスに使用されるインターフェイスを表すインターフェイス識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="901d8-121">[in] A pointer to the interface identifier that represents the interface to be used to access the object to receive the properties that are copied or moved.</span></span>
    
 <span data-ttu-id="901d8-122">_lpdestobj_</span><span class="sxs-lookup"><span data-stu-id="901d8-122">_lpDestObj_</span></span>
  
> <span data-ttu-id="901d8-123">順番コピーまたは移動したプロパティを受け取るオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="901d8-123">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="901d8-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="901d8-124">_ulFlags_</span></span>
  
> <span data-ttu-id="901d8-125">順番コピー操作または移動操作の実行方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="901d8-125">[in] A bitmask of flags that controls how the copy or move operation is performed.</span></span> <span data-ttu-id="901d8-126">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="901d8-126">The following flags can be set:</span></span>
    
<span data-ttu-id="901d8-127">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="901d8-127">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="901d8-128">進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="901d8-128">Displays a progress indicator.</span></span>
    
<span data-ttu-id="901d8-129">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="901d8-129">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="901d8-130">**docopyprops**は、コピー操作ではなく、移動操作を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="901d8-130">**DoCopyProps** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="901d8-131">このフラグが設定されていない場合、 **docopyprops**はコピー操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="901d8-131">When this flag is not set, **DoCopyProps** performs a copy operation.</span></span> 
    
<span data-ttu-id="901d8-132">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="901d8-132">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="901d8-133">対象のオブジェクト内の既存のプロパティは、上書きしないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="901d8-133">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="901d8-134">このフラグが設定されていない場合、 **docopyprops**は既存のプロパティを上書きします。</span><span class="sxs-lookup"><span data-stu-id="901d8-134">When this flag is not set, **DoCopyProps** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="901d8-135">_lppproblems 問題_</span><span class="sxs-lookup"><span data-stu-id="901d8-135">_lppProblems_</span></span>
  
> <span data-ttu-id="901d8-136">[入力]input の場合は、 [spropの配列](spropproblemarray.md)構造体へのポインターへのポインターを返します。それ以外の場合は、エラー情報を必要としないことを示す NULL。</span><span class="sxs-lookup"><span data-stu-id="901d8-136">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates no need for error information.</span></span> <span data-ttu-id="901d8-137">_lppproblems_が入力の有効なポインターである場合、 **docopyprops**は、1つ以上のプロパティをコピーする際のエラーに関する詳細情報を返します。</span><span class="sxs-lookup"><span data-stu-id="901d8-137">If  _lppProblems_ is a valid pointer on input, **DoCopyProps** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="901d8-138">戻り値</span><span class="sxs-lookup"><span data-stu-id="901d8-138">Return value</span></span>

<span data-ttu-id="901d8-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="901d8-139">S_OK</span></span> 
  
> <span data-ttu-id="901d8-140">プロパティが正常にコピーまたは移動されました。</span><span class="sxs-lookup"><span data-stu-id="901d8-140">Properties were successfully copied or moved.</span></span>
    
<span data-ttu-id="901d8-141">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="901d8-141">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="901d8-142">コピーまたは移動されるプロパティは、対象オブジェクトに既に存在し、MAPI_NOREPLACE フラグが設定されています。</span><span class="sxs-lookup"><span data-stu-id="901d8-142">A property to be copied or moved already exists in the destination object and the MAPI_NOREPLACE flag is set.</span></span> 
    
<span data-ttu-id="901d8-143">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="901d8-143">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="901d8-144">source オブジェクトは、直接または間接的に対象のオブジェクトを含みます。</span><span class="sxs-lookup"><span data-stu-id="901d8-144">The source object directly or indirectly contains the destination object.</span></span> <span data-ttu-id="901d8-145">この条件が検出される前に、重要な作業が実行されている可能性があるので、移行元と移行先のオブジェクトの一部が変更されている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="901d8-145">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="901d8-146">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="901d8-146">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="901d8-147">_lpsrcinterface_パラメーターによって識別されるインターフェイスは、source オブジェクトではサポートされていません。また、 _lpsrcinterface_パラメーターで指定されたインターフェイスは、destination オブジェクトではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="901d8-147">The interface identified by the  _lpSrcInterface_ parameter is not supported by the source object, or the interface identified by the  _lpDestInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="901d8-148">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="901d8-148">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="901d8-149">発信者が十分なアクセス許可を持っていないオブジェクトにアクセスしようとしました。</span><span class="sxs-lookup"><span data-stu-id="901d8-149">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="901d8-150">destination オブジェクトがソースオブジェクトと同じ場合、このエラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="901d8-150">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="901d8-151">次の値は、 **spropの配列**構造で返すことができますが、 **docopyprops**の戻り値としては返されません。</span><span class="sxs-lookup"><span data-stu-id="901d8-151">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **DoCopyProps**.</span></span> <span data-ttu-id="901d8-152">これらのエラーは、1つのプロパティに適用されます。</span><span class="sxs-lookup"><span data-stu-id="901d8-152">These errors apply to a single property.</span></span>
  
<span data-ttu-id="901d8-153">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="901d8-153">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="901d8-154">MAPI_UNICODE フラグが設定されており、 **docopyprops**が unicode をサポートしていないか、MAPI_UNICODE が設定されておらず、 **docopyprops**が unicode のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="901d8-154">Either the MAPI_UNICODE flag was set and **DoCopyProps** does not support Unicode, or MAPI_UNICODE was not set and **DoCopyProps** supports only Unicode.</span></span> 
    
<span data-ttu-id="901d8-155">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="901d8-155">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="901d8-156">このプロパティは読み取り専用プロパティであるため、呼び出し元が変更することはできません。これは、対象オブジェクトの所有者によって計算されます。</span><span class="sxs-lookup"><span data-stu-id="901d8-156">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="901d8-157">このエラーは重大ではありません。呼び出し元がコピー操作を続行できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="901d8-157">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="901d8-158">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="901d8-158">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="901d8-159">プロパティの種類が無効です。</span><span class="sxs-lookup"><span data-stu-id="901d8-159">The property type is invalid.</span></span>
    
<span data-ttu-id="901d8-160">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="901d8-160">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="901d8-161">プロパティの型が、呼び出し元が想定している型ではありません。</span><span class="sxs-lookup"><span data-stu-id="901d8-161">The property type is not the type that the caller expects.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="901d8-162">注釈</span><span class="sxs-lookup"><span data-stu-id="901d8-162">Remarks</span></span>

<span data-ttu-id="901d8-163">**imapisupport::D ocopyprops**メソッドは、メッセージストアプロバイダーサポートオブジェクトに実装されています。</span><span class="sxs-lookup"><span data-stu-id="901d8-163">The **IMAPISupport::DoCopyProps** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="901d8-164">メッセージストアプロバイダーは、 **docopyprops**を呼び出して、フォルダーとメッセージに[imapiprop:: copyprops](imapiprop-copyprops.md)メソッドを実装できます。</span><span class="sxs-lookup"><span data-stu-id="901d8-164">Message store providers can call **DoCopyProps** to implement the [IMAPIProp::CopyProps](imapiprop-copyprops.md) method for their folders and messages.</span></span> <span data-ttu-id="901d8-165">**docopyprops**は、 _lpincludeprops_が指すプロパティタグ配列で指定されているプロパティをコピーまたは移動します。これは、 _lpsrcobj_が指すオブジェクトに存在します。</span><span class="sxs-lookup"><span data-stu-id="901d8-165">**DoCopyProps** copies or moves the properties that are identified in the property tag array pointed to by  _lpIncludeProps_ and that are present in the object pointed to by  _lpSrcObj_.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="901d8-166">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="901d8-166">Notes to callers</span></span>

<span data-ttu-id="901d8-167">2つのメッセージなど、同じ種類のオブジェクト間でプロパティをコピーする場合、 _lpsrcinterface_パラメーターと_lpsrcinterface_パラメーターには同じインターフェイス識別子を含める必要があります。 _lpsrcobj_パラメーターと lpsrcinterface パラメーターは同じである必要があります。 __ 同じ種類のオブジェクトをポイントする必要があります。</span><span class="sxs-lookup"><span data-stu-id="901d8-167">When you copy properties between objects of the same type, such as two messages, the  _lpSrcInterface_ and  _lpDestInterface_ parameters must contain the same interface identifier, and the  _lpSrcObj_ and  _lpDestObj_ parameters must point to objects of the same type.</span></span> <span data-ttu-id="901d8-168">_lpdestinterface_が NULL に設定されている場合、 **docopyprops**は MAPI_E_INVALID_PARAMETER を返します。</span><span class="sxs-lookup"><span data-stu-id="901d8-168">If  _lpDestInterface_ is set to NULL, **DoCopyProps** returns MAPI_E_INVALID_PARAMETER.</span></span> <span data-ttu-id="901d8-169">_lpdestinterface_を受け入れ可能なインターフェイス識別子に設定しても、 _lpdestinterface_を無効なポインターに設定した場合、結果は予測できません。</span><span class="sxs-lookup"><span data-stu-id="901d8-169">If you set  _lpDestInterface_ to an acceptable interface identifier, but set  _lpDestObj_ to an invalid pointer, the results are unpredictable.</span></span> <span data-ttu-id="901d8-170">多くの場合、プロバイダーは失敗します。</span><span class="sxs-lookup"><span data-stu-id="901d8-170">Most likely your provider will fail.</span></span> 
  
<span data-ttu-id="901d8-171">変換先オブジェクトのプロパティを上書きする必要がない場合は、MAPI_NOREPLACE フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="901d8-171">Set the MAPI_NOREPLACE flag if you do not want any of the properties in the destination object to be overwritten.</span></span> <span data-ttu-id="901d8-172">コピー元のオブジェクトに存在し、上書きされていない対象のオブジェクトのプロパティは、削除または変更されません。</span><span class="sxs-lookup"><span data-stu-id="901d8-172">Properties in the destination object that exist in the source object and are not overwritten are not deleted or modified.</span></span>
  
<span data-ttu-id="901d8-173">メッセージの宛先リストをコピーするには、 _lpincludeprops_パラメーターで指定されたプロパティタグ配列に**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) プロパティを含めます。</span><span class="sxs-lookup"><span data-stu-id="901d8-173">To copy a message's recipient list, include the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in the property tag array pointed to by the  _lpIncludeProps_ parameter.</span></span> <span data-ttu-id="901d8-174">メッセージの添付ファイルをコピーするには、 **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) プロパティを含めます。</span><span class="sxs-lookup"><span data-stu-id="901d8-174">To copy the message's attachments, include the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="901d8-175">フォルダーまたはアドレス帳コンテナーの階層またはコンテンツテーブルをコピーするには、 **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) または**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) をプロパティタグ配列に含めます。</span><span class="sxs-lookup"><span data-stu-id="901d8-175">To copy a folder or address book container's hierarchy or contents table, include **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag array.</span></span> <span data-ttu-id="901d8-176">フォルダーに関連付けられたコンテンツテーブルを含めるには、 **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) プロパティを配列に含めます。</span><span class="sxs-lookup"><span data-stu-id="901d8-176">To include a folder's associated contents table, include the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property in the array.</span></span>
  
<span data-ttu-id="901d8-177">サブフォルダーをコピーまたは移動すると、 **SPropTagArray**構造で指定されているプロパティの使用に関係なく、その内容がコピーまたは移動されます。</span><span class="sxs-lookup"><span data-stu-id="901d8-177">If subfolders are copied or moved, their contents are copied or moved in their entirety, regardless of the use of properties indicated by the **SPropTagArray** structure.</span></span> 
  
 <span data-ttu-id="901d8-178">**docopyprops**は、操作が全体として発生するグローバルエラーと、1つ以上のプロパティで発生する個々のエラーを報告します。</span><span class="sxs-lookup"><span data-stu-id="901d8-178">**DoCopyProps** reports global errors that occur with the operation as a whole, and individual errors that occur with one or more of the properties.</span></span> <span data-ttu-id="901d8-179">これらの個々のエラーは、 **sprop問題の配列**構造に配置されます。</span><span class="sxs-lookup"><span data-stu-id="901d8-179">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="901d8-180">プロパティ問題の array 構造パラメーターに対して、有効なポインターではなく NULL を渡すことにより、プロパティレベルでエラー報告を抑制することができます。</span><span class="sxs-lookup"><span data-stu-id="901d8-180">You can suppress error reporting at the property level by passing NULL, rather than a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="901d8-181">エラーに関する情報を受信する必要がある場合は、 _lppproblems_パラメーターに有効な**sprop問題の配列**構造ポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="901d8-181">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="901d8-182">**docopyprops**が S_OK を返す場合、構造内の各プロパティにエラーがあるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="901d8-182">When **DoCopyProps** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="901d8-183">**docopyprops**がエラーを返す場合、 **sprop問題の配列**構造に情報は返されません。</span><span class="sxs-lookup"><span data-stu-id="901d8-183">When **DoCopyProps** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="901d8-184">代わりに、 [imapisupport:: GetLastError](imapisupport-getlasterror.md)メソッドを呼び出して詳細なエラー情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="901d8-184">Instead, call the [IMAPISupport::GetLastError](imapisupport-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="901d8-185">**docopyprops**が S_OK を返す場合は、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによって返された**spropの配列**構造を解放します。</span><span class="sxs-lookup"><span data-stu-id="901d8-185">If **DoCopyProps** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="901d8-186">関連項目</span><span class="sxs-lookup"><span data-stu-id="901d8-186">See also</span></span>



[<span data-ttu-id="901d8-187">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="901d8-187">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
  
[<span data-ttu-id="901d8-188">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="901d8-188">IMAPISupport::CopyMessages</span></span>](imapisupport-copymessages.md)
  
[<span data-ttu-id="901d8-189">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="901d8-189">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
  
[<span data-ttu-id="901d8-190">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="901d8-190">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="901d8-191">PidTagContainerContents 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="901d8-191">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="901d8-192">PidTagContainerHierarchy 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="901d8-192">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="901d8-193">PidTagFolderAssociatedContents 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="901d8-193">PidTagFolderAssociatedContents Canonical Property</span></span>](pidtagfolderassociatedcontents-canonical-property.md)
  
[<span data-ttu-id="901d8-194">PidTagMessageAttachments 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="901d8-194">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="901d8-195">PidTagMessageRecipients 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="901d8-195">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="901d8-196">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="901d8-196">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="901d8-197">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="901d8-197">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="901d8-198">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="901d8-198">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

