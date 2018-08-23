---
title: MAPI エントリの識別子
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 84c37696-da7a-42e0-b8c0-29658a6c9a48
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b8212f4a055125858b77ee615a5d929a4a62bb82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801353"
---
# <a name="mapi-entry-identifiers"></a><span data-ttu-id="b3904-103">MAPI エントリの識別子</span><span class="sxs-lookup"><span data-stu-id="b3904-103">MAPI Entry Identifiers</span></span>

  
  
<span data-ttu-id="b3904-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b3904-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b3904-105">エントリの識別子は、一意に識別し、MAPI オブジェクトを開くに使用される[エントリ ID](entryid.md)の構造体に格納されているバイナリのデータの一部です。</span><span class="sxs-lookup"><span data-stu-id="b3904-105">Entry identifiers are pieces of binary data stored in an [ENTRYID](entryid.md) structure that are used to uniquely identify and open a MAPI object.</span></span> <span data-ttu-id="b3904-106">MAPI オブジェクトのほとんどは、エントリ id を持ちます。</span><span class="sxs-lookup"><span data-stu-id="b3904-106">Most MAPI objects have entry identifiers.</span></span> <span data-ttu-id="b3904-107">オブジェクトのエントリ id は、ファイルのファイル名に似ています。</span><span class="sxs-lookup"><span data-stu-id="b3904-107">Entry identifiers for objects are analogous to file names for files.</span></span> <span data-ttu-id="b3904-108">ただし、送信できる、できないに発生したシステム以外のシステムでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="b3904-108">However, they are not transmittable and cannot be used on systems other than the system they originated on.</span></span> 
  
## <a name="entry-identifiers"></a><span data-ttu-id="b3904-109">エントリ ID</span><span class="sxs-lookup"><span data-stu-id="b3904-109">Entry Identifiers</span></span>

<span data-ttu-id="b3904-110">メッセージ ストア プロバイダーでは、エントリ id を割り当てるにメッセージ ・ ストア、フォルダー、およびメッセージです。アドレス帳プロバイダーでは、アドレス帳コンテナー、配布リスト、およびメッセージングのユーザーに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="b3904-110">Message store providers assign entry identifiers to message stores, folders, and messages; address book providers assign them to address book containers, distribution lists, and messaging users.</span></span> <span data-ttu-id="b3904-111">状態テーブル内の状態のオブジェクトなど、テーブル内の行によって表されるオブジェクトを開くには、エントリ id は使用されます。</span><span class="sxs-lookup"><span data-stu-id="b3904-111">Entry identifiers are also used to open an object represented by a row in a table, such as a status object in the status table.</span></span> <span data-ttu-id="b3904-112">オブジェクトは、それぞれのプロパティの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) でそれらのエントリの識別子を格納します。</span><span class="sxs-lookup"><span data-stu-id="b3904-112">Objects store their entry identifiers in their **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="b3904-113">サービス ・ プロバイダーを作成、割り当て、およびエントリの識別子を調べて、クライアント アプリケーションとしてのみ使用してツールのオブジェクトを開くためです。</span><span class="sxs-lookup"><span data-stu-id="b3904-113">Whereas service providers create, assign, and examine entry identifiers, client applications use them only as tools for opening objects.</span></span> <span data-ttu-id="b3904-114">クライアントでは、エントリ id は、不透明なバイナリ データに基になるメッセージング システムとは無関係します。</span><span class="sxs-lookup"><span data-stu-id="b3904-114">To clients, entry identifiers are opaque pieces of binary data and have nothing to do with the underlying messaging system.</span></span> 
  
<span data-ttu-id="b3904-115">クライアントは、その**PR_ENTRYID**プロパティを取得するオブジェクトの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドまたは**PR_ENTRYID**プロパティを保持する列を取得するテーブルの[IMAPITable::QueryColumns](imapitable-querycolumns.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b3904-115">Clients call an object's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_ENTRYID** property or a table's [IMAPITable::QueryColumns](imapitable-querycolumns.md) method to retrieve the column that holds the **PR_ENTRYID** property.</span></span> 
  
<span data-ttu-id="b3904-116">エントリ id は、 **OpenEntry**と**CompareEntryIDs**メソッドにパラメーターとして渡されます。</span><span class="sxs-lookup"><span data-stu-id="b3904-116">Entry identifiers are passed as parameters to the **OpenEntry** and **CompareEntryIDs** methods.</span></span> <span data-ttu-id="b3904-117">MAPI オブジェクトのいくつかは、 **OpenEntry**と**CompareEntryIDs**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="b3904-117">Several MAPI objects implement the **OpenEntry** and **CompareEntryIDs** methods.</span></span> <span data-ttu-id="b3904-118">**OpenEntry**クライアントはオブジェクトを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="b3904-118">With **OpenEntry**, clients can open an object.</span></span> <span data-ttu-id="b3904-119">**CompareEntryIDs**クライアントは同じオブジェクトを参照しているかどうかを決定する 2 つのエントリ id を比較できます。</span><span class="sxs-lookup"><span data-stu-id="b3904-119">With **CompareEntryIDs**, clients can compare two entry identifiers to determine whether they refer to the same object.</span></span> <span data-ttu-id="b3904-120">エントリ id は必ずしもバイナリではないため同等で、クライアントする必要がありますそれらを比較、 **CompareEntryIDs**メソッドによって。</span><span class="sxs-lookup"><span data-stu-id="b3904-120">Because entry identifiers are not necessarily binary comparable, clients must compare them by the **CompareEntryIDs** method.</span></span> 
  
<span data-ttu-id="b3904-121">クライアントは常に成功必然的に配置されたエントリの識別子でサービス ・ プロバイダーへの呼び出しが、サービス プロバイダーは、任意に調整されているエントリの識別子を処理する必要があります、これが常に大文字と小文字。</span><span class="sxs-lookup"><span data-stu-id="b3904-121">Clients should always pass naturally aligned entry identifiers in their calls to service providers, because although service providers should handle entry identifiers that are arbitrarily aligned, this is not always the case.</span></span> <span data-ttu-id="b3904-122">自然にアラインメントされたメモリ アドレスでは、整列エラーを生成することがなくそのアドレスをサポートしている任意のデータ型にアクセスするコンピューターを使用できます。</span><span class="sxs-lookup"><span data-stu-id="b3904-122">A naturally aligned memory address enables the computer to access any data type it supports at that address without generating an alignment fault.</span></span> <span data-ttu-id="b3904-123">自然配列の要素は、通常、システムのメモリ アロケーターによって使用される同じ配置係数、通常 8 バイトです。</span><span class="sxs-lookup"><span data-stu-id="b3904-123">The natural alignment factor is typically the same alignment factor used by the system memory allocator and is usually 8 bytes.</span></span>
  
<span data-ttu-id="b3904-124">エントリの識別子には 2 つのタイプ: 短期および長期的な。</span><span class="sxs-lookup"><span data-stu-id="b3904-124">Entry identifiers come in two types: short-term and long-term.</span></span> <span data-ttu-id="b3904-125">短期的なエントリ id は、構成する際、高速ですが、現在のセッションの現在のワークステーションの寿命を延ばす上でのみ、一意性が保証されます。</span><span class="sxs-lookup"><span data-stu-id="b3904-125">Short-term entry identifiers are faster to construct, but their uniqueness is guaranteed only over the life of the current session on the current workstation.</span></span> <span data-ttu-id="b3904-126">長期のエントリ id より長寿命があります。</span><span class="sxs-lookup"><span data-stu-id="b3904-126">Long-term entry identifiers have a more prolonged lifespan.</span></span> <span data-ttu-id="b3904-127">短期的なエントリ id は、多くのオブジェクト、フォルダー、メッセージなどの長期のエントリ id を使用し、配布リストが、テーブル内の行と、ダイアログ ボックス内のエントリの主に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b3904-127">Short-term entry identifiers are used primarily for rows in tables and entries in dialog boxes, whereas long-term entry identifiers are used for many objects such as messages, folders, and distribution lists.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b3904-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="b3904-128">See also</span></span>



<span data-ttu-id="b3904-129">[MAPI �A�v���P�[�V�����̊J��](mapi-application-development.md)</span><span class="sxs-lookup"><span data-stu-id="b3904-129">[MAPI Application Development](mapi-application-development.md)</span></span>

