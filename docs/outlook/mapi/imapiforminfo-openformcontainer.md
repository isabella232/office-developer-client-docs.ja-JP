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
ms.openlocfilehash: 16e1d45806755bad8caff6847b0ecdea5b4ba78b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590422"
---
# <a name="imapiforminfoopenformcontainer"></a><span data-ttu-id="70e5a-103">IMAPIFormInfo::OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="70e5a-103">IMAPIFormInfo::OpenFormContainer</span></span>

  
  
<span data-ttu-id="70e5a-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70e5a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70e5a-105">特定のフォームがインストールされているフォームのコンテナーへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="70e5a-105">Returns a pointer to the form container in which a particular form is installed.</span></span>
  
```cpp
HRESULT OpenFormContainer(
  LPMAPIFORMCONTAINER FAR * ppformcontainer
);
```

## <a name="parameters"></a><span data-ttu-id="70e5a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="70e5a-106">Parameters</span></span>

 <span data-ttu-id="70e5a-107">_ppformcontainer_</span><span class="sxs-lookup"><span data-stu-id="70e5a-107">_ppformcontainer_</span></span>
  
> <span data-ttu-id="70e5a-108">[out]返されるフォームのコンテナー オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="70e5a-108">[out] A pointer to a pointer to the returned form container object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="70e5a-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="70e5a-109">Return value</span></span>

<span data-ttu-id="70e5a-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="70e5a-110">S_OK</span></span> 
  
> <span data-ttu-id="70e5a-111">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="70e5a-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="70e5a-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="70e5a-112">See also</span></span>



[<span data-ttu-id="70e5a-113">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="70e5a-113">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

