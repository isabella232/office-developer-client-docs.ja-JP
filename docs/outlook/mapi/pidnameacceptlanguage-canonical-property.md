---
title: PidNameAcceptLanguage の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameAcceptLanguage
api_type:
- COM
ms.assetid: 4b202bc1-f718-446a-950f-634ffee47baf
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: d2c2fb31b722e76034b08077632c817d6adde802
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802301"
---
# <a name="pidnameacceptlanguage-canonical-property"></a><span data-ttu-id="4125c-103">PidNameAcceptLanguage の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="4125c-103">PidNameAcceptLanguage Canonical Property</span></span>

  
  
<span data-ttu-id="4125c-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4125c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4125c-105">[RFC3282] Accept-language ヘッダー フィールドの値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4125c-105">Contains an [RFC3282] Accept-Language header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4125c-106">フレンドリ名:</span><span class="sxs-lookup"><span data-stu-id="4125c-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="4125c-107">AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="4125c-107">AcceptLanguage</span></span>  <br/> |
|<span data-ttu-id="4125c-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="4125c-108">Property set:</span></span>  <br/> |<span data-ttu-id="4125c-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="4125c-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="4125c-110">プロパティ名:</span><span class="sxs-lookup"><span data-stu-id="4125c-110">Property name:</span></span>  <br/> |<span data-ttu-id="4125c-111">Accept-Language</span><span class="sxs-lookup"><span data-stu-id="4125c-111">Accept-Language</span></span>  <br/> |
|<span data-ttu-id="4125c-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="4125c-112">Data type:</span></span>  <br/> |<span data-ttu-id="4125c-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4125c-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4125c-114">領域:</span><span class="sxs-lookup"><span data-stu-id="4125c-114">Area:</span></span>  <br/> |<span data-ttu-id="4125c-115">Email</span><span class="sxs-lookup"><span data-stu-id="4125c-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4125c-116">備考</span><span class="sxs-lookup"><span data-stu-id="4125c-116">Remarks</span></span>

<span data-ttu-id="4125c-117">このプロパティの値を設定するには、多目的のインターネット メッセージの拡張機能 (MIME) クライアントが目的の値を持つ、Accept-language ヘッダー フィールドを記述しておきます。</span><span class="sxs-lookup"><span data-stu-id="4125c-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients should write an Accept-Language header field with the desired value.</span></span> <span data-ttu-id="4125c-118">MIME クライアントでは、X-ブラウザーの言語のヘッダー フィールドを代わりに書き込むことがあります。</span><span class="sxs-lookup"><span data-stu-id="4125c-118">MIME clients may write an X-Accept-Language header field instead.</span></span> <span data-ttu-id="4125c-119">MIME のリーダーは、このプロパティの値をいずれかのヘッダー フィールドの値をコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4125c-119">MIME readers should copy the value of either header field to the value of this property.</span></span> <span data-ttu-id="4125c-120">両方のヘッダー フィールドが存在する場合は、MIME のリーダーは、Accept-language ヘッダー フィールドを使用してください。</span><span class="sxs-lookup"><span data-stu-id="4125c-120">If both header fields are present, MIME readers should use the Accept-Language header field.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4125c-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4125c-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4125c-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="4125c-122">Protocol specifications</span></span>

<span data-ttu-id="4125c-123">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4125c-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4125c-124">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="4125c-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4125c-125">[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4125c-125">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4125c-126">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="4125c-126">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4125c-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="4125c-127">Header files</span></span>

<span data-ttu-id="4125c-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4125c-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="4125c-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4125c-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4125c-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="4125c-130">See also</span></span>



[<span data-ttu-id="4125c-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4125c-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4125c-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4125c-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4125c-133">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="4125c-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4125c-134">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="4125c-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

