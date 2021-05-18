---
title: アドレス帳通知の処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0dc4bb48-c8a1-447f-9e38-1c234a358fca
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 122e50328272a4009e5a129233d449613817dfc8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413536"
---
# <a name="handing-address-book-notification"></a><span data-ttu-id="d34c8-103">アドレス帳通知の処理</span><span class="sxs-lookup"><span data-stu-id="d34c8-103">Handing address book notification</span></span>
  
<span data-ttu-id="d34c8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d34c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d34c8-105">アドレス帳通知を使用すると、クライアントは、任意のアドレス帳エントリまたは特定のエントリに発生するイベントを学習できます。</span><span class="sxs-lookup"><span data-stu-id="d34c8-105">Address book notifications allow a client to learn of events that occur to any address book entry or to a particular entry.</span></span> <span data-ttu-id="d34c8-106">これらの通知に登録するには、MAPI アドレス帳を使用して [IAddrBook::Advise](iaddrbook-advise.md) を呼び出するか [、IMAPITable::Advise](imapitable-advise.md)を呼び出してアドレス帳コンテナーの階層またはコンテンツ テーブルを使用します。</span><span class="sxs-lookup"><span data-stu-id="d34c8-106">You can register for these notifications either through the MAPI address book by calling [IAddrBook::Advise](iaddrbook-advise.md) or through an address book container's hierarchy or contents table by calling [IMAPITable::Advise](imapitable-advise.md).</span></span> 
  
<span data-ttu-id="d34c8-107">特定のエントリの通知に登録する場合はアドレス帳コンテナー、配布リスト、またはメッセージング ユーザーのエントリ識別子を指定し、アドレス帳全体で通知に登録する場合は NULL を指定します。</span><span class="sxs-lookup"><span data-stu-id="d34c8-107">Specify the entry identifier of an address book container, distribution list, or messaging user if you are registering for notifications on a particular entry and NULL if registering for notifications on the entire address book.</span></span> <span data-ttu-id="d34c8-108">エントリ識別子は、アドレス帳コンテナー内のメッセージング ユーザーまたは配布リストを表す必要があります。</span><span class="sxs-lookup"><span data-stu-id="d34c8-108">The entry identifier must represent a messaging user or distribution list in an address book container.</span></span> <span data-ttu-id="d34c8-109">**IAddrBook::Advise** は、このエントリ識別子を調べて、対応するオブジェクトを担当するアドレス帳プロバイダーを特定し、適切なアドレス帳プロバイダーの [IABLogon::Advise](iablogon-advise.md) メソッドに呼び出しを転送します。</span><span class="sxs-lookup"><span data-stu-id="d34c8-109">**IAddrBook::Advise** examines this entry identifier to determine which address book provider is responsible for the corresponding object and forwards the call to the appropriate address book provider's [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
<span data-ttu-id="d34c8-110">クライアントは、アドレス帳エントリで次の種類のイベントに登録できます。</span><span class="sxs-lookup"><span data-stu-id="d34c8-110">Clients can register for the following types of events on address book entries:</span></span>
  
- <span data-ttu-id="d34c8-111">重大なエラー</span><span class="sxs-lookup"><span data-stu-id="d34c8-111">Critical error</span></span>
    
- <span data-ttu-id="d34c8-112">オブジェクト イベント (作成、変更、削除、移動、またはコピー)</span><span class="sxs-lookup"><span data-stu-id="d34c8-112">Any of the object events (created, modified, deleted, moved, or copied)</span></span>
    
- <span data-ttu-id="d34c8-113">変更されたテーブル</span><span class="sxs-lookup"><span data-stu-id="d34c8-113">Table modified</span></span>
    
<span data-ttu-id="d34c8-114">通常、登録はアドレス帳コンテナーの内容と階層テーブルでのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="d34c8-114">Typically, registration occurs only on address book container contents and hierarchy tables.</span></span> <span data-ttu-id="d34c8-115">クライアントが下位レベルのメッセージング ユーザーおよび配布リスト オブジェクトに登録されるのはまれです。</span><span class="sxs-lookup"><span data-stu-id="d34c8-115">It is rare that clients register with the lower level messaging user and distribution list objects.</span></span> <span data-ttu-id="d34c8-116">これは、次の理由が理由です。</span><span class="sxs-lookup"><span data-stu-id="d34c8-116">This is because:</span></span>
  
- <span data-ttu-id="d34c8-117">多くのアドレス帳プロバイダーは、メッセージング ユーザーと配布リストの通知をサポートしていない。</span><span class="sxs-lookup"><span data-stu-id="d34c8-117">Many address book providers do not support notifications on their messaging users and distribution lists.</span></span>
    
- <span data-ttu-id="d34c8-118">テーブル通知は、変更を追跡し、ユーザーに報告するのに十分です。</span><span class="sxs-lookup"><span data-stu-id="d34c8-118">Table notifications are sufficient for tracking changes and reporting them to users.</span></span>
    

