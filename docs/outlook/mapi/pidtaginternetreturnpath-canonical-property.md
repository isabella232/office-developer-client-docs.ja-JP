---
title: PidTagInternetReturnPath 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInternetReturnPath
api_type:
- HeaderDef
ms.assetid: 4530dbcf-9436-4f29-b79e-1bb0f791f60b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c2d8eaf627f789c3e862a83d71e4ca2e3e55e1e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327959"
---
# <a name="pidtaginternetreturnpath-canonical-property"></a><span data-ttu-id="2098a-103">PidTagInternetReturnPath 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2098a-103">PidTagInternetReturnPath Canonical Property</span></span>

  
  
<span data-ttu-id="2098a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2098a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2098a-105">多目的インターネット メール拡張機能 (MIME) メッセージのヘッダー フィールドの値Return-Pathします。</span><span class="sxs-lookup"><span data-stu-id="2098a-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's Return-Path header field.</span></span> <span data-ttu-id="2098a-106">メッセージの送信者の電子メール アドレス。</span><span class="sxs-lookup"><span data-stu-id="2098a-106">The email address of the message's sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2098a-107">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2098a-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="2098a-108">PR_INTERNET_RETURN_PATH、PR_INTERNET_RETURN_PATH_A、PR_INTERNET_RETURN_PATH_W</span><span class="sxs-lookup"><span data-stu-id="2098a-108">PR_INTERNET_RETURN_PATH, PR_INTERNET_RETURN_PATH_A, PR_INTERNET_RETURN_PATH_W</span></span>  <br/> |
|<span data-ttu-id="2098a-109">識別子:</span><span class="sxs-lookup"><span data-stu-id="2098a-109">Identifier:</span></span>  <br/> |<span data-ttu-id="2098a-110">0x1046</span><span class="sxs-lookup"><span data-stu-id="2098a-110">0x1046</span></span>  <br/> |
|<span data-ttu-id="2098a-111">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2098a-111">Data type:</span></span>  <br/> |<span data-ttu-id="2098a-112">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2098a-112">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2098a-113">エリア:</span><span class="sxs-lookup"><span data-stu-id="2098a-113">Area:</span></span>  <br/> |<span data-ttu-id="2098a-114">MIME</span><span class="sxs-lookup"><span data-stu-id="2098a-114">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2098a-115">注釈</span><span class="sxs-lookup"><span data-stu-id="2098a-115">Remarks</span></span>

<span data-ttu-id="2098a-116">このプロパティの値を取得するには、まず [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) を使用してプロパティ タグを取得し [、IMAPIProp::GetProps](imapiprop-getprops.md) でこのプロパティ タグを指定して値を取得します。</span><span class="sxs-lookup"><span data-stu-id="2098a-116">To retrieve the value of this property, first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="2098a-117">[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を呼び出す場合は、入力パラメーター _lppPropNames_ が指す [MAPINAMEID](mapinameid.md)構造体に次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="2098a-117">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2098a-118">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="2098a-118">lpGuid:</span></span>  <br/> |<span data-ttu-id="2098a-119">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="2098a-119">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="2098a-120">ulKind:</span><span class="sxs-lookup"><span data-stu-id="2098a-120">ulKind:</span></span>  <br/> |<span data-ttu-id="2098a-121">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="2098a-121">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="2098a-122">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="2098a-122">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="2098a-123">L"return-path"</span><span class="sxs-lookup"><span data-stu-id="2098a-123">L"return-path"</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="2098a-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2098a-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2098a-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="2098a-125">Protocol specifications</span></span>

<span data-ttu-id="2098a-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2098a-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2098a-127">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="2098a-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2098a-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2098a-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2098a-129">IETF RFC2445、RFC2446、RFC2447、および予定オブジェクトと会議オブジェクトの間で変換します。</span><span class="sxs-lookup"><span data-stu-id="2098a-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2098a-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="2098a-130">Header files</span></span>

<span data-ttu-id="2098a-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2098a-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="2098a-132">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2098a-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="2098a-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2098a-133">Mapitags.h</span></span>
  
> <span data-ttu-id="2098a-134">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="2098a-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2098a-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="2098a-135">See also</span></span>



[<span data-ttu-id="2098a-136">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="2098a-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2098a-137">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="2098a-137">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="2098a-138">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2098a-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2098a-139">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="2098a-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2098a-140">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="2098a-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

