---
title: 制限の作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 12abbd8c-f825-493e-af42-344371d9658e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 38182abd922cd5806a14b6541c22ce675b997387
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422511"
---
# <a name="building-a-restriction"></a><span data-ttu-id="079d0-103">制限の作成</span><span class="sxs-lookup"><span data-stu-id="079d0-103">Building a restriction</span></span>

<span data-ttu-id="079d0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="079d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="079d0-105">制限を構築するために、クライアント アプリケーションは、さまざまな種類の 1 つ以上の制限構造の階層を作成し、階層へのポインターを [IMAPITable::Restrict](imapitable-restrict.md) メソッドまたは [IMAPITable::FindRow](imapitable-findrow.md) メソッドに渡します。</span><span class="sxs-lookup"><span data-stu-id="079d0-105">To build a restriction, a client application creates a hierarchy of one or more restriction structures of various types and passes a pointer to the hierarchy to the [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) method.</span></span> <span data-ttu-id="079d0-106">次の図とサンプル制限コードのコード[](sample-restriction-code.md)サンプルは、さまざまな種類のリンクされた制限構造で一般的な制限がどのように実装されるのか示しています。</span><span class="sxs-lookup"><span data-stu-id="079d0-106">The illustration that follows and the code sample in [Sample Restriction Code](sample-restriction-code.md) demonstrate how a typical restriction is implemented with linked restriction structures of different types.</span></span> 

<span data-ttu-id="079d0-107">この例では、クライアント アプリケーションのユーザーが、件名行に "バレー" という単語を含み、Sam から Sue に送信されたメッセージを検索します。</span><span class="sxs-lookup"><span data-stu-id="079d0-107">In this example, a user of a client application is trying to find all messages that contain the word "volleyball" in the subject line and were sent to Sue from Sam.</span></span> <span data-ttu-id="079d0-108">最初に、 [汎用の SRestriction 構造体](srestriction.md) が割り当てられている。</span><span class="sxs-lookup"><span data-stu-id="079d0-108">First, a generic [SRestriction](srestriction.md) structure is allocated.</span></span> <span data-ttu-id="079d0-109">この構造体は[、MAPIAllocateMore](mapiallocatemore.md)関数への他の呼び出しの基礎になり[、MAPIFreeBuffer](mapifreebuffer.md)への 1 回の呼び出しで解放できるリンク[された SRestriction](srestriction.md)構造体と[SPropValue](spropvalue.md)構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="079d0-109">This structure becomes the basis for other calls to the [MAPIAllocateMore](mapiallocatemore.md) function to create linked [SRestriction](srestriction.md) and [SPropValue](spropvalue.md) structures that can be freed with a single call to [MAPIFreeBuffer](mapifreebuffer.md).</span></span> <span data-ttu-id="079d0-110">メッセージのセットに適用する条件は 3 つの部分にあるため、トップ レベルの制限構造は **AND** 制限です。</span><span class="sxs-lookup"><span data-stu-id="079d0-110">Because the criteria to apply to the set of messages is in three parts, the top level restriction structure is an **AND** restriction.</span></span> <span data-ttu-id="079d0-111">[SAndRestriction](sandrestriction.md)構造体の **cRes** メンバーは 3 に設定され、評価する 3 つの制限を示し **、lpRes** メンバーは **SRestriction** 構造体の 3 つのメンバー配列に設定されます。</span><span class="sxs-lookup"><span data-stu-id="079d0-111">The [SAndRestriction](sandrestriction.md) structure's **cRes** member is set to 3 to indicate the three restrictions to evaluate and its **lpRes** member is set to a three member array of **SRestriction** structures.</span></span> 
  
<span data-ttu-id="079d0-112">特定の受信者に送信されるメッセージを検索するには、メッセージ自体ではなく、メッセージごとに受信者テーブルを検索する必要があります。</span><span class="sxs-lookup"><span data-stu-id="079d0-112">To search for messages that are sent to a particular recipient, it is necessary to search the recipient table for each message rather than the message itself.</span></span> <span data-ttu-id="079d0-113">サブオブジェクトの制限は、受信者テーブルの検索を実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="079d0-113">A subobject restriction is used to perform the recipient table search.</span></span> <span data-ttu-id="079d0-114">したがって、配列の最初のメンバーは **、ulSubObject** メンバーが PR_MESSAGE_RECIPIENTS **(** [PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)に設定された [SSubRestriction](ssubrestriction.md)構造体をポイントします。</span><span class="sxs-lookup"><span data-stu-id="079d0-114">Therefore, the first member of the array points to an [SSubRestriction](ssubrestriction.md) structure with its **ulSubObject** member set to **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)).</span></span> <span data-ttu-id="079d0-115">次に、受信者テーブルで検索する内容を指定するために、コンテンツ制限が使用されます。</span><span class="sxs-lookup"><span data-stu-id="079d0-115">Then, to specify what to look for in the recipient table, a content restriction is used.</span></span> 
  
<span data-ttu-id="079d0-116">配列の 2 番目と 3 番目のメンバーは、より簡単です。</span><span class="sxs-lookup"><span data-stu-id="079d0-116">The second and third members of the array are more straightforward.</span></span> <span data-ttu-id="079d0-117">どちらもコンテンツ制限構造を指し示し、PR_SENDER_NAME ([PidTagSenderName](pidtagsendername-canonical-property.md)) プロパティが "Sam" に設定されているメッセージと **、PR_SUBJECT** **(** [PidTagSubject](pidtagsubject-canonical-property.md)) プロパティが "バレーボール" に設定されているメッセージを検索します。</span><span class="sxs-lookup"><span data-stu-id="079d0-117">They both point to content restriction structures, one to search for messages that have a **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) property set to "Sam" and another that has a **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property set to "volleyball."</span></span>
  
<span data-ttu-id="079d0-118">**実装の制限**</span><span class="sxs-lookup"><span data-stu-id="079d0-118">**Restriction implementation**</span></span>
  
<span data-ttu-id="079d0-119">![制限の実装](media/amapi_61.gif "制限の実装")</span><span class="sxs-lookup"><span data-stu-id="079d0-119">![Restriction implementation](media/amapi_61.gif "Restriction implementation")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="079d0-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="079d0-120">See also</span></span>

- [<span data-ttu-id="079d0-121">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="079d0-121">MAPI Tables</span></span>](mapi-tables.md)

