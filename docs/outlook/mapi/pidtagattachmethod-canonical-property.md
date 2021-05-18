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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327259"
---
# <a name="pidtagattachmethod-canonical-property"></a><span data-ttu-id="af58e-103">PidTagAttachMethod 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="af58e-103">PidTagAttachMethod Canonical Property</span></span>

 
  
<span data-ttu-id="af58e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af58e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af58e-105">添付ファイルの内容にアクセスする方法を表す MAPI 定義の定数を格納します。</span><span class="sxs-lookup"><span data-stu-id="af58e-105">Contains a MAPI-defined constant representing the way the contents of an attachment can be accessed.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="af58e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="af58e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="af58e-107">PR_ATTACH_METHOD</span><span class="sxs-lookup"><span data-stu-id="af58e-107">PR_ATTACH_METHOD</span></span>  <br/> |
|<span data-ttu-id="af58e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="af58e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="af58e-109">0x3705</span><span class="sxs-lookup"><span data-stu-id="af58e-109">0x3705</span></span>  <br/> |
|<span data-ttu-id="af58e-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="af58e-110">Data type:</span></span>  <br/> |<span data-ttu-id="af58e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="af58e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="af58e-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="af58e-112">Area:</span></span>  <br/> |<span data-ttu-id="af58e-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="af58e-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af58e-114">注釈</span><span class="sxs-lookup"><span data-stu-id="af58e-114">Remarks</span></span>

<span data-ttu-id="af58e-115">このプロパティには、次のいずれかの値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="af58e-115">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="af58e-116">NO_ATTACHMENT</span><span class="sxs-lookup"><span data-stu-id="af58e-116">NO_ATTACHMENT</span></span> 
  
> <span data-ttu-id="af58e-117">添付ファイルが作成されたばかりです。</span><span class="sxs-lookup"><span data-stu-id="af58e-117">The attachment has just been created.</span></span> 
    
<span data-ttu-id="af58e-118">ATTACH_BY_VALUE</span><span class="sxs-lookup"><span data-stu-id="af58e-118">ATTACH_BY_VALUE</span></span> 
  
> <span data-ttu-id="af58e-119">プロパティ **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) プロパティには、添付ファイル データが含まれる。</span><span class="sxs-lookup"><span data-stu-id="af58e-119">The **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property contains the attachment data.</span></span> 
    
<span data-ttu-id="af58e-120">ATTACH_BY_REFERENCE</span><span class="sxs-lookup"><span data-stu-id="af58e-120">ATTACH_BY_REFERENCE</span></span> 
  
> <span data-ttu-id="af58e-121">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) プロパティまたは PR_ATTACH_LONG_PATHNAME ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) プロパティには、共通ファイル サーバーへのアクセス権を持つ受信者への添付ファイルを識別する完全修飾パスが含まれる。 </span><span class="sxs-lookup"><span data-stu-id="af58e-121">The **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) or **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) property contains a fully-qualified path identifying the attachment to recipients with access to a common file server.</span></span> 
    
<span data-ttu-id="af58e-122">ATTACH_BY_REF_RESOLVE</span><span class="sxs-lookup"><span data-stu-id="af58e-122">ATTACH_BY_REF_RESOLVE</span></span> 
  
> <span data-ttu-id="af58e-123">プロパティ **PR_ATTACH_PATHNAME** または **PR_ATTACH_LONG_PATHNAME** には、添付ファイルを識別する完全修飾パスが含まれる。</span><span class="sxs-lookup"><span data-stu-id="af58e-123">The **PR_ATTACH_PATHNAME** or **PR_ATTACH_LONG_PATHNAME** property contains a fully-qualified path identifying the attachment.</span></span> 
    
<span data-ttu-id="af58e-124">ATTACH_BY_REF_ONLY</span><span class="sxs-lookup"><span data-stu-id="af58e-124">ATTACH_BY_REF_ONLY</span></span> 
  
> <span data-ttu-id="af58e-125">プロパティ **PR_ATTACH_PATHNAME** または **PR_ATTACH_LONG_PATHNAME** には、添付ファイルを識別する完全修飾パスが含まれる。</span><span class="sxs-lookup"><span data-stu-id="af58e-125">The **PR_ATTACH_PATHNAME** or **PR_ATTACH_LONG_PATHNAME** property contains a fully-qualified path identifying the attachment.</span></span> 
    
<span data-ttu-id="af58e-126">ATTACH_EMBEDDED_MSG</span><span class="sxs-lookup"><span data-stu-id="af58e-126">ATTACH_EMBEDDED_MSG</span></span> 
  
> <span data-ttu-id="af58e-127">プロパティ **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) プロパティには **、IMessage** インターフェイスをサポートする埋め込みオブジェクトが含まれる。</span><span class="sxs-lookup"><span data-stu-id="af58e-127">The **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property contains an embedded object that supports the **IMessage** interface.</span></span> 
    
<span data-ttu-id="af58e-128">ATTACH_OLE</span><span class="sxs-lookup"><span data-stu-id="af58e-128">ATTACH_OLE</span></span> 
  
> <span data-ttu-id="af58e-129">添付ファイルは埋め込み OLE オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="af58e-129">The attachment is an embedded OLE object.</span></span>
    
<span data-ttu-id="af58e-130">ATTACH_BY_WEBREFERENCE</span><span class="sxs-lookup"><span data-stu-id="af58e-130">ATTACH_BY_WEBREFERENCE</span></span> 
  
> <span data-ttu-id="af58e-131">添付ファイルのコンテンツはメッセージに含めされません。</span><span class="sxs-lookup"><span data-stu-id="af58e-131">The attachment content is not in the message.</span></span> 
    
<span data-ttu-id="af58e-132">作成すると、すべての添付ファイル オブジェクトの初期 **PR_ATTACH_METHOD値が\*\*\*\*NO_ATTACHMENT。**</span><span class="sxs-lookup"><span data-stu-id="af58e-132">When created, all attachment objects have an initial **PR_ATTACH_METHOD** value of **NO_ATTACHMENT**.</span></span> 
  
<span data-ttu-id="af58e-133">クライアント アプリケーションとサービス プロバイダーは、この値で表される添付ファイルメソッドをサポートするために **ATTACH_BY_VALUE** です。</span><span class="sxs-lookup"><span data-stu-id="af58e-133">Client applications and service providers are only required to support the attachment method represented by the **ATTACH_BY_VALUE** value.</span></span> <span data-ttu-id="af58e-134">その他の添付ファイル メソッドはオプションです。</span><span class="sxs-lookup"><span data-stu-id="af58e-134">The other attachment methods are optional.</span></span> <span data-ttu-id="af58e-135">メッセージ ストアでは、メッセージ ストアの値と他の添付ファイル プロパティPR_ATTACH_METHOD一貫性は適用されません。</span><span class="sxs-lookup"><span data-stu-id="af58e-135">The message store does not enforce any consistency between the value of **PR_ATTACH_METHOD** and the values of the other attachment properties.</span></span> 
  
<span data-ttu-id="af58e-136">汎用名前付け規則 (UNC) 名は、完全修飾パスに対して推奨されます。この名前は、ATTACH_BY_REFERENCEおよび **ATTACH_BY_REF_ONLY。**</span><span class="sxs-lookup"><span data-stu-id="af58e-136">Universal naming convention (UNC) names are recommended for fully-qualified paths, which should be used with **ATTACH_BY_REFERENCE** and **ATTACH_BY_REF_ONLY**.</span></span> <span data-ttu-id="af58e-137">この **ATTACH_BY_REF_RESOLVE、MAPI** スプーラーは添付ファイルをファイルに変換するために、絶対パス **ATTACH_BY_VALUE。**</span><span class="sxs-lookup"><span data-stu-id="af58e-137">With **ATTACH_BY_REF_RESOLVE**, an absolute path is faster, because the MAPI spooler converts the attachment to **ATTACH_BY_VALUE**.</span></span> 
  
<span data-ttu-id="af58e-138">この **ATTACH_BY_REFERENCE** 設定 **されている場合** 、PR_ATTACH_DATA_BINが空である必要があります。</span><span class="sxs-lookup"><span data-stu-id="af58e-138">If **ATTACH_BY_REFERENCE** is set, **PR_ATTACH_DATA_BIN** must be empty.</span></span> <span data-ttu-id="af58e-139">送信ゲートウェイは、添付ファイル データ **を** ATTACH_BY_REFERENCEプロパティにコピーすることでATTACH_BY_VALUE添付ファイルに **PR_ATTACH_DATA_BINできます。**</span><span class="sxs-lookup"><span data-stu-id="af58e-139">An outbound gateway can turn an **ATTACH_BY_REFERENCE** attachment into an **ATTACH_BY_VALUE** attachment by copying the attachment data into the **PR_ATTACH_DATA_BIN** property.</span></span> 
  
<span data-ttu-id="af58e-140">この **ATTACH_BY_REF_RESOLVE** 設定 **されている場合** 、PR_ATTACH_DATA_BINが空である必要があります。</span><span class="sxs-lookup"><span data-stu-id="af58e-140">If **ATTACH_BY_REF_RESOLVE** is set, **PR_ATTACH_DATA_BIN** must be empty.</span></span> <span data-ttu-id="af58e-141">添付ファイルを含むメッセージATTACH_BY_REF_RESOLVE送信すると、MAPI スプーラーは添付ファイル データを添付ファイルに **ATTACH_BY_VALUE** します。</span><span class="sxs-lookup"><span data-stu-id="af58e-141">When the message that contains the **ATTACH_BY_REF_RESOLVE** attachment is sent, the MAPI spooler copies the attachment data into an **ATTACH_BY_VALUE** attachment.</span></span> <span data-ttu-id="af58e-142">この解決プロセスでは、添付ファイル データを **PR_ATTACH_DATA_BIN。**</span><span class="sxs-lookup"><span data-stu-id="af58e-142">This resolution process places the attachment data in **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="af58e-143">この **ATTACH_BY_REF_ONLY** 設定されている **場合、PR_ATTACH_DATA_BIN** は空にする必要があります。メッセージング システムは添付ファイル参照を解決しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="af58e-143">If **ATTACH_BY_REF_ONLY** is set, **PR_ATTACH_DATA_BIN** must be empty, and the messaging system never resolves the attachment reference.</span></span> <span data-ttu-id="af58e-144">この値は、データではなくリンクを送信する場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="af58e-144">Use this value when you want to send the link but not the data.</span></span> 
  
<span data-ttu-id="af58e-145">OLE オブジェクトが OLE 2.0 **IStorage** 形式の場合、データにアクセスするには、次の **PR_ATTACH_DATA_OBJ。**</span><span class="sxs-lookup"><span data-stu-id="af58e-145">When the OLE object is in OLE 2.0 **IStorage** format, the data is accessible through **PR_ATTACH_DATA_OBJ**.</span></span> <span data-ttu-id="af58e-146">OLE オブジェクトが OLE 1.0 **OLESTREAM** 形式の場合、データには IStream **PR_ATTACH_DATA_BINを使用\*\*\*\*してアクセスできます**。</span><span class="sxs-lookup"><span data-stu-id="af58e-146">When the OLE object is in OLE 1.0 **OLESTREAM** format, the data is accessible through **PR_ATTACH_DATA_BIN** as an **IStream**.</span></span> <span data-ttu-id="af58e-147">OLE エンコードの種類は、次の値 [(PidTagAttachTag)](pidtagattachtag-canonical-property.md) **PR_ATTACH_TAGによって決** まります。</span><span class="sxs-lookup"><span data-stu-id="af58e-147">The type of the OLE encoding can be determined by the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) value.</span></span> 
  
<span data-ttu-id="af58e-148">OLE インターフェイスと形式の詳細については  *、「OLE プログラマリファレンス」を参照してください*  。</span><span class="sxs-lookup"><span data-stu-id="af58e-148">For more information on OLE interfaces and formats, see the  *OLE Programmer's Reference*  .</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="af58e-149">注釈</span><span class="sxs-lookup"><span data-stu-id="af58e-149">Remarks</span></span>

<span data-ttu-id="af58e-150">メッセージが **PR_ATTACH_METHOD** 場合 **ATTACH_BY_WEBREFERENCE** 添付ファイルのコンテンツはメッセージに含めされません。</span><span class="sxs-lookup"><span data-stu-id="af58e-150">When the **PR_ATTACH_METHOD** is **ATTACH_BY_WEBREFERENCE**, the attachment content is not in the message.</span></span> <span data-ttu-id="af58e-151">代わりに **、PR_ATTACH_LONG_FILENAME** プロパティには、添付ファイルコンテンツの絶対 URL が含まれるので、オンラインで保存されます。</span><span class="sxs-lookup"><span data-stu-id="af58e-151">Instead, the **PR_ATTACH_LONG_FILENAME** property contains an absolute URL to the attachment content, which is stored online.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="af58e-152">関連リソース</span><span class="sxs-lookup"><span data-stu-id="af58e-152">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="af58e-153">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="af58e-153">Protocol specifications</span></span>

<span data-ttu-id="af58e-154">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af58e-154">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af58e-155">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="af58e-155">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="af58e-156">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="af58e-156">Header files</span></span>

<span data-ttu-id="af58e-157">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="af58e-157">Mapidefs.h</span></span>
  
> <span data-ttu-id="af58e-158">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="af58e-158">Provides data type definitions.</span></span>
    
<span data-ttu-id="af58e-159">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="af58e-159">Mapitags.h</span></span>
  
> <span data-ttu-id="af58e-160">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="af58e-160">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="af58e-161">関連項目</span><span class="sxs-lookup"><span data-stu-id="af58e-161">See also</span></span>



[<span data-ttu-id="af58e-162">PidTagStoreSupportMask 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="af58e-162">PidTagStoreSupportMask Canonical Property</span></span>](pidtagstoresupportmask-canonical-property.md)


[<span data-ttu-id="af58e-163">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="af58e-163">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="af58e-164">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="af58e-164">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="af58e-165">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="af58e-165">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="af58e-166">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="af58e-166">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

