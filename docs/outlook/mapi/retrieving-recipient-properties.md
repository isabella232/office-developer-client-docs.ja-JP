---
title: 受信者のプロパティの取得
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 358f892b-54a7-4213-b3c0-94f28f99716f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 38063cebe70b153decce6713ac5fc31d6916dbf6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279595"
---
# <a name="retrieving-recipient-properties"></a><span data-ttu-id="225ab-103">受信者のプロパティの取得</span><span class="sxs-lookup"><span data-stu-id="225ab-103">Retrieving recipient properties</span></span>
  
<span data-ttu-id="225ab-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="225ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a><span data-ttu-id="225ab-105">アドレス帳エントリの1つまたは複数のプロパティにアクセスするには</span><span class="sxs-lookup"><span data-stu-id="225ab-105">To access one or more properties of an address book entry</span></span>
  
1. <span data-ttu-id="225ab-106">対象のアドレス帳のエントリごとに、 [IAddrBook:: openentry](iaddrbook-openentry.md)を呼び出して、対象のメッセージングユーザーまたは配布リストのエントリ識別子を渡します。</span><span class="sxs-lookup"><span data-stu-id="225ab-106">For each address book entry of interest, call [IAddrBook::OpenEntry](iaddrbook-openentry.md), passing the entry identifier of the target messaging user or distribution list.</span></span>
    
2. <span data-ttu-id="225ab-107">その後、次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="225ab-107">Then do one of the following:</span></span>
    
   - <span data-ttu-id="225ab-108">対象のアドレス帳エントリごとに、メッセージユーザーまたは配布リストの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、取得する1つまたは複数のプロパティの一覧を指定します。</span><span class="sxs-lookup"><span data-stu-id="225ab-108">Call the messaging user or distribution list's [IMAPIProp::GetProps](imapiprop-getprops.md) method for each address book entry of interest, with a list of the one or more properties to retrieve.</span></span> 
    
   - <span data-ttu-id="225ab-109">[IAddrBook::P reparerecips](iaddrbook-preparerecips.md)を呼び出し、必要なすべてのアドレス帳エントリのすべてのプロパティを保持する[adrlist](adrlist.md)構造体を渡します。</span><span class="sxs-lookup"><span data-stu-id="225ab-109">Call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), passing an [ADRLIST](adrlist.md) structure that holds all of the properties for all of the desired address book entries.</span></span> <span data-ttu-id="225ab-110">**PrepareRecips**の1回の呼び出しで複数のアドレス帳エントリの情報が返される可能性があるため、複数の受信者に関心がある場合は、この方法をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="225ab-110">Because one call to **PrepareRecips** can return information for multiple address book entries, it is the preferable strategy when you are interested in more than one recipient.</span></span> 
    

