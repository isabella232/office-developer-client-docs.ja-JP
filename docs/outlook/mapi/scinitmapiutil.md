---
title: ScInitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ScInitMapiUtil
api_type:
- HeaderDef
ms.assetid: d83b8ea8-a3b8-4038-a226-de1869c5d722
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 090a73ed908d2a647d00de27b93538a77766c258
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351262"
---
# <a name="scinitmapiutil"></a><span data-ttu-id="3bab8-103">ScInitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="3bab8-103">ScInitMapiUtil</span></span>

  
  
<span data-ttu-id="3bab8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3bab8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3bab8-105">select ユーティリティ関数のみが使用されている場合は、 [MAPIInitialize](mapiinitialize.md)を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="3bab8-105">Replaces [MAPIInitialize](mapiinitialize.md) when only select utility functions are being used.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3bab8-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="3bab8-106">Header file:</span></span>  <br/> |<span data-ttu-id="3bab8-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="3bab8-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="3bab8-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="3bab8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3bab8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3bab8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3bab8-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="3bab8-110">Called by:</span></span>  <br/> |<span data-ttu-id="3bab8-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="3bab8-111">Client applications</span></span>  <br/> |
   
```cpp
SCODE ScInitMapiUtil(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="3bab8-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3bab8-112">Parameters</span></span>

 <span data-ttu-id="3bab8-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3bab8-113">_ulFlags_</span></span>
  
> <span data-ttu-id="3bab8-114">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="3bab8-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3bab8-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="3bab8-115">Return value</span></span>

<span data-ttu-id="3bab8-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="3bab8-116">S_OK</span></span> 
  
> <span data-ttu-id="3bab8-117">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="3bab8-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3bab8-118">解説</span><span class="sxs-lookup"><span data-stu-id="3bab8-118">Remarks</span></span>

<span data-ttu-id="3bab8-119">**ScInitMapiUtil**および[DeinitMapiUtil](deinitmapiutil.md)関数は、連携して、コアとユーティリティ関数を呼び出す[MAPIInitialize](mapiinitialize.md)ではなく、選択ユーティリティ関数を呼び出しおよび解放します。</span><span class="sxs-lookup"><span data-stu-id="3bab8-119">The **ScInitMapiUtil** and [DeinitMapiUtil](deinitmapiutil.md) functions cooperate to call and release select utility functions, as opposed to [MAPIInitialize](mapiinitialize.md), which calls core as well as utility functions.</span></span> <span data-ttu-id="3bab8-120">**ScInitMapiUtil**がユーティリティ関数を呼び出すと、必要なメモリも初期化されます。</span><span class="sxs-lookup"><span data-stu-id="3bab8-120">When **ScInitMapiUtil** calls utility functions, it also initializes the necessary memory.</span></span> 
  
<span data-ttu-id="3bab8-121">**ScInitMapiUtil**が呼び出された関数の使用が完了したら、 **DeinitMapiUtil**を明示的に呼び出して解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3bab8-121">When use of the functions that **ScInitMapiUtil** has called is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="3bab8-122">これに対して、 **MAPIInitialize**は暗黙的に**DeinitMapiUtil**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3bab8-122">In contrast, **MAPIInitialize** implicitly calls **DeinitMapiUtil**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3bab8-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="3bab8-123">See also</span></span>



[<span data-ttu-id="3bab8-124">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="3bab8-124">MAPIUninitialize</span></span>](mapiuninitialize.md)

