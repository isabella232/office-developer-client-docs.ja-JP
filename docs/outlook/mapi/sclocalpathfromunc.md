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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e303361f4f0dd3a08dbb362096d07b8b391a6d97
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594419"
---
# <a name="sclocalpathfromunc"></a><span data-ttu-id="f91b7-103">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="f91b7-103">ScLocalPathFromUNC</span></span>

  
  
<span data-ttu-id="f91b7-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f91b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f91b7-105">特定の汎用名前付け規則 (UNC) パスをローカル パスに対応するを検索します。</span><span class="sxs-lookup"><span data-stu-id="f91b7-105">Locates a local path counterpart to the given universal naming convention (UNC) path.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f91b7-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="f91b7-106">Header file:</span></span>  <br/> |<span data-ttu-id="f91b7-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f91b7-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f91b7-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="f91b7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f91b7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f91b7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f91b7-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f91b7-110">Called by:</span></span>  <br/> |<span data-ttu-id="f91b7-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="f91b7-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScLocalPathFromUNC(
  LPSTR szUNC,
  LPSTR szLocal,
  UINT cchLocal
);
```

## <a name="parameters"></a><span data-ttu-id="f91b7-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f91b7-112">Parameters</span></span>

 <span data-ttu-id="f91b7-113">_szUNC_</span><span class="sxs-lookup"><span data-stu-id="f91b7-113">_szUNC_</span></span>
  
> <span data-ttu-id="f91b7-114">[in]形式のパス\\[_サーバー_]\[ _を共有_]\[ _のパス_] ファイルまたはディレクトリの。</span><span class="sxs-lookup"><span data-stu-id="f91b7-114">[in] A path in the format \\[ _server_]\[ _share_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="f91b7-115">_szLocal_</span><span class="sxs-lookup"><span data-stu-id="f91b7-115">_szLocal_</span></span>
  
> <span data-ttu-id="f91b7-116">[out]形式でパス [_ドライブ:_]\[ _のパス_] の同じファイルまたはディレクトリの場合、 _szUNC_パラメーターとします。</span><span class="sxs-lookup"><span data-stu-id="f91b7-116">[out] A path in the format [ _drive:_]\[ _path_] of the same file or directory as for the  _szUNC_ parameter.</span></span> 
    
 <span data-ttu-id="f91b7-117">_cchLocal_</span><span class="sxs-lookup"><span data-stu-id="f91b7-117">_cchLocal_</span></span>
  
> <span data-ttu-id="f91b7-118">[in]出力文字列のバッファーのサイズです。</span><span class="sxs-lookup"><span data-stu-id="f91b7-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f91b7-119">�߂�l</span><span class="sxs-lookup"><span data-stu-id="f91b7-119">Return value</span></span>

<span data-ttu-id="f91b7-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="f91b7-120">S_OK</span></span>
  
> <span data-ttu-id="f91b7-121">ローカル パスでは、正常に配置されました。</span><span class="sxs-lookup"><span data-stu-id="f91b7-121">A local path was successfully located.</span></span>
    
<span data-ttu-id="f91b7-122">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="f91b7-122">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="f91b7-123">_szLocal_は、結果を保持するのに十分な大きさでした。</span><span class="sxs-lookup"><span data-stu-id="f91b7-123">_szLocal_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="f91b7-124">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="f91b7-124">S_FALSE</span></span>
  
> <span data-ttu-id="f91b7-125">UNC 文字列は、ローカル パスでは既にいました。</span><span class="sxs-lookup"><span data-stu-id="f91b7-125">The UNC string was already a local path.</span></span>
    
<span data-ttu-id="f91b7-126">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="f91b7-126">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="f91b7-127">ローカル パスが見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="f91b7-127">A local path was not found.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f91b7-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="f91b7-128">See also</span></span>



[<span data-ttu-id="f91b7-129">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="f91b7-129">ScUNCFromLocalPath</span></span>](scuncfromlocalpath.md)

