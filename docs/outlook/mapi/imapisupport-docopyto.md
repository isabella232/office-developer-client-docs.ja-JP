---
title: IMAPISupportDoCopyTo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoCopyTo
api_type:
- COM
ms.assetid: 84019475-5176-4fc5-a3ee-871095077498
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5ce5aa8c43e284b493a0709808a196c6c6889f88
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592109"
---
# <a name="imapisupportdocopyto"></a><span data-ttu-id="d776f-103">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="d776f-103">IMAPISupport::DoCopyTo</span></span>

  
  
<span data-ttu-id="d776f-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d776f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d776f-105">明確に除外されたプロパティを 1 つのオブジェクトのすべてのプロパティを別のオブジェクトを移動またはコピーします。</span><span class="sxs-lookup"><span data-stu-id="d776f-105">Copies or moves all properties of one object, except for specifically excluded properties, to another object.</span></span>
  
```cpp
HRESULT DoCopyTo(
  LPCIID lpSrcInterface,
  LPVOID lpSrcObj,
  ULONG ciidExclude,
  LPCIID rgiidExclude,
  LPSPropTagArray lpExcludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpDestInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="d776f-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d776f-106">Parameters</span></span>

 <span data-ttu-id="d776f-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="d776f-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="d776f-108">[in]コピーまたは移動するにはプロパティを持つオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d776f-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object that has the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="d776f-109">_lpSrcObj_</span><span class="sxs-lookup"><span data-stu-id="d776f-109">_lpSrcObj_</span></span>
  
> <span data-ttu-id="d776f-110">[in]コピーまたは移動するにはプロパティを持つオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d776f-110">[in] A pointer to the object that has the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="d776f-111">_ciidExclude_</span><span class="sxs-lookup"><span data-stu-id="d776f-111">_ciidExclude_</span></span>
  
> <span data-ttu-id="d776f-112">[in]コピーまたはプロパティを移動する際に除外するインターフェイスの数。</span><span class="sxs-lookup"><span data-stu-id="d776f-112">[in] The count of interfaces to exclude when you copy or move properties.</span></span>
    
 <span data-ttu-id="d776f-113">_rgiidExclude_</span><span class="sxs-lookup"><span data-stu-id="d776f-113">_rgiidExclude_</span></span>
  
> <span data-ttu-id="d776f-114">[in]コピーまたは変換先オブジェクトに補足的な情報を移動するときに使用しないインターフェイスを示すインターフェイス識別子の配列。</span><span class="sxs-lookup"><span data-stu-id="d776f-114">[in] An array of interface identifiers that indicates interfaces that should not be used when you copy or move supplemental information to the destination object.</span></span>
    
 <span data-ttu-id="d776f-115">_lpExcludeProps_</span><span class="sxs-lookup"><span data-stu-id="d776f-115">_lpExcludeProps_</span></span>
  
> <span data-ttu-id="d776f-116">[in]コピーから除外する必要がありますまたは移動操作のプロパティ タグを識別するプロパティ タグ配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d776f-116">[in] A pointer to a property tag array that identifies the property tags that should be excluded from the copy or move operation.</span></span> <span data-ttu-id="d776f-117">_LpExcludeProps_パラメーターに NULL を渡すことでは、あるすべてのオブジェクトのプロパティがコピーまたは移動することを示します。</span><span class="sxs-lookup"><span data-stu-id="d776f-117">Passing NULL in the  _lpExcludeProps_ parameter indicates that all of the object's properties should be copied or moved.</span></span> <span data-ttu-id="d776f-118">**DoCopyTo**は、MAPI_E_INVALID_PARAMETER、**あう**、 [SPropTagArray](sproptagarray.md)構造体のメンバーが_lpExcludeProps_で示される場合は 0 に設定を取得します。</span><span class="sxs-lookup"><span data-stu-id="d776f-118">**DoCopyTo** returns MAPI_E_INVALID_PARAMETER when the **cValues** member of the [SPropTagArray](sproptagarray.md) structure pointed to by  _lpExcludeProps_ is set to 0.</span></span> 
    
 <span data-ttu-id="d776f-119">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="d776f-119">_ulUIParam_</span></span>
  
> <span data-ttu-id="d776f-120">[in]進行状況インジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="d776f-120">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="d776f-121">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="d776f-121">_lpProgress_</span></span>
  
> <span data-ttu-id="d776f-122">[in]進行状況インジケーターの実装へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d776f-122">[in] A pointer to a progress indicator implementation.</span></span> <span data-ttu-id="d776f-123">_LpProgress_パラメーターに NULL を渡した場合、MAPI は、進行状況の実装を提供します。</span><span class="sxs-lookup"><span data-stu-id="d776f-123">If NULL is passed in the  _lpProgress_ parameter, MAPI provides the progress implementation.</span></span> <span data-ttu-id="d776f-124">_UlFlags_パラメーターで MAPI_DIALOG フラグが設定されていない場合、 _lpProgress_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="d776f-124">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="d776f-125">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="d776f-125">_lpDestInterface_</span></span>
  
> <span data-ttu-id="d776f-126">[in]コピーまたは移動先のプロパティを表示するオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d776f-126">[in] A pointer to the interface identifier that represents the interface to be used to access the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="d776f-127">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="d776f-127">_lpDestObj_</span></span>
  
> <span data-ttu-id="d776f-128">[in]コピーまたは移動先のプロパティを表示するオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d776f-128">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="d776f-129">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d776f-129">_ulFlags_</span></span>
  
> <span data-ttu-id="d776f-130">[in]コピーまたは移動操作を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="d776f-130">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="d776f-131">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="d776f-131">The following flags can be set:</span></span>
    
<span data-ttu-id="d776f-132">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="d776f-132">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="d776f-133">進行状況のインジケーターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d776f-133">Displays a progress indicator.</span></span> 
    
<span data-ttu-id="d776f-134">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="d776f-134">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="d776f-135">**DoCopyTo**は、コピー操作ではなく移動操作を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d776f-135">**DoCopyTo** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="d776f-136">このフラグが設定されていない場合、 **DoCopyTo**は、コピー操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="d776f-136">When this flag is not set, **DoCopyTo** performs a copy operation.</span></span> 
    
<span data-ttu-id="d776f-137">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="d776f-137">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="d776f-138">コピー先オブジェクトの既存のプロパティを上書きしてはなりません。</span><span class="sxs-lookup"><span data-stu-id="d776f-138">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="d776f-139">このフラグが設定されていない場合、 **DoCopyTo**には、既存のプロパティが上書きされます。</span><span class="sxs-lookup"><span data-stu-id="d776f-139">When this flag is not set, **DoCopyTo** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="d776f-140">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="d776f-140">_lppProblems_</span></span>
  
> <span data-ttu-id="d776f-141">[out][SPropProblemArray](spropproblemarray.md)構造体へのポインターへのポインターの入力でそれ以外の場合、NULL、エラー情報の必要性を示すしません。</span><span class="sxs-lookup"><span data-stu-id="d776f-141">[out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates no need for error information.</span></span> <span data-ttu-id="d776f-142">_LppProblems_が入力時に有効なポインターである場合は、 **DoCopyTo**は、1 つまたは複数のプロパティのコピーでエラーに関する詳細な情報を返します。</span><span class="sxs-lookup"><span data-stu-id="d776f-142">If  _lppProblems_ is a valid pointer on input, **DoCopyTo** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d776f-143">�߂�l</span><span class="sxs-lookup"><span data-stu-id="d776f-143">Return value</span></span>

<span data-ttu-id="d776f-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="d776f-144">S_OK</span></span> 
  
> <span data-ttu-id="d776f-145">プロパティは、正常にコピーまたは移動されています。</span><span class="sxs-lookup"><span data-stu-id="d776f-145">The properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="d776f-146">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="d776f-146">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="d776f-147">先のオブジェクトのプロパティをコピーまたは移動を既にが存在して MAPI_NOREPLACE フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="d776f-147">A property to be copied or moved already exists in the destination object and the MAPI_NOREPLACE flag is set.</span></span> 
    
<span data-ttu-id="d776f-148">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="d776f-148">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="d776f-149">ソース オブジェクトには直接または間接的に目的のオブジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d776f-149">The source object directly or indirectly contains the destination object.</span></span> <span data-ttu-id="d776f-150">重要な作業が実行された前に、この条件が検出された元とコピー先のオブジェクトを部分的に変更された可能性がありますので。</span><span class="sxs-lookup"><span data-stu-id="d776f-150">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="d776f-151">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="d776f-151">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="d776f-152">_LpSrcObj_が指すオブジェクトでは、 _lpSrcInterface_パラメーターで指定されたインターフェイスはサポートされていない、または_の lpDestObj が指すオブジェクトでは、 _lpDestInterface_パラメーターで指定されたインターフェイスはサポートされていません_.</span><span class="sxs-lookup"><span data-stu-id="d776f-152">The interface identified by the  _lpSrcInterface_ parameter is not supported by the object pointed to by  _lpSrcObj_, or the interface identified by the  _lpDestInterface_ parameter is not supported by the object pointed to by  _lpDestObj_.</span></span> 
    
<span data-ttu-id="d776f-153">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="d776f-153">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="d776f-154">呼び出し元が十分なアクセス許可を持っているオブジェクトにアクセスしようとしました。</span><span class="sxs-lookup"><span data-stu-id="d776f-154">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="d776f-155">目的のオブジェクトは、ソース オブジェクトと同じ場合、このエラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="d776f-155">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="d776f-156">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d776f-156">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="d776f-157">_LpSrcInterface_パラメーターは、NULL です。</span><span class="sxs-lookup"><span data-stu-id="d776f-157">The  _lpSrcInterface_ parameter is NULL.</span></span> 
    
<span data-ttu-id="d776f-158">次の値が返される、 **SPropProblemArray**構造体には戻り値としてではなく**DoCopyTo**。</span><span class="sxs-lookup"><span data-stu-id="d776f-158">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **DoCopyTo**.</span></span> <span data-ttu-id="d776f-159">これらのエラーは、1 つのプロパティに適用されます。</span><span class="sxs-lookup"><span data-stu-id="d776f-159">These errors apply to a single property.</span></span>
  
<span data-ttu-id="d776f-160">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="d776f-160">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="d776f-161">か、MAPI_UNICODE フラグが設定された**DoCopyTo**は、Unicode をサポートしていませんまたは MAPI_UNICODE が設定されていないと**DoCopyTo**は、Unicode だけをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="d776f-161">Either the MAPI_UNICODE flag was set and **DoCopyTo** does not support Unicode, or MAPI_UNICODE was not set and **DoCopyTo** supports only Unicode.</span></span> 
    
<span data-ttu-id="d776f-162">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="d776f-162">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="d776f-163">コピー先オブジェクトの所有者によって計算される、読み取り専用プロパティであるために、呼び出し元がプロパティを変更できません。</span><span class="sxs-lookup"><span data-stu-id="d776f-163">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="d776f-164">このエラーは重大です。呼び出し元は、コピー操作を続行を許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d776f-164">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="d776f-165">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="d776f-165">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="d776f-166">プロパティの型が正しくありません。</span><span class="sxs-lookup"><span data-stu-id="d776f-166">The property type is invalid.</span></span>
    
<span data-ttu-id="d776f-167">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="d776f-167">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="d776f-168">プロパティの型は、呼び出し元の型ではありません。</span><span class="sxs-lookup"><span data-stu-id="d776f-168">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d776f-169">注釈</span><span class="sxs-lookup"><span data-stu-id="d776f-169">Remarks</span></span>

<span data-ttu-id="d776f-170">メッセージ ストア プロバイダーのサポート オブジェクトの**IMAPISupport::DoCopyTo**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="d776f-170">The **IMAPISupport::DoCopyTo** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="d776f-171">メッセージ ストア プロバイダーは、そのフォルダーとメッセージの[IMAPIProp::CopyTo](imapiprop-copyto.md)メソッドを実装するために**DoCopyTo**を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="d776f-171">Message store providers can call **DoCopyTo** to implement the [IMAPIProp::CopyTo](imapiprop-copyto.md) method for their folders and messages.</span></span> 
  
<span data-ttu-id="d776f-172">既定では、 **DoCopyTo**にコピーまたはすべて 1 つのオブジェクトのプロパティの別のオブジェクトを移動します。</span><span class="sxs-lookup"><span data-stu-id="d776f-172">By default, **DoCopyTo** copies or moves all of the properties of one object to another object.</span></span> <span data-ttu-id="d776f-173">ソース オブジェクトのサブオブジェクトに自動的に操作に含まれているとコピーまたは移動の全体です。</span><span class="sxs-lookup"><span data-stu-id="d776f-173">Any subobjects in the source object are automatically included in the operation and copied or moved in their entirety.</span></span> 
  
<span data-ttu-id="d776f-174">コピー先オブジェクトにコピーまたは移動先のプロパティのいずれかの場合、 _ulFlags_パラメーターに MAPI_NOREPLACE フラグが設定されていない限り、既存のプロパティが新しいプロパティによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="d776f-174">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="d776f-175">変更は上書きされず、変換先オブジェクトの既存の情報は行われないです。</span><span class="sxs-lookup"><span data-stu-id="d776f-175">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d776f-176">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="d776f-176">Notes to callers</span></span>

<span data-ttu-id="d776f-177">除外するプロパティのコピーか移動の操作を_lpExcludeProps_パラメーターで、プロパティ タグが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d776f-177">To exclude properties from the copy or move operation, include their property tags in the  _lpExcludeProps_ parameter.</span></span> <span data-ttu-id="d776f-178">プロパティ タグ プロパティ タグ配列内の特定の識別子からを構築する[PROP_TAG](prop_tag.md)マクロを使用する場合の結果を渡すと、その識別子を持つすべてのプロパティは除外されます。</span><span class="sxs-lookup"><span data-stu-id="d776f-178">If you pass the results of using the [PROP_TAG](prop_tag.md) macro to build a property tag from a specific identifier in the property tag array, all properties with that identifier will be excluded.</span></span> <span data-ttu-id="d776f-179">たとえば、プロパティ タグ配列内の次のエントリでは、種類に関係なく、除外する 0x8002 の識別子を持つすべてのプロパティが発生します。</span><span class="sxs-lookup"><span data-stu-id="d776f-179">For example, the following entry in the property tag array causes all properties with an identifier of 0x8002 to be excluded, regardless of type:</span></span> 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
<span data-ttu-id="d776f-180">プロパティをコピーすると、メッセージを別のフォルダーに**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) を指定するメッセージの配信時刻をコピーしないようにするのには、タグは、配列を除外します。</span><span class="sxs-lookup"><span data-stu-id="d776f-180">To avoid copying a message's delivery time when you copy the message to a different folder, specify **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) in the property tag exclude array.</span></span> <span data-ttu-id="d776f-181">メッセージの受信者の一覧を除外するには、除外アレイに**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) のプロパティを追加します。</span><span class="sxs-lookup"><span data-stu-id="d776f-181">To exclude a message's recipient list, add the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property to the exclude array.</span></span> <span data-ttu-id="d776f-182">メッセージの添付ファイルを除外するには、配列に**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) のプロパティを追加します。</span><span class="sxs-lookup"><span data-stu-id="d776f-182">To exclude a message's attachments, add the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property to the array.</span></span>
  
<span data-ttu-id="d776f-183">同様に、コピーまたはフォルダー、アドレス帳コンテナーの階層、または内容のテーブルの移動を防ぐためには、 **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) または**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) プロパティのタグは配列を除外します。</span><span class="sxs-lookup"><span data-stu-id="d776f-183">Similarly, to prevent the copying or moving of a folder or address book container's hierarchy or contents table, include **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag exclude array.</span></span>
  
<span data-ttu-id="d776f-184">MAPI_E_COMPUTED を無視して、 **SPropProblemArray**パラメーターに構造体の_lppProblems_でエラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="d776f-184">Ignore MAPI_E_COMPUTED errors returned in the **SPropProblemArray** structure in the  _lppProblems_ parameter.</span></span> 
  
<span data-ttu-id="d776f-185">_LpSrcInterface_ポイントは、通常、インターフェイス識別子と同じを_lpDestInterface_が指すインターフェイスの識別子です。</span><span class="sxs-lookup"><span data-stu-id="d776f-185">The interface identifier that  _lpSrcInterface_ points to is usually the same as the interface identifier that  _lpDestInterface_ points to.</span></span> 
  
<span data-ttu-id="d776f-186">_LpDestInterface_で受け入れ可能なインタ フェース識別子が_lpDestObj_に無効なポインターを渡す場合、結果は予測できません。</span><span class="sxs-lookup"><span data-stu-id="d776f-186">If you pass an acceptable interface identifier in  _lpDestInterface_ but an invalid pointer in  _lpDestObj_, the results are unpredictable.</span></span> <span data-ttu-id="d776f-187">ほとんどの場合、プロバイダーは失敗になります。</span><span class="sxs-lookup"><span data-stu-id="d776f-187">Most likely this will cause your provider to fail.</span></span> 
  
<span data-ttu-id="d776f-188">逆に、コピーまたは移動する必要がありますはない補足的な情報に注意してください場合は、 _rgiidExclude_パラメーターに渡される配列に除外するインターフェイスのインターフェイス識別子を追加します。</span><span class="sxs-lookup"><span data-stu-id="d776f-188">Conversely, if you are aware of supplemental information that should not be copied or moved, add the interface identifiers for the interfaces to be excluded in the array passed in the  _rgiidExclude_ parameter.</span></span> <span data-ttu-id="d776f-189">たとえば、コピーする場合は、メッセージが、メッセージの添付ファイルのいずれかのない、 _rgiidExclude_配列の IID_IMessage を渡します。</span><span class="sxs-lookup"><span data-stu-id="d776f-189">For example, if you are copying messages, but not any of their message attachments, pass IID_IMessage in the  _rgiidExclude_ array.</span></span> <span data-ttu-id="d776f-190">**DoCopyTo**では、認識されない_rgiidExclude_に記載されているすべてのインタ フェースを無視します。</span><span class="sxs-lookup"><span data-stu-id="d776f-190">**DoCopyTo** ignores any interfaces listed in  _rgiidExclude_ that it does not recognize.</span></span> 
  
<span data-ttu-id="d776f-191">インタ フェースを除外するのには、 _rgiidExclude_パラメーターを使用する場合も、そのインターフェイスから派生するすべてのインタ フェースを除外します。</span><span class="sxs-lookup"><span data-stu-id="d776f-191">When you use the  _rgiidExclude_ parameter to exclude an interface, it also excludes all interfaces derived from that interface.</span></span> <span data-ttu-id="d776f-192">などの[IMAPIContainer](imapicontainerimapiprop.md)インタ フェースを除外すると、フォルダーまたはプロバイダーの種類によって、除外するアドレス帳のコンテナー。</span><span class="sxs-lookup"><span data-stu-id="d776f-192">For example, excluding the [IMAPIContainer](imapicontainerimapiprop.md) interface causes folders or address book containers to be excluded, depending on the type of provider.</span></span> <span data-ttu-id="d776f-193">非常に多くのインターフェイスは、それらから派生するために[IMAPIProp](imapipropiunknown.md)または[IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)を除外しません。</span><span class="sxs-lookup"><span data-stu-id="d776f-193">Do not exclude [IMAPIProp](imapipropiunknown.md) or [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) because so many interfaces derive from them.</span></span> 
  
 <span data-ttu-id="d776f-194">**DoCopyTo**では、全体として操作に適用されるグローバル エラーと個々 のプロパティに適用される個々 のエラーを報告します。</span><span class="sxs-lookup"><span data-stu-id="d776f-194">**DoCopyTo** reports global errors that apply to the operation as a whole, and individual errors that apply to individual properties.</span></span> <span data-ttu-id="d776f-195">これらの個々 のエラーは、 **SPropProblemArray**構造体に配置されます。</span><span class="sxs-lookup"><span data-stu-id="d776f-195">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="d776f-196">プロパティ問題配列構造体パラメーターに有効なポインターではなく NULL を渡すことにより、プロパティ レベルでレポートのエラーを抑制できます。</span><span class="sxs-lookup"><span data-stu-id="d776f-196">You can suppress error reporting at the property level by passing NULL, rather than a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="d776f-197">エラーに関する情報を受信する場合は、 _lppProblems_パラメーターに有効な**SPropProblemArray**構造体のポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="d776f-197">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="d776f-198">**DoCopyTo**に S_OK が返されるときは、構造内の個々 のプロパティを持つ可能性のあるエラーを確認します。</span><span class="sxs-lookup"><span data-stu-id="d776f-198">When **DoCopyTo** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="d776f-199">**DoCopyTo**にエラーが返されるとき、 **SPropProblemArray**構造体の情報は返されません。</span><span class="sxs-lookup"><span data-stu-id="d776f-199">When **DoCopyTo** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="d776f-200">代わりに、詳細なエラー情報を取得するために[IMAPISupport::GetLastError](imapisupport-getlasterror.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d776f-200">Instead, call the [IMAPISupport::GetLastError](imapisupport-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="d776f-201">**DoCopyTo**では、S_OK が返された場合は、 [MAPIFreeBuffer](mapifreebuffer.md)関数の呼び出しによって返された**SPropProblemArray**構造体を解放します。</span><span class="sxs-lookup"><span data-stu-id="d776f-201">If **DoCopyTo** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="d776f-202">**DoCopyTo**の呼び出しでは、グローバル エラーが発生する場合を使用したりしないで、 **SPropProblemArray**構造体を解放します。</span><span class="sxs-lookup"><span data-stu-id="d776f-202">If a global error occurs on the **DoCopyTo** call, do not use or free the **SPropProblemArray** structure.</span></span> <span data-ttu-id="d776f-203">プロバイダーは、 **DoCopyTo**によって返された**SPropProblemArray**構造体の_ulIndex_メンバーを無視してください。</span><span class="sxs-lookup"><span data-stu-id="d776f-203">Providers should ignore the  _ulIndex_ member in **SPropProblemArray** structures returned by **DoCopyTo**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d776f-204">関連項目</span><span class="sxs-lookup"><span data-stu-id="d776f-204">See also</span></span>



[<span data-ttu-id="d776f-205">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="d776f-205">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="d776f-206">IMAPISupport::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="d776f-206">IMAPISupport::CopyFolder</span></span>](imapisupport-copyfolder.md)
  
[<span data-ttu-id="d776f-207">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="d776f-207">IMAPISupport::CopyMessages</span></span>](imapisupport-copymessages.md)
  
[<span data-ttu-id="d776f-208">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="d776f-208">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="d776f-209">PidTagContainerContents 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d776f-209">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="d776f-210">PidTagContainerHierarchy 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d776f-210">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="d776f-211">PidTagMessageAttachments 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d776f-211">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="d776f-212">PidTagMessageDeliveryTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d776f-212">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)
  
[<span data-ttu-id="d776f-213">PidTagMessageRecipients 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d776f-213">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="d776f-214">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="d776f-214">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="d776f-215">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="d776f-215">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="d776f-216">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d776f-216">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

