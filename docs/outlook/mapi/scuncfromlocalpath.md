---
title: ScUNCFromLocalPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScUNCFromLocalPath
api_type:
- COM
ms.assetid: cc4abf1a-c08c-4462-9d7c-6af506dc07c9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b53dd9aaaf18dba5c7e33e0bc7d984de757634a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358773"
---
# <a name="scuncfromlocalpath"></a><span data-ttu-id="85178-103">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="85178-103">ScUNCFromLocalPath</span></span>

  
  
<span data-ttu-id="85178-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85178-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85178-105">指定したローカルパスに相当する汎用名前付け規則 (UNC) パスを検索します。</span><span class="sxs-lookup"><span data-stu-id="85178-105">Locates a universal naming convention (UNC) path counterpart to the given local path.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="85178-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="85178-106">Header file:</span></span>  <br/> |<span data-ttu-id="85178-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="85178-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="85178-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="85178-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="85178-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="85178-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="85178-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="85178-110">Called by:</span></span>  <br/> |<span data-ttu-id="85178-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="85178-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScUNCFromLocalPath(
  LPSTR szLocal,
  LPSTR szUNC,
  UINT cchUNC
);
```

## <a name="parameters"></a><span data-ttu-id="85178-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="85178-112">Parameters</span></span>

 <span data-ttu-id="85178-113">_szlocal_</span><span class="sxs-lookup"><span data-stu-id="85178-113">_szLocal_</span></span>
  
> <span data-ttu-id="85178-114">順番ファイルまたはディレクトリの形式 [ _drive:_]\[ _path_のパス。</span><span class="sxs-lookup"><span data-stu-id="85178-114">[in] A path in the format [ _drive:_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="85178-115">_szunc_</span><span class="sxs-lookup"><span data-stu-id="85178-115">_szUNC_</span></span>
  
> <span data-ttu-id="85178-116">読み上げ_szlocal_パラメーターと同じ\\ファイルまたはディレクトリの形式 [ _server_]\[ _share_]\[ _path_] のパス。</span><span class="sxs-lookup"><span data-stu-id="85178-116">[out] A path in the format \\[ _server_]\[ _share_]\[ _path_] of the same file or directory as for the  _szLocal_ parameter.</span></span> 
    
 <span data-ttu-id="85178-117">_cchunc_</span><span class="sxs-lookup"><span data-stu-id="85178-117">_cchUNC_</span></span>
  
> <span data-ttu-id="85178-118">順番出力文字列のバッファーのサイズ。</span><span class="sxs-lookup"><span data-stu-id="85178-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="85178-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="85178-119">Return value</span></span>

<span data-ttu-id="85178-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="85178-120">S_OK</span></span>
  
> <span data-ttu-id="85178-121">対応する UNC パスが正常に配置されている。</span><span class="sxs-lookup"><span data-stu-id="85178-121">The UNC path counterpart was successfully located.</span></span>
    
<span data-ttu-id="85178-122">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="85178-122">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="85178-123">1 つ以上のパラメーターが無効です。</span><span class="sxs-lookup"><span data-stu-id="85178-123">One or more parameters are invalid.</span></span>
    
<span data-ttu-id="85178-124">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="85178-124">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="85178-125">_szunc_は、結果を保持するのに十分な大きさがありませんでした。</span><span class="sxs-lookup"><span data-stu-id="85178-125">_szUNC_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="85178-126">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="85178-126">S_FALSE</span></span>
  
> <span data-ttu-id="85178-127">ローカルパスは、既に UNC 文字列です。</span><span class="sxs-lookup"><span data-stu-id="85178-127">The local path was already a UNC string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="85178-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="85178-128">See also</span></span>



[<span data-ttu-id="85178-129">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="85178-129">ScLocalPathFromUNC</span></span>](sclocalpathfromunc.md)

