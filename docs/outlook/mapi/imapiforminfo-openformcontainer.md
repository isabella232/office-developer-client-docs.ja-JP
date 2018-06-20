---
title: IMAPIFormInfoOpenFormContainer
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.OpenFormContainer
api_type:
- COM
ms.assetid: 1d6eec99-59f9-4700-9b83-7f7f8787a9f8
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f6461a1e47437c5d0c2c422d727e2b00819629b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800536"
---
# <a name="imapiforminfoopenformcontainer"></a><span data-ttu-id="e9f18-103">IMAPIFormInfo::OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="e9f18-103">IMAPIFormInfo::OpenFormContainer</span></span>

  
  
<span data-ttu-id="e9f18-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e9f18-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e9f18-105">特定のフォームがインストールされているフォームのコンテナーへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="e9f18-105">Returns a pointer to the form container in which a particular form is installed.</span></span>
  
```cpp
HRESULT OpenFormContainer(
  LPMAPIFORMCONTAINER FAR * ppformcontainer
);
```

## <a name="parameters"></a><span data-ttu-id="e9f18-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="e9f18-106">Parameters</span></span>

 <span data-ttu-id="e9f18-107">_ppformcontainer_</span><span class="sxs-lookup"><span data-stu-id="e9f18-107">_ppformcontainer_</span></span>
  
> <span data-ttu-id="e9f18-108">[out]返されるフォームのコンテナー オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e9f18-108">[out] A pointer to a pointer to the returned form container object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e9f18-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="e9f18-109">Return value</span></span>

<span data-ttu-id="e9f18-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="e9f18-110">S_OK</span></span> 
  
> <span data-ttu-id="e9f18-111">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="e9f18-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e9f18-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="e9f18-112">See also</span></span>



[<span data-ttu-id="e9f18-113">IMAPIFormInfo: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e9f18-113">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

