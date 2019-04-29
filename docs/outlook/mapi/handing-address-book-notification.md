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
# <a name="handing-address-book-notification"></a><span data-ttu-id="5f04d-103">アドレス帳通知の処理</span><span class="sxs-lookup"><span data-stu-id="5f04d-103">Handing address book notification</span></span>
  
<span data-ttu-id="5f04d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f04d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f04d-105">アドレス帳の通知により、クライアントは、アドレス帳のエントリまたは特定のエントリに発生するイベントを知ることができます。</span><span class="sxs-lookup"><span data-stu-id="5f04d-105">Address book notifications allow a client to learn of events that occur to any address book entry or to a particular entry.</span></span> <span data-ttu-id="5f04d-106">これらの通知は、 [IAddrBook:: advise](iaddrbook-advise.md)を呼び出すことによって、またはアドレス帳コンテナーの hierarchy または contents テーブルによって、 [IMAPITable:: advise](imapitable-advise.md)を呼び出すことによって登録できます。</span><span class="sxs-lookup"><span data-stu-id="5f04d-106">You can register for these notifications either through the MAPI address book by calling [IAddrBook::Advise](iaddrbook-advise.md) or through an address book container's hierarchy or contents table by calling [IMAPITable::Advise](imapitable-advise.md).</span></span> 
  
<span data-ttu-id="5f04d-107">特定のエントリに対して登録する場合は、アドレス帳のコンテナー、配布リスト、またはメッセージングユーザーのエントリ識別子を指定し、アドレス帳全体に通知を登録する場合は NULL を指定します。</span><span class="sxs-lookup"><span data-stu-id="5f04d-107">Specify the entry identifier of an address book container, distribution list, or messaging user if you are registering for notifications on a particular entry and NULL if registering for notifications on the entire address book.</span></span> <span data-ttu-id="5f04d-108">エントリ識別子は、アドレス帳コンテナー内のメッセージングユーザーまたは配布リストを表す必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f04d-108">The entry identifier must represent a messaging user or distribution list in an address book container.</span></span> <span data-ttu-id="5f04d-109">**IAddrBook:: advise**は、このエントリ識別子を調べて、対応するオブジェクトをどのアドレス帳プロバイダーが担当しているかを判断し、その呼び出しを適切なアドレス帳プロバイダーの[IABLogon:: advise](iablogon-advise.md)メソッドに転送します。</span><span class="sxs-lookup"><span data-stu-id="5f04d-109">**IAddrBook::Advise** examines this entry identifier to determine which address book provider is responsible for the corresponding object and forwards the call to the appropriate address book provider's [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
<span data-ttu-id="5f04d-110">クライアントは、アドレス帳のエントリに次の種類のイベントを登録できます。</span><span class="sxs-lookup"><span data-stu-id="5f04d-110">Clients can register for the following types of events on address book entries:</span></span>
  
- <span data-ttu-id="5f04d-111">重大なエラー</span><span class="sxs-lookup"><span data-stu-id="5f04d-111">Critical error</span></span>
    
- <span data-ttu-id="5f04d-112">任意のオブジェクトイベント (作成、変更、削除、移動、またはコピー)</span><span class="sxs-lookup"><span data-stu-id="5f04d-112">Any of the object events (created, modified, deleted, moved, or copied)</span></span>
    
- <span data-ttu-id="5f04d-113">変更されたテーブル</span><span class="sxs-lookup"><span data-stu-id="5f04d-113">Table modified</span></span>
    
<span data-ttu-id="5f04d-114">通常、登録はアドレス帳のコンテナーの内容と階層テーブルに対してのみ行われます。</span><span class="sxs-lookup"><span data-stu-id="5f04d-114">Typically, registration occurs only on address book container contents and hierarchy tables.</span></span> <span data-ttu-id="5f04d-115">クライアントが低レベルのメッセージングユーザーおよび配布リストオブジェクトに登録することはまれです。</span><span class="sxs-lookup"><span data-stu-id="5f04d-115">It is rare that clients register with the lower level messaging user and distribution list objects.</span></span> <span data-ttu-id="5f04d-116">理由は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="5f04d-116">This is because:</span></span>
  
- <span data-ttu-id="5f04d-117">多くのアドレス帳プロバイダーは、メッセージングユーザーおよび配布リストに対する通知をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="5f04d-117">Many address book providers do not support notifications on their messaging users and distribution lists.</span></span>
    
- <span data-ttu-id="5f04d-118">テーブル通知は、変更を追跡してユーザーに報告するのに十分です。</span><span class="sxs-lookup"><span data-stu-id="5f04d-118">Table notifications are sufficient for tracking changes and reporting them to users.</span></span>
    

