---
title: 受信トレイ フォルダーのトラバー
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
# <a name="traversing-the-inbox-folder"></a><span data-ttu-id="5cf5e-103">受信トレイ フォルダーのトラバー</span><span class="sxs-lookup"><span data-stu-id="5cf5e-103">Traversing the Inbox Folder</span></span>

  
  
<span data-ttu-id="5cf5e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5cf5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="5cf5e-105">**受信トレイ内のすべてのメッセージを循環するには**</span><span class="sxs-lookup"><span data-stu-id="5cf5e-105">**To cycle through all of the messages in the Inbox**</span></span>
  
1. <span data-ttu-id="5cf5e-106">受信 [トレイのエントリ識別子を取得するには、IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5cf5e-106">Call [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to retrieve the entry identifier of the Inbox.</span></span> 
    
2. <span data-ttu-id="5cf5e-107">**IMAPIFolder::OpenEntry を呼び出して** 受信トレイを開きます。</span><span class="sxs-lookup"><span data-stu-id="5cf5e-107">Call **IMAPIFolder::OpenEntry** to open the Inbox.</span></span> 
    
3. <span data-ttu-id="5cf5e-108">受信トレイの [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) メソッドを呼び出して、コンテンツ テーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="5cf5e-108">Call the Inbox's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to retrieve the contents table.</span></span> 
    
4. <span data-ttu-id="5cf5e-109">**コンテンツ** テーブルの [IMAPITable::SetColumns](imapitable-setcolumns.md)メソッドを呼び出して、列セットを PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) および必要なその他の列に制限します。</span><span class="sxs-lookup"><span data-stu-id="5cf5e-109">Call the contents table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) and any other columns you require.</span></span> 
    
5. <span data-ttu-id="5cf5e-110">[IMAPITable::QueryRows を呼び出して](imapitable-queryrows.md)、行のグループを取得します。</span><span class="sxs-lookup"><span data-stu-id="5cf5e-110">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve a group of rows.</span></span> 
    
6. <span data-ttu-id="5cf5e-111">コンテンツ テーブルに行がなくなるまで、次の処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="5cf5e-111">Until there are no longer any rows in the contents table:</span></span>
    
1. <span data-ttu-id="5cf5e-112">[IMsgStore::OpenEntry](imsgstore-openentry.md)を呼び出して、各行のエントリ識別子で表されるメッセージを開きます。</span><span class="sxs-lookup"><span data-stu-id="5cf5e-112">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the message represented by the entry identifier from each row.</span></span> 
    
2. <span data-ttu-id="5cf5e-113">_lppUnk パラメーターを_ ローカルの IMessage インターフェイス ポインター **に割り** 当てる。</span><span class="sxs-lookup"><span data-stu-id="5cf5e-113">Assign the  _lppUnk_ parameter to a local **IMessage** interface pointer.</span></span> 
    
3. <span data-ttu-id="5cf5e-114">メッセージのプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="5cf5e-114">Work with the properties of the message.</span></span>
    
4. <span data-ttu-id="5cf5e-115">_lppUnk_ パラメーターが指すポインターを離します。</span><span class="sxs-lookup"><span data-stu-id="5cf5e-115">Release the pointer pointed to by the  _lppUnk_ parameter.</span></span> 
    
5. <span data-ttu-id="5cf5e-116">[IMAPITable::QueryRows を呼び出して](imapitable-queryrows.md)、次の行グループを取得します。</span><span class="sxs-lookup"><span data-stu-id="5cf5e-116">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the next group of rows.</span></span> 
    
7. <span data-ttu-id="5cf5e-117">コンテンツ テーブルを解放します。</span><span class="sxs-lookup"><span data-stu-id="5cf5e-117">Release the contents table.</span></span>
    

