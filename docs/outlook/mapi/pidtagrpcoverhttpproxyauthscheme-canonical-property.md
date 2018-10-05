---
title: PidTagRpcOverHttpProxyAuthScheme 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6da78f1a-6423-460c-b3a9-fd6441df9cef
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ea4b90bf1190fd71701f82d43aaee384c7987ed0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387196"
---
# <a name="pidtagrpcoverhttpproxyauthscheme-canonical-property"></a><span data-ttu-id="66353-103">PidTagRpcOverHttpProxyAuthScheme 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="66353-103">PidTagRpcOverHttpProxyAuthScheme Canonical Property</span></span>

  
  
<span data-ttu-id="66353-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66353-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66353-105">このプロファイルに使用する認証プロトコルを表します。</span><span class="sxs-lookup"><span data-stu-id="66353-105">Represents the authentication protocol to be used for this profile.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="66353-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="66353-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="66353-107">PR_ROH_PROXY_AUTH_SCHEME</span><span class="sxs-lookup"><span data-stu-id="66353-107">PR_ROH_PROXY_AUTH_SCHEME</span></span>  <br/> |
|<span data-ttu-id="66353-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="66353-108">Identifier:</span></span>  <br/> |<span data-ttu-id="66353-109">0x6627</span><span class="sxs-lookup"><span data-stu-id="66353-109">0x6627</span></span>  <br/> |
|<span data-ttu-id="66353-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="66353-110">Data type:</span></span>  <br/> |<span data-ttu-id="66353-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="66353-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="66353-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="66353-112">Area:</span></span>  <br/> |<span data-ttu-id="66353-113">その他</span><span class="sxs-lookup"><span data-stu-id="66353-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66353-114">備考</span><span class="sxs-lookup"><span data-stu-id="66353-114">Remarks</span></span>

<span data-ttu-id="66353-115">このプロパティは、基本認証または NT LAN マネージャー (NTLM) 認証のいずれかを設定できます。</span><span class="sxs-lookup"><span data-stu-id="66353-115">This property can be set for either basic authentication or NT LAN Manager (NTLM) authentication.</span></span> <span data-ttu-id="66353-116">このプロパティの有効な値は、次のような。</span><span class="sxs-lookup"><span data-stu-id="66353-116">The possible values for this property are as follow.</span></span>
  
|<span data-ttu-id="66353-117">**名前**</span><span class="sxs-lookup"><span data-stu-id="66353-117">**Name**</span></span>|<span data-ttu-id="66353-118">**値**</span><span class="sxs-lookup"><span data-stu-id="66353-118">**Value**</span></span>|<span data-ttu-id="66353-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="66353-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="66353-120">**ROHAUTH_BASIC**</span><span class="sxs-lookup"><span data-stu-id="66353-120">**ROHAUTH_BASIC**</span></span> <br/> |<span data-ttu-id="66353-121">0x1</span><span class="sxs-lookup"><span data-stu-id="66353-121">0x1</span></span>  <br/> |<span data-ttu-id="66353-122">基本認証</span><span class="sxs-lookup"><span data-stu-id="66353-122">Basic authentication</span></span>  <br/> |
|<span data-ttu-id="66353-123">**ROHAUTH_NTLM**</span><span class="sxs-lookup"><span data-stu-id="66353-123">**ROHAUTH_NTLM**</span></span> <br/> |<span data-ttu-id="66353-124">0x2</span><span class="sxs-lookup"><span data-stu-id="66353-124">0x2</span></span>  <br/> |<span data-ttu-id="66353-125">NTLM 認証</span><span class="sxs-lookup"><span data-stu-id="66353-125">NTLM authentication</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="66353-126">関連リソース</span><span class="sxs-lookup"><span data-stu-id="66353-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="66353-127">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="66353-127">Protocol specifications</span></span>

<span data-ttu-id="66353-128">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="66353-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="66353-129">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="66353-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="66353-130">[[MS OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="66353-130">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="66353-131">リモート操作で使用される基本的なデータ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="66353-131">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="66353-132">[[MS OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="66353-132">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="66353-133">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="66353-133">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="66353-134">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="66353-134">Header files</span></span>

<span data-ttu-id="66353-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="66353-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="66353-136">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="66353-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="66353-137">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="66353-137">Mapitags.h</span></span>
  
> <span data-ttu-id="66353-138">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="66353-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="66353-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="66353-139">See also</span></span>



[<span data-ttu-id="66353-140">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="66353-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="66353-141">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="66353-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="66353-142">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="66353-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="66353-143">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="66353-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

