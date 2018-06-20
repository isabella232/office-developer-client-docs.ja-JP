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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 56aaf5caf93f90f54d152ab3684ca592cd45cd1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801163"
---
# <a name="ipstoverride1getpersistedregistrations"></a><span data-ttu-id="af97b-103">IPSTOVERRIDE1::GetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="af97b-103">IPSTOVERRIDE1::GetPersistedRegistrations</span></span>

  
  
<span data-ttu-id="af97b-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="af97b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="af97b-105">個人用フォルダー (.pst) ファイルの登録の一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="af97b-105">Retrieves the list of registrations for the Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a><span data-ttu-id="af97b-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="af97b-106">Parameters</span></span>

 <span data-ttu-id="af97b-107">_ppmval_</span><span class="sxs-lookup"><span data-stu-id="af97b-107">_ppmval_</span></span>
  
> <span data-ttu-id="af97b-108">[in][SPropValue](spropvalue.md)構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="af97b-108">[in] A pointer to a pointer to an [SPropValue](spropvalue.md) structure.</span></span> <span data-ttu-id="af97b-109">この構造体の ulPropTag メンバーは、型の PT_MV_UNICODE と MVszW の値のメンバーが null で終わる Unicode 文字列の配列になります。</span><span class="sxs-lookup"><span data-stu-id="af97b-109">The ulPropTag member of this structure is of the type PT_MV_UNICODE, and the MVszW value member will be an array of null-terminated Unicode strings.</span></span> <span data-ttu-id="af97b-110">これらの文字列は、登録の永続化するための Dll へのパスです。</span><span class="sxs-lookup"><span data-stu-id="af97b-110">These strings are paths to DLLs for which registration has been persisted.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="af97b-111">ANSI .pst のサポートが実装されていません。</span><span class="sxs-lookup"><span data-stu-id="af97b-111">.pst support for ANSI is not implemented.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="af97b-112">�߂�l</span><span class="sxs-lookup"><span data-stu-id="af97b-112">Return value</span></span>

<span data-ttu-id="af97b-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="af97b-113">S_OK</span></span> 
  
> <span data-ttu-id="af97b-114">関数の呼び出しに成功しました。</span><span class="sxs-lookup"><span data-stu-id="af97b-114">The function call was successful.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="af97b-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="af97b-115">See also</span></span>



[<span data-ttu-id="af97b-116">IPSTOVERRIDE1: IUnknown</span><span class="sxs-lookup"><span data-stu-id="af97b-116">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="af97b-117">IPSTOVERRIDEREQ: IUnknown</span><span class="sxs-lookup"><span data-stu-id="af97b-117">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

