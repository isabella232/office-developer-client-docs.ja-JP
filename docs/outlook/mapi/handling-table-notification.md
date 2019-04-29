---
title: テーブル通知の処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: edc9bc71-4885-4783-b465-0bafa20eff73
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6e6c24c3836f295054c1880dc506c5051078a9ab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435895"
---
# <a name="handling-table-notification"></a><span data-ttu-id="9c001-103">テーブル通知の処理</span><span class="sxs-lookup"><span data-stu-id="9c001-103">Handling table notification</span></span>

<span data-ttu-id="9c001-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c001-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c001-105">フォルダーやメッセージングユーザーなど、アドバイズソースオブジェクトを直接登録する代わりに、クライアントはコンテンツまたは階層テーブルに通知を登録することができます。</span><span class="sxs-lookup"><span data-stu-id="9c001-105">As an alternative to registering directly with an advise source object, such as a folder or a messaging user, a client can register for notifications on a contents or hierarchy table.</span></span> <span data-ttu-id="9c001-106">コンテンツまたは階層テーブルを介してアドレス帳のエントリ、フォルダー、およびメッセージに加えられた変更を追跡することは、個々のオブジェクトを使用するよりも簡単でわかりやすくなります。</span><span class="sxs-lookup"><span data-stu-id="9c001-106">Tracking changes to address book entries, folders, and messages through a contents or hierarchy table can be simpler and more straightforward than through individual objects.</span></span> 

<span data-ttu-id="9c001-107">たとえば、フォルダーの階層テーブルに対して[IMAPITable:: アドバイズ](imapitable-advise.md)を呼び出して、そのサブフォルダーの1つに変更が発生したことを検出できます。</span><span class="sxs-lookup"><span data-stu-id="9c001-107">For example, you can call [IMAPITable::Advise](imapitable-advise.md) on a folder's hierarchy table to discover when changes occur to one of its subfolders.</span></span> <span data-ttu-id="9c001-108">リモートメッセージの表示をサポートしている場合は、[状態] テーブルに登録して、トランスポートプロバイダーと MAPI スプーラーによるアクティビティを監視します。</span><span class="sxs-lookup"><span data-stu-id="9c001-108">If you support the viewing of remote messages, register with the status table to observe activity by transport providers and the MAPI spooler.</span></span> 
  
<span data-ttu-id="9c001-109">ただし、オブジェクト通知ではなくテーブル通知の使用を常に推奨するわけではありません。</span><span class="sxs-lookup"><span data-stu-id="9c001-109">However, it is not always preferable to use table notifications instead of object notifications.</span></span> <span data-ttu-id="9c001-110">フォルダー内のメッセージ数の変更の監視は、クライアントがフォルダーで実装されたテーブルではなく、フォルダーにオブジェクト通知を登録する必要がある場合の例です。</span><span class="sxs-lookup"><span data-stu-id="9c001-110">Monitoring changes in the number of messages in a folder is an example of when your client might need to register for object notifications on a folder rather than on a table implemented by the folder.</span></span>
  

