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
ms.openlocfilehash: faba91d813d27f7ea45e978724ce0d4707803cba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590107"
---
# <a name="scuncfromlocalpath"></a><span data-ttu-id="cf04d-103">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="cf04d-103">ScUNCFromLocalPath</span></span>

  
  
<span data-ttu-id="cf04d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf04d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf04d-105">汎用名前付け規則 (UNC) パスに対応する指定されたローカル パスを検索します。</span><span class="sxs-lookup"><span data-stu-id="cf04d-105">Locates a universal naming convention (UNC) path counterpart to the given local path.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cf04d-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="cf04d-106">Header file:</span></span>  <br/> |<span data-ttu-id="cf04d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cf04d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="cf04d-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="cf04d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="cf04d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="cf04d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="cf04d-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="cf04d-110">Called by:</span></span>  <br/> |<span data-ttu-id="cf04d-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="cf04d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScUNCFromLocalPath(
  LPSTR szLocal,
  LPSTR szUNC,
  UINT cchUNC
);
```

## <a name="parameters"></a><span data-ttu-id="cf04d-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cf04d-112">Parameters</span></span>

 <span data-ttu-id="cf04d-113">_szLocal_</span><span class="sxs-lookup"><span data-stu-id="cf04d-113">_szLocal_</span></span>
  
> <span data-ttu-id="cf04d-114">[in]パスの形式で [_ドライブ:_]\[ _のパス_] ファイルまたはディレクトリの。</span><span class="sxs-lookup"><span data-stu-id="cf04d-114">[in] A path in the format [ _drive:_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="cf04d-115">_szUNC_</span><span class="sxs-lookup"><span data-stu-id="cf04d-115">_szUNC_</span></span>
  
> <span data-ttu-id="cf04d-116">[out]形式のパス\\[_サーバー_]\[ _を共有_]\[ _パス_] の同じファイルまたはディレクトリの場合、 _szLocal_パラメーターとします。</span><span class="sxs-lookup"><span data-stu-id="cf04d-116">[out] A path in the format \\[ _server_]\[ _share_]\[ _path_] of the same file or directory as for the  _szLocal_ parameter.</span></span> 
    
 <span data-ttu-id="cf04d-117">_cchUNC_</span><span class="sxs-lookup"><span data-stu-id="cf04d-117">_cchUNC_</span></span>
  
> <span data-ttu-id="cf04d-118">[in]出力文字列のバッファーのサイズです。</span><span class="sxs-lookup"><span data-stu-id="cf04d-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cf04d-119">�߂�l</span><span class="sxs-lookup"><span data-stu-id="cf04d-119">Return value</span></span>

<span data-ttu-id="cf04d-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="cf04d-120">S_OK</span></span>
  
> <span data-ttu-id="cf04d-121">UNC パスに対応するでは、正常に配置されました。</span><span class="sxs-lookup"><span data-stu-id="cf04d-121">The UNC path counterpart was successfully located.</span></span>
    
<span data-ttu-id="cf04d-122">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="cf04d-122">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="cf04d-123">1 つ以上のパラメーターが無効です。</span><span class="sxs-lookup"><span data-stu-id="cf04d-123">One or more parameters are invalid.</span></span>
    
<span data-ttu-id="cf04d-124">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="cf04d-124">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="cf04d-125">_szUNC_は、結果を保持するのに十分な大きさでした。</span><span class="sxs-lookup"><span data-stu-id="cf04d-125">_szUNC_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="cf04d-126">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="cf04d-126">S_FALSE</span></span>
  
> <span data-ttu-id="cf04d-127">ローカル パスは、UNC 文字列では既にいました。</span><span class="sxs-lookup"><span data-stu-id="cf04d-127">The local path was already a UNC string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cf04d-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="cf04d-128">See also</span></span>



[<span data-ttu-id="cf04d-129">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="cf04d-129">ScLocalPathFromUNC</span></span>](sclocalpathfromunc.md)

