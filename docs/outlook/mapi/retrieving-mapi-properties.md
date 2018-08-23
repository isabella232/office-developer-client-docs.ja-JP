---
title: MAPI プロパティを取得します。
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bd3f9f59-9020-46e6-9560-86a7a0eeca20
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: 41157b97eb28787deaf19c2e974da23dfb77e0be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803765"
---
# <a name="retrieving-mapi-properties"></a><span data-ttu-id="15b06-103">MAPI プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="15b06-103">Retrieving MAPI Properties</span></span>

 
  
<span data-ttu-id="15b06-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="15b06-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="15b06-105">クライアントまたはサービス プロバイダーは、オブジェクトからプロパティを取得、プロパティの値、型、および識別子、オブジェクトに、利用できます。</span><span class="sxs-lookup"><span data-stu-id="15b06-105">When a client or service provider retrieves a property from an object, the object makes available the property's value, type, and identifier.</span></span> 
  
<span data-ttu-id="15b06-106">クライアントとサービス ・ プロバイダーは、次のいずれかを呼び出すことによってオブジェクトのプロパティを取得できます。</span><span class="sxs-lookup"><span data-stu-id="15b06-106">Clients and service providers can retrieve an object's properties by calling one of the following:</span></span>
  
[<span data-ttu-id="15b06-107">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="15b06-107">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="15b06-108">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="15b06-108">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="15b06-109">HrGetOneProp</span><span class="sxs-lookup"><span data-stu-id="15b06-109">HrGetOneProp</span></span>](hrgetoneprop.md)
  
<span data-ttu-id="15b06-110">**GetProps**メソッドを使用して、アクセスの特別なまたは代替のインタ フェースの必要がない 1 つまたは複数のプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="15b06-110">The **GetProps** method is used to retrieve one or more properties that do not need a specialized or alternate interface for access.</span></span> <span data-ttu-id="15b06-111">これは**GetProps**に使用できるプロパティは整数、ブール値など、小さなことを意味します。</span><span class="sxs-lookup"><span data-stu-id="15b06-111">This implies that the properties available with **GetProps** are small, such as integers and Boolean values.</span></span> 
  
 <span data-ttu-id="15b06-112">**複数のプロパティを取得するには**</span><span class="sxs-lookup"><span data-stu-id="15b06-112">**To retrieve multiple properties**</span></span>
  
1. <span data-ttu-id="15b06-113">取得するプロパティの数を保持するのに十分な大きさ[SPropTagArray](sproptagarray.md)構造体を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="15b06-113">Allocate an [SPropTagArray](sproptagarray.md) structure large enough to hold the number of properties to be retrieved.</span></span> 
    
2. <span data-ttu-id="15b06-114">**あう**、 **SPropTagArray**構造体のメンバーを取得しても、ターゲット プロパティのいずれかの可能な場合は、識別子と型に**aulPropTag**の各メンバーを設定するプロパティの数を設定します。</span><span class="sxs-lookup"><span data-stu-id="15b06-114">Set the **cValues** member of the **SPropTagArray** structure to the number of properties to be retrieved and set each **aulPropTag** member to the identifier and type, if possible, of one of the target properties.</span></span> <span data-ttu-id="15b06-115">型が不明な場合は、PT_UNSPECIFIED に設定します。</span><span class="sxs-lookup"><span data-stu-id="15b06-115">If the type is unknown, set it to PT_UNSPECIFIED.</span></span> <span data-ttu-id="15b06-116">型と識別子の両方がない既知の場合は、 [IMAPIProp::GetPropList](imapiprop-getproplist.md)を呼び出すことによってこの情報を検索します。</span><span class="sxs-lookup"><span data-stu-id="15b06-116">If both the type and the identifier are unknown, locate this information by calling [IMAPIProp::GetPropList](imapiprop-getproplist.md).</span></span> <span data-ttu-id="15b06-117">**Getproplist メソッド**は、すべてのオブジェクトのサポートされているプロパティを持つプロパティ タグ配列を返します。</span><span class="sxs-lookup"><span data-stu-id="15b06-117">**GetPropList** returns a property tag array with all of the object's supported properties.</span></span> <span data-ttu-id="15b06-118">プロパティの名前があるのみの場合は、関連付けられている識別子にアクセスする[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="15b06-118">If only a property name is available, call [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to access the associated identifier.</span></span> 
    
3. <span data-ttu-id="15b06-119">プロパティまたはプロパティを開くには、 [IMAPIProp::GetProps](imapiprop-getprops.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="15b06-119">Call [IMAPIProp::GetProps](imapiprop-getprops.md) to open the property or properties.</span></span> 
    
<span data-ttu-id="15b06-120">**OpenProperty**メソッドを使用して、アクセスの**IStream**または[IMAPITable](imapitableiunknown.md)などの代替のインタ フェースを必要とする大規模なプロパティを開きます。</span><span class="sxs-lookup"><span data-stu-id="15b06-120">The **OpenProperty** method is used to open larger properties that require an alternate interface such as **IStream** or [IMAPITable](imapitableiunknown.md) for access.</span></span> <span data-ttu-id="15b06-121">**OpenProperty**は、通常大きな文字の文字列、バイナリ、およびオブジェクトのプロパティを開くに使用し、のみ 1 つのプロパティを同時に開くことができます。</span><span class="sxs-lookup"><span data-stu-id="15b06-121">**OpenProperty** is typically used to open large character string, binary, and object properties and can only open one property at a time.</span></span> <span data-ttu-id="15b06-122">呼び出し元は、入力パラメーターの 1 つとして要求されるその他のインターフェイスの識別子を渡します。</span><span class="sxs-lookup"><span data-stu-id="15b06-122">Callers pass in the identifier of the additional interface that is required as one of the input parameters.</span></span> 
  
<span data-ttu-id="15b06-123">**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))、テキスト ベースのメッセージの本文、 **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) を保持するプロパティを保持するプロパティを開くときは、 **OpenProperty**の一般的な用途のいくつか、OLE オブジェクトまたはメッセージの添付ファイルと**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) は、フォルダーまたはアドレス帳コンテナーの内容テーブルを保持するプロパティです。</span><span class="sxs-lookup"><span data-stu-id="15b06-123">Some of the common uses of **OpenProperty** include opening **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), the property that holds the body of a text-based message, **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)), the property that holds an OLE object or message attachment, and **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), the property that holds a folder or address book container contents table.</span></span> 
  
<span data-ttu-id="15b06-124">プロパティに応じて、 **OpenProperty**から別のインターフェイスが要求されます。</span><span class="sxs-lookup"><span data-stu-id="15b06-124">Depending on the property, a different interface is requested from **OpenProperty**.</span></span> <span data-ttu-id="15b06-125">**IStream**をバイトのストリームとして読み書きするプロパティのデータを可能にするインタ フェースは通常、 **PR_BODY**にアクセスするため使用されます。</span><span class="sxs-lookup"><span data-stu-id="15b06-125">**IStream**, an interface that allows property data to be read and written as a stream of bytes, is typically used to access **PR_BODY**.</span></span> <span data-ttu-id="15b06-126">[IMessage](imessageimapiprop.md)または**IStream**のいずれかが**PR_ATTACH_DATA_OBJ**にアクセスするために使えます。</span><span class="sxs-lookup"><span data-stu-id="15b06-126">Either [IMessage](imessageimapiprop.md) or **IStream** can be used to access **PR_ATTACH_DATA_OBJ**.</span></span> <span data-ttu-id="15b06-127">**IStream**を使用して、TNEF 形式のメッセージは、標準的なメッセージは、埋め込みメッセージの添付ファイルは**IMessage**を使用します。</span><span class="sxs-lookup"><span data-stu-id="15b06-127">Embedded message attachments that are standard messages use **IMessage** whereas messages in the TNEF format use **IStream**.</span></span> <span data-ttu-id="15b06-128">**PR_CONTAINER_CONTENTS**は、table オブジェクトであるために、 [IMAPITable](imapitableiunknown.md)にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="15b06-128">Because **PR_CONTAINER_CONTENTS** is a table object, it is accessed with [IMAPITable](imapitableiunknown.md).</span></span>
  
 <span data-ttu-id="15b06-129">**PR_ATTACH_DATA_BIN プロパティの添付ファイルの取得**</span><span class="sxs-lookup"><span data-stu-id="15b06-129">**To retrieve an attachment's PR_ATTACH_DATA_BIN property**</span></span>
  
1. <span data-ttu-id="15b06-130">ファイルのストリームを開く[OpenStreamOnFile](openstreamonfile.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="15b06-130">Call the [OpenStreamOnFile](openstreamonfile.md) function to open a stream for the file.</span></span> 
    
2. <span data-ttu-id="15b06-131">**IStream**インターフェイスを使用して**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) のプロパティを取得するメッセージの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)のメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="15b06-131">Call the message's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to retrieve the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property with the **IStream** interface.</span></span> <span data-ttu-id="15b06-132">MAPI_MODIFY とタグの両方のフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="15b06-132">Set both the MAPI_MODIFY and MAPI_CREATE flags.</span></span> 
    
3. <span data-ttu-id="15b06-133">**STATSTG**構造体を割り当てるし、そのサイズを決定するファイル ストリームの**IStream::Stat**メソッドの呼び出しで渡すことです。</span><span class="sxs-lookup"><span data-stu-id="15b06-133">Allocate a **STATSTG** structure and pass it in a call to the file stream's **IStream::Stat** method to determine its size.</span></span> <span data-ttu-id="15b06-134">フラグ STREAM_SEEK_END を使用して**IStream::Seek**を呼び出すには、ストリームのサイズを決定する別の方法です。</span><span class="sxs-lookup"><span data-stu-id="15b06-134">Another way to determine stream size is to call **IStream::Seek** with the flag STREAM_SEEK_END.</span></span> 
    
4. <span data-ttu-id="15b06-135">添付ファイルのストリームに、ファイルのストリームからデータをコピーするのには、ストリームの**IStream::CopyTo**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="15b06-135">Call the stream's **IStream::CopyTo** method to copy the data from the file's stream into the attachment stream.</span></span> 
    
5. <span data-ttu-id="15b06-136">コピー操作が完了すると、それぞれ**が**メソッドを呼び出すことによって両方のストリームを解放します。</span><span class="sxs-lookup"><span data-stu-id="15b06-136">When the copy operation is finished, release both streams by calling their **IUnknown::Release** methods.</span></span> 
    
<span data-ttu-id="15b06-137">**IStream**を使用すると、プロパティへのアクセスのサービス プロバイダーによっては、ストリームでのプロパティのサイズを自動的に送信します。</span><span class="sxs-lookup"><span data-stu-id="15b06-137">When **IStream** is used for property access, some service providers automatically send the size of the property back with the stream.</span></span> <span data-ttu-id="15b06-138">ストリーム サイズの戻り値のプロパティを開くときに、フラグを遅らせることができます、MAPI_DEFERRED_ERRORS と**OpenProperty**を呼び出すことです。</span><span class="sxs-lookup"><span data-stu-id="15b06-138">Calling **OpenProperty** with the MAPI_DEFERRED_ERRORS flag can delay the opening of the property and the return of the stream size.</span></span> <span data-ttu-id="15b06-139">**IStream::Stat**が、MAPI_DEFERRED_ERRORS と**OpenProperty**フラグを設定した後に、このサイズを取得するために呼び出される場合は、この一連の呼び出しは、余分なリモート プロシージャ呼び出しを強制するためにパフォーマンスが低下します。</span><span class="sxs-lookup"><span data-stu-id="15b06-139">If **IStream::Stat** is called to retrieve this size after **OpenProperty** with the MAPI_DEFERRED_ERRORS flag set, performance will be impacted because this sequence of calls forces an extra remote procedure call.</span></span> <span data-ttu-id="15b06-140">パフォーマンスへの影響を避けるためには、クライアントが**OpenProperty**し、**統計値**の呼び出しの間の任意の MAPI メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="15b06-140">To avoid the performance hit, clients can call any MAPI method between the calls to **OpenProperty** and to **Stat**.</span></span>
  
<span data-ttu-id="15b06-141">**OpenProperty**と同様に、 [HrGetOneProp](hrgetoneprop.md)関数は、一度に 1 つのプロパティを開きます。</span><span class="sxs-lookup"><span data-stu-id="15b06-141">The [HrGetOneProp](hrgetoneprop.md) function, like **OpenProperty**, opens one property at a time.</span></span> <span data-ttu-id="15b06-142">**HrGetOneProp**は、ローカル マシン上に対象のオブジェクトが存在する場合にのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="15b06-142">**HrGetOneProp** should only be used when the target object exists on the local machine.</span></span> <span data-ttu-id="15b06-143">対象のオブジェクトをローカルで使用できない場合は、複数のリモート プロシージャ コールとパフォーマンスの低下につながる**HrGetOneProp**を繰り返し使用します。</span><span class="sxs-lookup"><span data-stu-id="15b06-143">When the target object is not locally available, using **HrGetOneProp** repeatedly can result in multiple remote procedure calls and a performance degradation.</span></span> 
  
<span data-ttu-id="15b06-144">いくつかのプロパティを必要とする呼び出し元ループ内で**HrGetOneProp**または**OpenProperty**を呼び出すか、 **GetProps**に 1 つの呼び出しを実行します。</span><span class="sxs-lookup"><span data-stu-id="15b06-144">Callers that need several properties can either call **HrGetOneProp** or **OpenProperty** in a loop or make one call to **GetProps**.</span></span> <span data-ttu-id="15b06-145">**GetProps**を 1 回呼び出すことは、効率的です。</span><span class="sxs-lookup"><span data-stu-id="15b06-145">Calling **GetProps** once is more efficient.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="15b06-146">セキュリティで保護されたプロパティは、 **GetProps**、 **HrGetOneProp**、または**getproplist メソッド**の呼び出しでは、他のプロパティを使用して自動的にご利用いただけません。</span><span class="sxs-lookup"><span data-stu-id="15b06-146">Secure properties are not automatically available with other properties in a **GetProps**, **HrGetOneProp**, or **GetPropList** call.</span></span> <span data-ttu-id="15b06-147">セキュリティで保護されたプロパティは、そのプロパティの識別子を使用して明示的に要求する必要があります。</span><span class="sxs-lookup"><span data-stu-id="15b06-147">Secure properties must be explicitly requested using their property identifiers.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="15b06-148">関連項目</span><span class="sxs-lookup"><span data-stu-id="15b06-148">See also</span></span>



[<span data-ttu-id="15b06-149">MAPI のプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="15b06-149">MAPI Property Overview</span></span>](mapi-property-overview.md)

