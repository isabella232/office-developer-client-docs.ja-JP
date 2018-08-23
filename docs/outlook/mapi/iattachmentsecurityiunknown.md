---
title: IAttachmentSecurity IUnknown
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 040be6cea64dd58e23d79c20a9ae9dddf02fa87d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800391"
---
# <a name="iattachmentsecurity--iunknown"></a><span data-ttu-id="fa117-103">IAttachmentSecurity : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fa117-103">IAttachmentSecurity : IUnknown</span></span>

  
  
<span data-ttu-id="fa117-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fa117-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fa117-105">添付ファイルが安全でないと表示して、インデックス作成のブロックと見なされますかどうかを確認する Microsoft Outlook 2010、Outlook 2013 のマイクロソフトのソリューションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="fa117-105">Allows Microsoft Outlook 2010 and Microsoft Outlook 2013 solutions to find out if an attachment is considered unsafe and blocked for viewing and indexing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fa117-106">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="fa117-106">Interface identifier:</span></span>  <br/> |<span data-ttu-id="fa117-107">IID_IAttachmentSecurity</span><span class="sxs-lookup"><span data-stu-id="fa117-107">IID_IAttachmentSecurity</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="fa117-108">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="fa117-108">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="fa117-109">IAttachmentSecurity::IsAttachmentBlocked</span><span class="sxs-lookup"><span data-stu-id="fa117-109">IAttachmentSecurity::IsAttachmentBlocked</span></span>](iattachmentsecurity-isattachmentblocked.md) <br/> |<span data-ttu-id="fa117-110">指定した添付ファイルが表示して、インデックス作成の Outlook 2010 または Outlook 2013 でブロックされているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="fa117-110">Checks if a specified attachment is blocked by Outlook 2010 or Outlook 2013 for viewing and indexing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa117-111">注釈</span><span class="sxs-lookup"><span data-stu-id="fa117-111">Remarks</span></span>

<span data-ttu-id="fa117-112">Outlook 2010、Outlook 2013 のソリューションでは、添付ファイルがブロックされているかどうかを確認するには、このインターフェイスを照会できます。</span><span class="sxs-lookup"><span data-stu-id="fa117-112">Outlook 2010 and Outlook 2013 solutions can query this interface to see if an attachment is blocked.</span></span> <span data-ttu-id="fa117-113">Outlook 2010 または Outlook 2013 でブロックされる添付ファイルは、どのように Outlook 2010 または Outlook 2013 が構成され、管理者が適用するポリシーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="fa117-113">The attachments that are blocked by Outlook 2010 or Outlook 2013 vary depending on how Outlook 2010 or Outlook 2013 has been configured and the policies that an administrator has applied.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fa117-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="fa117-114">See also</span></span>



[<span data-ttu-id="fa117-115">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="fa117-115">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="fa117-116">添付がプロセスされていることを確認する</span><span class="sxs-lookup"><span data-stu-id="fa117-116">Verify an Attachment is Blocked</span></span>](how-to-verify-an-attachment-is-blocked.md)

