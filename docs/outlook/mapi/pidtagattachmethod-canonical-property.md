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
description: '最終更新日: 2016 年9月7日'
ms.openlocfilehash: b84549ab31c939b4e6115795916ebd3520a96dbd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327259"
---
# <a name="pidtagattachmethod-canonical-property"></a><span data-ttu-id="491b2-103">PidTagAttachMethod 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="491b2-103">PidTagAttachMethod Canonical Property</span></span>

 
  
<span data-ttu-id="491b2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="491b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="491b2-105">添付ファイルのコンテンツにアクセスできる方法を表す MAPI 定義の定数が格納されています。</span><span class="sxs-lookup"><span data-stu-id="491b2-105">Contains a MAPI-defined constant representing the way the contents of an attachment can be accessed.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="491b2-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="491b2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="491b2-107">PR_ATTACH_METHOD</span><span class="sxs-lookup"><span data-stu-id="491b2-107">PR_ATTACH_METHOD</span></span>  <br/> |
|<span data-ttu-id="491b2-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="491b2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="491b2-109">0x3705</span><span class="sxs-lookup"><span data-stu-id="491b2-109">0x3705</span></span>  <br/> |
|<span data-ttu-id="491b2-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="491b2-110">Data type:</span></span>  <br/> |<span data-ttu-id="491b2-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="491b2-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="491b2-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="491b2-112">Area:</span></span>  <br/> |<span data-ttu-id="491b2-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="491b2-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="491b2-114">解説</span><span class="sxs-lookup"><span data-stu-id="491b2-114">Remarks</span></span>

<span data-ttu-id="491b2-115">このプロパティには、次のいずれかの値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="491b2-115">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="491b2-116">NO_ATTACHMENT</span><span class="sxs-lookup"><span data-stu-id="491b2-116">NO_ATTACHMENT</span></span> 
  
> <span data-ttu-id="491b2-117">添付ファイルは作成されたばかりです。</span><span class="sxs-lookup"><span data-stu-id="491b2-117">The attachment has just been created.</span></span> 
    
<span data-ttu-id="491b2-118">ATTACH_BY_VALUE</span><span class="sxs-lookup"><span data-stu-id="491b2-118">ATTACH_BY_VALUE</span></span> 
  
> <span data-ttu-id="491b2-119">**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) プロパティには、添付ファイルデータが含まれています。</span><span class="sxs-lookup"><span data-stu-id="491b2-119">The **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property contains the attachment data.</span></span> 
    
<span data-ttu-id="491b2-120">ATTACH_BY_REFERENCE</span><span class="sxs-lookup"><span data-stu-id="491b2-120">ATTACH_BY_REFERENCE</span></span> 
  
> <span data-ttu-id="491b2-121">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) または**PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) プロパティには、共通ファイルへのアクセス権を持つ受信者への添付ファイルを識別する完全修飾パスが含まれています。server.</span><span class="sxs-lookup"><span data-stu-id="491b2-121">The **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) or **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) property contains a fully-qualified path identifying the attachment to recipients with access to a common file server.</span></span> 
    
<span data-ttu-id="491b2-122">ATTACH_BY_REF_RESOLVE</span><span class="sxs-lookup"><span data-stu-id="491b2-122">ATTACH_BY_REF_RESOLVE</span></span> 
  
> <span data-ttu-id="491b2-123">**PR_ATTACH_PATHNAME**または**PR_ATTACH_LONG_PATHNAME**プロパティには、添付ファイルを識別する完全修飾パスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="491b2-123">The **PR_ATTACH_PATHNAME** or **PR_ATTACH_LONG_PATHNAME** property contains a fully-qualified path identifying the attachment.</span></span> 
    
<span data-ttu-id="491b2-124">ATTACH_BY_REF_ONLY</span><span class="sxs-lookup"><span data-stu-id="491b2-124">ATTACH_BY_REF_ONLY</span></span> 
  
> <span data-ttu-id="491b2-125">**PR_ATTACH_PATHNAME**または**PR_ATTACH_LONG_PATHNAME**プロパティには、添付ファイルを識別する完全修飾パスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="491b2-125">The **PR_ATTACH_PATHNAME** or **PR_ATTACH_LONG_PATHNAME** property contains a fully-qualified path identifying the attachment.</span></span> 
    
<span data-ttu-id="491b2-126">ATTACH_EMBEDDED_MSG</span><span class="sxs-lookup"><span data-stu-id="491b2-126">ATTACH_EMBEDDED_MSG</span></span> 
  
> <span data-ttu-id="491b2-127">**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) プロパティには、 **IMessage**インターフェイスをサポートする埋め込みオブジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="491b2-127">The **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property contains an embedded object that supports the **IMessage** interface.</span></span> 
    
<span data-ttu-id="491b2-128">ATTACH_OLE</span><span class="sxs-lookup"><span data-stu-id="491b2-128">ATTACH_OLE</span></span> 
  
> <span data-ttu-id="491b2-129">添付ファイルは、埋め込み OLE オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="491b2-129">The attachment is an embedded OLE object.</span></span>
    
<span data-ttu-id="491b2-130">ATTACH_BY_WEBREFERENCE</span><span class="sxs-lookup"><span data-stu-id="491b2-130">ATTACH_BY_WEBREFERENCE</span></span> 
  
> <span data-ttu-id="491b2-131">添付ファイルの内容がメッセージに含まれていません。</span><span class="sxs-lookup"><span data-stu-id="491b2-131">The attachment content is not in the message.</span></span> 
    
<span data-ttu-id="491b2-132">作成されると、すべての attachment オブジェクトには、 **NO_ATTACHMENT**の初期**PR_ATTACH_METHOD**値が設定されます。</span><span class="sxs-lookup"><span data-stu-id="491b2-132">When created, all attachment objects have an initial **PR_ATTACH_METHOD** value of **NO_ATTACHMENT**.</span></span> 
  
<span data-ttu-id="491b2-133">クライアントアプリケーションおよびサービスプロバイダーは、 **ATTACH_BY_VALUE**値で表される attachment メソッドをサポートするためにのみ必要です。</span><span class="sxs-lookup"><span data-stu-id="491b2-133">Client applications and service providers are only required to support the attachment method represented by the **ATTACH_BY_VALUE** value.</span></span> <span data-ttu-id="491b2-134">その他の添付ファイルメソッドはオプションです。</span><span class="sxs-lookup"><span data-stu-id="491b2-134">The other attachment methods are optional.</span></span> <span data-ttu-id="491b2-135">メッセージストアでは、 **PR_ATTACH_METHOD**の値と他の添付ファイルのプロパティの値との間の整合性は適用されません。</span><span class="sxs-lookup"><span data-stu-id="491b2-135">The message store does not enforce any consistency between the value of **PR_ATTACH_METHOD** and the values of the other attachment properties.</span></span> 
  
<span data-ttu-id="491b2-136">汎用名前付け規則 (UNC) 名は、 **ATTACH_BY_REFERENCE**および**ATTACH_BY_REF_ONLY**で使用する必要がある完全修飾パスに対してお勧めします。</span><span class="sxs-lookup"><span data-stu-id="491b2-136">Universal naming convention (UNC) names are recommended for fully-qualified paths, which should be used with **ATTACH_BY_REFERENCE** and **ATTACH_BY_REF_ONLY**.</span></span> <span data-ttu-id="491b2-137">**ATTACH_BY_REF_RESOLVE**では、MAPI スプーラーが添付ファイルを**ATTACH_BY_VALUE**に変換するため、絶対パスの方が高速になります。</span><span class="sxs-lookup"><span data-stu-id="491b2-137">With **ATTACH_BY_REF_RESOLVE**, an absolute path is faster, because the MAPI spooler converts the attachment to **ATTACH_BY_VALUE**.</span></span> 
  
<span data-ttu-id="491b2-138">**ATTACH_BY_REFERENCE**が設定されている場合、 **PR_ATTACH_DATA_BIN**は空である必要があります。</span><span class="sxs-lookup"><span data-stu-id="491b2-138">If **ATTACH_BY_REFERENCE** is set, **PR_ATTACH_DATA_BIN** must be empty.</span></span> <span data-ttu-id="491b2-139">送信ゲートウェイは、添付ファイルのデータを**PR_ATTACH_DATA_BIN**プロパティにコピーすることによって、 **ATTACH_BY_REFERENCE**の添付ファイルを**ATTACH_BY_VALUE**添付ファイルに変換できます。</span><span class="sxs-lookup"><span data-stu-id="491b2-139">An outbound gateway can turn an **ATTACH_BY_REFERENCE** attachment into an **ATTACH_BY_VALUE** attachment by copying the attachment data into the **PR_ATTACH_DATA_BIN** property.</span></span> 
  
<span data-ttu-id="491b2-140">**ATTACH_BY_REF_RESOLVE**が設定されている場合、 **PR_ATTACH_DATA_BIN**は空である必要があります。</span><span class="sxs-lookup"><span data-stu-id="491b2-140">If **ATTACH_BY_REF_RESOLVE** is set, **PR_ATTACH_DATA_BIN** must be empty.</span></span> <span data-ttu-id="491b2-141">**ATTACH_BY_REF_RESOLVE**添付ファイルを含むメッセージが送信されると、MAPI スプーラーは添付ファイルデータを**ATTACH_BY_VALUE**添付ファイルにコピーします。</span><span class="sxs-lookup"><span data-stu-id="491b2-141">When the message that contains the **ATTACH_BY_REF_RESOLVE** attachment is sent, the MAPI spooler copies the attachment data into an **ATTACH_BY_VALUE** attachment.</span></span> <span data-ttu-id="491b2-142">この解決プロセスでは、添付ファイルのデータを**PR_ATTACH_DATA_BIN**に配置します。</span><span class="sxs-lookup"><span data-stu-id="491b2-142">This resolution process places the attachment data in **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="491b2-143">**ATTACH_BY_REF_ONLY**が設定されている場合、 **PR_ATTACH_DATA_BIN**は空である必要があり、メッセージングシステムは添付ファイルの参照を解決しません。</span><span class="sxs-lookup"><span data-stu-id="491b2-143">If **ATTACH_BY_REF_ONLY** is set, **PR_ATTACH_DATA_BIN** must be empty, and the messaging system never resolves the attachment reference.</span></span> <span data-ttu-id="491b2-144">この値は、リンクを送信するがデータは送信しない場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="491b2-144">Use this value when you want to send the link but not the data.</span></span> 
  
<span data-ttu-id="491b2-145">ole オブジェクトが ole 2.0 **IStorage**形式の場合は、 **PR_ATTACH_DATA_OBJ**を使用してデータにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="491b2-145">When the OLE object is in OLE 2.0 **IStorage** format, the data is accessible through **PR_ATTACH_DATA_OBJ**.</span></span> <span data-ttu-id="491b2-146">ole オブジェクトが ole 1.0 **olestream**形式の場合、データは**IStream**として**PR_ATTACH_DATA_BIN**を通じてアクセスされます。</span><span class="sxs-lookup"><span data-stu-id="491b2-146">When the OLE object is in OLE 1.0 **OLESTREAM** format, the data is accessible through **PR_ATTACH_DATA_BIN** as an **IStream**.</span></span> <span data-ttu-id="491b2-147">OLE エンコードの種類は、 **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) 値で決定できます。</span><span class="sxs-lookup"><span data-stu-id="491b2-147">The type of the OLE encoding can be determined by the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) value.</span></span> 
  
<span data-ttu-id="491b2-148">ole のインターフェイスと形式の詳細については、「 *ole プログラマーズリファレンス*」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="491b2-148">For more information on OLE interfaces and formats, see the  *OLE Programmer's Reference*  .</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="491b2-149">解説</span><span class="sxs-lookup"><span data-stu-id="491b2-149">Remarks</span></span>

<span data-ttu-id="491b2-150">**PR_ATTACH_METHOD**が**ATTACH_BY_WEBREFERENCE**の場合、添付ファイルの内容はメッセージに含まれません。</span><span class="sxs-lookup"><span data-stu-id="491b2-150">When the **PR_ATTACH_METHOD** is **ATTACH_BY_WEBREFERENCE**, the attachment content is not in the message.</span></span> <span data-ttu-id="491b2-151">代わりに、 **PR_ATTACH_LONG_FILENAME**プロパティには、オンラインで格納されている添付ファイルの内容への絶対 URL が含まれています。</span><span class="sxs-lookup"><span data-stu-id="491b2-151">Instead, the **PR_ATTACH_LONG_FILENAME** property contains an absolute URL to the attachment content, which is stored online.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="491b2-152">関連リソース</span><span class="sxs-lookup"><span data-stu-id="491b2-152">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="491b2-153">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="491b2-153">Protocol specifications</span></span>

<span data-ttu-id="491b2-154">[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="491b2-154">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="491b2-155">メッセージと添付ファイルオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="491b2-155">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="491b2-156">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="491b2-156">Header files</span></span>

<span data-ttu-id="491b2-157">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="491b2-157">Mapidefs.h</span></span>
  
> <span data-ttu-id="491b2-158">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="491b2-158">Provides data type definitions.</span></span>
    
<span data-ttu-id="491b2-159">Mapitags</span><span class="sxs-lookup"><span data-stu-id="491b2-159">Mapitags.h</span></span>
  
> <span data-ttu-id="491b2-160">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="491b2-160">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="491b2-161">関連項目</span><span class="sxs-lookup"><span data-stu-id="491b2-161">See also</span></span>



[<span data-ttu-id="491b2-162">PidTagStoreSupportMask 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="491b2-162">PidTagStoreSupportMask Canonical Property</span></span>](pidtagstoresupportmask-canonical-property.md)


[<span data-ttu-id="491b2-163">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="491b2-163">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="491b2-164">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="491b2-164">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="491b2-165">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="491b2-165">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="491b2-166">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="491b2-166">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

