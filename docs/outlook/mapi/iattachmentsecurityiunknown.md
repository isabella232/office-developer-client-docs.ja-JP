---
title: iattachmentsecurity IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttachmentSecurity
api_type:
- COM
ms.assetid: 69609f73-5884-9e2b-ab78-a2e0ece3a1d1
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a8464c8265ebc1754f7909be5413620e7f76db5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411415"
---
# <a name="iattachmentsecurity--iunknown"></a><span data-ttu-id="a2c5a-103">IAttachmentSecurity : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a2c5a-103">IAttachmentSecurity : IUnknown</span></span>

  
  
<span data-ttu-id="a2c5a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a2c5a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a2c5a-105">microsoft outlook 2010 および microsoft outlook 2013 ソリューションを使用して、添付ファイルが安全でないと見なされ、表示およびインデックス作成がブロックされているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="a2c5a-105">Allows Microsoft Outlook 2010 and Microsoft Outlook 2013 solutions to find out if an attachment is considered unsafe and blocked for viewing and indexing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a2c5a-106">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="a2c5a-106">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a2c5a-107">IID_IAttachmentSecurity</span><span class="sxs-lookup"><span data-stu-id="a2c5a-107">IID_IAttachmentSecurity</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a2c5a-108">v の順序</span><span class="sxs-lookup"><span data-stu-id="a2c5a-108">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a2c5a-109">IAttachmentSecurity::IsAttachmentBlocked</span><span class="sxs-lookup"><span data-stu-id="a2c5a-109">IAttachmentSecurity::IsAttachmentBlocked</span></span>](iattachmentsecurity-isattachmentblocked.md) <br/> |<span data-ttu-id="a2c5a-110">指定された添付ファイルが outlook 2010 または outlook 2013 によってブロックされているかどうかを確認し、表示およびインデックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="a2c5a-110">Checks if a specified attachment is blocked by Outlook 2010 or Outlook 2013 for viewing and indexing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a2c5a-111">注釈</span><span class="sxs-lookup"><span data-stu-id="a2c5a-111">Remarks</span></span>

<span data-ttu-id="a2c5a-112">outlook 2010 および outlook 2013 ソリューションは、このインターフェイスを照会して、添付ファイルがブロックされているかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="a2c5a-112">Outlook 2010 and Outlook 2013 solutions can query this interface to see if an attachment is blocked.</span></span> <span data-ttu-id="a2c5a-113">outlook 2010 または outlook 2013 によってブロックされている添付ファイルは、outlook 2010 または outlook 2013 がどのように構成されているか、および管理者が適用したポリシーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="a2c5a-113">The attachments that are blocked by Outlook 2010 or Outlook 2013 vary depending on how Outlook 2010 or Outlook 2013 has been configured and the policies that an administrator has applied.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a2c5a-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="a2c5a-114">See also</span></span>



[<span data-ttu-id="a2c5a-115">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="a2c5a-115">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="a2c5a-116">添付ファイルがブロックされていることを確認する</span><span class="sxs-lookup"><span data-stu-id="a2c5a-116">Verify an Attachment is Blocked</span></span>](how-to-verify-an-attachment-is-blocked.md)

