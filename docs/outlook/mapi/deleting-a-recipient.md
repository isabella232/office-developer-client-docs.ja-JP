---
title: 受信者の削除
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f7495030-e3b8-4c7c-9e19-284ba820e846
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: bd01c66d9fff7c94ffb1ce9f956f1951bc482020
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421047"
---
# <a name="deleting-a-recipient"></a><span data-ttu-id="9650b-103">受信者の削除</span><span class="sxs-lookup"><span data-stu-id="9650b-103">Deleting a Recipient</span></span>

  
  
<span data-ttu-id="9650b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9650b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="9650b-105">**変更可能なコンテナーから 1 つ以上のアドレス帳エントリを削除するには**</span><span class="sxs-lookup"><span data-stu-id="9650b-105">**To remove one or more address book entries from a modifiable container**</span></span>
  
- <span data-ttu-id="9650b-106">[IABContainer::D eleteEntries](iabcontainer-deleteentries.md)メソッドを呼び出し、削除するアドレス帳エントリを表すエントリ識別子の配列を渡します。</span><span class="sxs-lookup"><span data-stu-id="9650b-106">Call the [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) method, passing an array of entry identifiers that represent the address book entries to be deleted.</span></span> <span data-ttu-id="9650b-107">**DeleteEntries は** 、1 つ以上のMAPI_W_PARTIAL_COMPLETION削除できなかったという警告を返すメッセージを返す場合があります。</span><span class="sxs-lookup"><span data-stu-id="9650b-107">**DeleteEntries** can return a warning, MAPI_W_PARTIAL_COMPLETION, to indicate that it couldn't delete one or more of the entries.</span></span> <span data-ttu-id="9650b-108">**HR_FAILED** マクロを使用してこの戻り値をテストし、問題の詳細が必要な場合は、コンテナーの [IMAPIProp::GetLastError](imapiprop-getlasterror.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9650b-108">Test for this return value with the **HR_FAILED** macro and call the container's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method if more information about the problem is needed.</span></span> 
    
<span data-ttu-id="9650b-109">削除されたエントリの [ADRENTRY](adrentry.md) 構造へのポインターをキャッシュに保持すると、そのエントリ識別子を使用してプロパティを取得できます。</span><span class="sxs-lookup"><span data-stu-id="9650b-109">When you hold a pointer to a deleted entry's [ADRENTRY](adrentry.md) structure in your cache, you will still be able to retrieve properties using its entry identifier.</span></span> <span data-ttu-id="9650b-110">これは、エントリが削除のマークのみ付いているためです。</span><span class="sxs-lookup"><span data-stu-id="9650b-110">This is because the entry is only marked for deletion.</span></span> <span data-ttu-id="9650b-111">MAPI は、デザインによってこれらのマークされたエントリへのアクセスレベルを維持します。</span><span class="sxs-lookup"><span data-stu-id="9650b-111">MAPI maintains a level of access to these marked entries by design.</span></span> 
  

