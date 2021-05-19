---
title: attConversationID and attParentID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bed36900-e44d-434b-a4f2-d10f2d6f70da
description: '最終更新日: 2013 年 3 月 12 日'
ms.openlocfilehash: c5880aefe7c2dba2e5e4c5405aae2020bb86c711
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410050"
---
# <a name="attconversationid-and-attparentid"></a><span data-ttu-id="f297e-103">attConversationID and attParentID</span><span class="sxs-lookup"><span data-stu-id="f297e-103">attConversationID and attParentID</span></span>

<span data-ttu-id="f297e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f297e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f297e-105">ワークWindows 3.1 メール会話キーのプロパティは、テキスト文字列です。</span><span class="sxs-lookup"><span data-stu-id="f297e-105">The Windows for Workgroups 3.1 Mail conversation key is a text string.</span></span> <span data-ttu-id="f297e-106">MAPI に相当する値はバイナリ値です。</span><span class="sxs-lookup"><span data-stu-id="f297e-106">The MAPI equivalent is a binary value.</span></span> <span data-ttu-id="f297e-107">下位互換性を提供するために、TNEF 実装はバイナリ データをテキストに変換し、終端の null 文字を追加します。</span><span class="sxs-lookup"><span data-stu-id="f297e-107">To provide backward compatibility, the TNEF implementation converts the binary data to text and adds a terminating null character.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f297e-108">これらの TNEF 属性がマップされている MAPI の対応するプロパティ PR_CONVERSATION_KEY および PR_PARENT_KEY は、ipM を検索するために Microsoft Exchange Server: **PR_CONVERSATION_KEY** の使用 [、PidTagConversationKey](pidtagconversationkey-canonical-property.md)標準プロパティの使用で使用されなくなったが、Outlook でのみ保持されます。 **MessageManager** メッセージ。</span><span class="sxs-lookup"><span data-stu-id="f297e-108">The corresponding properties in MAPI to which these TNEF attributes are mapped, PR_CONVERSATION_KEY and PR_PARENT_KEY, have been deprecated in Microsoft Exchange Server: Use of **PR_CONVERSATION_KEY**, the [PidTagConversationKey Canonical Property](pidtagconversationkey-canonical-property.md), persists in Outlook only, for locating **IPM.MessageManager** messages.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f297e-109">注釈</span><span class="sxs-lookup"><span data-stu-id="f297e-109">Remarks</span></span>

<span data-ttu-id="f297e-110">**PR_CONVERSATION_KEY** プロパティは **、代** わりに使用する必要がある PR_CONVERSATION_INDEX [、PidTagConversationIndex](pidtagconversationindex-canonical-property.md)標準プロパティ、**および PR_CONVERSATION_TOPIC** [、PidTagConversationTopic 標準](pidtagconversationtopic-canonical-property.md)プロパティのそれ以外の場合は古い前駆です。</span><span class="sxs-lookup"><span data-stu-id="f297e-110">The **PR_CONVERSATION_KEY** property is the otherwise obsolete precursor of the **PR_CONVERSATION_INDEX**, [PidTagConversationIndex Canonical Property](pidtagconversationindex-canonical-property.md) and **PR_CONVERSATION_TOPIC**, [PidTagConversationTopic Canonical Property](pidtagconversationtopic-canonical-property.md), which should be used instead.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f297e-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="f297e-111">See also</span></span>

- [<span data-ttu-id="f297e-112">IPM サブツリー</span><span class="sxs-lookup"><span data-stu-id="f297e-112">IPM Subtree</span></span>](ipm-subtree.md)
- [<span data-ttu-id="f297e-113">MAPI の特別なフォルダー</span><span class="sxs-lookup"><span data-stu-id="f297e-113">MAPI Special Folders</span></span>](mapi-special-folders.md)

