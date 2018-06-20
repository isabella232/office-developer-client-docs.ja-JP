---
title: PidTagInternetReturnPath の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: aa8a683c0033682aa46944c5cc78503dc1a7d729
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802879"
---
# <a name="pidtaginternetreturnpath-canonical-property"></a><span data-ttu-id="f9ab4-103">PidTagInternetReturnPath の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="f9ab4-103">PidTagInternetReturnPath Canonical Property</span></span>

  
  
<span data-ttu-id="f9ab4-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f9ab4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f9ab4-105">多目的インターネット メール拡張 (MIME) メッセージのリターン ・ パスのヘッダー フィールドの値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f9ab4-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's Return-Path header field.</span></span> <span data-ttu-id="f9ab4-106">メッセージの送信者の電子メール アドレスです。</span><span class="sxs-lookup"><span data-stu-id="f9ab4-106">The email address of the message's sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f9ab4-107">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="f9ab4-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="f9ab4-108">PR_INTERNET_RETURN_PATH、PR_INTERNET_RETURN_PATH_A、PR_INTERNET_RETURN_PATH_W</span><span class="sxs-lookup"><span data-stu-id="f9ab4-108">PR_INTERNET_RETURN_PATH, PR_INTERNET_RETURN_PATH_A, PR_INTERNET_RETURN_PATH_W</span></span>  <br/> |
|<span data-ttu-id="f9ab4-109">識別子:</span><span class="sxs-lookup"><span data-stu-id="f9ab4-109">Identifier:</span></span>  <br/> |<span data-ttu-id="f9ab4-110">0x1046</span><span class="sxs-lookup"><span data-stu-id="f9ab4-110">0x1046</span></span>  <br/> |
|<span data-ttu-id="f9ab4-111">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="f9ab4-111">Data type:</span></span>  <br/> |<span data-ttu-id="f9ab4-112">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f9ab4-112">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f9ab4-113">領域:</span><span class="sxs-lookup"><span data-stu-id="f9ab4-113">Area:</span></span>  <br/> |<span data-ttu-id="f9ab4-114">MIME</span><span class="sxs-lookup"><span data-stu-id="f9ab4-114">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f9ab4-115">備考</span><span class="sxs-lookup"><span data-stu-id="f9ab4-115">Remarks</span></span>

<span data-ttu-id="f9ab4-116">このプロパティの値を取得するには、まず[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を使用して、プロパティ タグを取得して値を取得する[IMAPIProp::GetProps](imapiprop-getprops.md)でこのプロパティのタグを指定します。</span><span class="sxs-lookup"><span data-stu-id="f9ab4-116">To retrieve the value of this property, first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="f9ab4-117">[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を呼び出すときは、 _lppPropNames_の入力パラメーターで示される[MAPINAMEID](mapinameid.md)構造体の次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="f9ab4-117">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f9ab4-118">lpGuid。</span><span class="sxs-lookup"><span data-stu-id="f9ab4-118">lpGuid:</span></span>  <br/> |<span data-ttu-id="f9ab4-119">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="f9ab4-119">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="f9ab4-120">ulKind。</span><span class="sxs-lookup"><span data-stu-id="f9ab4-120">ulKind:</span></span>  <br/> |<span data-ttu-id="f9ab4-121">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="f9ab4-121">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="f9ab4-122">Kind.lpwstrName。</span><span class="sxs-lookup"><span data-stu-id="f9ab4-122">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="f9ab4-123">L「リターン ・ パス」</span><span class="sxs-lookup"><span data-stu-id="f9ab4-123">L"return-path"</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="f9ab4-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f9ab4-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f9ab4-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f9ab4-125">Protocol specifications</span></span>

<span data-ttu-id="f9ab4-126">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f9ab4-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f9ab4-127">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="f9ab4-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f9ab4-128">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f9ab4-128">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f9ab4-129">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="f9ab4-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f9ab4-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f9ab4-130">Header files</span></span>

<span data-ttu-id="f9ab4-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f9ab4-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="f9ab4-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f9ab4-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="f9ab4-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f9ab4-133">Mapitags.h</span></span>
  
> <span data-ttu-id="f9ab4-134">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f9ab4-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f9ab4-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="f9ab4-135">See also</span></span>



[<span data-ttu-id="f9ab4-136">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f9ab4-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f9ab4-137">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="f9ab4-137">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="f9ab4-138">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f9ab4-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f9ab4-139">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="f9ab4-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f9ab4-140">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="f9ab4-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

