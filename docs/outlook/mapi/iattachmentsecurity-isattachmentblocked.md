---
title: iattachmentsecurityisattachmentblocked ブロックされました
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttachmentSecurity.IsAttachmentBlocked
api_type:
- COM
ms.assetid: 6986d27a-9602-e44a-0797-4c47f2184ef7
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: d255d7b6e80fe0c080fa0a27a7976db758a8c2ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350849"
---
# <a name="iattachmentsecurityisattachmentblocked"></a><span data-ttu-id="c190e-103">IAttachmentSecurity::IsAttachmentBlocked</span><span class="sxs-lookup"><span data-stu-id="c190e-103">IAttachmentSecurity::IsAttachmentBlocked</span></span>

  
  
<span data-ttu-id="c190e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c190e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c190e-105">指定された添付ファイルが microsoft outlook 2010 または microsoft outlook 2013 によってブロックされているかどうかを確認し、表示およびインデックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="c190e-105">Checks if a specified attachment is blocked by Microsoft Outlook 2010 or Microsoft Outlook 2013 for viewing and indexing.</span></span>
  
```cpp
HRESULT IAttachmentSecurity::IsAttachmentBlocked( 
    LPCWSTR pwszFileName,  
    BOOL *pfBlocked 
);
```

## <a name="parameters"></a><span data-ttu-id="c190e-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c190e-106">Parameters</span></span>

 <span data-ttu-id="c190e-107">_pwszFileName_</span><span class="sxs-lookup"><span data-stu-id="c190e-107">_pwszFileName_</span></span>
  
> <span data-ttu-id="c190e-108">順番添付ファイルのファイル名へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c190e-108">[in] Pointer to the filename of an attachment.</span></span>
    
 <span data-ttu-id="c190e-109">_pfblocked_</span><span class="sxs-lookup"><span data-stu-id="c190e-109">_pfBlocked_</span></span>
  
> <span data-ttu-id="c190e-110">読み上げ指定された添付ファイルがブロックされている場合は**true**を示す値へのポインター。それ以外の場合は**false**。</span><span class="sxs-lookup"><span data-stu-id="c190e-110">[out] Pointer to a value indicating **true** if the specified attachment is blocked; otherwise, **false**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c190e-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="c190e-111">See also</span></span>



[<span data-ttu-id="c190e-112">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="c190e-112">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="c190e-113">添付ファイルがブロックされていることを確認する</span><span class="sxs-lookup"><span data-stu-id="c190e-113">Verify an Attachment is Blocked</span></span>](how-to-verify-an-attachment-is-blocked.md)

