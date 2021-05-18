---
title: PidNameAcceptLanguage 標準プロパティ
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 855610c43cfaa64fa69e6987743b137b188d84a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360943"
---
# <a name="pidnameacceptlanguage-canonical-property"></a><span data-ttu-id="60224-103">PidNameAcceptLanguage 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="60224-103">PidNameAcceptLanguage Canonical Property</span></span>

  
  
<span data-ttu-id="60224-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60224-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60224-105">[RFC3282] ヘッダー フィールドAccept-Language含まれています。</span><span class="sxs-lookup"><span data-stu-id="60224-105">Contains an [RFC3282] Accept-Language header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="60224-106">分名:</span><span class="sxs-lookup"><span data-stu-id="60224-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="60224-107">AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="60224-107">AcceptLanguage</span></span>  <br/> |
|<span data-ttu-id="60224-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="60224-108">Property set:</span></span>  <br/> |<span data-ttu-id="60224-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="60224-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="60224-110">プロパティ名:</span><span class="sxs-lookup"><span data-stu-id="60224-110">Property name:</span></span>  <br/> |<span data-ttu-id="60224-111">Accept-Language</span><span class="sxs-lookup"><span data-stu-id="60224-111">Accept-Language</span></span>  <br/> |
|<span data-ttu-id="60224-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="60224-112">Data type:</span></span>  <br/> |<span data-ttu-id="60224-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="60224-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="60224-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="60224-114">Area:</span></span>  <br/> |<span data-ttu-id="60224-115">メール</span><span class="sxs-lookup"><span data-stu-id="60224-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="60224-116">注釈</span><span class="sxs-lookup"><span data-stu-id="60224-116">Remarks</span></span>

<span data-ttu-id="60224-117">このプロパティの値を設定するには、Multipurpose Internet Message Extensions (MIME) クライアントは、目的の値を持つ Accept-Language ヘッダー フィールドを記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60224-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients should write an Accept-Language header field with the desired value.</span></span> <span data-ttu-id="60224-118">MIME クライアントは、代わりに X-Accept-Language ヘッダー フィールドを書き込む場合があります。</span><span class="sxs-lookup"><span data-stu-id="60224-118">MIME clients may write an X-Accept-Language header field instead.</span></span> <span data-ttu-id="60224-119">MIME リーダーは、いずれかのヘッダー フィールドの値をこのプロパティの値にコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="60224-119">MIME readers should copy the value of either header field to the value of this property.</span></span> <span data-ttu-id="60224-120">両方のヘッダー フィールドが存在する場合、MIME リーダーはヘッダー フィールドのAccept-Language使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60224-120">If both header fields are present, MIME readers should use the Accept-Language header field.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="60224-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="60224-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="60224-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="60224-122">Protocol specifications</span></span>

<span data-ttu-id="60224-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="60224-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="60224-124">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="60224-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="60224-125">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="60224-125">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="60224-126">インターネット標準の電子メール規則からメッセージ オブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="60224-126">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="60224-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="60224-127">Header files</span></span>

<span data-ttu-id="60224-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="60224-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="60224-129">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="60224-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="60224-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="60224-130">See also</span></span>



[<span data-ttu-id="60224-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="60224-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="60224-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="60224-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="60224-133">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="60224-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="60224-134">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="60224-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

