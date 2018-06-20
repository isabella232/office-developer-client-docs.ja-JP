---
title: PidLidAutoProcessState の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAutoProcessState
api_type:
- COM
ms.assetid: 9e724af6-5b56-4eb3-a94c-1015ebce197c
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 86ef98ac7b4084de3a96210298fe0d5509d12103
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801822"
---
# <a name="pidlidautoprocessstate-canonical-property"></a><span data-ttu-id="7acf4-103">PidLidAutoProcessState の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="7acf4-103">PidLidAutoProcessState Canonical Property</span></span>

  
  
<span data-ttu-id="7acf4-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7acf4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7acf4-105">電子メール メッセージの自動処理で使用されるオプションを指定します。</span><span class="sxs-lookup"><span data-stu-id="7acf4-105">Specifies the options that are used in automatic processing of email messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7acf4-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="7acf4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7acf4-107">dispidSniffState</span><span class="sxs-lookup"><span data-stu-id="7acf4-107">dispidSniffState</span></span>  <br/> |
|<span data-ttu-id="7acf4-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="7acf4-108">Property set:</span></span>  <br/> |<span data-ttu-id="7acf4-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="7acf4-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="7acf4-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="7acf4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7acf4-111">0x0000851A</span><span class="sxs-lookup"><span data-stu-id="7acf4-111">0x0000851A</span></span>  <br/> |
|<span data-ttu-id="7acf4-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="7acf4-112">Data type:</span></span>  <br/> |<span data-ttu-id="7acf4-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7acf4-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7acf4-114">領域:</span><span class="sxs-lookup"><span data-stu-id="7acf4-114">Area:</span></span>  <br/> |<span data-ttu-id="7acf4-115">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="7acf4-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7acf4-116">備考</span><span class="sxs-lookup"><span data-stu-id="7acf4-116">Remarks</span></span>

<span data-ttu-id="7acf4-117">プロパティは"0x00000000"の既定値を使用する場合に入力が失われている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7acf4-117">The property may be absent, in which case the default value of "0x00000000" is used.</span></span> <span data-ttu-id="7acf4-118">設定するとこのプロパティに次の表の値のいずれかに設定します。</span><span class="sxs-lookup"><span data-stu-id="7acf4-118">If set, this property must be set to one of the values in the following table.</span></span>
  
|<span data-ttu-id="7acf4-119">**値**</span><span class="sxs-lookup"><span data-stu-id="7acf4-119">**Value**</span></span>|<span data-ttu-id="7acf4-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="7acf4-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7acf4-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7acf4-121">0x00000000</span></span>  <br/> |<span data-ttu-id="7acf4-122">メッセージを自動的に処理しません。</span><span class="sxs-lookup"><span data-stu-id="7acf4-122">Do not automatically process the message.</span></span>  <br/> |
|<span data-ttu-id="7acf4-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7acf4-123">0x00000001</span></span>  <br/> |<span data-ttu-id="7acf4-124">メッセージを自動的に処理するか、メッセージを開いたとき。</span><span class="sxs-lookup"><span data-stu-id="7acf4-124">Process the message automatically or when the message is opened.</span></span>  <br/> |
|<span data-ttu-id="7acf4-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="7acf4-125">0x00000002</span></span>  <br/> |<span data-ttu-id="7acf4-126">メッセージを開いたときにのみメッセージを処理します。</span><span class="sxs-lookup"><span data-stu-id="7acf4-126">Process the message only when the message is opened.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="7acf4-127">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7acf4-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7acf4-128">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7acf4-128">Protocol specifications</span></span>

<span data-ttu-id="7acf4-129">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7acf4-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7acf4-130">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="7acf4-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7acf4-131">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7acf4-131">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7acf4-132">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="7acf4-132">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7acf4-133">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="7acf4-133">Header files</span></span>

<span data-ttu-id="7acf4-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7acf4-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="7acf4-135">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7acf4-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7acf4-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="7acf4-136">See also</span></span>



[<span data-ttu-id="7acf4-137">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7acf4-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7acf4-138">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7acf4-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7acf4-139">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="7acf4-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7acf4-140">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="7acf4-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

