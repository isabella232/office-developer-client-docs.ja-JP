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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 91985d3dc8a7816c3da3215e505097c57c63e035
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407572"
---
# <a name="ipersistmessageisdirty"></a><span data-ttu-id="e5a4c-103">IPersistMessage::IsDirty</span><span class="sxs-lookup"><span data-stu-id="e5a4c-103">IPersistMessage::IsDirty</span></span>

  
  
<span data-ttu-id="e5a4c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5a4c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5a4c-105">前回の保存以降に加えられた変更について、フォームをチェックします。</span><span class="sxs-lookup"><span data-stu-id="e5a4c-105">Checks the form for changes that were made since the last save.</span></span>
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a><span data-ttu-id="e5a4c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e5a4c-106">Parameters</span></span>

<span data-ttu-id="e5a4c-107">なし</span><span class="sxs-lookup"><span data-stu-id="e5a4c-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="e5a4c-108">戻り値</span><span class="sxs-lookup"><span data-stu-id="e5a4c-108">Return value</span></span>

<span data-ttu-id="e5a4c-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="e5a4c-109">S_OK</span></span> 
  
> <span data-ttu-id="e5a4c-110">フォームには、最後に保存されてから変更が加えられています。</span><span class="sxs-lookup"><span data-stu-id="e5a4c-110">The form has changes that were made since it was last saved.</span></span>
    
<span data-ttu-id="e5a4c-111">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="e5a4c-111">S_FALSE</span></span> 
  
> <span data-ttu-id="e5a4c-112">フォームには、最後に保存されてから加えられた変更はありません。</span><span class="sxs-lookup"><span data-stu-id="e5a4c-112">The form does not have changes that were made since it was last saved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e5a4c-113">注釈</span><span class="sxs-lookup"><span data-stu-id="e5a4c-113">Remarks</span></span>

<span data-ttu-id="e5a4c-114">フォームビューアーは**IPersistMessage:: IsDirty**メソッドを呼び出して、メッセージに保存されていないデータがあるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="e5a4c-114">Form viewers call the **IPersistMessage::IsDirty** method to determine whether the message has unsaved data.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e5a4c-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="e5a4c-115">See also</span></span>



[<span data-ttu-id="e5a4c-116">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e5a4c-116">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

