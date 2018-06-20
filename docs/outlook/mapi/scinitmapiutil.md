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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 771b466e58bf57a7eb4285c6f6ce94c815ec7288
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803824"
---
# <a name="scinitmapiutil"></a><span data-ttu-id="6af45-103">ScInitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="6af45-103">ScInitMapiUtil</span></span>

  
  
<span data-ttu-id="6af45-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6af45-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6af45-105">[ユーティリティ関数だけを使用する場合に[生じます](mapiinitialize.md)を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="6af45-105">Replaces [MAPIInitialize](mapiinitialize.md) when only select utility functions are being used.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6af45-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="6af45-106">Header file:</span></span>  <br/> |<span data-ttu-id="6af45-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="6af45-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="6af45-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="6af45-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6af45-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6af45-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6af45-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6af45-110">Called by:</span></span>  <br/> |<span data-ttu-id="6af45-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="6af45-111">Client applications</span></span>  <br/> |
   
```cpp
SCODE ScInitMapiUtil(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="6af45-112">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="6af45-112">Parameters</span></span>

 <span data-ttu-id="6af45-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6af45-113">_ulFlags_</span></span>
  
> <span data-ttu-id="6af45-114">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="6af45-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6af45-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="6af45-115">Return value</span></span>

<span data-ttu-id="6af45-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="6af45-116">S_OK</span></span> 
  
> <span data-ttu-id="6af45-117">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="6af45-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6af45-118">����</span><span class="sxs-lookup"><span data-stu-id="6af45-118">Remarks</span></span>

<span data-ttu-id="6af45-119">[生じます](mapiinitialize.md)コアとユーティリティを呼び出すのではなく、機能の選択のユーティリティ関数を解放し、 **ScInitMapiUtil**および[DeinitMapiUtil](deinitmapiutil.md)関数が協力します。</span><span class="sxs-lookup"><span data-stu-id="6af45-119">The **ScInitMapiUtil** and [DeinitMapiUtil](deinitmapiutil.md) functions cooperate to call and release select utility functions, as opposed to [MAPIInitialize](mapiinitialize.md), which calls core as well as utility functions.</span></span> <span data-ttu-id="6af45-120">**ScInitMapiUtil**では、ユーティリティ関数を呼び出すと、も、必要なメモリを初期化します。</span><span class="sxs-lookup"><span data-stu-id="6af45-120">When **ScInitMapiUtil** calls utility functions, it also initializes the necessary memory.</span></span> 
  
<span data-ttu-id="6af45-121">**ScInitMapiUtil**が呼び出されている関数の使用が完了すると、それらを解放する**DeinitMapiUtil**を明示的に呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="6af45-121">When use of the functions that **ScInitMapiUtil** has called is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="6af45-122">**生じます**は対照的に、 **DeinitMapiUtil**を暗黙的に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6af45-122">In contrast, **MAPIInitialize** implicitly calls **DeinitMapiUtil**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6af45-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="6af45-123">See also</span></span>



[<span data-ttu-id="6af45-124">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="6af45-124">MAPIUninitialize</span></span>](mapiuninitialize.md)

