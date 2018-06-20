---
title: PidTagAttachPayloadProviderGuidString の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPayloadProviderGuidString
api_type:
- HeaderDef
ms.assetid: c9d4b561-53b3-492b-9324-9376dd7abddf
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 9e581f040b3d7d9e204dd41431b1eba650b971a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802494"
---
# <a name="pidtagattachpayloadproviderguidstring-canonical-property"></a><span data-ttu-id="2afa9-103">PidTagAttachPayloadProviderGuidString の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="2afa9-103">PidTagAttachPayloadProviderGuidString Canonical Property</span></span>

  
  
<span data-ttu-id="2afa9-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2afa9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2afa9-105">MIME X ・ ペイロード ・ プロバイダーの Guid のヘッダー フィールドの値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2afa9-105">Contains the value of a MIME X-Payload-Provider-Guid header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2afa9-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="2afa9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2afa9-107">PR_ATTACH_PAYLOAD_PROV_GUID_STR、PR_ATTACH_PAYLOAD_PROV_GUID_STR_A、PR_ATTACH_PAYLOAD_PROV_GUID_STR_W</span><span class="sxs-lookup"><span data-stu-id="2afa9-107">PR_ATTACH_PAYLOAD_PROV_GUID_STR, PR_ATTACH_PAYLOAD_PROV_GUID_STR_A, PR_ATTACH_PAYLOAD_PROV_GUID_STR_W</span></span>  <br/> |
|<span data-ttu-id="2afa9-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="2afa9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2afa9-109">0x3719</span><span class="sxs-lookup"><span data-stu-id="2afa9-109">0x3719</span></span>  <br/> |
|<span data-ttu-id="2afa9-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="2afa9-110">Data type:</span></span>  <br/> |<span data-ttu-id="2afa9-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2afa9-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2afa9-112">領域:</span><span class="sxs-lookup"><span data-stu-id="2afa9-112">Area:</span></span>  <br/> |<span data-ttu-id="2afa9-113">Outlook アプリケーション</span><span class="sxs-lookup"><span data-stu-id="2afa9-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2afa9-114">備考</span><span class="sxs-lookup"><span data-stu-id="2afa9-114">Remarks</span></span>

<span data-ttu-id="2afa9-115">これらのプロパティの値を設定するのには MIME クライアントは、添付ファイルとして解析される MIME エンティティに X のペイロード ・ プロバイダーの Guid のヘッダー フィールドを記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2afa9-115">To set the value of these properties, MIME clients should write an X-Payload-Provider-Guid header field to a MIME entity that will be analyzed as an attachment.</span></span>
  
<span data-ttu-id="2afa9-116">MIME のリーダーでは、このヘッダー フィールドの値を対応するプロパティの値にコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2afa9-116">MIME readers must copy this header field value to the value of the corresponding property.</span></span> <span data-ttu-id="2afa9-117">MIME のリーダーは、添付ファイルとしてではなく、メッセージまたはメッセージの本文として分析する MIME エンティティ上に表示されるとき、このヘッダー フィールドを無視してください。</span><span class="sxs-lookup"><span data-stu-id="2afa9-117">MIME readers should ignore this header field when it appears on a MIME entity that is analyzed as a message or message body, rather than as an attachment.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2afa9-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2afa9-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2afa9-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="2afa9-119">Protocol specifications</span></span>

<span data-ttu-id="2afa9-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2afa9-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2afa9-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="2afa9-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2afa9-122">[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2afa9-122">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2afa9-123">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="2afa9-123">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2afa9-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="2afa9-124">Header files</span></span>

<span data-ttu-id="2afa9-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2afa9-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="2afa9-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2afa9-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="2afa9-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2afa9-127">Mapitags.h</span></span>
  
> <span data-ttu-id="2afa9-128">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2afa9-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2afa9-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="2afa9-129">See also</span></span>



[<span data-ttu-id="2afa9-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2afa9-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2afa9-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2afa9-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2afa9-132">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="2afa9-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2afa9-133">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="2afa9-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

