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
# <a name="attconversationid-and-attparentid"></a><span data-ttu-id="61956-103">attConversationID and attParentID</span><span class="sxs-lookup"><span data-stu-id="61956-103">attConversationID and attParentID</span></span>

<span data-ttu-id="61956-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61956-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61956-105">[ワークグループの Windows 用] 3.1 メールの会話キーはテキスト文字列です。</span><span class="sxs-lookup"><span data-stu-id="61956-105">The Windows for Workgroups 3.1 Mail conversation key is a text string.</span></span> <span data-ttu-id="61956-106">MAPI に相当する値はバイナリ値です。</span><span class="sxs-lookup"><span data-stu-id="61956-106">The MAPI equivalent is a binary value.</span></span> <span data-ttu-id="61956-107">下位互換性を確保するために、TNEF 実装はバイナリデータをテキストに変換し、終端の null 文字を追加します。</span><span class="sxs-lookup"><span data-stu-id="61956-107">To provide backward compatibility, the TNEF implementation converts the binary data to text and adds a terminating null character.</span></span>
  
> [!NOTE]
> <span data-ttu-id="61956-108">これらの TNEF 属性がマップされている MAPI の対応するプロパティ、PR_CONVERSATION_KEY および PR_PARENT_KEY は、Microsoft Exchange Server で廃止されました。 **PR_CONVERSATION_KEY**の使用、 [PidTagConversationKey 標準プロパティ](pidtagconversationkey-canonical-property.md)は、IPM を検索する場合にのみ、Outlook で保持さ**れます。MessageManager**メッセージ。</span><span class="sxs-lookup"><span data-stu-id="61956-108">The corresponding properties in MAPI to which these TNEF attributes are mapped, PR_CONVERSATION_KEY and PR_PARENT_KEY, have been deprecated in Microsoft Exchange Server: Use of **PR_CONVERSATION_KEY**, the [PidTagConversationKey Canonical Property](pidtagconversationkey-canonical-property.md), persists in Outlook only, for locating **IPM.MessageManager** messages.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="61956-109">注釈</span><span class="sxs-lookup"><span data-stu-id="61956-109">Remarks</span></span>

<span data-ttu-id="61956-110">**PR_CONVERSATION_KEY**プロパティは、 **PR_CONVERSATION_INDEX**、 [PidTagConversationIndex 標準プロパティ](pidtagconversationindex-canonical-property.md)、 **PR_CONVERSATION_TOPIC**、PidTagConversationTopic 標準の precursor のうち、使用されていないものです。 [プロパティ](pidtagconversationtopic-canonical-property.md)。代わりに使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="61956-110">The **PR_CONVERSATION_KEY** property is the otherwise obsolete precursor of the **PR_CONVERSATION_INDEX**, [PidTagConversationIndex Canonical Property](pidtagconversationindex-canonical-property.md) and **PR_CONVERSATION_TOPIC**, [PidTagConversationTopic Canonical Property](pidtagconversationtopic-canonical-property.md), which should be used instead.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="61956-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="61956-111">See also</span></span>

- [<span data-ttu-id="61956-112">IPM サブツリー</span><span class="sxs-lookup"><span data-stu-id="61956-112">IPM Subtree</span></span>](ipm-subtree.md)
- [<span data-ttu-id="61956-113">MAPI の特殊フォルダー</span><span class="sxs-lookup"><span data-stu-id="61956-113">MAPI Special Folders</span></span>](mapi-special-folders.md)

