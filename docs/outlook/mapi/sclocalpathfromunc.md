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
# <a name="sclocalpathfromunc"></a><span data-ttu-id="406d8-103">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="406d8-103">ScLocalPathFromUNC</span></span>

  
  
<span data-ttu-id="406d8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="406d8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="406d8-105">指定した汎用名前付け規則 (UNC) パスに対応するローカルパスを検索します。</span><span class="sxs-lookup"><span data-stu-id="406d8-105">Locates a local path counterpart to the given universal naming convention (UNC) path.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="406d8-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="406d8-106">Header file:</span></span>  <br/> |<span data-ttu-id="406d8-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="406d8-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="406d8-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="406d8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="406d8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="406d8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="406d8-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="406d8-110">Called by:</span></span>  <br/> |<span data-ttu-id="406d8-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="406d8-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScLocalPathFromUNC(
  LPSTR szUNC,
  LPSTR szLocal,
  UINT cchLocal
);
```

## <a name="parameters"></a><span data-ttu-id="406d8-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="406d8-112">Parameters</span></span>

 <span data-ttu-id="406d8-113">_szunc_</span><span class="sxs-lookup"><span data-stu-id="406d8-113">_szUNC_</span></span>
  
> <span data-ttu-id="406d8-114">順番ファイルまたはディレクトリの\\形式__[サーバー\[ ] [_共有_]\[ _パス_] のパス。</span><span class="sxs-lookup"><span data-stu-id="406d8-114">[in] A path in the format \\[ _server_]\[ _share_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="406d8-115">_szlocal_</span><span class="sxs-lookup"><span data-stu-id="406d8-115">_szLocal_</span></span>
  
> <span data-ttu-id="406d8-116">読み上げ_szunc_パラメーターと同じファイルまたはディレクトリの形式 [ _drive:_]\[ _path_] のパス。</span><span class="sxs-lookup"><span data-stu-id="406d8-116">[out] A path in the format [ _drive:_]\[ _path_] of the same file or directory as for the  _szUNC_ parameter.</span></span> 
    
 <span data-ttu-id="406d8-117">_cchlocal_</span><span class="sxs-lookup"><span data-stu-id="406d8-117">_cchLocal_</span></span>
  
> <span data-ttu-id="406d8-118">順番出力文字列のバッファーのサイズ。</span><span class="sxs-lookup"><span data-stu-id="406d8-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="406d8-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="406d8-119">Return value</span></span>

<span data-ttu-id="406d8-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="406d8-120">S_OK</span></span>
  
> <span data-ttu-id="406d8-121">ローカルパスが正常に配置されました。</span><span class="sxs-lookup"><span data-stu-id="406d8-121">A local path was successfully located.</span></span>
    
<span data-ttu-id="406d8-122">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="406d8-122">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="406d8-123">_szlocal_は、結果を保持するのに十分な大きさがありませんでした。</span><span class="sxs-lookup"><span data-stu-id="406d8-123">_szLocal_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="406d8-124">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="406d8-124">S_FALSE</span></span>
  
> <span data-ttu-id="406d8-125">UNC 文字列は、既にローカルパスになっています。</span><span class="sxs-lookup"><span data-stu-id="406d8-125">The UNC string was already a local path.</span></span>
    
<span data-ttu-id="406d8-126">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="406d8-126">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="406d8-127">ローカルパスが見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="406d8-127">A local path was not found.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="406d8-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="406d8-128">See also</span></span>



[<span data-ttu-id="406d8-129">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="406d8-129">ScUNCFromLocalPath</span></span>](scuncfromlocalpath.md)

