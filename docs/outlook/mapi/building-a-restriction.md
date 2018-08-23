---
title: 制限を作成します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 12abbd8c-f825-493e-af42-344371d9658e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 3b40c8433f93237db2ae4fd5449fe8a0da486539
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799745"
---
# <a name="building-a-restriction"></a><span data-ttu-id="a09d0-103">制限を作成します。</span><span class="sxs-lookup"><span data-stu-id="a09d0-103">Building a restriction</span></span>

<span data-ttu-id="a09d0-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a09d0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a09d0-105">制限を作成するには、クライアント アプリケーションは、さまざまな種類の 1 つまたは複数の制限の構造の階層を作成して、 [IMAPITable::Restrict](imapitable-restrict.md)または[IMAPITable::FindRow](imapitable-findrow.md)メソッドを階層構造にポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="a09d0-105">To build a restriction, a client application creates a hierarchy of one or more restriction structures of various types and passes a pointer to the hierarchy to the [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) method.</span></span> <span data-ttu-id="a09d0-106">次の図および[制限のサンプル コード](sample-restriction-code.md)のサンプル コードは、さまざまな種類の構造体をリンクの制限を持つ標準的な制限を実装する方法をデモンストレーションします。</span><span class="sxs-lookup"><span data-stu-id="a09d0-106">The illustration that follows and the code sample in [Sample Restriction Code](sample-restriction-code.md) demonstrate how a typical restriction is implemented with linked restriction structures of different types.</span></span> 

<span data-ttu-id="a09d0-107">この例では、クライアント アプリケーションのユーザーは、件名に「バレーボール」という単語が含まれているし、、Sam から政美に送信されたすべてのメッセージを検索するとしています。</span><span class="sxs-lookup"><span data-stu-id="a09d0-107">In this example, a user of a client application is trying to find all messages that contain the word "volleyball" in the subject line and were sent to Sue from Sam.</span></span> <span data-ttu-id="a09d0-108">最初に[SRestriction](srestriction.md)ジェネリック構造体が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="a09d0-108">First, a generic [SRestriction](srestriction.md) structure is allocated.</span></span> <span data-ttu-id="a09d0-109">この構造体の他の[MAPIFreeBuffer](mapifreebuffer.md)を 1 回の呼び出しでリンクされている[SRestriction](srestriction.md)と[SPropValue](spropvalue.md)構造体を解放することができますを作成する[MAPIAllocateMore](mapiallocatemore.md)関数の呼び出しの基盤となります。</span><span class="sxs-lookup"><span data-stu-id="a09d0-109">This structure becomes the basis for other calls to the [MAPIAllocateMore](mapiallocatemore.md) function to create linked [SRestriction](srestriction.md) and [SPropValue](spropvalue.md) structures that can be freed with a single call to [MAPIFreeBuffer](mapifreebuffer.md).</span></span> <span data-ttu-id="a09d0-110">一連のメッセージに適用する基準が 3 つの部分にあるため、最上位レベル制限構造は、**および**制限です。</span><span class="sxs-lookup"><span data-stu-id="a09d0-110">Because the criteria to apply to the set of messages is in three parts, the top level restriction structure is an **AND** restriction.</span></span> <span data-ttu-id="a09d0-111">[SAndRestriction](sandrestriction.md)構造体の**cRes**のメンバーは、評価するために 3 つの制限を示すために 3 に設定されてし、 **lpRes**メンバーが**SRestriction**構造体の 3 つのメンバーの配列を設定します。</span><span class="sxs-lookup"><span data-stu-id="a09d0-111">The [SAndRestriction](sandrestriction.md) structure's **cRes** member is set to 3 to indicate the three restrictions to evaluate and its **lpRes** member is set to a three member array of **SRestriction** structures.</span></span> 
  
<span data-ttu-id="a09d0-112">特定の受信者に送信されたメッセージを検索するには、メッセージ自体ではなく、各メッセージの受信者テーブルを検索する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a09d0-112">To search for messages that are sent to a particular recipient, it is necessary to search the recipient table for each message rather than the message itself.</span></span> <span data-ttu-id="a09d0-113">サブオブジェクトの制限を使用して、受信者テーブルの検索を実行します。</span><span class="sxs-lookup"><span data-stu-id="a09d0-113">A subobject restriction is used to perform the recipient table search.</span></span> <span data-ttu-id="a09d0-114">したがって、 [SSubRestriction](ssubrestriction.md)構造体を配列の要素の最初のメンバーの**ulSubObject**のメンバーでは、 **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) に設定します。</span><span class="sxs-lookup"><span data-stu-id="a09d0-114">Therefore, the first member of the array points to an [SSubRestriction](ssubrestriction.md) structure with its **ulSubObject** member set to **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)).</span></span> <span data-ttu-id="a09d0-115">次に、受信者テーブル内で検索するアイテムを指定するには、コンテンツの制限を使用します。</span><span class="sxs-lookup"><span data-stu-id="a09d0-115">Then, to specify what to look for in the recipient table, a content restriction is used.</span></span> 
  
<span data-ttu-id="a09d0-116">配列の 2 番目と 3 番目のメンバーより簡単です。</span><span class="sxs-lookup"><span data-stu-id="a09d0-116">The second and third members of the array are more straightforward.</span></span> <span data-ttu-id="a09d0-117">両方ともは、コンテンツの制限、構造体、 **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) プロパティが設定された"Sam"と**あるの PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) プロパティに設定されているメッセージを検索する 1 つをポイント」バレーボール。」</span><span class="sxs-lookup"><span data-stu-id="a09d0-117">They both point to content restriction structures, one to search for messages that have a **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) property set to "Sam" and another that has a **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property set to "volleyball."</span></span>
  
<span data-ttu-id="a09d0-118">**実装の制限**</span><span class="sxs-lookup"><span data-stu-id="a09d0-118">**Restriction implementation**</span></span>
  
<span data-ttu-id="a09d0-119">![制限の実装](media/amapi_61.gif "制限の実装")</span><span class="sxs-lookup"><span data-stu-id="a09d0-119">![Restriction implementation](media/amapi_61.gif "Restriction implementation")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a09d0-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="a09d0-120">See also</span></span>

- [<span data-ttu-id="a09d0-121">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="a09d0-121">MAPI Tables</span></span>](mapi-tables.md)

