---
title: IPSTOVERRIDE1GetPersistedRegistrations
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1.GetPersistedRegistrations
api_type:
- COM
ms.assetid: 027092f0-f2d6-49e8-a8d0-8926824953a2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 822b4164737aa6010ccce108b544410104ac023d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415132"
---
# <a name="ipstoverride1getpersistedregistrations"></a><span data-ttu-id="d9866-103">IPSTOVERRIDE1::GetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="d9866-103">IPSTOVERRIDE1::GetPersistedRegistrations</span></span>

  
  
<span data-ttu-id="d9866-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9866-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9866-105">個人用フォルダー (.pst) ファイルの登録リストを取得します。</span><span class="sxs-lookup"><span data-stu-id="d9866-105">Retrieves the list of registrations for the Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a><span data-ttu-id="d9866-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9866-106">Parameters</span></span>

 <span data-ttu-id="d9866-107">_ppmval_</span><span class="sxs-lookup"><span data-stu-id="d9866-107">_ppmval_</span></span>
  
> <span data-ttu-id="d9866-108">順番[spropvalue](spropvalue.md)構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d9866-108">[in] A pointer to a pointer to an [SPropValue](spropvalue.md) structure.</span></span> <span data-ttu-id="d9866-109">この構造体の ulPropTag メンバーの型は PT_MV_UNICODE で、MVszW value メンバーは、null で終了する UNICODE 文字列の配列になります。</span><span class="sxs-lookup"><span data-stu-id="d9866-109">The ulPropTag member of this structure is of the type PT_MV_UNICODE, and the MVszW value member will be an array of null-terminated Unicode strings.</span></span> <span data-ttu-id="d9866-110">これらの文字列は、登録が永続化されている dll へのパスです。</span><span class="sxs-lookup"><span data-stu-id="d9866-110">These strings are paths to DLLs for which registration has been persisted.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="d9866-111">ANSI の .pst サポートは実装されていません。</span><span class="sxs-lookup"><span data-stu-id="d9866-111">.pst support for ANSI is not implemented.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="d9866-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9866-112">Return value</span></span>

<span data-ttu-id="d9866-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="d9866-113">S_OK</span></span> 
  
> <span data-ttu-id="d9866-114">関数呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="d9866-114">The function call was successful.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d9866-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="d9866-115">See also</span></span>



[<span data-ttu-id="d9866-116">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d9866-116">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="d9866-117">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d9866-117">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

