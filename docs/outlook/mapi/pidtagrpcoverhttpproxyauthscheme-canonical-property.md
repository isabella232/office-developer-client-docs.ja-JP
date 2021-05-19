---
title: PidTagRpcOverHttpProxyAuthScheme 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6da78f1a-6423-460c-b3a9-fd6441df9cef
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ea4b90bf1190fd71701f82d43aaee384c7987ed0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331312"
---
# <a name="pidtagrpcoverhttpproxyauthscheme-canonical-property"></a><span data-ttu-id="bd1e8-103">PidTagRpcOverHttpProxyAuthScheme 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bd1e8-103">PidTagRpcOverHttpProxyAuthScheme Canonical Property</span></span>

  
  
<span data-ttu-id="bd1e8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd1e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd1e8-105">このプロファイルに使用する認証プロトコルを表します。</span><span class="sxs-lookup"><span data-stu-id="bd1e8-105">Represents the authentication protocol to be used for this profile.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bd1e8-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="bd1e8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bd1e8-107">PR_ROH_PROXY_AUTH_SCHEME</span><span class="sxs-lookup"><span data-stu-id="bd1e8-107">PR_ROH_PROXY_AUTH_SCHEME</span></span>  <br/> |
|<span data-ttu-id="bd1e8-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="bd1e8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bd1e8-109">0x6627</span><span class="sxs-lookup"><span data-stu-id="bd1e8-109">0x6627</span></span>  <br/> |
|<span data-ttu-id="bd1e8-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="bd1e8-110">Data type:</span></span>  <br/> |<span data-ttu-id="bd1e8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="bd1e8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="bd1e8-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="bd1e8-112">Area:</span></span>  <br/> |<span data-ttu-id="bd1e8-113">その他</span><span class="sxs-lookup"><span data-stu-id="bd1e8-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd1e8-114">注釈</span><span class="sxs-lookup"><span data-stu-id="bd1e8-114">Remarks</span></span>

<span data-ttu-id="bd1e8-115">このプロパティは、基本認証または NT LAN Manager (NTLM) 認証に対して設定できます。</span><span class="sxs-lookup"><span data-stu-id="bd1e8-115">This property can be set for either basic authentication or NT LAN Manager (NTLM) authentication.</span></span> <span data-ttu-id="bd1e8-116">このプロパティに使用できる値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="bd1e8-116">The possible values for this property are as follow.</span></span>
  
|<span data-ttu-id="bd1e8-117">**名前**</span><span class="sxs-lookup"><span data-stu-id="bd1e8-117">**Name**</span></span>|<span data-ttu-id="bd1e8-118">**値**</span><span class="sxs-lookup"><span data-stu-id="bd1e8-118">**Value**</span></span>|<span data-ttu-id="bd1e8-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="bd1e8-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bd1e8-120">**ROHAUTH_BASIC**</span><span class="sxs-lookup"><span data-stu-id="bd1e8-120">**ROHAUTH_BASIC**</span></span> <br/> |<span data-ttu-id="bd1e8-121">0x1</span><span class="sxs-lookup"><span data-stu-id="bd1e8-121">0x1</span></span>  <br/> |<span data-ttu-id="bd1e8-122">基本認証</span><span class="sxs-lookup"><span data-stu-id="bd1e8-122">Basic authentication</span></span>  <br/> |
|<span data-ttu-id="bd1e8-123">**ROHAUTH_NTLM**</span><span class="sxs-lookup"><span data-stu-id="bd1e8-123">**ROHAUTH_NTLM**</span></span> <br/> |<span data-ttu-id="bd1e8-124">0x2</span><span class="sxs-lookup"><span data-stu-id="bd1e8-124">0x2</span></span>  <br/> |<span data-ttu-id="bd1e8-125">NTLM 認証</span><span class="sxs-lookup"><span data-stu-id="bd1e8-125">NTLM authentication</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="bd1e8-126">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bd1e8-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bd1e8-127">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="bd1e8-127">Protocol specifications</span></span>

<span data-ttu-id="bd1e8-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd1e8-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd1e8-129">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="bd1e8-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bd1e8-130">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd1e8-130">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd1e8-131">リモート操作で使用される基本的なデータ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="bd1e8-131">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="bd1e8-132">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd1e8-132">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd1e8-133">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="bd1e8-133">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bd1e8-134">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="bd1e8-134">Header files</span></span>

<span data-ttu-id="bd1e8-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bd1e8-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="bd1e8-136">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bd1e8-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="bd1e8-137">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bd1e8-137">Mapitags.h</span></span>
  
> <span data-ttu-id="bd1e8-138">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="bd1e8-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bd1e8-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="bd1e8-139">See also</span></span>



[<span data-ttu-id="bd1e8-140">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="bd1e8-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bd1e8-141">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bd1e8-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bd1e8-142">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="bd1e8-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bd1e8-143">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="bd1e8-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

