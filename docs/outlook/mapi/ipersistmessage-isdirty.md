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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309612"
---
# <a name="ipersistmessageisdirty"></a><span data-ttu-id="a9653-103">IPersistMessage::IsDirty</span><span class="sxs-lookup"><span data-stu-id="a9653-103">IPersistMessage::IsDirty</span></span>

  
  
<span data-ttu-id="a9653-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9653-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a9653-105">前回の保存以降に加えられた変更について、フォームをチェックします。</span><span class="sxs-lookup"><span data-stu-id="a9653-105">Checks the form for changes that were made since the last save.</span></span>
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a><span data-ttu-id="a9653-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a9653-106">Parameters</span></span>

<span data-ttu-id="a9653-107">なし</span><span class="sxs-lookup"><span data-stu-id="a9653-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="a9653-108">戻り値</span><span class="sxs-lookup"><span data-stu-id="a9653-108">Return value</span></span>

<span data-ttu-id="a9653-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="a9653-109">S_OK</span></span> 
  
> <span data-ttu-id="a9653-110">フォームには、最後に保存されてから変更が加えられています。</span><span class="sxs-lookup"><span data-stu-id="a9653-110">The form has changes that were made since it was last saved.</span></span>
    
<span data-ttu-id="a9653-111">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="a9653-111">S_FALSE</span></span> 
  
> <span data-ttu-id="a9653-112">フォームには、最後に保存されてから加えられた変更はありません。</span><span class="sxs-lookup"><span data-stu-id="a9653-112">The form does not have changes that were made since it was last saved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a9653-113">解説</span><span class="sxs-lookup"><span data-stu-id="a9653-113">Remarks</span></span>

<span data-ttu-id="a9653-114">フォームビューアーは**IPersistMessage:: IsDirty**メソッドを呼び出して、メッセージに保存されていないデータがあるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="a9653-114">Form viewers call the **IPersistMessage::IsDirty** method to determine whether the message has unsaved data.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a9653-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="a9653-115">See also</span></span>



[<span data-ttu-id="a9653-116">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a9653-116">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

