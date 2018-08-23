---
title: IMAPIPropOpenProperty
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.OpenProperty
api_type:
- COM
ms.assetid: e400e6cc-4e36-43fc-9304-b688a0a7fd77
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e5f35474910f2257e18bcdc3b6b1dc661e2dc63a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563976"
---
# <a name="imapipropopenproperty"></a><span data-ttu-id="9f08e-103">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="9f08e-103">IMAPIProp::OpenProperty</span></span>

<span data-ttu-id="9f08e-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f08e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f08e-105">プロパティにアクセスするために使用するインターフェイスへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="9f08e-105">Returns a pointer to an interface that can be used to access a property.</span></span>
  
```cpp
HRESULT OpenProperty(
  ULONG ulPropTag,
  LPCIID lpiid,
  ULONG ulInterfaceOptions,
  ULONG ulFlags,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="9f08e-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9f08e-106">Parameters</span></span>

 <span data-ttu-id="9f08e-107">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="9f08e-107">_ulPropTag_</span></span>
  
> <span data-ttu-id="9f08e-108">[in]アクセスするプロパティのプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="9f08e-108">[in] The property tag for the property to be accessed.</span></span> <span data-ttu-id="9f08e-109">識別子と型の両方は、プロパティ タグに含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f08e-109">Both the identifier and the type must be included in the property tag.</span></span>
    
 <span data-ttu-id="9f08e-110">_lpiid_</span><span class="sxs-lookup"><span data-stu-id="9f08e-110">_lpiid_</span></span>
  
> <span data-ttu-id="9f08e-111">[in]プロパティへのアクセスに使用するインターフェイスの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9f08e-111">[in] A pointer to the identifier for the interface to be used to access the property.</span></span> <span data-ttu-id="9f08e-112">_Lpiid_パラメーターを**null**にするにはできません。</span><span class="sxs-lookup"><span data-stu-id="9f08e-112">The  _lpiid_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="9f08e-113">_ulInterfaceOptions_</span><span class="sxs-lookup"><span data-stu-id="9f08e-113">_ulInterfaceOptions_</span></span>
  
> <span data-ttu-id="9f08e-114">[in]_Lpiid_パラメーターで識別されるインターフェイスに関連するデータです。</span><span class="sxs-lookup"><span data-stu-id="9f08e-114">[in] Data that relates to the interface identified by the  _lpiid_ parameter.</span></span> 
    
 <span data-ttu-id="9f08e-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9f08e-115">_ulFlags_</span></span>
  
> <span data-ttu-id="9f08e-116">[in]プロパティへのアクセスを制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="9f08e-116">[in] A bitmask of flags that controls access to the property.</span></span> <span data-ttu-id="9f08e-117">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="9f08e-117">The following flags can be set:</span></span>
    
<span data-ttu-id="9f08e-118">タグ</span><span class="sxs-lookup"><span data-stu-id="9f08e-118">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="9f08e-119">プロパティが存在しない場合は作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f08e-119">If the property does not exist, it should be created.</span></span> <span data-ttu-id="9f08e-120">プロパティが存在する場合、プロパティの現在の値は破棄されます。</span><span class="sxs-lookup"><span data-stu-id="9f08e-120">If the property does exist, the current value of the property should be discarded.</span></span> <span data-ttu-id="9f08e-121">タグ フラグを設定すると、呼び出し元としても、MAPI_MODIFY フラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f08e-121">When a caller sets the MAPI_CREATE flag, it should also set the MAPI_MODIFY flag.</span></span>
    
<span data-ttu-id="9f08e-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="9f08e-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="9f08e-123">正常に戻す、可能性のあるオブジェクトが呼び出し元に完全に利用できる前に**OpenProperty**を使用できます。</span><span class="sxs-lookup"><span data-stu-id="9f08e-123">Allows **OpenProperty** to return successfully, possibly before the object is fully available to the caller.</span></span> <span data-ttu-id="9f08e-124">オブジェクトが使用できない場合は、後続のオブジェクトの呼び出しを行うとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="9f08e-124">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="9f08e-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="9f08e-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="9f08e-126">MAPI_MODIFY がこのような状況で必要です。</span><span class="sxs-lookup"><span data-stu-id="9f08e-126">MAPI_MODIFY is required in these situations:</span></span>
    
  - <span data-ttu-id="9f08e-127">時、 **IID_IStream**、それを変更するなどのストリームのプロパティを開いています。</span><span class="sxs-lookup"><span data-stu-id="9f08e-127">When opening a stream property, such as **IID_IStream**, to modify it.</span></span>
    
  - <span data-ttu-id="9f08e-128">時、 [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md)を**IID_IMessage**、それを変更すると開くように、埋め込みメッセージの添付ファイルを開いています。</span><span class="sxs-lookup"><span data-stu-id="9f08e-128">When opening an embedded message attachment, such as [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) opened with **IID_IMessage**, to modify it.</span></span>
    
 <span data-ttu-id="9f08e-129">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="9f08e-129">_lppUnk_</span></span>
  
> <span data-ttu-id="9f08e-130">[out]プロパティへのアクセスに使用する要求されたインターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="9f08e-130">[out] A pointer to the requested interface to be used for property access.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9f08e-131">�߂�l</span><span class="sxs-lookup"><span data-stu-id="9f08e-131">Return value</span></span>

<span data-ttu-id="9f08e-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="9f08e-132">S_OK</span></span> 
  
> <span data-ttu-id="9f08e-133">要求されたインターフェイス ポインターが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="9f08e-133">The requested interface pointer was successfully returned.</span></span>
    
<span data-ttu-id="9f08e-134">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="9f08e-134">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="9f08e-135">このプロパティには、要求されたインターフェイスはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="9f08e-135">The requested interface is not supported for this property.</span></span>
    
<span data-ttu-id="9f08e-136">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="9f08e-136">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="9f08e-137">呼び出し側では、プロパティにアクセスする十分なアクセス許可を持っています。</span><span class="sxs-lookup"><span data-stu-id="9f08e-137">The caller has insufficient permissions to access the property.</span></span>
    
<span data-ttu-id="9f08e-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="9f08e-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="9f08e-139">オブジェクトは、要求されたインターフェイスには、このプロパティへのアクセスを提供できません。</span><span class="sxs-lookup"><span data-stu-id="9f08e-139">The object cannot provide access to this property through the requested interface.</span></span>
    
<span data-ttu-id="9f08e-140">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="9f08e-140">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="9f08e-141">要求されたプロパティが存在しないため、 _ulFlags_パラメーターのタグが設定されていませんでした。</span><span class="sxs-lookup"><span data-stu-id="9f08e-141">The requested property does not exist and MAPI_CREATE was not set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="9f08e-142">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9f08e-142">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="9f08e-143">タグのプロパティの型は、PT_UNSPECIFIED に設定されます。</span><span class="sxs-lookup"><span data-stu-id="9f08e-143">The property type in the tag is set to PT_UNSPECIFIED.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9f08e-144">注釈</span><span class="sxs-lookup"><span data-stu-id="9f08e-144">Remarks</span></span>

<span data-ttu-id="9f08e-145">**IMAPIProp::OpenProperty**メソッドは、特定のインターフェイスからプロパティへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="9f08e-145">The **IMAPIProp::OpenProperty** method provides access to a property through a particular interface.</span></span> <span data-ttu-id="9f08e-146">**OpenProperty**は、 [IMAPIProp::GetProps](imapiprop-getprops.md)と[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドの代替です。</span><span class="sxs-lookup"><span data-stu-id="9f08e-146">**OpenProperty** is an alternative to the [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::SetProps](imapiprop-setprops.md) methods.</span></span> <span data-ttu-id="9f08e-147">**GetProps**または**SetProps**のいずれかのプロパティには、大きすぎる、または複雑すぎるために失敗した場合、 **OpenProperty**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9f08e-147">When either **GetProps** or **SetProps** fails because the property is too large or too complex, call **OpenProperty**.</span></span> <span data-ttu-id="9f08e-148">**OpenProperty**は、PT_OBJECT の種類のプロパティにアクセスするのには通常使用されます。</span><span class="sxs-lookup"><span data-stu-id="9f08e-148">**OpenProperty** is typically used to access properties of type PT_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9f08e-149">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="9f08e-149">Notes to callers</span></span>

<span data-ttu-id="9f08e-150">メッセージの添付ファイルにアクセスするには、添付ファイルの種類に応じて、別のインターフェイス識別子を使用して**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) のプロパティを開きます。</span><span class="sxs-lookup"><span data-stu-id="9f08e-150">To access message attachments, open the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property with a different interface identifier, depending on the type of attachment.</span></span> <span data-ttu-id="9f08e-151">次の表には、さまざまな種類の添付ファイルの**OpenProperty**を呼び出す方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9f08e-151">The following table describes how to call **OpenProperty** for the different types of attachments:</span></span> 
  
|<span data-ttu-id="9f08e-152">**添付ファイルの種類**</span><span class="sxs-lookup"><span data-stu-id="9f08e-152">**Type of attachment**</span></span>|<span data-ttu-id="9f08e-153">**インターフェイス識別子を使用するには**</span><span class="sxs-lookup"><span data-stu-id="9f08e-153">**Interface identifier to use**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9f08e-154">バイナリ型 (Binary)</span><span class="sxs-lookup"><span data-stu-id="9f08e-154">Binary</span></span>  <br/> |<span data-ttu-id="9f08e-155">IID_IStream</span><span class="sxs-lookup"><span data-stu-id="9f08e-155">IID_IStream</span></span>  <br/> |
|<span data-ttu-id="9f08e-156">String</span><span class="sxs-lookup"><span data-stu-id="9f08e-156">String</span></span>  <br/> |<span data-ttu-id="9f08e-157">IID_IStream</span><span class="sxs-lookup"><span data-stu-id="9f08e-157">IID_IStream</span></span>  <br/> |
|<span data-ttu-id="9f08e-158">Message</span><span class="sxs-lookup"><span data-stu-id="9f08e-158">Message</span></span>  <br/> |<span data-ttu-id="9f08e-159">IID_IMessage</span><span class="sxs-lookup"><span data-stu-id="9f08e-159">IID_IMessage</span></span>  <br/> |
|<span data-ttu-id="9f08e-160">OLE 2.0</span><span class="sxs-lookup"><span data-stu-id="9f08e-160">OLE 2.0</span></span>  <br/> |<span data-ttu-id="9f08e-161">IID_IStreamDocfile</span><span class="sxs-lookup"><span data-stu-id="9f08e-161">IID_IStreamDocfile</span></span>  <br/> |
   
<span data-ttu-id="9f08e-162">**IStreamDocfile**は、OLE 2.0 の複合ファイルに基づく[IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx)インターフェイスの派生物です。</span><span class="sxs-lookup"><span data-stu-id="9f08e-162">**IStreamDocfile** is a derivative of the [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) interface that is based on an OLE 2.0 compound file.</span></span> <span data-ttu-id="9f08e-163">**IStreamDocfile**は、最小限のオーバーヘッドが伴うので、OLE 2.0 の添付ファイルをアクセスするための最適な選択肢です。</span><span class="sxs-lookup"><span data-stu-id="9f08e-163">**IStreamDocfile** is the best choice for accessing OLE 2.0 attachments because it involves the least amount of overhead.</span></span> <span data-ttu-id="9f08e-164">[IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx)インターフェイスを使用できるが構造化ストレージに保存されたデータが含まれているこれらのプロパティには、IID_IStreamDocFile を使用できます。</span><span class="sxs-lookup"><span data-stu-id="9f08e-164">You can use IID_IStreamDocFile for those properties that contain data stored in structured storage available through the [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) interface.</span></span> 
  
<span data-ttu-id="9f08e-165">添付ファイル付きの**OpenProperty**を使用する方法の詳細については、 **PR_ATTACH_DATA_OBJ**プロパティと[添付ファイルを開く](opening-an-attachment.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9f08e-165">For more information about how to use **OpenProperty** with attachments, see the **PR_ATTACH_DATA_OBJ** property and [Opening an Attachment](opening-an-attachment.md).</span></span>
  
<span data-ttu-id="9f08e-166">メソッドを呼び出すときに、[シーク](http://msdn.microsoft.com/en-us/library/aa380043%28v=VS.85%29.aspx)または[setsize 関数](http://msdn.microsoft.com/en-us/library/aa380044%28v=VS.85%29.aspx)のいずれか、ゼロの位置またはサイズの変数を使用する場合を除き、受信した**IStream**ポインターを使用しません。</span><span class="sxs-lookup"><span data-stu-id="9f08e-166">Do not use the **IStream** pointer that you receive to call either its [Seek](http://msdn.microsoft.com/en-us/library/aa380043%28v=VS.85%29.aspx) or [SetSize](http://msdn.microsoft.com/en-us/library/aa380044%28v=VS.85%29.aspx) method unless you use a zero position or size variable.</span></span> <span data-ttu-id="9f08e-167">**シーク**の呼び出しから返された_plibNewPosition_の出力パラメーターの値に依存しないでも、します。</span><span class="sxs-lookup"><span data-stu-id="9f08e-167">Also, do not rely on the value of the  _plibNewPosition_ output parameter returned from the **Seek** call.</span></span> 
  
<span data-ttu-id="9f08e-168">**IStream**インターフェイスを使用してプロパティにアクセスするのには**OpenProperty**を呼び出す場合は、変更することをそのインタ フェースを使用します。</span><span class="sxs-lookup"><span data-stu-id="9f08e-168">If you call **OpenProperty** to access a property with the **IStream** interface, use only that interface to make changes to it.</span></span> <span data-ttu-id="9f08e-169">その他のプロパティを更新しようとはしないで[IMAPIProp: IUnknown](imapipropiunknown.md) **SetProps**や[IMAPIProp::DeleteProps](imapiprop-deleteprops.md)などのメソッドです。</span><span class="sxs-lookup"><span data-stu-id="9f08e-169">Do not attempt to update the property with any of the other [IMAPIProp : IUnknown](imapipropiunknown.md) methods, such as **SetProps** or [IMAPIProp::DeleteProps](imapiprop-deleteprops.md).</span></span> 
  
<span data-ttu-id="9f08e-170">**OpenProperty**のプロパティを複数回開くしないでください。</span><span class="sxs-lookup"><span data-stu-id="9f08e-170">Do not try to open a property with **OpenProperty** more than once.</span></span> <span data-ttu-id="9f08e-171">プロバイダーによって異なる場合があるため、結果は定義されていません。</span><span class="sxs-lookup"><span data-stu-id="9f08e-171">The results are undefined because they can vary from provider to provider.</span></span> 
  
<span data-ttu-id="9f08e-172">開く] プロパティを変更する場合は、MAPI_MODIFY フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="9f08e-172">If you need to modify the property to be opened, set the MAPI_MODIFY flag.</span></span> <span data-ttu-id="9f08e-173">オブジェクトがプロパティをサポートするかどうかがわからない場合は、必要と思われるタグと MAPI_MODIFY フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="9f08e-173">If you are not sure whether the object supports the property but you think it should, set the MAPI_CREATE and MAPI_MODIFY flags.</span></span> <span data-ttu-id="9f08e-174">タグを設定すると、MAPI_MODIFY も設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f08e-174">Whenever MAPI_CREATE is set, MAPI_MODIFY must also be set.</span></span>
  
<span data-ttu-id="9f08e-175">_Lpiid_パラメーターで指定されたインターフェイスに対応する 1 つに、 _lppUnk_パラメーターで返されるインターフェイス ポインターを見直すために責任があります。</span><span class="sxs-lookup"><span data-stu-id="9f08e-175">You are responsible for recasting the interface pointer returned in the  _lppUnk_ parameter to one that is appropriate for the interface specified in the  _lpiid_ parameter.</span></span> <span data-ttu-id="9f08e-176">メソッドを呼び出す[が](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx)操作を終了するときに返されたポインターを使用することもする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f08e-176">You must also use the returned pointer to call its [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method when you are finished with it.</span></span> 
  
<span data-ttu-id="9f08e-177">_UlFlags_パラメーターでフラグを設定ことがあります不足のために必要なプロパティへのアクセスの種類を示すためにではありません。</span><span class="sxs-lookup"><span data-stu-id="9f08e-177">Sometimes setting the flags in the  _ulFlags_ parameter is not enough to indicate the type of access to the property that is required.</span></span> <span data-ttu-id="9f08e-178">_UlInterfaceOptions_パラメーターには、フラグなどの追加データを配置できます。</span><span class="sxs-lookup"><span data-stu-id="9f08e-178">You can put additional data, such as flags, in the  _ulInterfaceOptions_ parameter.</span></span> <span data-ttu-id="9f08e-179">依存するインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="9f08e-179">This data is interface dependent.</span></span> <span data-ttu-id="9f08e-180">いくつかのインタ フェース ( **IStream**) が使われ、そうでないです。</span><span class="sxs-lookup"><span data-stu-id="9f08e-180">Some interfaces (such as **IStream**) use it, and others do not.</span></span> <span data-ttu-id="9f08e-181">たとえば、 **IStream**を変更するプロパティを開くと MAPI_MODIFY だけでなく、 _ulInterfaceOptions_パラメーターに STGM_WRITE フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="9f08e-181">For example, when you open a property to be modified with **IStream**, set the STGM_WRITE flag in the  _ulInterfaceOptions_ parameter in addition to MAPI_MODIFY.</span></span> <span data-ttu-id="9f08e-182">[IMAPITable](imapitableiunknown.md)インターフェイスを使用してテーブルを開くときは、文字列のプロパティを保持するテーブルの列が Unicode 形式である必要があるかどうかを示すために MAPI_UNICODE に_ulInterfaceOptions_を設定できます。</span><span class="sxs-lookup"><span data-stu-id="9f08e-182">When you open a table by using the [IMAPITable](imapitableiunknown.md) interface, you can set  _ulInterfaceOptions_ to MAPI_UNICODE to indicate whether the columns in the table that hold string properties should be in Unicode format.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9f08e-183">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="9f08e-183">MFCMAPI reference</span></span>

<span data-ttu-id="9f08e-184">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="9f08e-184">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9f08e-185">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="9f08e-185">**File**</span></span>|<span data-ttu-id="9f08e-186">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="9f08e-186">**Function**</span></span>|<span data-ttu-id="9f08e-187">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="9f08e-187">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9f08e-188">StreamEditor.cpp</span><span class="sxs-lookup"><span data-stu-id="9f08e-188">StreamEditor.cpp</span></span>  <br/> |<span data-ttu-id="9f08e-189">CStreamEditor::ReadTextStreamFromProperty</span><span class="sxs-lookup"><span data-stu-id="9f08e-189">CStreamEditor::ReadTextStreamFromProperty</span></span>  <br/> |<span data-ttu-id="9f08e-190">MFCMAPI では、 **IMAPIProp::OpenProperty**メソッドを使用して、サイズの大きなテキストおよびバイナリのプロパティのストリーム インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="9f08e-190">MFCMAPI uses the **IMAPIProp::OpenProperty** method to retrieve a stream interface for large text and binary properties.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9f08e-191">関連項目</span><span class="sxs-lookup"><span data-stu-id="9f08e-191">See also</span></span>

- [<span data-ttu-id="9f08e-192">HrIStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="9f08e-192">HrIStorageFromStream</span></span>](hristoragefromstream.md) 
- [<span data-ttu-id="9f08e-193">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="9f08e-193">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md) 
- [<span data-ttu-id="9f08e-194">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="9f08e-194">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
- [<span data-ttu-id="9f08e-195">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="9f08e-195">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
- [<span data-ttu-id="9f08e-196">IMAPISupport::IStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="9f08e-196">IMAPISupport::IStorageFromStream</span></span>](imapisupport-istoragefromstream.md)
- [<span data-ttu-id="9f08e-197">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9f08e-197">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
- [<span data-ttu-id="9f08e-198">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9f08e-198">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
- <span data-ttu-id="9f08e-199">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="9f08e-199">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
- [<span data-ttu-id="9f08e-200">添付ファイルを開く</span><span class="sxs-lookup"><span data-stu-id="9f08e-200">Opening an Attachment</span></span>](opening-an-attachment.md)

