---
title: ScLocalPathFromUNC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScLocalPathFromUNC
api_type:
- COM
ms.assetid: ef5eb5c6-251e-4a3a-8855-7c28804a29ab
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e7607a57da5b618a20d6c8e360c7e3cb4f933856
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432234"
---
# <a name="sclocalpathfromunc"></a><span data-ttu-id="76725-103">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="76725-103">ScLocalPathFromUNC</span></span>

  
  
<span data-ttu-id="76725-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76725-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76725-105">指定された汎用名前付け規則 (UNC) パスに対応するローカル パスを検索します。</span><span class="sxs-lookup"><span data-stu-id="76725-105">Locates a local path counterpart to the given universal naming convention (UNC) path.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="76725-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="76725-106">Header file:</span></span>  <br/> |<span data-ttu-id="76725-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="76725-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="76725-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="76725-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="76725-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="76725-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="76725-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="76725-110">Called by:</span></span>  <br/> |<span data-ttu-id="76725-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="76725-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScLocalPathFromUNC(
  LPSTR szUNC,
  LPSTR szLocal,
  UINT cchLocal
);
```

## <a name="parameters"></a><span data-ttu-id="76725-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="76725-112">Parameters</span></span>

 <span data-ttu-id="76725-113">_szUNC_</span><span class="sxs-lookup"><span data-stu-id="76725-113">_szUNC_</span></span>
  
> <span data-ttu-id="76725-114">[in]ファイルまたはディレクトリの \\ _[server_] \[ _share_] \[ _パス_] 形式のパス。</span><span class="sxs-lookup"><span data-stu-id="76725-114">[in] A path in the format \\[ _server_]\[ _share_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="76725-115">_szLocal_</span><span class="sxs-lookup"><span data-stu-id="76725-115">_szLocal_</span></span>
  
> <span data-ttu-id="76725-116">[out]szUNC パラメーターと同じファイルまたはディレクトリの形式 [ _drive:_] path ] の \[ パス。 </span><span class="sxs-lookup"><span data-stu-id="76725-116">[out] A path in the format [ _drive:_]\[ _path_] of the same file or directory as for the  _szUNC_ parameter.</span></span> 
    
 <span data-ttu-id="76725-117">_cchLocal_</span><span class="sxs-lookup"><span data-stu-id="76725-117">_cchLocal_</span></span>
  
> <span data-ttu-id="76725-118">[in]出力文字列のバッファーのサイズ。</span><span class="sxs-lookup"><span data-stu-id="76725-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="76725-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="76725-119">Return value</span></span>

<span data-ttu-id="76725-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="76725-120">S_OK</span></span>
  
> <span data-ttu-id="76725-121">ローカル パスが正常に見つからされました。</span><span class="sxs-lookup"><span data-stu-id="76725-121">A local path was successfully located.</span></span>
    
<span data-ttu-id="76725-122">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="76725-122">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="76725-123">_szLocal は_ 、結果を保持するのに十分な大きさではなかった。</span><span class="sxs-lookup"><span data-stu-id="76725-123">_szLocal_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="76725-124">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="76725-124">S_FALSE</span></span>
  
> <span data-ttu-id="76725-125">UNC 文字列は既にローカル パスでした。</span><span class="sxs-lookup"><span data-stu-id="76725-125">The UNC string was already a local path.</span></span>
    
<span data-ttu-id="76725-126">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="76725-126">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="76725-127">ローカル パスが見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="76725-127">A local path was not found.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="76725-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="76725-128">See also</span></span>



[<span data-ttu-id="76725-129">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="76725-129">ScUNCFromLocalPath</span></span>](scuncfromlocalpath.md)

