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
ms.openlocfilehash: f182610f9cf4874cc18c409960e1f8b23f853d4f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574827"
---
# <a name="iattachmentsecurity--iunknown"></a><span data-ttu-id="7f430-103">IAttachmentSecurity : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7f430-103">IAttachmentSecurity : IUnknown</span></span>

  
  
<span data-ttu-id="7f430-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f430-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f430-105">添付ファイルが安全でないと表示して、インデックス作成のブロックと見なされますかどうかを確認する Microsoft Outlook 2010、Outlook 2013 のマイクロソフトのソリューションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="7f430-105">Allows Microsoft Outlook 2010 and Microsoft Outlook 2013 solutions to find out if an attachment is considered unsafe and blocked for viewing and indexing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7f430-106">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="7f430-106">Interface identifier:</span></span>  <br/> |<span data-ttu-id="7f430-107">IID_IAttachmentSecurity</span><span class="sxs-lookup"><span data-stu-id="7f430-107">IID_IAttachmentSecurity</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="7f430-108">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="7f430-108">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="7f430-109">IAttachmentSecurity::IsAttachmentBlocked</span><span class="sxs-lookup"><span data-stu-id="7f430-109">IAttachmentSecurity::IsAttachmentBlocked</span></span>](iattachmentsecurity-isattachmentblocked.md) <br/> |<span data-ttu-id="7f430-110">指定した添付ファイルが表示して、インデックス作成の Outlook 2010 または Outlook 2013 でブロックされているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="7f430-110">Checks if a specified attachment is blocked by Outlook 2010 or Outlook 2013 for viewing and indexing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7f430-111">注釈</span><span class="sxs-lookup"><span data-stu-id="7f430-111">Remarks</span></span>

<span data-ttu-id="7f430-112">Outlook 2010、Outlook 2013 のソリューションでは、添付ファイルがブロックされているかどうかを確認するには、このインターフェイスを照会できます。</span><span class="sxs-lookup"><span data-stu-id="7f430-112">Outlook 2010 and Outlook 2013 solutions can query this interface to see if an attachment is blocked.</span></span> <span data-ttu-id="7f430-113">Outlook 2010 または Outlook 2013 でブロックされる添付ファイルは、どのように Outlook 2010 または Outlook 2013 が構成され、管理者が適用するポリシーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="7f430-113">The attachments that are blocked by Outlook 2010 or Outlook 2013 vary depending on how Outlook 2010 or Outlook 2013 has been configured and the policies that an administrator has applied.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7f430-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="7f430-114">See also</span></span>



[<span data-ttu-id="7f430-115">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="7f430-115">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="7f430-116">添付がプロセスされていることを確認する</span><span class="sxs-lookup"><span data-stu-id="7f430-116">Verify an Attachment is Blocked</span></span>](how-to-verify-an-attachment-is-blocked.md)

