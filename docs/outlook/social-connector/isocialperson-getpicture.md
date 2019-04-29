---
title: i形式 al個人 getpicture
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 02fcaf25-42b5-4584-95c6-d44a3d035128
description: ユーザーの picture リソースを含むバイトの配列を取得します。
ms.openlocfilehash: 755e2138378136a3c1d810a1957923f4e8db721d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406711"
---
# <a name="isocialpersongetpicture"></a><span data-ttu-id="50525-103">ISocialPerson::GetPicture</span><span class="sxs-lookup"><span data-stu-id="50525-103">ISocialPerson::GetPicture</span></span>

<span data-ttu-id="50525-104">ユーザーの picture リソースを含むバイトの配列を取得します。</span><span class="sxs-lookup"><span data-stu-id="50525-104">Gets an array of bytes that contains the picture resource for the person.</span></span> 
  
```cpp
HRESULT _stdcall GetPicture([out, retval] SAFEARRAY(unsigned char)* picture);
```

## <a name="parameters"></a><span data-ttu-id="50525-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50525-105">Parameters</span></span>

<span data-ttu-id="50525-106">_表_</span><span class="sxs-lookup"><span data-stu-id="50525-106">_picture_</span></span>
  
> <span data-ttu-id="50525-107">読み上げ個人の画像リソースを表すバイト配列を指定する構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="50525-107">[out] A pointer to a structure that specifies an array of bytes that represent the picture resource for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="50525-108">注釈</span><span class="sxs-lookup"><span data-stu-id="50525-108">Remarks</span></span>

<span data-ttu-id="50525-109">サポートされている画像リソースは .bmp、.jpeg、または .png 形式です。</span><span class="sxs-lookup"><span data-stu-id="50525-109">Supported picture resources are in .bmp, .jpeg, or .png format.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="50525-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="50525-110">See also</span></span>

- [<span data-ttu-id="50525-111">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="50525-111">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

