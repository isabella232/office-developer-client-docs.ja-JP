---
title: 受信トレイフォルダーのスキャン
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ad1459f-d59a-4784-94ea-4cad194e6e50
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e954cb2d8029a31e7f69daaa7e8ed55a7953ac02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406557"
---
# <a name="traversing-the-inbox-folder"></a><span data-ttu-id="e1354-103">受信トレイフォルダーのスキャン</span><span class="sxs-lookup"><span data-stu-id="e1354-103">Traversing the Inbox Folder</span></span>

  
  
<span data-ttu-id="e1354-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1354-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="e1354-105">**受信トレイ内のすべてのメッセージを巡回するには**</span><span class="sxs-lookup"><span data-stu-id="e1354-105">**To cycle through all of the messages in the Inbox**</span></span>
  
1. <span data-ttu-id="e1354-106">[IMsgStore:: getreceivefolder](imsgstore-getreceivefolder.md)を呼び出して、受信トレイのエントリ識別子を取得します。</span><span class="sxs-lookup"><span data-stu-id="e1354-106">Call [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to retrieve the entry identifier of the Inbox.</span></span> 
    
2. <span data-ttu-id="e1354-107">**imapifolder:: openentry**を呼び出して、受信トレイを開きます。</span><span class="sxs-lookup"><span data-stu-id="e1354-107">Call **IMAPIFolder::OpenEntry** to open the Inbox.</span></span> 
    
3. <span data-ttu-id="e1354-108">受信トレイの[IMAPIContainer:: getcontentstable](imapicontainer-getcontentstable.md)メソッドを呼び出して、contents テーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="e1354-108">Call the Inbox's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to retrieve the contents table.</span></span> 
    
4. <span data-ttu-id="e1354-109">コンテンツテーブルの[IMAPITable:: SetColumns](imapitable-setcolumns.md)メソッドを呼び出して、列が**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) に設定され、その他の必要な列を制限します。</span><span class="sxs-lookup"><span data-stu-id="e1354-109">Call the contents table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) and any other columns you require.</span></span> 
    
5. <span data-ttu-id="e1354-110">行のグループを取得するには、 [IMAPITable:: QueryRows](imapitable-queryrows.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e1354-110">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve a group of rows.</span></span> 
    
6. <span data-ttu-id="e1354-111">contents テーブルに行がなくなるまで、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="e1354-111">Until there are no longer any rows in the contents table:</span></span>
    
1. <span data-ttu-id="e1354-112">[IMsgStore:: openentry](imsgstore-openentry.md)を呼び出して、各行からのエントリ id で表されるメッセージを開きます。</span><span class="sxs-lookup"><span data-stu-id="e1354-112">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the message represented by the entry identifier from each row.</span></span> 
    
2. <span data-ttu-id="e1354-113">_lppunk_パラメーターをローカルの**IMessage**インターフェイスポインターに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="e1354-113">Assign the  _lppUnk_ parameter to a local **IMessage** interface pointer.</span></span> 
    
3. <span data-ttu-id="e1354-114">メッセージのプロパティを操作します。</span><span class="sxs-lookup"><span data-stu-id="e1354-114">Work with the properties of the message.</span></span>
    
4. <span data-ttu-id="e1354-115">_lppunk_パラメーターで示されているポインターを解放します。</span><span class="sxs-lookup"><span data-stu-id="e1354-115">Release the pointer pointed to by the  _lppUnk_ parameter.</span></span> 
    
5. <span data-ttu-id="e1354-116">次の行グループを取得するには、 [IMAPITable:: QueryRows](imapitable-queryrows.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e1354-116">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the next group of rows.</span></span> 
    
7. <span data-ttu-id="e1354-117">目次表を解放します。</span><span class="sxs-lookup"><span data-stu-id="e1354-117">Release the contents table.</span></span>
    

