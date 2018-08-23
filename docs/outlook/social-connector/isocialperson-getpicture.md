---
title: ISocialPersonGetPicture
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 02fcaf25-42b5-4584-95c6-d44a3d035128
description: 個人の画像リソースを格納するバイトの配列を取得します。
ms.openlocfilehash: dcb0da5bc36c2166d569c770d1f182cd21339435
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804341"
---
# <a name="isocialpersongetpicture"></a><span data-ttu-id="9aa64-103">ISocialPerson::GetPicture</span><span class="sxs-lookup"><span data-stu-id="9aa64-103">ISocialPerson::GetPicture</span></span>

<span data-ttu-id="9aa64-104">個人の画像リソースを格納するバイトの配列を取得します。</span><span class="sxs-lookup"><span data-stu-id="9aa64-104">Gets an array of bytes that contains the picture resource for the person.</span></span> 
  
```cpp
HRESULT _stdcall GetPicture([out, retval] SAFEARRAY(unsigned char)* picture);
```

## <a name="parameters"></a><span data-ttu-id="9aa64-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9aa64-105">Parameters</span></span>

<span data-ttu-id="9aa64-106">_画像_</span><span class="sxs-lookup"><span data-stu-id="9aa64-106">_picture_</span></span>
  
> <span data-ttu-id="9aa64-107">[out]人の画像リソースを表すバイトの配列を指定する構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9aa64-107">[out] A pointer to a structure that specifies an array of bytes that represent the picture resource for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9aa64-108">注釈</span><span class="sxs-lookup"><span data-stu-id="9aa64-108">Remarks</span></span>

<span data-ttu-id="9aa64-109">リソースは .bmp、.jpeg、または .png 形式で、画像をサポートします。</span><span class="sxs-lookup"><span data-stu-id="9aa64-109">Supported picture resources are in .bmp, .jpeg, or .png format.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9aa64-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="9aa64-110">See also</span></span>

- [<span data-ttu-id="9aa64-111">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9aa64-111">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

