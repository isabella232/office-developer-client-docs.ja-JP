---
title: テーブルの通知を処理します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: edc9bc71-4885-4783-b465-0bafa20eff73
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 95ef351e4fe906608319a3e25de8f20a44e23d9d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800201"
---
# <a name="handling-table-notification"></a><span data-ttu-id="9e018-103">テーブルの通知を処理します。</span><span class="sxs-lookup"><span data-stu-id="9e018-103">Handling table notification</span></span>

<span data-ttu-id="9e018-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9e018-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9e018-105">アドバイズ ソース オブジェクト、フォルダーなど、ユーザーがメッセージを直接登録する代わりにクライアントは、内容の通知を登録できますか、階層テーブルです。</span><span class="sxs-lookup"><span data-stu-id="9e018-105">As an alternative to registering directly with an advise source object, such as a folder or a messaging user, a client can register for notifications on a contents or hierarchy table.</span></span> <span data-ttu-id="9e018-106">アドレスへの変更の追跡エントリ、フォルダー、および、内容を経由してメッセージを予約するか、階層テーブルは、個々 のオブジェクトをより簡単より単純です。</span><span class="sxs-lookup"><span data-stu-id="9e018-106">Tracking changes to address book entries, folders, and messages through a contents or hierarchy table can be simpler and more straightforward than through individual objects.</span></span> 

<span data-ttu-id="9e018-107">たとえば、いずれかのサブフォルダーに変更が発生したときを検出するフォルダーの階層テーブルで[IMAPITable::Advise](imapitable-advise.md)を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="9e018-107">For example, you can call [IMAPITable::Advise](imapitable-advise.md) on a folder's hierarchy table to discover when changes occur to one of its subfolders.</span></span> <span data-ttu-id="9e018-108">リモート メッセージの表示をサポートする場合は、トランスポート プロバイダーによって処理され、MAPI スプーラーを観察する状態テーブルに登録します。</span><span class="sxs-lookup"><span data-stu-id="9e018-108">If you support the viewing of remote messages, register with the status table to observe activity by transport providers and the MAPI spooler.</span></span> 
  
<span data-ttu-id="9e018-109">ただし、それは常にオブジェクトの通知ではなくテーブルの通知を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="9e018-109">However, it is not always preferable to use table notifications instead of object notifications.</span></span> <span data-ttu-id="9e018-110">クライアント可能性がありますフォルダーによって実装されているテーブルではなくフォルダーにオブジェクトの通知を登録する必要がある場合の例ではフォルダー内のメッセージの数の変更を監視します。</span><span class="sxs-lookup"><span data-stu-id="9e018-110">Monitoring changes in the number of messages in a folder is an example of when your client might need to register for object notifications on a folder rather than on a table implemented by the folder.</span></span>
  

