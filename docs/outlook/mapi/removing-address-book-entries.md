---
title: アドレス帳のエントリを削除します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 107ebcd7-b612-4139-b676-c3851f15bc74
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2c5d7a2114f4a85b9f63cd778e899a83d335ff45
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581280"
---
# <a name="removing-address-book-entries"></a><span data-ttu-id="81715-103">アドレス帳のエントリを削除します。</span><span class="sxs-lookup"><span data-stu-id="81715-103">Removing address book entries</span></span>
  
<span data-ttu-id="81715-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81715-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81715-105">1 つまたは複数の受信者を削除するのには、コンテナーの[IABContainer::DeleteEntries](iabcontainer-deleteentries.md)メソッドと呼びます。</span><span class="sxs-lookup"><span data-stu-id="81715-105">Your container's [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) method is called to remove one or more recipients.</span></span> <span data-ttu-id="81715-106">**DeleteEntries**には 2 つのパラメーター: 削除する受信者を表すエントリ id と予約済みのフラグの値の配列。</span><span class="sxs-lookup"><span data-stu-id="81715-106">**DeleteEntries** has two parameters: an array of entry identifiers representing the recipients to be deleted and a reserved flags value.</span></span> <span data-ttu-id="81715-107">コンテナーのコンテンツ テーブルに影響を受ける受信者を削除します。受信者を削除するには、ほかのコンテナーに受信者を表す内容のテーブルの行を削除しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="81715-107">Deleting a recipient affects the contents table of your container; in addition to deleting the recipient, your container must delete the contents table row that represents the recipient.</span></span> <span data-ttu-id="81715-108">行がテーブルから削除された、ときに、コンテナーは、各登録済みのクライアントにテーブルの通知を発行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="81715-108">When the row has been removed from the table, your container must issue a table notification to each registered client.</span></span> 
  
### <a name="to-implement-iabcontainerdeleteentries"></a><span data-ttu-id="81715-109">IABContainer::DeleteEntries を実装するには</span><span class="sxs-lookup"><span data-stu-id="81715-109">To implement IABContainer::DeleteEntries</span></span>
  
1. <span data-ttu-id="81715-110">コンテナーからのエントリの識別子によって表される各受信者を削除します。</span><span class="sxs-lookup"><span data-stu-id="81715-110">Delete each recipient represented by the entry identifier from your container.</span></span>
    
2. <span data-ttu-id="81715-111">コンテナーの内容のテーブルが開いている場合。</span><span class="sxs-lookup"><span data-stu-id="81715-111">If your container's contents table is open:</span></span>
    
   - <span data-ttu-id="81715-112">**UlTableEvent**メンバーが TABLE_ROW_DELETED に設定内容が削除されたテーブルの行ごとに登録されているクライアントに_fnevTableModified_の通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="81715-112">Send an  _fnevTableModified_ notification with the **ulTableEvent** member set to TABLE_ROW_DELETED to registered clients for each deleted contents table row.</span></span> <span data-ttu-id="81715-113">プロバイダーは、通知ユーティリティを使用する場合は、これらの通知を送信するのには[IMAPISupport::Notify](imapisupport-notify.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="81715-113">If your provider uses the notification utility, call [IMAPISupport::Notify](imapisupport-notify.md) to send these notifications.</span></span> 
    
   - <span data-ttu-id="81715-114">プロバイダーは、オブジェクトの通知をサポートする場合も、 _fnevObjectDeleted_通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="81715-114">If your provider supports object notifications, also send an  _fnevObjectDeleted_ notification.</span></span> 
    

