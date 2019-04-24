---
title: imapiforminfoopenformcontainer
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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a76d0c554d7cf06aceeaa2925c199e45411b999d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342092"
---
# <a name="imapiforminfoopenformcontainer"></a><span data-ttu-id="7c400-103">IMAPIFormInfo::OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="7c400-103">IMAPIFormInfo::OpenFormContainer</span></span>

  
  
<span data-ttu-id="7c400-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c400-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c400-105">特定のフォームがインストールされているフォームコンテナーへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="7c400-105">Returns a pointer to the form container in which a particular form is installed.</span></span>
  
```cpp
HRESULT OpenFormContainer(
  LPMAPIFORMCONTAINER FAR * ppformcontainer
);
```

## <a name="parameters"></a><span data-ttu-id="7c400-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7c400-106">Parameters</span></span>

 <span data-ttu-id="7c400-107">_ppformcontainer_</span><span class="sxs-lookup"><span data-stu-id="7c400-107">_ppformcontainer_</span></span>
  
> <span data-ttu-id="7c400-108">読み上げ返される form container オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="7c400-108">[out] A pointer to a pointer to the returned form container object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7c400-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="7c400-109">Return value</span></span>

<span data-ttu-id="7c400-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="7c400-110">S_OK</span></span> 
  
> <span data-ttu-id="7c400-111">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="7c400-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7c400-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="7c400-112">See also</span></span>



[<span data-ttu-id="7c400-113">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7c400-113">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

