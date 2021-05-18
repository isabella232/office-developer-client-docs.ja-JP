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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a8464c8265ebc1754f7909be5413620e7f76db5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411415"
---
# <a name="iattachmentsecurity--iunknown"></a><span data-ttu-id="9730a-103">IAttachmentSecurity : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9730a-103">IAttachmentSecurity : IUnknown</span></span>

  
  
<span data-ttu-id="9730a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9730a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9730a-105">ソリューションMicrosoft Outlook 2010およびMicrosoft Outlook 2013、添付ファイルが安全でないと見なされ、表示およびインデックス作成のためにブロックされるのを確認できます。</span><span class="sxs-lookup"><span data-stu-id="9730a-105">Allows Microsoft Outlook 2010 and Microsoft Outlook 2013 solutions to find out if an attachment is considered unsafe and blocked for viewing and indexing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9730a-106">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="9730a-106">Interface identifier:</span></span>  <br/> |<span data-ttu-id="9730a-107">IID_IAttachmentSecurity</span><span class="sxs-lookup"><span data-stu-id="9730a-107">IID_IAttachmentSecurity</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="9730a-108">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="9730a-108">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="9730a-109">IAttachmentSecurity::IsAttachmentBlocked</span><span class="sxs-lookup"><span data-stu-id="9730a-109">IAttachmentSecurity::IsAttachmentBlocked</span></span>](iattachmentsecurity-isattachmentblocked.md) <br/> |<span data-ttu-id="9730a-110">指定した添付ファイルが 2010 年または 2013 年Outlook 2013 年Outlook表示およびインデックス作成のためにブロックされている場合にチェックします。</span><span class="sxs-lookup"><span data-stu-id="9730a-110">Checks if a specified attachment is blocked by Outlook 2010 or Outlook 2013 for viewing and indexing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9730a-111">注釈</span><span class="sxs-lookup"><span data-stu-id="9730a-111">Remarks</span></span>

<span data-ttu-id="9730a-112">Outlook 2010 および 2013 Outlook 2013 ソリューションでは、このインターフェイスに対してクエリを実行して、添付ファイルがブロックされるのを確認できます。</span><span class="sxs-lookup"><span data-stu-id="9730a-112">Outlook 2010 and Outlook 2013 solutions can query this interface to see if an attachment is blocked.</span></span> <span data-ttu-id="9730a-113">Outlook 2010 または Outlook 2013 によってブロックされる添付ファイルは、Outlook 2010 または Outlook 2013 の構成方法と管理者が適用したポリシーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="9730a-113">The attachments that are blocked by Outlook 2010 or Outlook 2013 vary depending on how Outlook 2010 or Outlook 2013 has been configured and the policies that an administrator has applied.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9730a-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="9730a-114">See also</span></span>



[<span data-ttu-id="9730a-115">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="9730a-115">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="9730a-116">添付ファイルがブロックされているのを確認する</span><span class="sxs-lookup"><span data-stu-id="9730a-116">Verify an Attachment is Blocked</span></span>](how-to-verify-an-attachment-is-blocked.md)

