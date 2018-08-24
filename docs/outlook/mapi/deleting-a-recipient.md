---
title: 受信者の削除
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f7495030-e3b8-4c7c-9e19-284ba820e846
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 03917ad52f1dc1ce4d0b59cd54fe33f58f352061
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582946"
---
# <a name="deleting-a-recipient"></a><span data-ttu-id="8d9c8-103">受信者の削除</span><span class="sxs-lookup"><span data-stu-id="8d9c8-103">Deleting a Recipient</span></span>

  
  
<span data-ttu-id="8d9c8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d9c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="8d9c8-105">**変更可能なコンテナーから 1 つまたは複数のアドレス帳のエントリを削除するのには**</span><span class="sxs-lookup"><span data-stu-id="8d9c8-105">**To remove one or more address book entries from a modifiable container**</span></span>
  
- <span data-ttu-id="8d9c8-106">削除するアドレス帳のエントリを表すエントリの識別子の配列を渡して、 [IABContainer::DeleteEntries](iabcontainer-deleteentries.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8d9c8-106">Call the [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) method, passing an array of entry identifiers that represent the address book entries to be deleted.</span></span> <span data-ttu-id="8d9c8-107">**DeleteEntries**は、警告、MAPI_W_PARTIAL_COMPLETION、1 つまたは複数のエントリを削除できなかったことを示すためを返すことができます。</span><span class="sxs-lookup"><span data-stu-id="8d9c8-107">**DeleteEntries** can return a warning, MAPI_W_PARTIAL_COMPLETION, to indicate that it couldn't delete one or more of the entries.</span></span> <span data-ttu-id="8d9c8-108">**HR_FAILED**マクロに戻り値をテストし、問題の詳細については、必要な場合は、コンテナーの[IMAPIProp::GetLastError](imapiprop-getlasterror.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8d9c8-108">Test for this return value with the **HR_FAILED** macro and call the container's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method if more information about the problem is needed.</span></span> 
    
<span data-ttu-id="8d9c8-109">キャッシュに削除されたエントリの[ADRENTRY](adrentry.md)構造体へのポインターを保持する場合、そのエントリの識別子を使用してプロパティを取得することができます。</span><span class="sxs-lookup"><span data-stu-id="8d9c8-109">When you hold a pointer to a deleted entry's [ADRENTRY](adrentry.md) structure in your cache, you will still be able to retrieve properties using its entry identifier.</span></span> <span data-ttu-id="8d9c8-110">エントリが削除用にマークするためです。</span><span class="sxs-lookup"><span data-stu-id="8d9c8-110">This is because the entry is only marked for deletion.</span></span> <span data-ttu-id="8d9c8-111">MAPI では、仕様ではこれらのマークを付けたエントリへのアクセスのレベルを維持します。</span><span class="sxs-lookup"><span data-stu-id="8d9c8-111">MAPI maintains a level of access to these marked entries by design.</span></span> 
  

