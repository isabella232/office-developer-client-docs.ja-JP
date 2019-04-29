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
# <a name="mapi-entry-identifiers"></a><span data-ttu-id="c77fe-103">MAPI エントリ識別子</span><span class="sxs-lookup"><span data-stu-id="c77fe-103">MAPI Entry Identifiers</span></span>

  
  
<span data-ttu-id="c77fe-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c77fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c77fe-105">エントリ識別子は、MAPI オブジェクトを一意に識別して開くために使用される[ENTRYID](entryid.md)構造体に格納されるバイナリデータの一部です。</span><span class="sxs-lookup"><span data-stu-id="c77fe-105">Entry identifiers are pieces of binary data stored in an [ENTRYID](entryid.md) structure that are used to uniquely identify and open a MAPI object.</span></span> <span data-ttu-id="c77fe-106">ほとんどの MAPI オブジェクトには、エントリ識別子があります。</span><span class="sxs-lookup"><span data-stu-id="c77fe-106">Most MAPI objects have entry identifiers.</span></span> <span data-ttu-id="c77fe-107">オブジェクトのエントリ識別子は、ファイルのファイル名に似ています。</span><span class="sxs-lookup"><span data-stu-id="c77fe-107">Entry identifiers for objects are analogous to file names for files.</span></span> <span data-ttu-id="c77fe-108">ただし、これらは、送信されたシステム以外のシステムでは、送信テーブルではないため、使用できません。</span><span class="sxs-lookup"><span data-stu-id="c77fe-108">However, they are not transmittable and cannot be used on systems other than the system they originated on.</span></span> 
  
## <a name="entry-identifiers"></a><span data-ttu-id="c77fe-109">エントリ識別子</span><span class="sxs-lookup"><span data-stu-id="c77fe-109">Entry Identifiers</span></span>

<span data-ttu-id="c77fe-110">メッセージストアプロバイダーは、メッセージストア、フォルダー、およびメッセージにエントリ id を割り当てます。アドレス帳プロバイダーは、アドレス帳コンテナー、配布リスト、およびメッセージングユーザーにそれらを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="c77fe-110">Message store providers assign entry identifiers to message stores, folders, and messages; address book providers assign them to address book containers, distribution lists, and messaging users.</span></span> <span data-ttu-id="c77fe-111">[状態] テーブル内の status オブジェクトなど、テーブル内の行で表されるオブジェクトを開くには、エントリ識別子も使用されます。</span><span class="sxs-lookup"><span data-stu-id="c77fe-111">Entry identifiers are also used to open an object represented by a row in a table, such as a status object in the status table.</span></span> <span data-ttu-id="c77fe-112">オブジェクトは、エントリ id を**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティに格納します。</span><span class="sxs-lookup"><span data-stu-id="c77fe-112">Objects store their entry identifiers in their **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="c77fe-113">サービスプロバイダーは、エントリ識別子の作成、割り当て、および調査を行いますが、クライアントアプリケーションはオブジェクトを開くためのツールとしてのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="c77fe-113">Whereas service providers create, assign, and examine entry identifiers, client applications use them only as tools for opening objects.</span></span> <span data-ttu-id="c77fe-114">クライアントにとって、エントリ識別子は非透過バイナリデータであり、基になるメッセージングシステムとは何も実行しません。</span><span class="sxs-lookup"><span data-stu-id="c77fe-114">To clients, entry identifiers are opaque pieces of binary data and have nothing to do with the underlying messaging system.</span></span> 
  
<span data-ttu-id="c77fe-115">クライアントはオブジェクトの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、 **PR_ENTRYID**プロパティを取得するか、またはテーブルの[IMAPITable:: querycolumns](imapitable-querycolumns.md)メソッドを呼び出して、 **PR_ENTRYID**プロパティを保持する列を取得します。</span><span class="sxs-lookup"><span data-stu-id="c77fe-115">Clients call an object's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_ENTRYID** property or a table's [IMAPITable::QueryColumns](imapitable-querycolumns.md) method to retrieve the column that holds the **PR_ENTRYID** property.</span></span> 
  
<span data-ttu-id="c77fe-116">エントリ識別子は、 **openentry**および**compareentryids**メソッドにパラメーターとして渡されます。</span><span class="sxs-lookup"><span data-stu-id="c77fe-116">Entry identifiers are passed as parameters to the **OpenEntry** and **CompareEntryIDs** methods.</span></span> <span data-ttu-id="c77fe-117">いくつかの MAPI オブジェクトは、 **openentry**メソッドと**compareentryids**メソッドを実装しています。</span><span class="sxs-lookup"><span data-stu-id="c77fe-117">Several MAPI objects implement the **OpenEntry** and **CompareEntryIDs** methods.</span></span> <span data-ttu-id="c77fe-118">**openentry**を使用すると、クライアントはオブジェクトを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="c77fe-118">With **OpenEntry**, clients can open an object.</span></span> <span data-ttu-id="c77fe-119">**compareentryids**を使用すると、クライアントは2つのエントリ識別子を比較して、同じオブジェクトを参照しているかどうかを判断できます。</span><span class="sxs-lookup"><span data-stu-id="c77fe-119">With **CompareEntryIDs**, clients can compare two entry identifiers to determine whether they refer to the same object.</span></span> <span data-ttu-id="c77fe-120">エントリ識別子は必ずしも二項比較ではないため、クライアントは**compareentryids**メソッドで比較する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c77fe-120">Because entry identifiers are not necessarily binary comparable, clients must compare them by the **CompareEntryIDs** method.</span></span> 
  
<span data-ttu-id="c77fe-121">サービスプロバイダーは任意に配置されたエントリ識別子を処理する必要があるので、クライアントは常にサービスプロバイダーへの呼び出しで、自然に配置されたエントリ識別子を渡す必要があります。これは常に該当するわけではありません。</span><span class="sxs-lookup"><span data-stu-id="c77fe-121">Clients should always pass naturally aligned entry identifiers in their calls to service providers, because although service providers should handle entry identifiers that are arbitrarily aligned, this is not always the case.</span></span> <span data-ttu-id="c77fe-122">自然に配置されたメモリアドレスを使用すると、コンピューターは、配置エラーを生成せずに、そのアドレスでサポートされているデータ型にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="c77fe-122">A naturally aligned memory address enables the computer to access any data type it supports at that address without generating an alignment fault.</span></span> <span data-ttu-id="c77fe-123">通常、自然配置係数は、システムメモリアロケーターで使用される配置要素と同じで、通常は8バイトです。</span><span class="sxs-lookup"><span data-stu-id="c77fe-123">The natural alignment factor is typically the same alignment factor used by the system memory allocator and is usually 8 bytes.</span></span>
  
<span data-ttu-id="c77fe-124">エントリ識別子には、短期的および長期間の2種類があります。</span><span class="sxs-lookup"><span data-stu-id="c77fe-124">Entry identifiers come in two types: short-term and long-term.</span></span> <span data-ttu-id="c77fe-125">短期間のエントリ識別子は、構築に高速になりますが、その一意性は現在のワークステーション上の現在のセッションが終了するまでのみ保証されます。</span><span class="sxs-lookup"><span data-stu-id="c77fe-125">Short-term entry identifiers are faster to construct, but their uniqueness is guaranteed only over the life of the current session on the current workstation.</span></span> <span data-ttu-id="c77fe-126">長期のエントリ識別子は、寿命が長くなります。</span><span class="sxs-lookup"><span data-stu-id="c77fe-126">Long-term entry identifiers have a more prolonged lifespan.</span></span> <span data-ttu-id="c77fe-127">短い用語エントリ識別子は、主にテーブル内の行やダイアログボックスのエントリに使用されますが、長い用語の入力識別子は、メッセージ、フォルダー、配布リストなどの多くのオブジェクトで使用されます。</span><span class="sxs-lookup"><span data-stu-id="c77fe-127">Short-term entry identifiers are used primarily for rows in tables and entries in dialog boxes, whereas long-term entry identifiers are used for many objects such as messages, folders, and distribution lists.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c77fe-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="c77fe-128">See also</span></span>



[<span data-ttu-id="c77fe-129">MAPI アプリケーションの開発</span><span class="sxs-lookup"><span data-stu-id="c77fe-129">MAPI Application Development</span></span>](mapi-application-development.md)

