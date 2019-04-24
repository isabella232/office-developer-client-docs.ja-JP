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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318262"
---
# <a name="building-a-restriction"></a><span data-ttu-id="0d545-103">制限の作成</span><span class="sxs-lookup"><span data-stu-id="0d545-103">Building a restriction</span></span>

<span data-ttu-id="0d545-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d545-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d545-105">制限を構築するために、クライアントアプリケーションは、さまざまな種類の1つ以上の制限構造から成る階層構造を作成し、その階層へのポインターを[imapitable:: Restrict](imapitable-restrict.md)または[imapitable:: FindRow](imapitable-findrow.md)メソッドに渡します。</span><span class="sxs-lookup"><span data-stu-id="0d545-105">To build a restriction, a client application creates a hierarchy of one or more restriction structures of various types and passes a pointer to the hierarchy to the [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) method.</span></span> <span data-ttu-id="0d545-106">次の図と[サンプル](sample-restriction-code.md)コードのコードサンプルでは、さまざまな種類のリンクされた制限構造を使用して一般的な制限を実装する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0d545-106">The illustration that follows and the code sample in [Sample Restriction Code](sample-restriction-code.md) demonstrate how a typical restriction is implemented with linked restriction structures of different types.</span></span> 

<span data-ttu-id="0d545-107">この例では、クライアントアプリケーションのユーザーが、題名行に "" という単語 "を含むすべてのメッセージを検索しようとしていますが、Sam から政美に送信されています。</span><span class="sxs-lookup"><span data-stu-id="0d545-107">In this example, a user of a client application is trying to find all messages that contain the word "volleyball" in the subject line and were sent to Sue from Sam.</span></span> <span data-ttu-id="0d545-108">最初に、一般的な[srestriction](srestriction.md)構造が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="0d545-108">First, a generic [SRestriction](srestriction.md) structure is allocated.</span></span> <span data-ttu-id="0d545-109">この構造体は、 [MAPIFreeBuffer](mapifreebuffer.md)への1回の呼び出しで解放できるリンクされた[srestriction](srestriction.md)および[spropvalue](spropvalue.md)構造を作成するための、 [MAPIAllocateMore](mapiallocatemore.md)関数への他の呼び出しの基礎となります。</span><span class="sxs-lookup"><span data-stu-id="0d545-109">This structure becomes the basis for other calls to the [MAPIAllocateMore](mapiallocatemore.md) function to create linked [SRestriction](srestriction.md) and [SPropValue](spropvalue.md) structures that can be freed with a single call to [MAPIFreeBuffer](mapifreebuffer.md).</span></span> <span data-ttu-id="0d545-110">一連のメッセージに適用する条件は3つの部分に分けられるため、最上位の制限構造は、**および**制限です。</span><span class="sxs-lookup"><span data-stu-id="0d545-110">Because the criteria to apply to the set of messages is in three parts, the top level restriction structure is an **AND** restriction.</span></span> <span data-ttu-id="0d545-111">[SAndRestriction](sandrestriction.md)構造体の**cres**メンバーは3に設定されており、評価する3つの制限を示し、その**lpres**メンバーは、**制限**構造の3つのメンバー配列に設定されています。</span><span class="sxs-lookup"><span data-stu-id="0d545-111">The [SAndRestriction](sandrestriction.md) structure's **cRes** member is set to 3 to indicate the three restrictions to evaluate and its **lpRes** member is set to a three member array of **SRestriction** structures.</span></span> 
  
<span data-ttu-id="0d545-112">特定の受信者に送信されたメッセージを検索するには、メッセージ自体ではなく、メッセージごとに受信者テーブルを検索する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d545-112">To search for messages that are sent to a particular recipient, it is necessary to search the recipient table for each message rather than the message itself.</span></span> <span data-ttu-id="0d545-113">サブテーブルの制限は、受信者テーブルの検索を実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="0d545-113">A subobject restriction is used to perform the recipient table search.</span></span> <span data-ttu-id="0d545-114">そのため、配列の最初のメンバーは、ulsubmember を**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) に設定した\*\*\*\* [ssubrestriction](ssubrestriction.md)構造体を指します。</span><span class="sxs-lookup"><span data-stu-id="0d545-114">Therefore, the first member of the array points to an [SSubRestriction](ssubrestriction.md) structure with its **ulSubObject** member set to **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)).</span></span> <span data-ttu-id="0d545-115">次に、recipient テーブルで検索する内容を指定するために、コンテンツ制限が使用されます。</span><span class="sxs-lookup"><span data-stu-id="0d545-115">Then, to specify what to look for in the recipient table, a content restriction is used.</span></span> 
  
<span data-ttu-id="0d545-116">配列の2番目と3番目のメンバーは、より簡単です。</span><span class="sxs-lookup"><span data-stu-id="0d545-116">The second and third members of the array are more straightforward.</span></span> <span data-ttu-id="0d545-117">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) プロパティが "Sam" に設定されており、もう一方が**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) プロパティが "" に設定されている別のメッセージを検索するために、コンテンツ制限構造をポイントしています。""</span><span class="sxs-lookup"><span data-stu-id="0d545-117">They both point to content restriction structures, one to search for messages that have a **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) property set to "Sam" and another that has a **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property set to "volleyball."</span></span>
  
<span data-ttu-id="0d545-118">**実装の制限**</span><span class="sxs-lookup"><span data-stu-id="0d545-118">**Restriction implementation**</span></span>
  
<span data-ttu-id="0d545-119">![制限の実装](media/amapi_61.gif "制限の実装")</span><span class="sxs-lookup"><span data-stu-id="0d545-119">![Restriction implementation](media/amapi_61.gif "Restriction implementation")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0d545-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="0d545-120">See also</span></span>

- [<span data-ttu-id="0d545-121">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="0d545-121">MAPI Tables</span></span>](mapi-tables.md)

