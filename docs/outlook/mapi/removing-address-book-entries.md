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
# <a name="removing-address-book-entries"></a><span data-ttu-id="e956a-103">アドレス帳エントリの削除</span><span class="sxs-lookup"><span data-stu-id="e956a-103">Removing address book entries</span></span>
  
<span data-ttu-id="e956a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e956a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e956a-105">コンテナーの[IABContainer::D eleteentries](iabcontainer-deleteentries.md)メソッドを呼び出して、1人または複数の受信者を削除します。</span><span class="sxs-lookup"><span data-stu-id="e956a-105">Your container's [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) method is called to remove one or more recipients.</span></span> <span data-ttu-id="e956a-106">**deleteentries**には、削除する受信者と予約済みのフラグ値を表すエントリ識別子の配列という2つのパラメーターがあります。</span><span class="sxs-lookup"><span data-stu-id="e956a-106">**DeleteEntries** has two parameters: an array of entry identifiers representing the recipients to be deleted and a reserved flags value.</span></span> <span data-ttu-id="e956a-107">受信者の削除は、コンテナーの contents テーブルに影響します。受信者を削除するだけでなく、コンテナーは、受信者を表すコンテンツテーブルの行を削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e956a-107">Deleting a recipient affects the contents table of your container; in addition to deleting the recipient, your container must delete the contents table row that represents the recipient.</span></span> <span data-ttu-id="e956a-108">行がテーブルから削除されている場合、コンテナーは登録された各クライアントに対してテーブル通知を発行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e956a-108">When the row has been removed from the table, your container must issue a table notification to each registered client.</span></span> 
  
### <a name="to-implement-iabcontainerdeleteentries"></a><span data-ttu-id="e956a-109">IABContainer を実装するには::D eleteentries</span><span class="sxs-lookup"><span data-stu-id="e956a-109">To implement IABContainer::DeleteEntries</span></span>
  
1. <span data-ttu-id="e956a-110">エントリ id で表される各受信者をコンテナーから削除します。</span><span class="sxs-lookup"><span data-stu-id="e956a-110">Delete each recipient represented by the entry identifier from your container.</span></span>
    
2. <span data-ttu-id="e956a-111">コンテナーの contents テーブルが開いている場合は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="e956a-111">If your container's contents table is open:</span></span>
    
   - <span data-ttu-id="e956a-112">**ultableevent**メンバーを TABLE_ROW_DELETED に設定して、削除された各目次の表の行について、登録済みのクライアントに_fnevTableModified_通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="e956a-112">Send an  _fnevTableModified_ notification with the **ulTableEvent** member set to TABLE_ROW_DELETED to registered clients for each deleted contents table row.</span></span> <span data-ttu-id="e956a-113">プロバイダーが通知ユーティリティを使用している場合は、次のような通知を送信するように、 [imapisupport:: Notify](imapisupport-notify.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e956a-113">If your provider uses the notification utility, call [IMAPISupport::Notify](imapisupport-notify.md) to send these notifications.</span></span> 
    
   - <span data-ttu-id="e956a-114">プロバイダーがオブジェクト通知をサポートしている場合は、 _fnevObjectDeleted_通知も送信します。</span><span class="sxs-lookup"><span data-stu-id="e956a-114">If your provider supports object notifications, also send an  _fnevObjectDeleted_ notification.</span></span> 
    

