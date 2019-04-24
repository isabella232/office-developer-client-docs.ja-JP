---
title: imapipropopenproperty
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
ms.openlocfilehash: 7bf1d6912e44319c36e288cd3870218e8c4e45ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319811"
---
# <a name="imapipropopenproperty"></a><span data-ttu-id="dc5f8-103">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="dc5f8-103">IMAPIProp::OpenProperty</span></span>

<span data-ttu-id="dc5f8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc5f8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc5f8-105">プロパティへのアクセスに使用できるインターフェイスへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-105">Returns a pointer to an interface that can be used to access a property.</span></span>
  
```cpp
HRESULT OpenProperty(
  ULONG ulPropTag,
  LPCIID lpiid,
  ULONG ulInterfaceOptions,
  ULONG ulFlags,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="dc5f8-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="dc5f8-106">Parameters</span></span>

 <span data-ttu-id="dc5f8-107">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="dc5f8-107">_ulPropTag_</span></span>
  
> <span data-ttu-id="dc5f8-108">順番アクセスされるプロパティのプロパティタグ。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-108">[in] The property tag for the property to be accessed.</span></span> <span data-ttu-id="dc5f8-109">識別子と型の両方が property タグに含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-109">Both the identifier and the type must be included in the property tag.</span></span>
    
 <span data-ttu-id="dc5f8-110">_lpiid_</span><span class="sxs-lookup"><span data-stu-id="dc5f8-110">_lpiid_</span></span>
  
> <span data-ttu-id="dc5f8-111">順番プロパティへのアクセスに使用するインターフェイスの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-111">[in] A pointer to the identifier for the interface to be used to access the property.</span></span> <span data-ttu-id="dc5f8-112">_lpiid_パラメーターを**null**にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-112">The  _lpiid_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="dc5f8-113">_ulinterfaceoptions_</span><span class="sxs-lookup"><span data-stu-id="dc5f8-113">_ulInterfaceOptions_</span></span>
  
> <span data-ttu-id="dc5f8-114">順番_lpiid_パラメーターによって識別されるインターフェイスに関連するデータ。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-114">[in] Data that relates to the interface identified by the  _lpiid_ parameter.</span></span> 
    
 <span data-ttu-id="dc5f8-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dc5f8-115">_ulFlags_</span></span>
  
> <span data-ttu-id="dc5f8-116">順番プロパティへのアクセスを制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-116">[in] A bitmask of flags that controls access to the property.</span></span> <span data-ttu-id="dc5f8-117">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-117">The following flags can be set:</span></span>
    
<span data-ttu-id="dc5f8-118">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="dc5f8-118">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="dc5f8-119">プロパティが存在しない場合は、作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-119">If the property does not exist, it should be created.</span></span> <span data-ttu-id="dc5f8-120">プロパティが存在する場合は、プロパティの現在の値を破棄する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-120">If the property does exist, the current value of the property should be discarded.</span></span> <span data-ttu-id="dc5f8-121">発信者が MAPI_CREATE フラグを設定する場合は、MAPI_MODIFY フラグも設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-121">When a caller sets the MAPI_CREATE flag, it should also set the MAPI_MODIFY flag.</span></span>
    
<span data-ttu-id="dc5f8-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="dc5f8-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="dc5f8-123">オブジェクトが完全に呼び出し元で使用可能になる前に、 **openproperty**を正常に返すことができるようにします。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-123">Allows **OpenProperty** to return successfully, possibly before the object is fully available to the caller.</span></span> <span data-ttu-id="dc5f8-124">オブジェクトが使用できない場合は、その後のオブジェクト呼び出しでエラーが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-124">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="dc5f8-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="dc5f8-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="dc5f8-126">MAPI_MODIFY は、次のような状況で必要になります。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-126">MAPI_MODIFY is required in these situations:</span></span>
    
  - <span data-ttu-id="dc5f8-127">stream プロパティ ( **IID_IStream**など) を開いて変更する場合。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-127">When opening a stream property, such as **IID_IStream**, to modify it.</span></span>
    
  - <span data-ttu-id="dc5f8-128">埋め込みメッセージ添付ファイル ( **IID_IMessage**で開かれた[PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md)など) を開いて変更する場合。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-128">When opening an embedded message attachment, such as [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) opened with **IID_IMessage**, to modify it.</span></span>
    
 <span data-ttu-id="dc5f8-129">_lppunk_</span><span class="sxs-lookup"><span data-stu-id="dc5f8-129">_lppUnk_</span></span>
  
> <span data-ttu-id="dc5f8-130">読み上げプロパティへのアクセスに使用する要求されたインターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-130">[out] A pointer to the requested interface to be used for property access.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dc5f8-131">戻り値</span><span class="sxs-lookup"><span data-stu-id="dc5f8-131">Return value</span></span>

<span data-ttu-id="dc5f8-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="dc5f8-132">S_OK</span></span> 
  
> <span data-ttu-id="dc5f8-133">要求されたインターフェイスポインターが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-133">The requested interface pointer was successfully returned.</span></span>
    
<span data-ttu-id="dc5f8-134">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="dc5f8-134">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="dc5f8-135">要求されたインターフェイスは、このプロパティではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-135">The requested interface is not supported for this property.</span></span>
    
<span data-ttu-id="dc5f8-136">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="dc5f8-136">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="dc5f8-137">呼び出し元に、プロパティにアクセスするための十分な権限がありません。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-137">The caller has insufficient permissions to access the property.</span></span>
    
<span data-ttu-id="dc5f8-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="dc5f8-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="dc5f8-139">オブジェクトは、要求されたインターフェイス経由でこのプロパティへのアクセスを提供できません。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-139">The object cannot provide access to this property through the requested interface.</span></span>
    
<span data-ttu-id="dc5f8-140">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="dc5f8-140">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="dc5f8-141">要求されたプロパティが存在せず、 _ulflags_パラメーターに MAPI_CREATE が設定されていません。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-141">The requested property does not exist and MAPI_CREATE was not set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="dc5f8-142">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="dc5f8-142">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="dc5f8-143">タグ内のプロパティの型は、PT_UNSPECIFIED に設定されています。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-143">The property type in the tag is set to PT_UNSPECIFIED.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dc5f8-144">解説</span><span class="sxs-lookup"><span data-stu-id="dc5f8-144">Remarks</span></span>

<span data-ttu-id="dc5f8-145">**imapiprop:: openproperty**メソッドは、特定のインターフェイスを介してプロパティへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-145">The **IMAPIProp::OpenProperty** method provides access to a property through a particular interface.</span></span> <span data-ttu-id="dc5f8-146">**openproperty**は、 [imapiprop:: GetProps](imapiprop-getprops.md)および[imapiprop:: setprops](imapiprop-setprops.md)メソッドの代わりになります。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-146">**OpenProperty** is an alternative to the [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::SetProps](imapiprop-setprops.md) methods.</span></span> <span data-ttu-id="dc5f8-147">プロパティが大きすぎるか、または複雑すぎるため、 **GetProps**または**setprops**が失敗する場合は、 **openproperty**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-147">When either **GetProps** or **SetProps** fails because the property is too large or too complex, call **OpenProperty**.</span></span> <span data-ttu-id="dc5f8-148">**openproperty**は、通常、PT_OBJECT 型のプロパティにアクセスするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-148">**OpenProperty** is typically used to access properties of type PT_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="dc5f8-149">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="dc5f8-149">Notes to callers</span></span>

<span data-ttu-id="dc5f8-150">メッセージの添付ファイルにアクセスするには、添付ファイルの種類に応じて、別のインターフェイス識別子を使用して**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) プロパティを開きます。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-150">To access message attachments, open the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property with a different interface identifier, depending on the type of attachment.</span></span> <span data-ttu-id="dc5f8-151">次の表では、さまざまな種類の添付ファイルの**openproperty**を呼び出す方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-151">The following table describes how to call **OpenProperty** for the different types of attachments:</span></span> 
  
|<span data-ttu-id="dc5f8-152">**添付ファイルの種類**</span><span class="sxs-lookup"><span data-stu-id="dc5f8-152">**Type of attachment**</span></span>|<span data-ttu-id="dc5f8-153">**使用するインターフェイス識別子**</span><span class="sxs-lookup"><span data-stu-id="dc5f8-153">**Interface identifier to use**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dc5f8-154">Binary</span><span class="sxs-lookup"><span data-stu-id="dc5f8-154">Binary</span></span>  <br/> |<span data-ttu-id="dc5f8-155">IID_IStream</span><span class="sxs-lookup"><span data-stu-id="dc5f8-155">IID_IStream</span></span>  <br/> |
|<span data-ttu-id="dc5f8-156">String</span><span class="sxs-lookup"><span data-stu-id="dc5f8-156">String</span></span>  <br/> |<span data-ttu-id="dc5f8-157">IID_IStream</span><span class="sxs-lookup"><span data-stu-id="dc5f8-157">IID_IStream</span></span>  <br/> |
|<span data-ttu-id="dc5f8-158">メッセージ</span><span class="sxs-lookup"><span data-stu-id="dc5f8-158">Message</span></span>  <br/> |<span data-ttu-id="dc5f8-159">IID_IMessage</span><span class="sxs-lookup"><span data-stu-id="dc5f8-159">IID_IMessage</span></span>  <br/> |
|<span data-ttu-id="dc5f8-160">OLE 2.0</span><span class="sxs-lookup"><span data-stu-id="dc5f8-160">OLE 2.0</span></span>  <br/> |<span data-ttu-id="dc5f8-161">IID_IStreamDocfile</span><span class="sxs-lookup"><span data-stu-id="dc5f8-161">IID_IStreamDocfile</span></span>  <br/> |
   
<span data-ttu-id="dc5f8-162">**IStreamDocfile**は、OLE 2.0 複合ファイルに基づく[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)インターフェイスから派生したものです。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-162">**IStreamDocfile** is a derivative of the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface that is based on an OLE 2.0 compound file.</span></span> <span data-ttu-id="dc5f8-163">**IStreamDocfile**は、最小限のオーバーヘッドを必要とするため、OLE 2.0 の添付ファイルにアクセスするのに最適です。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-163">**IStreamDocfile** is the best choice for accessing OLE 2.0 attachments because it involves the least amount of overhead.</span></span> <span data-ttu-id="dc5f8-164">IID_IStreamDocFile は、 [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx)インターフェイスを介して使用できる構造化ストレージに格納されているデータを含むプロパティに使用できます。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-164">You can use IID_IStreamDocFile for those properties that contain data stored in structured storage available through the [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) interface.</span></span> 
  
<span data-ttu-id="dc5f8-165">添付ファイル付きの**openproperty**の使用方法の詳細については、 **PR_ATTACH_DATA_OBJ**プロパティを参照し、[添付ファイルを開い](opening-an-attachment.md)てください。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-165">For more information about how to use **OpenProperty** with attachments, see the **PR_ATTACH_DATA_OBJ** property and [Opening an Attachment](opening-an-attachment.md).</span></span>
  
<span data-ttu-id="dc5f8-166">0の位置またはサイズ変数を使用しない場合は、受け取った**IStream**ポインターを使用して、 [Seek](https://msdn.microsoft.com/library/aa380043%28v=VS.85%29.aspx)メソッドまたは[SetSize](https://msdn.microsoft.com/library/aa380044%28v=VS.85%29.aspx)メソッドを呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-166">Do not use the **IStream** pointer that you receive to call either its [Seek](https://msdn.microsoft.com/library/aa380043%28v=VS.85%29.aspx) or [SetSize](https://msdn.microsoft.com/library/aa380044%28v=VS.85%29.aspx) method unless you use a zero position or size variable.</span></span> <span data-ttu-id="dc5f8-167">また、 **Seek**呼び出しから返される_plibnewposition_出力パラメーターの値に依存しないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-167">Also, do not rely on the value of the  _plibNewPosition_ output parameter returned from the **Seek** call.</span></span> 
  
<span data-ttu-id="dc5f8-168">**IStream**インターフェイスを使用してプロパティにアクセスするために**openproperty**を呼び出す場合は、そのインターフェイスのみを使用して変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-168">If you call **OpenProperty** to access a property with the **IStream** interface, use only that interface to make changes to it.</span></span> <span data-ttu-id="dc5f8-169">**setprops**や[imapiprop::D eleteprops](imapiprop-deleteprops.md)など、他の[imapiprop: IUnknown](imapipropiunknown.md)メソッドのいずれかを使用してプロパティを更新しないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-169">Do not attempt to update the property with any of the other [IMAPIProp : IUnknown](imapipropiunknown.md) methods, such as **SetProps** or [IMAPIProp::DeleteProps](imapiprop-deleteprops.md).</span></span> 
  
<span data-ttu-id="dc5f8-170">**openproperty**を持つプロパティを複数回開いてはいけません。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-170">Do not try to open a property with **OpenProperty** more than once.</span></span> <span data-ttu-id="dc5f8-171">結果は、プロバイダーによって異なる可能性があるため、未定義となります。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-171">The results are undefined because they can vary from provider to provider.</span></span> 
  
<span data-ttu-id="dc5f8-172">開くプロパティを変更する必要がある場合は、MAPI_MODIFY フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-172">If you need to modify the property to be opened, set the MAPI_MODIFY flag.</span></span> <span data-ttu-id="dc5f8-173">オブジェクトでプロパティがサポートされているかどうかがわからない場合は、MAPI_CREATE フラグと MAPI_MODIFY フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-173">If you are not sure whether the object supports the property but you think it should, set the MAPI_CREATE and MAPI_MODIFY flags.</span></span> <span data-ttu-id="dc5f8-174">MAPI_CREATE が設定されている場合は常に、MAPI_MODIFY も設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-174">Whenever MAPI_CREATE is set, MAPI_MODIFY must also be set.</span></span>
  
<span data-ttu-id="dc5f8-175">_lppunk_パラメーターで返されるインターフェイスポインターが、 _lpiid_パラメーターで指定されているインターフェイスに適したものになるように、recasting を担当しています。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-175">You are responsible for recasting the interface pointer returned in the  _lppUnk_ parameter to one that is appropriate for the interface specified in the  _lpiid_ parameter.</span></span> <span data-ttu-id="dc5f8-176">また、返されたポインターを使用して、終了時に[IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-176">You must also use the returned pointer to call its [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method when you are finished with it.</span></span> 
  
<span data-ttu-id="dc5f8-177">_ulflags_パラメーターのフラグを設定しても、必要なプロパティへのアクセスの種類を示すには不十分な場合があります。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-177">Sometimes setting the flags in the  _ulFlags_ parameter is not enough to indicate the type of access to the property that is required.</span></span> <span data-ttu-id="dc5f8-178">_ulinterfaceoptions_パラメーターには、フラグなどの追加データを入れることができます。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-178">You can put additional data, such as flags, in the  _ulInterfaceOptions_ parameter.</span></span> <span data-ttu-id="dc5f8-179">このデータはインターフェイスに依存します。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-179">This data is interface dependent.</span></span> <span data-ttu-id="dc5f8-180">**IStream**などの一部のインターフェイスは、それを使用します。そうでないものもあります。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-180">Some interfaces (such as **IStream**) use it, and others do not.</span></span> <span data-ttu-id="dc5f8-181">たとえば、 **IStream**を使用して変更するプロパティを開いた場合は、MAPI_MODIFY に加えて、 _ulinterfaceoptions_パラメーターの STGM_WRITE フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-181">For example, when you open a property to be modified with **IStream**, set the STGM_WRITE flag in the  _ulInterfaceOptions_ parameter in addition to MAPI_MODIFY.</span></span> <span data-ttu-id="dc5f8-182">[IMAPITable](imapitableiunknown.md)インターフェイスを使用してテーブルを開いた場合、MAPI_UNICODE に_ulinterfaceoptions_を設定して、テーブル内の文字列プロパティを保持する列が UNICODE 形式であるかどうかを示すことができます。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-182">When you open a table by using the [IMAPITable](imapitableiunknown.md) interface, you can set  _ulInterfaceOptions_ to MAPI_UNICODE to indicate whether the columns in the table that hold string properties should be in Unicode format.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="dc5f8-183">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="dc5f8-183">MFCMAPI reference</span></span>

<span data-ttu-id="dc5f8-184">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-184">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="dc5f8-185">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="dc5f8-185">**File**</span></span>|<span data-ttu-id="dc5f8-186">**関数**</span><span class="sxs-lookup"><span data-stu-id="dc5f8-186">**Function**</span></span>|<span data-ttu-id="dc5f8-187">**コメント**</span><span class="sxs-lookup"><span data-stu-id="dc5f8-187">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dc5f8-188">streameditor .cpp</span><span class="sxs-lookup"><span data-stu-id="dc5f8-188">StreamEditor.cpp</span></span>  <br/> |<span data-ttu-id="dc5f8-189">cstreameditor:: readtextstreamfromproperty</span><span class="sxs-lookup"><span data-stu-id="dc5f8-189">CStreamEditor::ReadTextStreamFromProperty</span></span>  <br/> |<span data-ttu-id="dc5f8-190">mfcmapi は、 **imapiprop:: openproperty**メソッドを使用して、大きなテキストおよびバイナリプロパティのストリームインターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="dc5f8-190">MFCMAPI uses the **IMAPIProp::OpenProperty** method to retrieve a stream interface for large text and binary properties.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dc5f8-191">関連項目</span><span class="sxs-lookup"><span data-stu-id="dc5f8-191">See also</span></span>

- [<span data-ttu-id="dc5f8-192">HrIStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="dc5f8-192">HrIStorageFromStream</span></span>](hristoragefromstream.md) 
- [<span data-ttu-id="dc5f8-193">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="dc5f8-193">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md) 
- [<span data-ttu-id="dc5f8-194">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="dc5f8-194">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
- [<span data-ttu-id="dc5f8-195">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="dc5f8-195">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
- [<span data-ttu-id="dc5f8-196">IMAPISupport::IStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="dc5f8-196">IMAPISupport::IStorageFromStream</span></span>](imapisupport-istoragefromstream.md)
- [<span data-ttu-id="dc5f8-197">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dc5f8-197">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
- [<span data-ttu-id="dc5f8-198">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dc5f8-198">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
- <span data-ttu-id="dc5f8-199">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="dc5f8-199">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
- [<span data-ttu-id="dc5f8-200">添付ファイルを開く</span><span class="sxs-lookup"><span data-stu-id="dc5f8-200">Opening an Attachment</span></span>](opening-an-attachment.md)

