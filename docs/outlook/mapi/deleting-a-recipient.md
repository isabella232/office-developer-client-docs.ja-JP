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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316815"
---
# <a name="deleting-a-recipient"></a><span data-ttu-id="cd52a-103">受信者の削除</span><span class="sxs-lookup"><span data-stu-id="cd52a-103">Deleting a Recipient</span></span>

  
  
<span data-ttu-id="cd52a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd52a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="cd52a-105">**変更可能なコンテナーから1つまたは複数のアドレス帳のエントリを削除するには**</span><span class="sxs-lookup"><span data-stu-id="cd52a-105">**To remove one or more address book entries from a modifiable container**</span></span>
  
- <span data-ttu-id="cd52a-106">[IABContainer::D eleteentries](iabcontainer-deleteentries.md)メソッドを呼び出して、削除するアドレス帳のエントリを表すエントリ識別子の配列を渡します。</span><span class="sxs-lookup"><span data-stu-id="cd52a-106">Call the [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) method, passing an array of entry identifiers that represent the address book entries to be deleted.</span></span> <span data-ttu-id="cd52a-107">**deleteentries**は、1つまたは複数のエントリを削除できなかったことを示すために、MAPI_W_PARTIAL_COMPLETION という警告を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="cd52a-107">**DeleteEntries** can return a warning, MAPI_W_PARTIAL_COMPLETION, to indicate that it couldn't delete one or more of the entries.</span></span> <span data-ttu-id="cd52a-108">**HR_FAILED**マクロを使用してこの戻り値をテストし、問題に関する詳細情報が必要な場合は、コンテナーの[imapiprop:: GetLastError](imapiprop-getlasterror.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="cd52a-108">Test for this return value with the **HR_FAILED** macro and call the container's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method if more information about the problem is needed.</span></span> 
    
<span data-ttu-id="cd52a-109">キャッシュ内の削除されたエントリの[adrentry](adrentry.md)構造体へのポインターを保持する場合でも、そのエントリ識別子を使用してプロパティを取得できます。</span><span class="sxs-lookup"><span data-stu-id="cd52a-109">When you hold a pointer to a deleted entry's [ADRENTRY](adrentry.md) structure in your cache, you will still be able to retrieve properties using its entry identifier.</span></span> <span data-ttu-id="cd52a-110">これは、エントリが削除対象としてマークされているためです。</span><span class="sxs-lookup"><span data-stu-id="cd52a-110">This is because the entry is only marked for deletion.</span></span> <span data-ttu-id="cd52a-111">MAPI では、これらのマークされたエントリに対して、設計によるレベルのアクセスが維持されます。</span><span class="sxs-lookup"><span data-stu-id="cd52a-111">MAPI maintains a level of access to these marked entries by design.</span></span> 
  

