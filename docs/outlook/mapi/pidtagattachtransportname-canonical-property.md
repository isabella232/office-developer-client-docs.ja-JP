---
title: PidTagAttachTransportName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachTransportName
api_type:
- HeaderDef
ms.assetid: 701fca52-0f96-4019-80cd-c0ccd059ff9b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6828a6436946de27020fa1177223955e07a08faf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802507"
---
# <a name="pidtagattachtransportname-canonical-property"></a><span data-ttu-id="d5bb6-103">PidTagAttachTransportName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d5bb6-103">PidTagAttachTransportName Canonical Property</span></span>

  
  
<span data-ttu-id="d5bb6-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d5bb6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d5bb6-105">TNEF メッセージに関連付けられるように変更された添付ファイルの名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d5bb6-105">Contains the name of an attachment file modified so that it can be associated with TNEF messages.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d5bb6-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d5bb6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d5bb6-107">PR_ATTACH_TRANSPORT_NAME、PR_ATTACH_TRANSPORT_NAME_A、PR_ATTACH_TRANSPORT_NAME_W</span><span class="sxs-lookup"><span data-stu-id="d5bb6-107">PR_ATTACH_TRANSPORT_NAME, PR_ATTACH_TRANSPORT_NAME_A, PR_ATTACH_TRANSPORT_NAME_W</span></span>  <br/> |
|<span data-ttu-id="d5bb6-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d5bb6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d5bb6-109">0x370C</span><span class="sxs-lookup"><span data-stu-id="d5bb6-109">0x370C</span></span>  <br/> |
|<span data-ttu-id="d5bb6-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d5bb6-110">Data type:</span></span>  <br/> |<span data-ttu-id="d5bb6-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d5bb6-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d5bb6-112">領域:</span><span class="sxs-lookup"><span data-stu-id="d5bb6-112">Area:</span></span>  <br/> |<span data-ttu-id="d5bb6-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="d5bb6-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d5bb6-114">注釈</span><span class="sxs-lookup"><span data-stu-id="d5bb6-114">Remarks</span></span>

<span data-ttu-id="d5bb6-115">TNEF およびトランスポート プロバイダーは、これらのプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="d5bb6-115">TNEF and the transport provider use these properties.</span></span> <span data-ttu-id="d5bb6-116">通常クライアント アプリケーションで使用します。</span><span class="sxs-lookup"><span data-stu-id="d5bb6-116">They are usually not available to client applications.</span></span> 
  
<span data-ttu-id="d5bb6-117">これらのプロパティは、基になるメッセージング システムでは、指定されたファイル名をサポートしていない場合、TNEF で通常使用されます。</span><span class="sxs-lookup"><span data-stu-id="d5bb6-117">These properties are commonly used by TNEF when the underlying messaging system does not support the supplied filenames.</span></span> <span data-ttu-id="d5bb6-118">などのユーザー設定を名前付きの 5 つのファイルなど、同じ名前の複数のファイルを添付するときに使用します。SYS です。</span><span class="sxs-lookup"><span data-stu-id="d5bb6-118">For example, they are used when the user attaches multiple files with the same name, such as five files named CONFIG.SYS.</span></span> <span data-ttu-id="d5bb6-119">トランスポート プロバイダーは、一意であるかどうかを確認するのには名前を変更しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="d5bb6-119">The transport provider must modify the names to make sure they are unique.</span></span> <span data-ttu-id="d5bb6-120">各変更後の名前は、その添付ファイルの**PR_ATTACH_TRANSPORT_NAME**および関連付けられたプロパティに表示されます。</span><span class="sxs-lookup"><span data-stu-id="d5bb6-120">Each modified name appears in its attachment's **PR_ATTACH_TRANSPORT_NAME** and associated properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d5bb6-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d5bb6-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d5bb6-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d5bb6-122">Protocol specifications</span></span>

<span data-ttu-id="d5bb6-123">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5bb6-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d5bb6-124">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="d5bb6-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d5bb6-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d5bb6-125">Header files</span></span>

<span data-ttu-id="d5bb6-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d5bb6-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="d5bb6-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d5bb6-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="d5bb6-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d5bb6-128">Mapitags.h</span></span>
  
> <span data-ttu-id="d5bb6-129">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d5bb6-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d5bb6-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="d5bb6-130">See also</span></span>



[<span data-ttu-id="d5bb6-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d5bb6-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d5bb6-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d5bb6-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d5bb6-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d5bb6-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d5bb6-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d5bb6-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

