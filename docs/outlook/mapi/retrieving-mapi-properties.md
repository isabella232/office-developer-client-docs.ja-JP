---
title: MAPI プロパティの取得
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bd3f9f59-9020-46e6-9560-86a7a0eeca20
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: 9666c551543cefd12ee8c902db1a2372aab20632
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328645"
---
# <a name="retrieving-mapi-properties"></a><span data-ttu-id="f12aa-103">MAPI プロパティの取得</span><span class="sxs-lookup"><span data-stu-id="f12aa-103">Retrieving MAPI Properties</span></span>

 
  
<span data-ttu-id="f12aa-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f12aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f12aa-105">クライアントまたはサービスプロバイダーがオブジェクトからプロパティを取得すると、そのオブジェクトはプロパティの値、型、および識別子を使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="f12aa-105">When a client or service provider retrieves a property from an object, the object makes available the property's value, type, and identifier.</span></span> 
  
<span data-ttu-id="f12aa-106">クライアントおよびサービスプロバイダーは、次のいずれかを呼び出すことによって、オブジェクトのプロパティを取得できます。</span><span class="sxs-lookup"><span data-stu-id="f12aa-106">Clients and service providers can retrieve an object's properties by calling one of the following:</span></span>
  
[<span data-ttu-id="f12aa-107">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="f12aa-107">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="f12aa-108">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="f12aa-108">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="f12aa-109">HrGetOneProp</span><span class="sxs-lookup"><span data-stu-id="f12aa-109">HrGetOneProp</span></span>](hrgetoneprop.md)
  
<span data-ttu-id="f12aa-110">**GetProps**メソッドは、access の特殊なインターフェイスまたは代替インターフェイスを必要としない1つ以上のプロパティを取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f12aa-110">The **GetProps** method is used to retrieve one or more properties that do not need a specialized or alternate interface for access.</span></span> <span data-ttu-id="f12aa-111">これは、 **GetProps**で使用できるプロパティが、整数やブール値などの小さいことを意味します。</span><span class="sxs-lookup"><span data-stu-id="f12aa-111">This implies that the properties available with **GetProps** are small, such as integers and Boolean values.</span></span> 
  
 <span data-ttu-id="f12aa-112">**複数のプロパティを取得するには**</span><span class="sxs-lookup"><span data-stu-id="f12aa-112">**To retrieve multiple properties**</span></span>
  
1. <span data-ttu-id="f12aa-113">取得するプロパティの数を保持するのに十分な大きさの[SPropTagArray](sproptagarray.md)構造体を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f12aa-113">Allocate an [SPropTagArray](sproptagarray.md) structure large enough to hold the number of properties to be retrieved.</span></span> 
    
2. <span data-ttu-id="f12aa-114">**SPropTagArray**構造体の**cvalues**メンバーを取得するプロパティの数に設定し、各**aulPropTag**メンバーを、可能であれば、いずれかのターゲットプロパティの識別子と種類に設定します。</span><span class="sxs-lookup"><span data-stu-id="f12aa-114">Set the **cValues** member of the **SPropTagArray** structure to the number of properties to be retrieved and set each **aulPropTag** member to the identifier and type, if possible, of one of the target properties.</span></span> <span data-ttu-id="f12aa-115">種類が不明な場合は、PT_UNSPECIFIED に設定します。</span><span class="sxs-lookup"><span data-stu-id="f12aa-115">If the type is unknown, set it to PT_UNSPECIFIED.</span></span> <span data-ttu-id="f12aa-116">型と識別子の両方が不明な場合は、 [imapiprop:: getproplist](imapiprop-getproplist.md)を呼び出すことによって、この情報を特定します。</span><span class="sxs-lookup"><span data-stu-id="f12aa-116">If both the type and the identifier are unknown, locate this information by calling [IMAPIProp::GetPropList](imapiprop-getproplist.md).</span></span> <span data-ttu-id="f12aa-117">**getproplist**は、オブジェクトでサポートされているすべてのプロパティを持つプロパティタグ配列を返します。</span><span class="sxs-lookup"><span data-stu-id="f12aa-117">**GetPropList** returns a property tag array with all of the object's supported properties.</span></span> <span data-ttu-id="f12aa-118">プロパティ名のみを使用できる場合は、関連付けられている識別子にアクセスするには、 [imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f12aa-118">If only a property name is available, call [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to access the associated identifier.</span></span> 
    
3. <span data-ttu-id="f12aa-119">プロパティまたはプロパティを開くには、 [imapiprop:: GetProps](imapiprop-getprops.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f12aa-119">Call [IMAPIProp::GetProps](imapiprop-getprops.md) to open the property or properties.</span></span> 
    
<span data-ttu-id="f12aa-120">**openproperty**メソッドを使用すると、access の**IStream**や[IMAPITable](imapitableiunknown.md)などの代替インターフェイスを必要とする、より大きなプロパティを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="f12aa-120">The **OpenProperty** method is used to open larger properties that require an alternate interface such as **IStream** or [IMAPITable](imapitableiunknown.md) for access.</span></span> <span data-ttu-id="f12aa-121">**openproperty**は、通常、ラージ文字列、バイナリ、およびオブジェクトのプロパティを開くために使用され、一度に1つのプロパティしか開くことができません。</span><span class="sxs-lookup"><span data-stu-id="f12aa-121">**OpenProperty** is typically used to open large character string, binary, and object properties and can only open one property at a time.</span></span> <span data-ttu-id="f12aa-122">発信者は、入力パラメーターの1つとして必要な追加インターフェイスの識別子を渡します。</span><span class="sxs-lookup"><span data-stu-id="f12aa-122">Callers pass in the identifier of the additional interface that is required as one of the input parameters.</span></span> 
  
<span data-ttu-id="f12aa-123">**openproperty**の一般的な使用方法には、 **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) を開くプロパティ (テキストベースのメッセージの本文を保持するプロパティ) **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) があります。OLE オブジェクトまたはメッセージの添付ファイル、および**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))。フォルダーまたはアドレス帳のコンテナーの内容の表を保持するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="f12aa-123">Some of the common uses of **OpenProperty** include opening **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), the property that holds the body of a text-based message, **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)), the property that holds an OLE object or message attachment, and **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), the property that holds a folder or address book container contents table.</span></span> 
  
<span data-ttu-id="f12aa-124">プロパティによっては、 **openproperty**から別のインターフェイスが要求されます。</span><span class="sxs-lookup"><span data-stu-id="f12aa-124">Depending on the property, a different interface is requested from **OpenProperty**.</span></span> <span data-ttu-id="f12aa-125">**IStream**は、プロパティデータをバイトストリームとして読み書きできるようにするインターフェイスです。通常、 **PR_BODY**へのアクセスに使用されます。</span><span class="sxs-lookup"><span data-stu-id="f12aa-125">**IStream**, an interface that allows property data to be read and written as a stream of bytes, is typically used to access **PR_BODY**.</span></span> <span data-ttu-id="f12aa-126">[IMessage](imessageimapiprop.md)または**IStream**のどちらかを使用して**PR_ATTACH_DATA_OBJ**にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="f12aa-126">Either [IMessage](imessageimapiprop.md) or **IStream** can be used to access **PR_ATTACH_DATA_OBJ**.</span></span> <span data-ttu-id="f12aa-127">標準メッセージである埋め込みメッセージ添付ファイルは**IMessage**を使用しますが、TNEF 形式のメッセージでは**IStream**が使用されます。</span><span class="sxs-lookup"><span data-stu-id="f12aa-127">Embedded message attachments that are standard messages use **IMessage** whereas messages in the TNEF format use **IStream**.</span></span> <span data-ttu-id="f12aa-128">**PR_CONTAINER_CONTENTS**は table オブジェクトなので、 [IMAPITable](imapitableiunknown.md)でアクセスします。</span><span class="sxs-lookup"><span data-stu-id="f12aa-128">Because **PR_CONTAINER_CONTENTS** is a table object, it is accessed with [IMAPITable](imapitableiunknown.md).</span></span>
  
 <span data-ttu-id="f12aa-129">**添付ファイルの PR_ATTACH_DATA_BIN プロパティを取得するには**</span><span class="sxs-lookup"><span data-stu-id="f12aa-129">**To retrieve an attachment's PR_ATTACH_DATA_BIN property**</span></span>
  
1. <span data-ttu-id="f12aa-130">[openstreamonfile](openstreamonfile.md)関数を呼び出して、ファイルのストリームを開きます。</span><span class="sxs-lookup"><span data-stu-id="f12aa-130">Call the [OpenStreamOnFile](openstreamonfile.md) function to open a stream for the file.</span></span> 
    
2. <span data-ttu-id="f12aa-131">メッセージの[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出して、 **IStream**インターフェイスを使用して**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="f12aa-131">Call the message's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to retrieve the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property with the **IStream** interface.</span></span> <span data-ttu-id="f12aa-132">MAPI_MODIFY と MAPI_CREATE の両方のフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="f12aa-132">Set both the MAPI_MODIFY and MAPI_CREATE flags.</span></span> 
    
3. <span data-ttu-id="f12aa-133">**STATSTG**構造体を割り当て、ファイルストリームの**IStream:: Stat**メソッドへの呼び出しに渡して、サイズを決定します。</span><span class="sxs-lookup"><span data-stu-id="f12aa-133">Allocate a **STATSTG** structure and pass it in a call to the file stream's **IStream::Stat** method to determine its size.</span></span> <span data-ttu-id="f12aa-134">ストリームのサイズを確認する別の方法として、 **IStream:: Seek**を STREAM_SEEK_END というフラグが付いています。</span><span class="sxs-lookup"><span data-stu-id="f12aa-134">Another way to determine stream size is to call **IStream::Seek** with the flag STREAM_SEEK_END.</span></span> 
    
4. <span data-ttu-id="f12aa-135">ストリームの**IStream:: CopyTo**メソッドを呼び出して、ファイルのストリームから添付ファイルストリームにデータをコピーします。</span><span class="sxs-lookup"><span data-stu-id="f12aa-135">Call the stream's **IStream::CopyTo** method to copy the data from the file's stream into the attachment stream.</span></span> 
    
5. <span data-ttu-id="f12aa-136">コピー操作が終了したら、 **IUnknown:: release**メソッドを呼び出して両方のストリームを解放します。</span><span class="sxs-lookup"><span data-stu-id="f12aa-136">When the copy operation is finished, release both streams by calling their **IUnknown::Release** methods.</span></span> 
    
<span data-ttu-id="f12aa-137">**IStream**がプロパティアクセスに使用されている場合、一部のサービスプロバイダーは、プロパティのサイズを stream に自動的に送り返します。</span><span class="sxs-lookup"><span data-stu-id="f12aa-137">When **IStream** is used for property access, some service providers automatically send the size of the property back with the stream.</span></span> <span data-ttu-id="f12aa-138">MAPI_DEFERRED_ERRORS フラグを使用して**openproperty**を呼び出すと、プロパティのオープンとストリームサイズの戻りが遅延する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f12aa-138">Calling **OpenProperty** with the MAPI_DEFERRED_ERRORS flag can delay the opening of the property and the return of the stream size.</span></span> <span data-ttu-id="f12aa-139">MAPI_DEFERRED_ERRORS フラグが設定された**openproperty** after でこの size を取得するために**IStream:: Stat**が呼び出された場合、この一連の呼び出しによってリモートプロシージャコールが強制的に実行されるため、パフォーマンスが影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="f12aa-139">If **IStream::Stat** is called to retrieve this size after **OpenProperty** with the MAPI_DEFERRED_ERRORS flag set, performance will be impacted because this sequence of calls forces an extra remote procedure call.</span></span> <span data-ttu-id="f12aa-140">パフォーマンスヒットを回避するために、クライアントは**openproperty**への呼び出しと**Stat**の間で任意の MAPI メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="f12aa-140">To avoid the performance hit, clients can call any MAPI method between the calls to **OpenProperty** and to **Stat**.</span></span>
  
<span data-ttu-id="f12aa-141">[hrgetoneprop](hrgetoneprop.md)関数 ( **openproperty**など) は、一度に1つのプロパティを開きます。</span><span class="sxs-lookup"><span data-stu-id="f12aa-141">The [HrGetOneProp](hrgetoneprop.md) function, like **OpenProperty**, opens one property at a time.</span></span> <span data-ttu-id="f12aa-142">**hrgetoneprop**は、ターゲットオブジェクトがローカルコンピューター上に存在する場合にのみ使用してください。</span><span class="sxs-lookup"><span data-stu-id="f12aa-142">**HrGetOneProp** should only be used when the target object exists on the local machine.</span></span> <span data-ttu-id="f12aa-143">ターゲットオブジェクトがローカルで使用できない場合、 **hrgetoneprop**を繰り返し使用すると、複数のリモートプロシージャコールが発生し、パフォーマンスが低下することがあります。</span><span class="sxs-lookup"><span data-stu-id="f12aa-143">When the target object is not locally available, using **HrGetOneProp** repeatedly can result in multiple remote procedure calls and a performance degradation.</span></span> 
  
<span data-ttu-id="f12aa-144">複数のプロパティを必要とする発信者は、ループで**hrgetoneprop**または**openproperty**を呼び出すか、 **GetProps**に対して1回の呼び出しを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="f12aa-144">Callers that need several properties can either call **HrGetOneProp** or **OpenProperty** in a loop or make one call to **GetProps**.</span></span> <span data-ttu-id="f12aa-145">**GetProps**の呼び出しは、より効率的です。</span><span class="sxs-lookup"><span data-stu-id="f12aa-145">Calling **GetProps** once is more efficient.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f12aa-146">セキュリティで保護されたプロパティは、 **GetProps**、 **hrgetoneprop**、または**getproplist**呼び出しの他のプロパティでは、自動的には使用できません。</span><span class="sxs-lookup"><span data-stu-id="f12aa-146">Secure properties are not automatically available with other properties in a **GetProps**, **HrGetOneProp**, or **GetPropList** call.</span></span> <span data-ttu-id="f12aa-147">セキュリティで保護されたプロパティは、プロパティ識別子を使用して明示的に要求する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f12aa-147">Secure properties must be explicitly requested using their property identifiers.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f12aa-148">関連項目</span><span class="sxs-lookup"><span data-stu-id="f12aa-148">See also</span></span>



[<span data-ttu-id="f12aa-149">MAPI のプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="f12aa-149">MAPI Property Overview</span></span>](mapi-property-overview.md)

