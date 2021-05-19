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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417085"
---
# <a name="retrieving-mapi-properties"></a><span data-ttu-id="63de9-103">MAPI プロパティの取得</span><span class="sxs-lookup"><span data-stu-id="63de9-103">Retrieving MAPI Properties</span></span>

 
  
<span data-ttu-id="63de9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63de9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63de9-105">クライアントまたはサービス プロバイダーがオブジェクトからプロパティを取得すると、オブジェクトはプロパティの値、型、識別子を使用できます。</span><span class="sxs-lookup"><span data-stu-id="63de9-105">When a client or service provider retrieves a property from an object, the object makes available the property's value, type, and identifier.</span></span> 
  
<span data-ttu-id="63de9-106">クライアントとサービス プロバイダーは、次のいずれかを呼び出すことによって、オブジェクトのプロパティを取得できます。</span><span class="sxs-lookup"><span data-stu-id="63de9-106">Clients and service providers can retrieve an object's properties by calling one of the following:</span></span>
  
[<span data-ttu-id="63de9-107">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="63de9-107">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="63de9-108">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="63de9-108">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="63de9-109">HrGetOneProp</span><span class="sxs-lookup"><span data-stu-id="63de9-109">HrGetOneProp</span></span>](hrgetoneprop.md)
  
<span data-ttu-id="63de9-110">**GetProps メソッドは**、アクセスに専用または代替インターフェイスを必要としない 1 つ以上のプロパティを取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="63de9-110">The **GetProps** method is used to retrieve one or more properties that do not need a specialized or alternate interface for access.</span></span> <span data-ttu-id="63de9-111">これは **、GetProps** で使用できるプロパティが小さいことを意味します (整数値やブール値など)。</span><span class="sxs-lookup"><span data-stu-id="63de9-111">This implies that the properties available with **GetProps** are small, such as integers and Boolean values.</span></span> 
  
 <span data-ttu-id="63de9-112">**複数のプロパティを取得するには**</span><span class="sxs-lookup"><span data-stu-id="63de9-112">**To retrieve multiple properties**</span></span>
  
1. <span data-ttu-id="63de9-113">取得するプロパティの数を保持するのに十分な大きい [SPropTagArray](sproptagarray.md) 構造体を割り当てる。</span><span class="sxs-lookup"><span data-stu-id="63de9-113">Allocate an [SPropTagArray](sproptagarray.md) structure large enough to hold the number of properties to be retrieved.</span></span> 
    
2. <span data-ttu-id="63de9-114">**SPropTagArray** 構造体の **cValues** メンバーを取得するプロパティの数に設定し、各 **aulPropTag** メンバーを、可能であればターゲット プロパティの 1 つの識別子と型に設定します。</span><span class="sxs-lookup"><span data-stu-id="63de9-114">Set the **cValues** member of the **SPropTagArray** structure to the number of properties to be retrieved and set each **aulPropTag** member to the identifier and type, if possible, of one of the target properties.</span></span> <span data-ttu-id="63de9-115">型が不明な場合は、この型を [PT_UNSPECIFIED] に設定します。</span><span class="sxs-lookup"><span data-stu-id="63de9-115">If the type is unknown, set it to PT_UNSPECIFIED.</span></span> <span data-ttu-id="63de9-116">型と識別子の両方が不明な場合は [、IMAPIProp::GetPropList](imapiprop-getproplist.md)を呼び出してこの情報を探します。</span><span class="sxs-lookup"><span data-stu-id="63de9-116">If both the type and the identifier are unknown, locate this information by calling [IMAPIProp::GetPropList](imapiprop-getproplist.md).</span></span> <span data-ttu-id="63de9-117">**GetPropList** は、オブジェクトのすべてのサポートされているプロパティを持つプロパティ タグ配列を返します。</span><span class="sxs-lookup"><span data-stu-id="63de9-117">**GetPropList** returns a property tag array with all of the object's supported properties.</span></span> <span data-ttu-id="63de9-118">プロパティ名のみを使用できる場合は [、IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) を呼び出して、関連付けられた識別子にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="63de9-118">If only a property name is available, call [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to access the associated identifier.</span></span> 
    
3. <span data-ttu-id="63de9-119">[IMAPIProp::GetProps を](imapiprop-getprops.md)呼び出して、プロパティまたはプロパティを開きます。</span><span class="sxs-lookup"><span data-stu-id="63de9-119">Call [IMAPIProp::GetProps](imapiprop-getprops.md) to open the property or properties.</span></span> 
    
<span data-ttu-id="63de9-120">**OpenProperty メソッドは**、アクセスに **IStream** や [IMAPITable](imapitableiunknown.md)などの代替インターフェイスを必要とする大きなプロパティを開くのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="63de9-120">The **OpenProperty** method is used to open larger properties that require an alternate interface such as **IStream** or [IMAPITable](imapitableiunknown.md) for access.</span></span> <span data-ttu-id="63de9-121">**OpenProperty は** 通常、大きな文字列、バイナリ、およびオブジェクトのプロパティを開くために使用され、一度に 1 つのプロパティのみを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="63de9-121">**OpenProperty** is typically used to open large character string, binary, and object properties and can only open one property at a time.</span></span> <span data-ttu-id="63de9-122">発信者は、入力パラメーターの 1 つとして必要な追加インターフェイスの識別子を渡します。</span><span class="sxs-lookup"><span data-stu-id="63de9-122">Callers pass in the identifier of the additional interface that is required as one of the input parameters.</span></span> 
  
<span data-ttu-id="63de9-123">**OpenProperty** の一般的な用途には、PR_BODY **(** [PidTagBody)](pidtagbody-canonical-property.md)を開く、テキスト ベースのメッセージの本文を保持するプロパティ **、PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject)、OLE](pidtagattachdataobject-canonical-property.md)オブジェクトまたはメッセージ添付ファイルを保持するプロパティ、および **PR_CONTAINER_CONTENTS** ([PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)、フォルダーまたはアドレス帳コンテナーのコンテンツ テーブルを保持するプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="63de9-123">Some of the common uses of **OpenProperty** include opening **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), the property that holds the body of a text-based message, **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)), the property that holds an OLE object or message attachment, and **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), the property that holds a folder or address book container contents table.</span></span> 
  
<span data-ttu-id="63de9-124">プロパティに応じて **、OpenProperty** から別のインターフェイスが要求されます。</span><span class="sxs-lookup"><span data-stu-id="63de9-124">Depending on the property, a different interface is requested from **OpenProperty**.</span></span> <span data-ttu-id="63de9-125">**IStream** は、プロパティ データをバイト ストリームとして読み取りおよび書き込みできるインターフェイスで、通常、プロパティ データにアクセス **PR_BODY。**</span><span class="sxs-lookup"><span data-stu-id="63de9-125">**IStream**, an interface that allows property data to be read and written as a stream of bytes, is typically used to access **PR_BODY**.</span></span> <span data-ttu-id="63de9-126">[IMessage](imessageimapiprop.md)または IStream を使用して、IMessage または **IStream** **にアクセスPR_ATTACH_DATA_OBJ。**</span><span class="sxs-lookup"><span data-stu-id="63de9-126">Either [IMessage](imessageimapiprop.md) or **IStream** can be used to access **PR_ATTACH_DATA_OBJ**.</span></span> <span data-ttu-id="63de9-127">標準メッセージである埋め込みメッセージ添付ファイルは **IMessage** を使用しますが、TNEF 形式のメッセージは **IStream を使用します**。</span><span class="sxs-lookup"><span data-stu-id="63de9-127">Embedded message attachments that are standard messages use **IMessage** whereas messages in the TNEF format use **IStream**.</span></span> <span data-ttu-id="63de9-128">テーブル **オブジェクト** PR_CONTAINER_CONTENTS、IMAPITable を使用 [してアクセスされます](imapitableiunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="63de9-128">Because **PR_CONTAINER_CONTENTS** is a table object, it is accessed with [IMAPITable](imapitableiunknown.md).</span></span>
  
 <span data-ttu-id="63de9-129">**添付ファイルのプロパティを取得PR_ATTACH_DATA_BINするには**</span><span class="sxs-lookup"><span data-stu-id="63de9-129">**To retrieve an attachment's PR_ATTACH_DATA_BIN property**</span></span>
  
1. <span data-ttu-id="63de9-130">[OpenStreamOnFile 関数を呼び](openstreamonfile.md)出して、ファイルのストリームを開きます。</span><span class="sxs-lookup"><span data-stu-id="63de9-130">Call the [OpenStreamOnFile](openstreamonfile.md) function to open a stream for the file.</span></span> 
    
2. <span data-ttu-id="63de9-131">メッセージの [IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出して **、IStream** インターフェイスで PR_ATTACH_DATA_BIN **(** [PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="63de9-131">Call the message's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to retrieve the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property with the **IStream** interface.</span></span> <span data-ttu-id="63de9-132">パラメーター フラグとMAPI_MODIFYフラグMAPI_CREATEします。</span><span class="sxs-lookup"><span data-stu-id="63de9-132">Set both the MAPI_MODIFY and MAPI_CREATE flags.</span></span> 
    
3. <span data-ttu-id="63de9-133">**STATSTG 構造を割** り当て、ファイル ストリームの **IStream::Stat** メソッドを呼び出してサイズを決定します。</span><span class="sxs-lookup"><span data-stu-id="63de9-133">Allocate a **STATSTG** structure and pass it in a call to the file stream's **IStream::Stat** method to determine its size.</span></span> <span data-ttu-id="63de9-134">ストリーム サイズを決定するもう 1 つの方法は、フラグを指定して **IStream::Seek** を呼び出STREAM_SEEK_END。</span><span class="sxs-lookup"><span data-stu-id="63de9-134">Another way to determine stream size is to call **IStream::Seek** with the flag STREAM_SEEK_END.</span></span> 
    
4. <span data-ttu-id="63de9-135">ストリームの **IStream::CopyTo** メソッドを呼び出して、ファイルのストリームから添付ファイル ストリームにデータをコピーします。</span><span class="sxs-lookup"><span data-stu-id="63de9-135">Call the stream's **IStream::CopyTo** method to copy the data from the file's stream into the attachment stream.</span></span> 
    
5. <span data-ttu-id="63de9-136">コピー操作が完了したら、両方のストリームを **IUnknown::Release** メソッドを呼び出して解放します。</span><span class="sxs-lookup"><span data-stu-id="63de9-136">When the copy operation is finished, release both streams by calling their **IUnknown::Release** methods.</span></span> 
    
<span data-ttu-id="63de9-137">**IStream をプロパティ** アクセスに使用すると、一部のサービス プロバイダーはプロパティのサイズをストリームと一緒に自動的に送信します。</span><span class="sxs-lookup"><span data-stu-id="63de9-137">When **IStream** is used for property access, some service providers automatically send the size of the property back with the stream.</span></span> <span data-ttu-id="63de9-138">**OpenProperty を** MAPI_DEFERRED_ERRORSフラグで呼び出す場合、プロパティの開き方とストリーム サイズの戻り値が遅れる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="63de9-138">Calling **OpenProperty** with the MAPI_DEFERRED_ERRORS flag can delay the opening of the property and the return of the stream size.</span></span> <span data-ttu-id="63de9-139">MAPI_DEFERRED_ERRORS フラグが設定された **OpenProperty** の後にこのサイズを取得するために **IStream::Stat** が呼び出された場合、この一連の呼び出しによって余分なリモート プロシージャ呼び出しが強制的に行なうので、パフォーマンスが影響を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="63de9-139">If **IStream::Stat** is called to retrieve this size after **OpenProperty** with the MAPI_DEFERRED_ERRORS flag set, performance will be impacted because this sequence of calls forces an extra remote procedure call.</span></span> <span data-ttu-id="63de9-140">パフォーマンスのヒットを回避するために、クライアントは **OpenProperty** と Stat の呼び出しの間で MAPI メソッドを **呼び出します**。</span><span class="sxs-lookup"><span data-stu-id="63de9-140">To avoid the performance hit, clients can call any MAPI method between the calls to **OpenProperty** and to **Stat**.</span></span>
  
<span data-ttu-id="63de9-141">[OpenProperty のような HrGetOneProp](hrgetoneprop.md) **関数は**、一度に 1 つのプロパティを開きます。</span><span class="sxs-lookup"><span data-stu-id="63de9-141">The [HrGetOneProp](hrgetoneprop.md) function, like **OpenProperty**, opens one property at a time.</span></span> <span data-ttu-id="63de9-142">**HrGetOneProp** は、ターゲット オブジェクトがローカル コンピューターに存在する場合にのみ使用してください。</span><span class="sxs-lookup"><span data-stu-id="63de9-142">**HrGetOneProp** should only be used when the target object exists on the local machine.</span></span> <span data-ttu-id="63de9-143">ターゲット オブジェクトをローカルで使用できない場合 **、HrGetOneProp** を繰り返し使用すると、複数のリモート プロシージャ呼び出しが発生し、パフォーマンスが低下する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="63de9-143">When the target object is not locally available, using **HrGetOneProp** repeatedly can result in multiple remote procedure calls and a performance degradation.</span></span> 
  
<span data-ttu-id="63de9-144">複数のプロパティを必要とする呼び出し元は、ループ内で **HrGetOneProp** または **OpenProperty** を呼び出すか **、GetProps** を 1 回呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="63de9-144">Callers that need several properties can either call **HrGetOneProp** or **OpenProperty** in a loop or make one call to **GetProps**.</span></span> <span data-ttu-id="63de9-145">**GetProps を 1 回呼** び出す方が効率的です。</span><span class="sxs-lookup"><span data-stu-id="63de9-145">Calling **GetProps** once is more efficient.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="63de9-146">**GetProps、HrGetOneProp、または** **GetPropList** 呼び出しの他のプロパティでは、セキュリティで保護されたプロパティを自動的に使用できません。</span><span class="sxs-lookup"><span data-stu-id="63de9-146">Secure properties are not automatically available with other properties in a **GetProps**, **HrGetOneProp**, or **GetPropList** call.</span></span> <span data-ttu-id="63de9-147">セキュリティで保護されたプロパティは、プロパティ識別子を使用して明示的に要求する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63de9-147">Secure properties must be explicitly requested using their property identifiers.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="63de9-148">関連項目</span><span class="sxs-lookup"><span data-stu-id="63de9-148">See also</span></span>



[<span data-ttu-id="63de9-149">MAPI のプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="63de9-149">MAPI Property Overview</span></span>](mapi-property-overview.md)

