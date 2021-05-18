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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7bf1d6912e44319c36e288cd3870218e8c4e45ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319811"
---
# <a name="imapipropopenproperty"></a><span data-ttu-id="81d76-103">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="81d76-103">IMAPIProp::OpenProperty</span></span>

<span data-ttu-id="81d76-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81d76-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81d76-105">プロパティへのアクセスに使用できるインターフェイスへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="81d76-105">Returns a pointer to an interface that can be used to access a property.</span></span>
  
```cpp
HRESULT OpenProperty(
  ULONG ulPropTag,
  LPCIID lpiid,
  ULONG ulInterfaceOptions,
  ULONG ulFlags,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="81d76-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="81d76-106">Parameters</span></span>

 <span data-ttu-id="81d76-107">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="81d76-107">_ulPropTag_</span></span>
  
> <span data-ttu-id="81d76-108">[in]アクセスするプロパティのプロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="81d76-108">[in] The property tag for the property to be accessed.</span></span> <span data-ttu-id="81d76-109">識別子と型の両方をプロパティ タグに含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="81d76-109">Both the identifier and the type must be included in the property tag.</span></span>
    
 <span data-ttu-id="81d76-110">_lpiid_</span><span class="sxs-lookup"><span data-stu-id="81d76-110">_lpiid_</span></span>
  
> <span data-ttu-id="81d76-111">[in]プロパティへのアクセスに使用するインターフェイスの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="81d76-111">[in] A pointer to the identifier for the interface to be used to access the property.</span></span> <span data-ttu-id="81d76-112">_lpiid パラメーターは_ null に **することはできません**。</span><span class="sxs-lookup"><span data-stu-id="81d76-112">The  _lpiid_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="81d76-113">_ulInterfaceOptions_</span><span class="sxs-lookup"><span data-stu-id="81d76-113">_ulInterfaceOptions_</span></span>
  
> <span data-ttu-id="81d76-114">[in]  _lpiid_ パラメーターで識別されるインターフェイスに関連するデータ。</span><span class="sxs-lookup"><span data-stu-id="81d76-114">[in] Data that relates to the interface identified by the  _lpiid_ parameter.</span></span> 
    
 <span data-ttu-id="81d76-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="81d76-115">_ulFlags_</span></span>
  
> <span data-ttu-id="81d76-116">[in]プロパティへのアクセスを制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="81d76-116">[in] A bitmask of flags that controls access to the property.</span></span> <span data-ttu-id="81d76-117">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="81d76-117">The following flags can be set:</span></span>
    
<span data-ttu-id="81d76-118">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="81d76-118">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="81d76-119">プロパティが存在しない場合は、作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="81d76-119">If the property does not exist, it should be created.</span></span> <span data-ttu-id="81d76-120">プロパティが存在する場合は、プロパティの現在の値を破棄する必要があります。</span><span class="sxs-lookup"><span data-stu-id="81d76-120">If the property does exist, the current value of the property should be discarded.</span></span> <span data-ttu-id="81d76-121">呼び出し元が MAPI_CREATEフラグを設定すると、呼び出し元フラグMAPI_MODIFYする必要があります。</span><span class="sxs-lookup"><span data-stu-id="81d76-121">When a caller sets the MAPI_CREATE flag, it should also set the MAPI_MODIFY flag.</span></span>
    
<span data-ttu-id="81d76-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="81d76-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="81d76-123">オブジェクトが呼び出し元で完全に使用できる前に **、OpenProperty** が正常に返されるのを許可します。</span><span class="sxs-lookup"><span data-stu-id="81d76-123">Allows **OpenProperty** to return successfully, possibly before the object is fully available to the caller.</span></span> <span data-ttu-id="81d76-124">オブジェクトを使用できない場合は、後続のオブジェクト呼び出しでエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="81d76-124">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="81d76-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="81d76-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="81d76-126">MAPI_MODIFYは、次の状況で必要です。</span><span class="sxs-lookup"><span data-stu-id="81d76-126">MAPI_MODIFY is required in these situations:</span></span>
    
  - <span data-ttu-id="81d76-127">ストリーム プロパティを開く場合 **(IID_IStreamなど)** を変更します。</span><span class="sxs-lookup"><span data-stu-id="81d76-127">When opening a stream property, such as **IID_IStream**, to modify it.</span></span>
    
  - <span data-ttu-id="81d76-128">埋め込みメッセージ添付ファイルを開く場合 (PR_ATTACH_DATA_OBJ [で開](pidtagattachdataobject-canonical-property.md) IID_IMessage **など)** を変更します。</span><span class="sxs-lookup"><span data-stu-id="81d76-128">When opening an embedded message attachment, such as [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) opened with **IID_IMessage**, to modify it.</span></span>
    
 <span data-ttu-id="81d76-129">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="81d76-129">_lppUnk_</span></span>
  
> <span data-ttu-id="81d76-130">[out]プロパティ アクセスに使用する要求されたインターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="81d76-130">[out] A pointer to the requested interface to be used for property access.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="81d76-131">戻り値</span><span class="sxs-lookup"><span data-stu-id="81d76-131">Return value</span></span>

<span data-ttu-id="81d76-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="81d76-132">S_OK</span></span> 
  
> <span data-ttu-id="81d76-133">要求されたインターフェイス ポインターが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="81d76-133">The requested interface pointer was successfully returned.</span></span>
    
<span data-ttu-id="81d76-134">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="81d76-134">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="81d76-135">要求されたインターフェイスは、このプロパティではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="81d76-135">The requested interface is not supported for this property.</span></span>
    
<span data-ttu-id="81d76-136">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="81d76-136">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="81d76-137">呼び出し元には、プロパティにアクセスするためのアクセス許可が不十分です。</span><span class="sxs-lookup"><span data-stu-id="81d76-137">The caller has insufficient permissions to access the property.</span></span>
    
<span data-ttu-id="81d76-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="81d76-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="81d76-139">オブジェクトは、要求されたインターフェイスを介してこのプロパティへのアクセスを提供できません。</span><span class="sxs-lookup"><span data-stu-id="81d76-139">The object cannot provide access to this property through the requested interface.</span></span>
    
<span data-ttu-id="81d76-140">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="81d76-140">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="81d76-141">要求されたプロパティは存在し  _MAPI_CREATE ulFlags パラメーターに設定_ されません。</span><span class="sxs-lookup"><span data-stu-id="81d76-141">The requested property does not exist and MAPI_CREATE was not set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="81d76-142">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="81d76-142">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="81d76-143">タグ内のプロパティの種類は、プロパティの種類にPT_UNSPECIFIED。</span><span class="sxs-lookup"><span data-stu-id="81d76-143">The property type in the tag is set to PT_UNSPECIFIED.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="81d76-144">注釈</span><span class="sxs-lookup"><span data-stu-id="81d76-144">Remarks</span></span>

<span data-ttu-id="81d76-145">**IMAPIProp::OpenProperty** メソッドは、特定のインターフェイスを介してプロパティにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="81d76-145">The **IMAPIProp::OpenProperty** method provides access to a property through a particular interface.</span></span> <span data-ttu-id="81d76-146">**OpenProperty は**[、IMAPIProp::GetProps](imapiprop-getprops.md)メソッドと [IMAPIProp::SetProps](imapiprop-setprops.md)メソッドの代替手段です。</span><span class="sxs-lookup"><span data-stu-id="81d76-146">**OpenProperty** is an alternative to the [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::SetProps](imapiprop-setprops.md) methods.</span></span> <span data-ttu-id="81d76-147">プロパティが **大きすぎる** か複雑すぎるため **、GetProps または SetProps** が失敗した場合は **、OpenProperty を呼び出します**。</span><span class="sxs-lookup"><span data-stu-id="81d76-147">When either **GetProps** or **SetProps** fails because the property is too large or too complex, call **OpenProperty**.</span></span> <span data-ttu-id="81d76-148">**OpenProperty は** 、通常、型のプロパティにアクセスするために使用PT_OBJECT。</span><span class="sxs-lookup"><span data-stu-id="81d76-148">**OpenProperty** is typically used to access properties of type PT_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="81d76-149">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="81d76-149">Notes to callers</span></span>

<span data-ttu-id="81d76-150">メッセージの添付ファイルにアクセスするには、添付 **PR_ATTACH_DATA_OBJ** の種類に応じて、異なるインターフェイス識別子を持つ PR_ATTACH_DATA_OBJ ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) プロパティを開きます。</span><span class="sxs-lookup"><span data-stu-id="81d76-150">To access message attachments, open the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property with a different interface identifier, depending on the type of attachment.</span></span> <span data-ttu-id="81d76-151">次の表では、さまざまな種類の添付ファイルに対して **OpenProperty** を呼び出す方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="81d76-151">The following table describes how to call **OpenProperty** for the different types of attachments:</span></span> 
  
|<span data-ttu-id="81d76-152">**添付ファイルの種類**</span><span class="sxs-lookup"><span data-stu-id="81d76-152">**Type of attachment**</span></span>|<span data-ttu-id="81d76-153">**使用するインターフェイス識別子**</span><span class="sxs-lookup"><span data-stu-id="81d76-153">**Interface identifier to use**</span></span>|
|:-----|:-----|
|<span data-ttu-id="81d76-154">バイナリ</span><span class="sxs-lookup"><span data-stu-id="81d76-154">Binary</span></span>  <br/> |<span data-ttu-id="81d76-155">IID_IStream</span><span class="sxs-lookup"><span data-stu-id="81d76-155">IID_IStream</span></span>  <br/> |
|<span data-ttu-id="81d76-156">String</span><span class="sxs-lookup"><span data-stu-id="81d76-156">String</span></span>  <br/> |<span data-ttu-id="81d76-157">IID_IStream</span><span class="sxs-lookup"><span data-stu-id="81d76-157">IID_IStream</span></span>  <br/> |
|<span data-ttu-id="81d76-158">メッセージ</span><span class="sxs-lookup"><span data-stu-id="81d76-158">Message</span></span>  <br/> |<span data-ttu-id="81d76-159">IID_IMessage</span><span class="sxs-lookup"><span data-stu-id="81d76-159">IID_IMessage</span></span>  <br/> |
|<span data-ttu-id="81d76-160">OLE 2.0</span><span class="sxs-lookup"><span data-stu-id="81d76-160">OLE 2.0</span></span>  <br/> |<span data-ttu-id="81d76-161">IID_IStreamDocfile</span><span class="sxs-lookup"><span data-stu-id="81d76-161">IID_IStreamDocfile</span></span>  <br/> |
   
<span data-ttu-id="81d76-162">**IStreamDocfile** は、OLE 2.0 複合ファイルに基づく [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) インターフェイスの派生物です。</span><span class="sxs-lookup"><span data-stu-id="81d76-162">**IStreamDocfile** is a derivative of the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface that is based on an OLE 2.0 compound file.</span></span> <span data-ttu-id="81d76-163">**IStreamDocfile は** 、オーバーヘッドが最も少ないので、OLE 2.0 添付ファイルにアクセスするための最適な選択肢です。</span><span class="sxs-lookup"><span data-stu-id="81d76-163">**IStreamDocfile** is the best choice for accessing OLE 2.0 attachments because it involves the least amount of overhead.</span></span> <span data-ttu-id="81d76-164">[IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx)インターフェイスIID_IStreamDocFile使用できる構造化ストレージに格納されているデータを含むプロパティには、このプロパティを使用できます。</span><span class="sxs-lookup"><span data-stu-id="81d76-164">You can use IID_IStreamDocFile for those properties that contain data stored in structured storage available through the [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) interface.</span></span> 
  
<span data-ttu-id="81d76-165">添付ファイルで **OpenProperty** を使用する方法の詳細については、「PR_ATTACH_DATA_OBJ」および「添付 **ファイルを開** く [」を参照してください](opening-an-attachment.md)。</span><span class="sxs-lookup"><span data-stu-id="81d76-165">For more information about how to use **OpenProperty** with attachments, see the **PR_ATTACH_DATA_OBJ** property and [Opening an Attachment](opening-an-attachment.md).</span></span>
  
<span data-ttu-id="81d76-166">0 の位置またはサイズ変数を使用しない限り、[](https://msdn.microsoft.com/library/aa380043%28v=VS.85%29.aspx)受け取った **IStream** ポインターを使用して Seek メソッドまたは [SetSize](https://msdn.microsoft.com/library/aa380044%28v=VS.85%29.aspx)メソッドを呼び出さません。</span><span class="sxs-lookup"><span data-stu-id="81d76-166">Do not use the **IStream** pointer that you receive to call either its [Seek](https://msdn.microsoft.com/library/aa380043%28v=VS.85%29.aspx) or [SetSize](https://msdn.microsoft.com/library/aa380044%28v=VS.85%29.aspx) method unless you use a zero position or size variable.</span></span> <span data-ttu-id="81d76-167">また **、Seek** 呼び出しから返される _plibNewPosition_ 出力パラメーターの値に依存しない。</span><span class="sxs-lookup"><span data-stu-id="81d76-167">Also, do not rely on the value of the  _plibNewPosition_ output parameter returned from the **Seek** call.</span></span> 
  
<span data-ttu-id="81d76-168">**OpenProperty を呼び出** して **IStream** インターフェイスを使用してプロパティにアクセスする場合は、そのインターフェイスのみを使用して変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="81d76-168">If you call **OpenProperty** to access a property with the **IStream** interface, use only that interface to make changes to it.</span></span> <span data-ttu-id="81d76-169">**SetProps** や [IMAPIProp::D eleteProps](imapiprop-deleteprops.md)など、他の [IMAPIProp : IUnknown](imapipropiunknown.md)メソッドを使用してプロパティを更新しようとはしない。</span><span class="sxs-lookup"><span data-stu-id="81d76-169">Do not attempt to update the property with any of the other [IMAPIProp : IUnknown](imapipropiunknown.md) methods, such as **SetProps** or [IMAPIProp::DeleteProps](imapiprop-deleteprops.md).</span></span> 
  
<span data-ttu-id="81d76-170">**OpenProperty** を使用してプロパティを 2 回以上開かれません。</span><span class="sxs-lookup"><span data-stu-id="81d76-170">Do not try to open a property with **OpenProperty** more than once.</span></span> <span data-ttu-id="81d76-171">結果はプロバイダーによって異なることがありますので、未定義です。</span><span class="sxs-lookup"><span data-stu-id="81d76-171">The results are undefined because they can vary from provider to provider.</span></span> 
  
<span data-ttu-id="81d76-172">開くプロパティを変更する必要がある場合は、プロパティフラグをMAPI_MODIFYします。</span><span class="sxs-lookup"><span data-stu-id="81d76-172">If you need to modify the property to be opened, set the MAPI_MODIFY flag.</span></span> <span data-ttu-id="81d76-173">オブジェクトがプロパティをサポートするかどうかが分からず、必要と思う場合は、プロパティフラグとMAPI_CREATE設定MAPI_MODIFYしてください。</span><span class="sxs-lookup"><span data-stu-id="81d76-173">If you are not sure whether the object supports the property but you think it should, set the MAPI_CREATE and MAPI_MODIFY flags.</span></span> <span data-ttu-id="81d76-174">設定されているMAPI_CREATE、MAPI_MODIFY設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="81d76-174">Whenever MAPI_CREATE is set, MAPI_MODIFY must also be set.</span></span>
  
<span data-ttu-id="81d76-175">_lppUnk_ パラメーターで返されるインターフェイス ポインターを、lpiid パラメーターで指定されたインターフェイスに適したインターフェイス ポインターに再キャストする _必要_ があります。</span><span class="sxs-lookup"><span data-stu-id="81d76-175">You are responsible for recasting the interface pointer returned in the  _lppUnk_ parameter to one that is appropriate for the interface specified in the  _lpiid_ parameter.</span></span> <span data-ttu-id="81d76-176">返されたポインターを使用して、終了したら [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="81d76-176">You must also use the returned pointer to call its [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method when you are finished with it.</span></span> 
  
<span data-ttu-id="81d76-177">_ulFlags_ パラメーターでフラグを設定すると、必要なプロパティへのアクセスの種類を示すのに十分ではない場合があります。</span><span class="sxs-lookup"><span data-stu-id="81d76-177">Sometimes setting the flags in the  _ulFlags_ parameter is not enough to indicate the type of access to the property that is required.</span></span> <span data-ttu-id="81d76-178">_ulInterfaceOptions_ パラメーターには、フラグなどの追加のデータを設定できます。</span><span class="sxs-lookup"><span data-stu-id="81d76-178">You can put additional data, such as flags, in the  _ulInterfaceOptions_ parameter.</span></span> <span data-ttu-id="81d76-179">このデータはインターフェイスに依存します。</span><span class="sxs-lookup"><span data-stu-id="81d76-179">This data is interface dependent.</span></span> <span data-ttu-id="81d76-180">一部のインターフェイス **(IStream** など) が使用し、使用しないインターフェイスもあります。</span><span class="sxs-lookup"><span data-stu-id="81d76-180">Some interfaces (such as **IStream**) use it, and others do not.</span></span> <span data-ttu-id="81d76-181">たとえば **、IStream** を使用して変更するプロパティを開く場合は、STGM_WRITE フラグに加えて  _ulInterfaceOptions_ パラメーター MAPI_MODIFY。</span><span class="sxs-lookup"><span data-stu-id="81d76-181">For example, when you open a property to be modified with **IStream**, set the STGM_WRITE flag in the  _ulInterfaceOptions_ parameter in addition to MAPI_MODIFY.</span></span> <span data-ttu-id="81d76-182">[IMAPITable](imapitableiunknown.md)インターフェイスを使用してテーブルを開く場合は _、ulInterfaceOptions_ を MAPI_UNICODE に設定して、文字列プロパティを保持するテーブル内の列を Unicode 形式にするかどうかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="81d76-182">When you open a table by using the [IMAPITable](imapitableiunknown.md) interface, you can set  _ulInterfaceOptions_ to MAPI_UNICODE to indicate whether the columns in the table that hold string properties should be in Unicode format.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="81d76-183">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="81d76-183">MFCMAPI reference</span></span>

<span data-ttu-id="81d76-184">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="81d76-184">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="81d76-185">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="81d76-185">**File**</span></span>|<span data-ttu-id="81d76-186">**関数**</span><span class="sxs-lookup"><span data-stu-id="81d76-186">**Function**</span></span>|<span data-ttu-id="81d76-187">**コメント**</span><span class="sxs-lookup"><span data-stu-id="81d76-187">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="81d76-188">StreamEditor.cpp</span><span class="sxs-lookup"><span data-stu-id="81d76-188">StreamEditor.cpp</span></span>  <br/> |<span data-ttu-id="81d76-189">CStreamEditor::ReadTextStreamFromProperty</span><span class="sxs-lookup"><span data-stu-id="81d76-189">CStreamEditor::ReadTextStreamFromProperty</span></span>  <br/> |<span data-ttu-id="81d76-190">MFCMAPI は **IMAPIProp::OpenProperty** メソッドを使用して、大きなテキストおよびバイナリ プロパティのストリーム インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="81d76-190">MFCMAPI uses the **IMAPIProp::OpenProperty** method to retrieve a stream interface for large text and binary properties.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="81d76-191">関連項目</span><span class="sxs-lookup"><span data-stu-id="81d76-191">See also</span></span>

- [<span data-ttu-id="81d76-192">HrIStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="81d76-192">HrIStorageFromStream</span></span>](hristoragefromstream.md) 
- [<span data-ttu-id="81d76-193">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="81d76-193">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md) 
- [<span data-ttu-id="81d76-194">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="81d76-194">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
- [<span data-ttu-id="81d76-195">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="81d76-195">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
- [<span data-ttu-id="81d76-196">IMAPISupport::IStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="81d76-196">IMAPISupport::IStorageFromStream</span></span>](imapisupport-istoragefromstream.md)
- [<span data-ttu-id="81d76-197">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="81d76-197">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
- [<span data-ttu-id="81d76-198">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="81d76-198">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
- <span data-ttu-id="81d76-199">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="81d76-199">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
- [<span data-ttu-id="81d76-200">添付ファイルを開く</span><span class="sxs-lookup"><span data-stu-id="81d76-200">Opening an Attachment</span></span>](opening-an-attachment.md)

