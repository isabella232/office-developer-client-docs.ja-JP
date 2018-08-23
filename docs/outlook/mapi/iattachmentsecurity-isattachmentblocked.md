---
title: IAttachmentSecurityIsAttachmentBlocked
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
ms.openlocfilehash: 45e4362fc025c1784e9432c5d641e865a044bd00
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800411"
---
# <a name="iattachmentsecurityisattachmentblocked"></a><span data-ttu-id="b24c3-103">IAttachmentSecurity::IsAttachmentBlocked</span><span class="sxs-lookup"><span data-stu-id="b24c3-103">IAttachmentSecurity::IsAttachmentBlocked</span></span>

  
  
<span data-ttu-id="b24c3-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b24c3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b24c3-105">指定した添付ファイルが表示して、インデックス作成の Microsoft Outlook 2010 または Microsoft Outlook 2013 でブロックされているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="b24c3-105">Checks if a specified attachment is blocked by Microsoft Outlook 2010 or Microsoft Outlook 2013 for viewing and indexing.</span></span>
  
```cpp
HRESULT IAttachmentSecurity::IsAttachmentBlocked( 
    LPCWSTR pwszFileName,  
    BOOL *pfBlocked 
);
```

## <a name="parameters"></a><span data-ttu-id="b24c3-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b24c3-106">Parameters</span></span>

 <span data-ttu-id="b24c3-107">_pwszFileName_</span><span class="sxs-lookup"><span data-stu-id="b24c3-107">_pwszFileName_</span></span>
  
> <span data-ttu-id="b24c3-108">[in]添付ファイルのファイル名へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b24c3-108">[in] Pointer to the filename of an attachment.</span></span>
    
 <span data-ttu-id="b24c3-109">_pfBlocked_</span><span class="sxs-lookup"><span data-stu-id="b24c3-109">_pfBlocked_</span></span>
  
> <span data-ttu-id="b24c3-110">[out]ポインターの値を示す**true の**場合は、指定した添付ファイルはブロックされます。それ以外の場合、 **false を指定**します。</span><span class="sxs-lookup"><span data-stu-id="b24c3-110">[out] Pointer to a value indicating **true** if the specified attachment is blocked; otherwise, **false**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b24c3-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="b24c3-111">See also</span></span>



[<span data-ttu-id="b24c3-112">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="b24c3-112">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="b24c3-113">添付がプロセスされていることを確認する</span><span class="sxs-lookup"><span data-stu-id="b24c3-113">Verify an Attachment is Blocked</span></span>](how-to-verify-an-attachment-is-blocked.md)

