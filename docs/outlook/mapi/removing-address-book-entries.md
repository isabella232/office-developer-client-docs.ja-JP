---
title: アドレス帳エントリの削除
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 107ebcd7-b612-4139-b676-c3851f15bc74
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1d5ae33b08c85c9ee93764d762c2ec251fddd265
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425261"
---
# <a name="removing-address-book-entries"></a><span data-ttu-id="20171-103">アドレス帳エントリの削除</span><span class="sxs-lookup"><span data-stu-id="20171-103">Removing address book entries</span></span>
  
<span data-ttu-id="20171-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20171-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20171-105">コンテナーの [IABContainer::D eleteEntries](iabcontainer-deleteentries.md) メソッドが呼び出され、1 つ以上の受信者が削除されます。</span><span class="sxs-lookup"><span data-stu-id="20171-105">Your container's [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) method is called to remove one or more recipients.</span></span> <span data-ttu-id="20171-106">**DeleteEntries には** 、削除する受信者を表すエントリ識別子の配列と予約済みのフラグ値の 2 つのパラメーターがあります。</span><span class="sxs-lookup"><span data-stu-id="20171-106">**DeleteEntries** has two parameters: an array of entry identifiers representing the recipients to be deleted and a reserved flags value.</span></span> <span data-ttu-id="20171-107">受信者を削除すると、コンテナーのコンテンツ テーブルに影響します。コンテナーは、受信者の削除に加えて、受信者を表す目次行を削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="20171-107">Deleting a recipient affects the contents table of your container; in addition to deleting the recipient, your container must delete the contents table row that represents the recipient.</span></span> <span data-ttu-id="20171-108">行がテーブルから削除されると、コンテナーは登録されている各クライアントにテーブル通知を発行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="20171-108">When the row has been removed from the table, your container must issue a table notification to each registered client.</span></span> 
  
### <a name="to-implement-iabcontainerdeleteentries"></a><span data-ttu-id="20171-109">IABContainer::D eleteEntries を実装するには</span><span class="sxs-lookup"><span data-stu-id="20171-109">To implement IABContainer::DeleteEntries</span></span>
  
1. <span data-ttu-id="20171-110">エントリ識別子によって表される各受信者をコンテナーから削除します。</span><span class="sxs-lookup"><span data-stu-id="20171-110">Delete each recipient represented by the entry identifier from your container.</span></span>
    
2. <span data-ttu-id="20171-111">コンテナーのコンテンツ テーブルが開いている場合:</span><span class="sxs-lookup"><span data-stu-id="20171-111">If your container's contents table is open:</span></span>
    
   - <span data-ttu-id="20171-112">削除されたコンテンツテーブル行ごとに **、ulTableEvent** メンバーが登録TABLE_ROW_DELETEDに設定された _fnevTableModified_ 通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="20171-112">Send an  _fnevTableModified_ notification with the **ulTableEvent** member set to TABLE_ROW_DELETED to registered clients for each deleted contents table row.</span></span> <span data-ttu-id="20171-113">プロバイダーが通知ユーティリティを使用している場合は [、IMAPISupport::Notify](imapisupport-notify.md) を呼び出して、これらの通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="20171-113">If your provider uses the notification utility, call [IMAPISupport::Notify](imapisupport-notify.md) to send these notifications.</span></span> 
    
   - <span data-ttu-id="20171-114">プロバイダーがオブジェクト通知をサポートしている場合は  _、fnevObjectDeleted 通知も送信_ します。</span><span class="sxs-lookup"><span data-stu-id="20171-114">If your provider supports object notifications, also send an  _fnevObjectDeleted_ notification.</span></span> 
    

