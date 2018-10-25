---
title: メッセージ ストアのフォルダーの公開
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d9309e47-2a92-4576-9921-c89cc48472c2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 62f50ed7925305eca7432da17130d2be0365ef03
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582596"
---
# <a name="exposing-folders-in-message-stores"></a><span data-ttu-id="bd13d-103">メッセージ ストアのフォルダーの公開</span><span class="sxs-lookup"><span data-stu-id="bd13d-103">Exposing Folders in Message Stores</span></span>

  
  
<span data-ttu-id="bd13d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd13d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd13d-105">すべてのメッセージ ストア プロバイダーは、クライアント アプリケーションに最上位の [IMAPIFolder](imapifolderimapicontainer.md) インターフェイスを提示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bd13d-105">Every message store provider must present a top-level [IMAPIFolder](imapifolderimapicontainer.md) interface to client applications.</span></span> <span data-ttu-id="bd13d-106">最上位フォルダーは、メッセージ ストア全体に対応し、メッセージ ストアの内容としてユーザーに表示されるフォルダーへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="bd13d-106">The top-level folder corresponds to the entire message store; it provides access to the folders that users see as the contents of the message store.</span></span> <span data-ttu-id="bd13d-107">さらに、最上位フォルダーは、IPC メッセージの既定の受信フォルダーや、既読レポートが送信されるフォルダーとしてもよく使用されます。</span><span class="sxs-lookup"><span data-stu-id="bd13d-107">In addition, the top-level folder is often used as the default receive folder for IPC messages and as the folder from which read reports are sent.</span></span> <span data-ttu-id="bd13d-108">メッセージ ストア プロバイダーはまた、クライアント アプリケーションに IPM メッセージの格納に使用する一連のフォルダーである、IPM サブツリーも提示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bd13d-108">Message store providers must also present an IPM subtree — a set of folders used to contain IPM messages — to client applications.</span></span> 
  
<span data-ttu-id="bd13d-p102">クライアント アプリケーションは、_cbEntryId_、_lpEntryId_ パラメーターにそれぞれ 0、Null 値を指定して [IMsgStore::OpenEntry](imsgstore-openentry.md) メソッドを呼び出し、最上位フォルダーを開くことができます。ただし、ほとんどの場合、クライアント アプリケーションは IPM メッセージが格納された一連のフォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="bd13d-p102">Client applications can open the top-level folder by calling the [IMsgStore::OpenEntry](imsgstore-openentry.md) method with 0 and NULL for the  _cbEntryId_ and  _lpEntryId_ parameters, respectively. In most cases, however, client applications open the set of folders that contain IPM messages.</span></span> 
  
<span data-ttu-id="bd13d-111">メッセージ ストアの IPM フォルダー ツリーにあるフォルダーのリストを取得するには、次のプロシージャを使用します。</span><span class="sxs-lookup"><span data-stu-id="bd13d-111">To get a list of folders in the message store's IPM folder tree, use the following procedure:</span></span>
  
1. <span data-ttu-id="bd13d-112">MAPI セッションを使って、[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="bd13d-112">Use your MAPI session to call the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> 
    
2. <span data-ttu-id="bd13d-113">結果として得られたメッセージ データベースのポインターを使って、**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) プロパティの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="bd13d-113">Use the resulting message database pointer to call the [IMAPIProp::GetProps](imapiprop-getprops.md) method for the **PR_IPM_SUBTREE_ENTRYID** ( [PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span>
    
3. <span data-ttu-id="bd13d-114">エントリ識別子付きの [IMsgStore::OpenEntry](imsgstore-openentry.md) メソッドを呼び出して、**IMAPIFolder** ポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="bd13d-114">Call the [IMsgStore::OpenEntry](imsgstore-openentry.md) method with the entry identifier to get an **IMAPIFolder** pointer.</span></span> 
    
4. <span data-ttu-id="bd13d-115">[IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) メソッドを呼び出して、フォルダーの目次を取得します。</span><span class="sxs-lookup"><span data-stu-id="bd13d-115">Call the [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to get a table of the contents of the folder.</span></span> 
    
5. <span data-ttu-id="bd13d-116">[IMAPITable::QueryRows](imapitable-queryrows.md) メソッドを呼び出して、最上位フォルダー内のフォルダーを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="bd13d-116">Call the [IMAPITable::QueryRows](imapitable-queryrows.md) method to list the folders in the top-level folder.</span></span> 
    
<span data-ttu-id="bd13d-117">MAPI クライアントは、これらのフォルダーを使って、メッセージ ストア内の他のフォルダー オブジェクトやメッセージ オブジェクトにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="bd13d-117">MAPI clients use these folders to access other folder objects and message objects in the message store.</span></span> <span data-ttu-id="bd13d-118">**IMAPIFolder** とその親インターフェイスである [IMAPIContainer](imapicontainerimapiprop.md) には、メッセージ ストア プロバイダーがフォルダーにメッセージ オブジェクトを追加し、クライアントの要求に応えてメッセージを処理するうえで、実装する必要のあるメソッドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="bd13d-118">**IMAPIFolder**, and its parent interface [IMAPIContainer](imapicontainerimapiprop.md), contain the methods your message store provider must implement to populate folders with message objects and respond to client requests to operate on messages.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bd13d-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="bd13d-119">See also</span></span>



[<span data-ttu-id="bd13d-120">メッセージ ストアのフォルダーの実装</span><span class="sxs-lookup"><span data-stu-id="bd13d-120">Implementing Folders in Message Stores</span></span>](implementing-folders-in-message-stores.md)

