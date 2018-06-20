---
title: PidTagRpcOverHttpProxyAuthScheme の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6da78f1a-6423-460c-b3a9-fd6441df9cef
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: b8c68c2cd34ba037dc725a7d15575159466d8123
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803364"
---
# <a name="pidtagrpcoverhttpproxyauthscheme-canonical-property"></a><span data-ttu-id="23e25-103">PidTagRpcOverHttpProxyAuthScheme の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="23e25-103">PidTagRpcOverHttpProxyAuthScheme Canonical Property</span></span>

  
  
<span data-ttu-id="23e25-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="23e25-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="23e25-105">このプロファイルに使用する認証プロトコルを表します。</span><span class="sxs-lookup"><span data-stu-id="23e25-105">Represents the authentication protocol to be used for this profile.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="23e25-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="23e25-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="23e25-107">PR_ROH_PROXY_AUTH_SCHEME</span><span class="sxs-lookup"><span data-stu-id="23e25-107">PR_ROH_PROXY_AUTH_SCHEME</span></span>  <br/> |
|<span data-ttu-id="23e25-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="23e25-108">Identifier:</span></span>  <br/> |<span data-ttu-id="23e25-109">0x6627</span><span class="sxs-lookup"><span data-stu-id="23e25-109">0x6627</span></span>  <br/> |
|<span data-ttu-id="23e25-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="23e25-110">Data type:</span></span>  <br/> |<span data-ttu-id="23e25-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="23e25-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="23e25-112">領域:</span><span class="sxs-lookup"><span data-stu-id="23e25-112">Area:</span></span>  <br/> |<span data-ttu-id="23e25-113">その他</span><span class="sxs-lookup"><span data-stu-id="23e25-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23e25-114">備考</span><span class="sxs-lookup"><span data-stu-id="23e25-114">Remarks</span></span>

<span data-ttu-id="23e25-115">このプロパティは、基本認証または NT LAN マネージャー (NTLM) 認証のいずれかを設定できます。</span><span class="sxs-lookup"><span data-stu-id="23e25-115">This property can be set for either basic authentication or NT LAN Manager (NTLM) authentication.</span></span> <span data-ttu-id="23e25-116">このプロパティの有効な値は、次のような。</span><span class="sxs-lookup"><span data-stu-id="23e25-116">The possible values for this property are as follow.</span></span>
  
|<span data-ttu-id="23e25-117">**名前**</span><span class="sxs-lookup"><span data-stu-id="23e25-117">**Name**</span></span>|<span data-ttu-id="23e25-118">**値**</span><span class="sxs-lookup"><span data-stu-id="23e25-118">**Value**</span></span>|<span data-ttu-id="23e25-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="23e25-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="23e25-120">**ROHAUTH_BASIC**</span><span class="sxs-lookup"><span data-stu-id="23e25-120">**ROHAUTH_BASIC**</span></span> <br/> |<span data-ttu-id="23e25-121">0x1</span><span class="sxs-lookup"><span data-stu-id="23e25-121">0x1</span></span>  <br/> |<span data-ttu-id="23e25-122">基本認証</span><span class="sxs-lookup"><span data-stu-id="23e25-122">Basic authentication</span></span>  <br/> |
|<span data-ttu-id="23e25-123">**ROHAUTH_NTLM**</span><span class="sxs-lookup"><span data-stu-id="23e25-123">**ROHAUTH_NTLM**</span></span> <br/> |<span data-ttu-id="23e25-124">0x2</span><span class="sxs-lookup"><span data-stu-id="23e25-124">0x2</span></span>  <br/> |<span data-ttu-id="23e25-125">NTLM 認証</span><span class="sxs-lookup"><span data-stu-id="23e25-125">NTLM authentication</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="23e25-126">関連リソース</span><span class="sxs-lookup"><span data-stu-id="23e25-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="23e25-127">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="23e25-127">Protocol specifications</span></span>

<span data-ttu-id="23e25-128">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="23e25-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="23e25-129">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="23e25-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="23e25-130">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="23e25-130">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="23e25-131">リモート操作で使用される基本的なデータ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="23e25-131">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="23e25-132">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="23e25-132">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="23e25-133">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="23e25-133">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="23e25-134">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="23e25-134">Header files</span></span>

<span data-ttu-id="23e25-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="23e25-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="23e25-136">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="23e25-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="23e25-137">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="23e25-137">Mapitags.h</span></span>
  
> <span data-ttu-id="23e25-138">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="23e25-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="23e25-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="23e25-139">See also</span></span>



[<span data-ttu-id="23e25-140">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="23e25-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="23e25-141">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="23e25-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="23e25-142">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="23e25-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="23e25-143">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="23e25-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

