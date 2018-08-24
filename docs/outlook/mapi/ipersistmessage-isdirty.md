---
title: IPersistMessageIsDirty
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.IsDirty
api_type:
- COM
ms.assetid: 57f688db-3a1c-49ff-a15a-8508bda5de68
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 0d2ae556f4dd98b5f6e274a21c608d4ea364d4ec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576205"
---
# <a name="ipersistmessageisdirty"></a><span data-ttu-id="bdfdd-103">IPersistMessage::IsDirty</span><span class="sxs-lookup"><span data-stu-id="bdfdd-103">IPersistMessage::IsDirty</span></span>

  
  
<span data-ttu-id="bdfdd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bdfdd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bdfdd-105">最後の保存以降に加えた変更のフォームをチェックします。</span><span class="sxs-lookup"><span data-stu-id="bdfdd-105">Checks the form for changes that were made since the last save.</span></span>
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a><span data-ttu-id="bdfdd-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bdfdd-106">Parameters</span></span>

<span data-ttu-id="bdfdd-107">なし</span><span class="sxs-lookup"><span data-stu-id="bdfdd-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="bdfdd-108">�߂�l</span><span class="sxs-lookup"><span data-stu-id="bdfdd-108">Return value</span></span>

<span data-ttu-id="bdfdd-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="bdfdd-109">S_OK</span></span> 
  
> <span data-ttu-id="bdfdd-110">フォームには、最後に保存された後に行われた変更があります。</span><span class="sxs-lookup"><span data-stu-id="bdfdd-110">The form has changes that were made since it was last saved.</span></span>
    
<span data-ttu-id="bdfdd-111">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="bdfdd-111">S_FALSE</span></span> 
  
> <span data-ttu-id="bdfdd-112">フォームには、最後に保存された後に加えられた変更はありません。</span><span class="sxs-lookup"><span data-stu-id="bdfdd-112">The form does not have changes that were made since it was last saved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bdfdd-113">注釈</span><span class="sxs-lookup"><span data-stu-id="bdfdd-113">Remarks</span></span>

<span data-ttu-id="bdfdd-114">フォームの閲覧者は、メッセージのデータが保存されているかどうかを決定する**IPersistMessage::IsDirty**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="bdfdd-114">Form viewers call the **IPersistMessage::IsDirty** method to determine whether the message has unsaved data.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bdfdd-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="bdfdd-115">See also</span></span>



[<span data-ttu-id="bdfdd-116">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bdfdd-116">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

