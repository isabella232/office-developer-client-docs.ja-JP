---
title: PidTagAttachMethod 標準プロパティ
manager: soliver
ms.date: 9/7/2016
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachMethod
api_type:
- HeaderDef
ms.assetid: 32089213-ef7b-4152-84ab-b44e9911332b
description: '最終更新日: 2016 年 9 月 7 日'
ms.openlocfilehash: b84549ab31c939b4e6115795916ebd3520a96dbd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400727"
---
# <a name="pidtagattachmethod-canonical-property"></a><span data-ttu-id="a51b6-103">PidTagAttachMethod 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a51b6-103">PidTagAttachMethod Canonical Property</span></span>

 
  
<span data-ttu-id="a51b6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a51b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a51b6-105">添付ファイルの内容にアクセスできる方法を示す MAPI 定義の定数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a51b6-105">Contains a MAPI-defined constant representing the way the contents of an attachment can be accessed.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a51b6-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a51b6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a51b6-107">PR_ATTACH_METHOD</span><span class="sxs-lookup"><span data-stu-id="a51b6-107">PR_ATTACH_METHOD</span></span>  <br/> |
|<span data-ttu-id="a51b6-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a51b6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a51b6-109">0x3705</span><span class="sxs-lookup"><span data-stu-id="a51b6-109">0x3705</span></span>  <br/> |
|<span data-ttu-id="a51b6-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a51b6-110">Data type:</span></span>  <br/> |<span data-ttu-id="a51b6-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a51b6-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a51b6-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="a51b6-112">Area:</span></span>  <br/> |<span data-ttu-id="a51b6-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="a51b6-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a51b6-114">備考</span><span class="sxs-lookup"><span data-stu-id="a51b6-114">Remarks</span></span>

<span data-ttu-id="a51b6-115">このプロパティは、次の値の 1 つだけ持つことができます。</span><span class="sxs-lookup"><span data-stu-id="a51b6-115">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="a51b6-116">NO_ATTACHMENT</span><span class="sxs-lookup"><span data-stu-id="a51b6-116">NO_ATTACHMENT</span></span> 
  
> <span data-ttu-id="a51b6-117">添付ファイルが作成された直後です。</span><span class="sxs-lookup"><span data-stu-id="a51b6-117">The attachment has just been created.</span></span> 
    
<span data-ttu-id="a51b6-118">ATTACH_BY_VALUE</span><span class="sxs-lookup"><span data-stu-id="a51b6-118">ATTACH_BY_VALUE</span></span> 
  
> <span data-ttu-id="a51b6-119">**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) のプロパティには、添付ファイルのデータが含まれています。</span><span class="sxs-lookup"><span data-stu-id="a51b6-119">The **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property contains the attachment data.</span></span> 
    
<span data-ttu-id="a51b6-120">ATTACH_BY_REFERENCE</span><span class="sxs-lookup"><span data-stu-id="a51b6-120">ATTACH_BY_REFERENCE</span></span> 
  
> <span data-ttu-id="a51b6-121">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) または**PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) のプロパティに共通のファイルへのアクセス権を持つ受信者に添付ファイルを識別する完全修飾パスが含まれていますサーバーです。</span><span class="sxs-lookup"><span data-stu-id="a51b6-121">The **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) or **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) property contains a fully-qualified path identifying the attachment to recipients with access to a common file server.</span></span> 
    
<span data-ttu-id="a51b6-122">ATTACH_BY_REF_RESOLVE</span><span class="sxs-lookup"><span data-stu-id="a51b6-122">ATTACH_BY_REF_RESOLVE</span></span> 
  
> <span data-ttu-id="a51b6-123">**PR_ATTACH_PATHNAME**または**PR_ATTACH_LONG_PATHNAME**のプロパティには、添付ファイルを識別する完全修飾パスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="a51b6-123">The **PR_ATTACH_PATHNAME** or **PR_ATTACH_LONG_PATHNAME** property contains a fully-qualified path identifying the attachment.</span></span> 
    
<span data-ttu-id="a51b6-124">ATTACH_BY_REF_ONLY</span><span class="sxs-lookup"><span data-stu-id="a51b6-124">ATTACH_BY_REF_ONLY</span></span> 
  
> <span data-ttu-id="a51b6-125">**PR_ATTACH_PATHNAME**または**PR_ATTACH_LONG_PATHNAME**のプロパティには、添付ファイルを識別する完全修飾パスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="a51b6-125">The **PR_ATTACH_PATHNAME** or **PR_ATTACH_LONG_PATHNAME** property contains a fully-qualified path identifying the attachment.</span></span> 
    
<span data-ttu-id="a51b6-126">ATTACH_EMBEDDED_MSG</span><span class="sxs-lookup"><span data-stu-id="a51b6-126">ATTACH_EMBEDDED_MSG</span></span> 
  
> <span data-ttu-id="a51b6-127">**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) のプロパティには、 **IMessage**インターフェイスをサポートする埋め込みオブジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="a51b6-127">The **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property contains an embedded object that supports the **IMessage** interface.</span></span> 
    
<span data-ttu-id="a51b6-128">ATTACH_OLE</span><span class="sxs-lookup"><span data-stu-id="a51b6-128">ATTACH_OLE</span></span> 
  
> <span data-ttu-id="a51b6-129">添付ファイルは、埋め込まれた OLE オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="a51b6-129">The attachment is an embedded OLE object.</span></span>
    
<span data-ttu-id="a51b6-130">ATTACH_BY_WEBREFERENCE</span><span class="sxs-lookup"><span data-stu-id="a51b6-130">ATTACH_BY_WEBREFERENCE</span></span> 
  
> <span data-ttu-id="a51b6-131">添付ファイルのコンテンツは、メッセージではありません。</span><span class="sxs-lookup"><span data-stu-id="a51b6-131">The attachment content is not in the message.</span></span> 
    
<span data-ttu-id="a51b6-132">作成するときは、 **NO_ATTACHMENT**の初期の**PR_ATTACH_METHOD**値がある添付ファイルのすべてのオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="a51b6-132">When created, all attachment objects have an initial **PR_ATTACH_METHOD** value of **NO_ATTACHMENT**.</span></span> 
  
<span data-ttu-id="a51b6-133">クライアント アプリケーションとサービス ・ プロバイダーは、 **ATTACH_BY_VALUE**の値で表される添付ファイルのメソッドをサポートするためにのみ必要です。</span><span class="sxs-lookup"><span data-stu-id="a51b6-133">Client applications and service providers are only required to support the attachment method represented by the **ATTACH_BY_VALUE** value.</span></span> <span data-ttu-id="a51b6-134">他の添付ファイルのメソッドは、オプションです。</span><span class="sxs-lookup"><span data-stu-id="a51b6-134">The other attachment methods are optional.</span></span> <span data-ttu-id="a51b6-135">メッセージ ・ ストアには、 **PR_ATTACH_METHOD**の値とその他の添付ファイルのプロパティの値との間の一貫性はありません。</span><span class="sxs-lookup"><span data-stu-id="a51b6-135">The message store does not enforce any consistency between the value of **PR_ATTACH_METHOD** and the values of the other attachment properties.</span></span> 
  
<span data-ttu-id="a51b6-136">汎用名前付け規則 (UNC) 名は、完全修飾パスは、 **ATTACH_BY_REFERENCE**と**ATTACH_BY_REF_ONLY**を使用する必要がありますに適しています。</span><span class="sxs-lookup"><span data-stu-id="a51b6-136">Universal naming convention (UNC) names are recommended for fully-qualified paths, which should be used with **ATTACH_BY_REFERENCE** and **ATTACH_BY_REF_ONLY**.</span></span> <span data-ttu-id="a51b6-137">**ATTACH_BY_REF_RESOLVE**、絶対パスは高速で、MAPI スプーラーが**ATTACH_BY_VALUE**の添付ファイルを変換するためです。</span><span class="sxs-lookup"><span data-stu-id="a51b6-137">With **ATTACH_BY_REF_RESOLVE**, an absolute path is faster, because the MAPI spooler converts the attachment to **ATTACH_BY_VALUE**.</span></span> 
  
<span data-ttu-id="a51b6-138">**ATTACH_BY_REFERENCE**が設定されている場合**PR_ATTACH_DATA_BIN**を空にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a51b6-138">If **ATTACH_BY_REFERENCE** is set, **PR_ATTACH_DATA_BIN** must be empty.</span></span> <span data-ttu-id="a51b6-139">送信ゲートウェイは、 **PR_ATTACH_DATA_BIN**プロパティに添付ファイルのデータをコピーすることによって、 **ATTACH_BY_REFERENCE** 、 **ATTACH_BY_VALUE**の添付ファイルに添付ファイルを有効にできます。</span><span class="sxs-lookup"><span data-stu-id="a51b6-139">An outbound gateway can turn an **ATTACH_BY_REFERENCE** attachment into an **ATTACH_BY_VALUE** attachment by copying the attachment data into the **PR_ATTACH_DATA_BIN** property.</span></span> 
  
<span data-ttu-id="a51b6-140">**ATTACH_BY_REF_RESOLVE**が設定されている場合**PR_ATTACH_DATA_BIN**を空にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a51b6-140">If **ATTACH_BY_REF_RESOLVE** is set, **PR_ATTACH_DATA_BIN** must be empty.</span></span> <span data-ttu-id="a51b6-141">**ATTACH_BY_REF_RESOLVE**添付ファイルを含むメッセージが送信されると、MAPI スプーラーは、 **ATTACH_BY_VALUE**の添付ファイルに添付ファイルのデータをコピーします。</span><span class="sxs-lookup"><span data-stu-id="a51b6-141">When the message that contains the **ATTACH_BY_REF_RESOLVE** attachment is sent, the MAPI spooler copies the attachment data into an **ATTACH_BY_VALUE** attachment.</span></span> <span data-ttu-id="a51b6-142">この解決プロセスは、 **PR_ATTACH_DATA_BIN**で添付ファイルのデータを配置します。</span><span class="sxs-lookup"><span data-stu-id="a51b6-142">This resolution process places the attachment data in **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="a51b6-143">**ATTACH_BY_REF_ONLY**が設定されている場合は、 **PR_ATTACH_DATA_BIN**を空にする必要があり、メッセージング システムに添付ファイルの参照が解決しません。</span><span class="sxs-lookup"><span data-stu-id="a51b6-143">If **ATTACH_BY_REF_ONLY** is set, **PR_ATTACH_DATA_BIN** must be empty, and the messaging system never resolves the attachment reference.</span></span> <span data-ttu-id="a51b6-144">リンクがデータではありませんを送信するときは、この値を使用します。</span><span class="sxs-lookup"><span data-stu-id="a51b6-144">Use this value when you want to send the link but not the data.</span></span> 
  
<span data-ttu-id="a51b6-145">OLE 2.0 **IStorage**の形式で OLE オブジェクトがある場合、データは、 **PR_ATTACH_DATA_OBJ**経由でアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="a51b6-145">When the OLE object is in OLE 2.0 **IStorage** format, the data is accessible through **PR_ATTACH_DATA_OBJ**.</span></span> <span data-ttu-id="a51b6-146">**OLESTREAM**の OLE 1.0 形式で OLE オブジェクトがある場合、データにはアクセス**PR_ATTACH_DATA_BIN**を**IStream**として。</span><span class="sxs-lookup"><span data-stu-id="a51b6-146">When the OLE object is in OLE 1.0 **OLESTREAM** format, the data is accessible through **PR_ATTACH_DATA_BIN** as an **IStream**.</span></span> <span data-ttu-id="a51b6-147">OLE のエンコードの種類は、 **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) の値によって決定できます。</span><span class="sxs-lookup"><span data-stu-id="a51b6-147">The type of the OLE encoding can be determined by the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) value.</span></span> 
  
<span data-ttu-id="a51b6-148">OLE インターフェイスとフォーマットの詳細については、 *OLE プログラマ リファレンス*を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a51b6-148">For more information on OLE interfaces and formats, see the  *OLE Programmer's Reference*  .</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a51b6-149">備考</span><span class="sxs-lookup"><span data-stu-id="a51b6-149">Remarks</span></span>

<span data-ttu-id="a51b6-150">**ATTACH_BY_WEBREFERENCE**を**PR_ATTACH_METHOD**には、添付ファイルのコンテンツは、メッセージには。</span><span class="sxs-lookup"><span data-stu-id="a51b6-150">When the **PR_ATTACH_METHOD** is **ATTACH_BY_WEBREFERENCE**, the attachment content is not in the message.</span></span> <span data-ttu-id="a51b6-151">代わりに、 **PR_ATTACH_LONG_FILENAME**プロパティには、オンラインで保存された添付ファイルのコンテンツに絶対 URL が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a51b6-151">Instead, the **PR_ATTACH_LONG_FILENAME** property contains an absolute URL to the attachment content, which is stored online.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a51b6-152">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a51b6-152">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a51b6-153">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a51b6-153">Protocol specifications</span></span>

<span data-ttu-id="a51b6-154">[[MS OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a51b6-154">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a51b6-155">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="a51b6-155">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a51b6-156">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="a51b6-156">Header files</span></span>

<span data-ttu-id="a51b6-157">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a51b6-157">Mapidefs.h</span></span>
  
> <span data-ttu-id="a51b6-158">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a51b6-158">Provides data type definitions.</span></span>
    
<span data-ttu-id="a51b6-159">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a51b6-159">Mapitags.h</span></span>
  
> <span data-ttu-id="a51b6-160">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a51b6-160">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a51b6-161">関連項目</span><span class="sxs-lookup"><span data-stu-id="a51b6-161">See also</span></span>



[<span data-ttu-id="a51b6-162">PidTagStoreSupportMask 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a51b6-162">PidTagStoreSupportMask Canonical Property</span></span>](pidtagstoresupportmask-canonical-property.md)


[<span data-ttu-id="a51b6-163">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a51b6-163">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a51b6-164">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a51b6-164">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a51b6-165">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a51b6-165">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a51b6-166">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a51b6-166">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

