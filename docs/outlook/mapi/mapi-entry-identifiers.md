---
title: MAPI エントリ識別子
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 84c37696-da7a-42e0-b8c0-29658a6c9a48
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4c414b9f8a1d70fd5eea94da326674a749ccefe2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414964"
---
# <a name="mapi-entry-identifiers"></a><span data-ttu-id="7b463-103">MAPI エントリ識別子</span><span class="sxs-lookup"><span data-stu-id="7b463-103">MAPI Entry Identifiers</span></span>

  
  
<span data-ttu-id="7b463-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b463-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b463-105">エントリ識別子は、MAPI オブジェクトを一意に識別して開くために使用される [ENTRYID](entryid.md) 構造に格納されたバイナリ データの一部です。</span><span class="sxs-lookup"><span data-stu-id="7b463-105">Entry identifiers are pieces of binary data stored in an [ENTRYID](entryid.md) structure that are used to uniquely identify and open a MAPI object.</span></span> <span data-ttu-id="7b463-106">ほとんどの MAPI オブジェクトには、エントリ識別子があります。</span><span class="sxs-lookup"><span data-stu-id="7b463-106">Most MAPI objects have entry identifiers.</span></span> <span data-ttu-id="7b463-107">オブジェクトのエントリ識別子は、ファイルのファイル名に類似しています。</span><span class="sxs-lookup"><span data-stu-id="7b463-107">Entry identifiers for objects are analogous to file names for files.</span></span> <span data-ttu-id="7b463-108">ただし、送信可能ではなく、発信元のシステム以外のシステムでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="7b463-108">However, they are not transmittable and cannot be used on systems other than the system they originated on.</span></span> 
  
## <a name="entry-identifiers"></a><span data-ttu-id="7b463-109">エントリ識別子</span><span class="sxs-lookup"><span data-stu-id="7b463-109">Entry Identifiers</span></span>

<span data-ttu-id="7b463-110">メッセージ ストア プロバイダーは、エントリ識別子をメッセージ ストア、フォルダー、およびメッセージに割り当てる。アドレス帳プロバイダーは、アドレス帳コンテナー、配布リスト、およびメッセージング ユーザーに割り当てる。</span><span class="sxs-lookup"><span data-stu-id="7b463-110">Message store providers assign entry identifiers to message stores, folders, and messages; address book providers assign them to address book containers, distribution lists, and messaging users.</span></span> <span data-ttu-id="7b463-111">エントリ識別子は、テーブル内の行で表されるオブジェクト (状態テーブルの状態オブジェクトなど) を開く場合にも使用されます。</span><span class="sxs-lookup"><span data-stu-id="7b463-111">Entry identifiers are also used to open an object represented by a row in a table, such as a status object in the status table.</span></span> <span data-ttu-id="7b463-112">オブジェクトは、エントリ識別子をプロパティ **(** [PidTagEntryId](pidtagentryid-canonical-property.md)) PR_ENTRYIDに格納します。</span><span class="sxs-lookup"><span data-stu-id="7b463-112">Objects store their entry identifiers in their **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="7b463-113">サービス プロバイダーはエントリ識別子を作成、割り当て、および確認しますが、クライアント アプリケーションはオブジェクトを開くツールとしてのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="7b463-113">Whereas service providers create, assign, and examine entry identifiers, client applications use them only as tools for opening objects.</span></span> <span data-ttu-id="7b463-114">クライアントでは、エントリ識別子はバイナリ データの不透明な部分であり、基になるメッセージング システムとは何の関係もありません。</span><span class="sxs-lookup"><span data-stu-id="7b463-114">To clients, entry identifiers are opaque pieces of binary data and have nothing to do with the underlying messaging system.</span></span> 
  
<span data-ttu-id="7b463-115">クライアントは、オブジェクトの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出して **、PR_ENTRYID** プロパティまたはテーブルの [IMAPITable::QueryColumns](imapitable-querycolumns.md) メソッドを取得して **、PR_ENTRYID** プロパティを保持する列を取得します。</span><span class="sxs-lookup"><span data-stu-id="7b463-115">Clients call an object's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_ENTRYID** property or a table's [IMAPITable::QueryColumns](imapitable-querycolumns.md) method to retrieve the column that holds the **PR_ENTRYID** property.</span></span> 
  
<span data-ttu-id="7b463-116">エントリ識別子は **、OpenEntry** メソッドと **CompareEntryIDs** メソッドにパラメーターとして渡されます。</span><span class="sxs-lookup"><span data-stu-id="7b463-116">Entry identifiers are passed as parameters to the **OpenEntry** and **CompareEntryIDs** methods.</span></span> <span data-ttu-id="7b463-117">いくつかの MAPI オブジェクトは **、OpenEntry メソッドと** **CompareEntryIDs** メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="7b463-117">Several MAPI objects implement the **OpenEntry** and **CompareEntryIDs** methods.</span></span> <span data-ttu-id="7b463-118">**OpenEntry を使用すると**、クライアントはオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="7b463-118">With **OpenEntry**, clients can open an object.</span></span> <span data-ttu-id="7b463-119">**CompareEntryIDs を使用** すると、クライアントは 2 つのエントリ識別子を比較して、同じオブジェクトを参照するかどうかを判断できます。</span><span class="sxs-lookup"><span data-stu-id="7b463-119">With **CompareEntryIDs**, clients can compare two entry identifiers to determine whether they refer to the same object.</span></span> <span data-ttu-id="7b463-120">エントリ識別子はバイナリと比較できるとは限らないので、クライアントは **CompareEntryIDs** メソッドで比較する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b463-120">Because entry identifiers are not necessarily binary comparable, clients must compare them by the **CompareEntryIDs** method.</span></span> 
  
<span data-ttu-id="7b463-121">サービス プロバイダーは任意に配置されたエントリ識別子を処理する必要があるが、必ずしもそうではないので、クライアントはサービス プロバイダーへの呼び出しで自然に配置されたエントリ識別子を常に渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b463-121">Clients should always pass naturally aligned entry identifiers in their calls to service providers, because although service providers should handle entry identifiers that are arbitrarily aligned, this is not always the case.</span></span> <span data-ttu-id="7b463-122">自然に配置されたメモリ アドレスを使用すると、コンピューターは、そのアドレスでサポートしている任意のデータ型に、配置エラーを生成せずにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="7b463-122">A naturally aligned memory address enables the computer to access any data type it supports at that address without generating an alignment fault.</span></span> <span data-ttu-id="7b463-123">自然な配置係数は、通常、システム メモリ アロケーターで使用されるのと同じ配置係数で、通常は 8 バイトです。</span><span class="sxs-lookup"><span data-stu-id="7b463-123">The natural alignment factor is typically the same alignment factor used by the system memory allocator and is usually 8 bytes.</span></span>
  
<span data-ttu-id="7b463-124">エントリ識別子には、短期と長期の 2 種類があります。</span><span class="sxs-lookup"><span data-stu-id="7b463-124">Entry identifiers come in two types: short-term and long-term.</span></span> <span data-ttu-id="7b463-125">短期的なエントリ識別子は、作成が高速ですが、その一意性は、現在のワークステーション上の現在のセッションの期間でのみ保証されます。</span><span class="sxs-lookup"><span data-stu-id="7b463-125">Short-term entry identifiers are faster to construct, but their uniqueness is guaranteed only over the life of the current session on the current workstation.</span></span> <span data-ttu-id="7b463-126">長期的なエントリ識別子の寿命は長持ちします。</span><span class="sxs-lookup"><span data-stu-id="7b463-126">Long-term entry identifiers have a more prolonged lifespan.</span></span> <span data-ttu-id="7b463-127">短期的なエントリ識別子は、主にテーブル内の行とダイアログ ボックス内のエントリに使用されます。一方、長期エントリ識別子は、メッセージ、フォルダー、配布リストなどの多くのオブジェクトに使用されます。</span><span class="sxs-lookup"><span data-stu-id="7b463-127">Short-term entry identifiers are used primarily for rows in tables and entries in dialog boxes, whereas long-term entry identifiers are used for many objects such as messages, folders, and distribution lists.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7b463-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="7b463-128">See also</span></span>



[<span data-ttu-id="7b463-129">MAPI アプリケーション開発</span><span class="sxs-lookup"><span data-stu-id="7b463-129">MAPI Application Development</span></span>](mapi-application-development.md)

