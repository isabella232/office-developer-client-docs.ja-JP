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
ms.openlocfilehash: 548ec33e39e181aba8a72b5325f3f426b9d51762
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575869"
---
# <a name="ipstoverride1getpersistedregistrations"></a><span data-ttu-id="71f8c-103">IPSTOVERRIDE1::GetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="71f8c-103">IPSTOVERRIDE1::GetPersistedRegistrations</span></span>

  
  
<span data-ttu-id="71f8c-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71f8c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71f8c-105">個人用フォルダー (.pst) ファイルの登録の一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="71f8c-105">Retrieves the list of registrations for the Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a><span data-ttu-id="71f8c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="71f8c-106">Parameters</span></span>

 <span data-ttu-id="71f8c-107">_ppmval_</span><span class="sxs-lookup"><span data-stu-id="71f8c-107">_ppmval_</span></span>
  
> <span data-ttu-id="71f8c-108">[in][SPropValue](spropvalue.md)構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="71f8c-108">[in] A pointer to a pointer to an [SPropValue](spropvalue.md) structure.</span></span> <span data-ttu-id="71f8c-109">この構造体の ulPropTag メンバーは、型の PT_MV_UNICODE と MVszW の値のメンバーが null で終わる Unicode 文字列の配列になります。</span><span class="sxs-lookup"><span data-stu-id="71f8c-109">The ulPropTag member of this structure is of the type PT_MV_UNICODE, and the MVszW value member will be an array of null-terminated Unicode strings.</span></span> <span data-ttu-id="71f8c-110">これらの文字列は、登録の永続化するための Dll へのパスです。</span><span class="sxs-lookup"><span data-stu-id="71f8c-110">These strings are paths to DLLs for which registration has been persisted.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="71f8c-111">ANSI .pst のサポートが実装されていません。</span><span class="sxs-lookup"><span data-stu-id="71f8c-111">.pst support for ANSI is not implemented.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="71f8c-112">�߂�l</span><span class="sxs-lookup"><span data-stu-id="71f8c-112">Return value</span></span>

<span data-ttu-id="71f8c-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="71f8c-113">S_OK</span></span> 
  
> <span data-ttu-id="71f8c-114">関数の呼び出しに成功しました。</span><span class="sxs-lookup"><span data-stu-id="71f8c-114">The function call was successful.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="71f8c-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="71f8c-115">See also</span></span>



[<span data-ttu-id="71f8c-116">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="71f8c-116">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="71f8c-117">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="71f8c-117">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

