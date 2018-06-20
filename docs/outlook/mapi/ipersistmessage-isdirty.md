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
ms.openlocfilehash: e748427b39418a80cae88e98b4aa7eef6df24393
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801120"
---
# <a name="ipersistmessageisdirty"></a><span data-ttu-id="d99f1-103">IPersistMessage::IsDirty</span><span class="sxs-lookup"><span data-stu-id="d99f1-103">IPersistMessage::IsDirty</span></span>

  
  
<span data-ttu-id="d99f1-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d99f1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d99f1-105">最後の保存以降に加えた変更のフォームをチェックします。</span><span class="sxs-lookup"><span data-stu-id="d99f1-105">Checks the form for changes that were made since the last save.</span></span>
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a><span data-ttu-id="d99f1-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d99f1-106">Parameters</span></span>

<span data-ttu-id="d99f1-107">なし</span><span class="sxs-lookup"><span data-stu-id="d99f1-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="d99f1-108">�߂�l</span><span class="sxs-lookup"><span data-stu-id="d99f1-108">Return value</span></span>

<span data-ttu-id="d99f1-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="d99f1-109">S_OK</span></span> 
  
> <span data-ttu-id="d99f1-110">フォームには、最後に保存された後に行われた変更があります。</span><span class="sxs-lookup"><span data-stu-id="d99f1-110">The form has changes that were made since it was last saved.</span></span>
    
<span data-ttu-id="d99f1-111">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="d99f1-111">S_FALSE</span></span> 
  
> <span data-ttu-id="d99f1-112">フォームには、最後に保存された後に加えられた変更はありません。</span><span class="sxs-lookup"><span data-stu-id="d99f1-112">The form does not have changes that were made since it was last saved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d99f1-113">備考</span><span class="sxs-lookup"><span data-stu-id="d99f1-113">Remarks</span></span>

<span data-ttu-id="d99f1-114">フォームの閲覧者は、メッセージのデータが保存されているかどうかを決定する**IPersistMessage::IsDirty**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d99f1-114">Form viewers call the **IPersistMessage::IsDirty** method to determine whether the message has unsaved data.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d99f1-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="d99f1-115">See also</span></span>



[<span data-ttu-id="d99f1-116">IPersistMessage: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d99f1-116">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

