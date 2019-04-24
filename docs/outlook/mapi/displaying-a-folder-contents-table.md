---
title: フォルダー コンテンツ テーブルの表示
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 14a4c123-776d-4a32-9688-8a4402dd1f53
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 56847283afaf41c1d45cdb875ddf49eaa5881175
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339936"
---
# <a name="displaying-a-folder-contents-table"></a><span data-ttu-id="22ed1-103">フォルダー コンテンツ テーブルの表示</span><span class="sxs-lookup"><span data-stu-id="22ed1-103">Displaying a folder contents table</span></span>

<span data-ttu-id="22ed1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22ed1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22ed1-105">フォルダーの contents テーブルには、すべてのメッセージに関する概要情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="22ed1-105">The contents table of a folder contains summary information about all of its messages.</span></span> <span data-ttu-id="22ed1-106">新しい受信メッセージに関する概要情報は、メッセージクラスの受信フォルダーのコンテンツテーブルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="22ed1-106">Summary information about new incoming messages appears in the contents table of the receive folder for the message class.</span></span> <span data-ttu-id="22ed1-107">ユーザーがこの情報を使用できるようにするには、テーブルを取得し、必要に応じて列と行を表示します。</span><span class="sxs-lookup"><span data-stu-id="22ed1-107">To make this information available to users, retrieve the table and display the columns and rows as appropriate.</span></span>
  
<span data-ttu-id="22ed1-108">**フォルダコンテンツテーブルを表示するには**</span><span class="sxs-lookup"><span data-stu-id="22ed1-108">**To display a folder contents table**</span></span>
  
1. <span data-ttu-id="22ed1-109">[IMsgStore:: openentry](imsgstore-openentry.md)を呼び出し、テーブルを含むフォルダーのエントリ識別子を渡します。</span><span class="sxs-lookup"><span data-stu-id="22ed1-109">Call [IMsgStore::OpenEntry](imsgstore-openentry.md), passing the entry identifier of the folder containing the table.</span></span>
    
2. <span data-ttu-id="22ed1-110">フォルダーの[IMAPIContainer:: getcontentstable](imapicontainer-getcontentstable.md)メソッドを呼び出して、そのコンテンツテーブルを開きます。</span><span class="sxs-lookup"><span data-stu-id="22ed1-110">Call the folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to open its contents table.</span></span> 
    
3. <span data-ttu-id="22ed1-111">必要に応じて、テーブルの[IMAPITable:: SetColumns](imapitable-setcolumns.md)メソッドを呼び出して特定の列を指定することによって、contents テーブルの表示を制限します。</span><span class="sxs-lookup"><span data-stu-id="22ed1-111">Limit your view of the contents table if desired by calling the table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to specify particular columns.</span></span> 
    
4. <span data-ttu-id="22ed1-112">必要に応じて、テーブルの[IMAPITable:: Restrict](imapitable-restrict.md)メソッドを呼び出して、特定の行をフィルター処理することによって、contents テーブルの表示を制限します。</span><span class="sxs-lookup"><span data-stu-id="22ed1-112">Limit your view of the contents table if desired by calling the table's [IMAPITable::Restrict](imapitable-restrict.md) method to filter particular rows.</span></span> <span data-ttu-id="22ed1-113">たとえば、まだ読まれていない特定のメッセージクラスを持つメッセージのみを表示する場合は、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="22ed1-113">If, for example, you want to show only messages with a specific message class that have yet to be read:</span></span> 
    
    1. <span data-ttu-id="22ed1-114">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) プロパティと目的のメッセージクラスを一致させるプロパティ制限を[spropertyrestriction](spropertyrestriction.md)構造で作成します。</span><span class="sxs-lookup"><span data-stu-id="22ed1-114">Create a property restriction in an [SPropertyRestriction](spropertyrestriction.md) structure that matches the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property with the desired message class.</span></span> 
        
    2. <span data-ttu-id="22ed1-115">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) をプロパティタグとして使用し、MSGFLAG_UNREAD 値をマスクとして使用する[sbitmaskrestriction](sbitmaskrestriction.md)構造で、ビットマスク制限を作成します。</span><span class="sxs-lookup"><span data-stu-id="22ed1-115">Create a bitmask restriction in an [SBitMaskRestriction](sbitmaskrestriction.md) structure that uses **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) as the property tag and the MSGFLAG_UNREAD value as the mask.</span></span>
        
    3. <span data-ttu-id="22ed1-116">プロパティとビットマスク制限を結合する[SAndRestriction](sandrestriction.md)構造で制限を作成します。</span><span class="sxs-lookup"><span data-stu-id="22ed1-116">Create a restriction in an [SAndRestriction](sandrestriction.md) structure that joins the property and bitmask restrictions.</span></span> 
    
5. <span data-ttu-id="22ed1-117">必要に応じて、テーブルの[IMAPITable:: sorttable](imapitable-sorttable.md)メソッドを呼び出して、コンテンツテーブルを並べ替えます。</span><span class="sxs-lookup"><span data-stu-id="22ed1-117">Sort the contents table if desired by calling the table's [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
    
6. <span data-ttu-id="22ed1-118">処理のために contents テーブルからすべての行を取得するには、 [IMAPITable:: QueryRows](imapitable-queryrows.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="22ed1-118">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve all of the rows from the contents table for processing.</span></span> 
    

