---
title: Outlook にエクスポート Api について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 7b251308-70ff-a1ec-e968-9d5993909505
description: 次の定義、データ構造体、関数、およびインターフェイスの内部使用のために設計された当初は一般公開されますを outlook にエクスポートします。
ms.openlocfilehash: 0ed68b6c1b8082ee5cc22deb96333a0bd4d29390
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316983"
---
# <a name="about-apis-exported-by-outlook"></a><span data-ttu-id="990fa-103">Outlook にエクスポート Api について</span><span class="sxs-lookup"><span data-stu-id="990fa-103">About APIs exported by Outlook</span></span>

<span data-ttu-id="990fa-104">次の定義、データ構造体、関数、およびインターフェイスの内部使用のために設計された当初は一般公開されますを outlook にエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="990fa-104">Outlook exports the following definitions, data structures, functions, and interfaces that were originally designed for internal use but are now exposed for public consumption.</span></span>
  
### <a name="definitions"></a><span data-ttu-id="990fa-105">定義</span><span class="sxs-lookup"><span data-stu-id="990fa-105">Definitions</span></span>
  
- [<span data-ttu-id="990fa-106">(Outlook エクスポート Api) 定数</span><span class="sxs-lookup"><span data-stu-id="990fa-106">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
    
### <a name="data-structures"></a><span data-ttu-id="990fa-107">データ構造</span><span class="sxs-lookup"><span data-stu-id="990fa-107">Data structures</span></span>
  
- [<span data-ttu-id="990fa-108">TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="990fa-108">TZDEFINITION</span></span>](tzdefinition.md)
    
- [<span data-ttu-id="990fa-109">TZREG</span><span class="sxs-lookup"><span data-stu-id="990fa-109">TZREG</span></span>](tzreg.md)
    
- [<span data-ttu-id="990fa-110">TZRULE</span><span class="sxs-lookup"><span data-stu-id="990fa-110">TZRULE</span></span>](tzrule.md)
    
### <a name="functions"></a><span data-ttu-id="990fa-111">関数</span><span class="sxs-lookup"><span data-stu-id="990fa-111">Functions</span></span>
  
- [<span data-ttu-id="990fa-112">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="990fa-112">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)
    
- [<span data-ttu-id="990fa-113">HrProcessConvActionForSentItem</span><span class="sxs-lookup"><span data-stu-id="990fa-113">HrProcessConvActionForSentItem</span></span>](hrprocessconvactionforsentitem.md)
    
- [<span data-ttu-id="990fa-114">RebaseTaskComplete</span><span class="sxs-lookup"><span data-stu-id="990fa-114">RebaseTaskComplete</span></span>](rebasetaskcomplete.md)
    
- [<span data-ttu-id="990fa-115">RebaseTaskProgress</span><span class="sxs-lookup"><span data-stu-id="990fa-115">RebaseTaskProgress</span></span>](rebasetaskprogress.md)
    
### <a name="interfaces"></a><span data-ttu-id="990fa-116">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="990fa-116">Interfaces</span></span>
  
- [<span data-ttu-id="990fa-117">IOlkApptRebaser</span><span class="sxs-lookup"><span data-stu-id="990fa-117">IOlkApptRebaser</span></span>](iolkapptrebaser.md)
    
### <a name="events"></a><span data-ttu-id="990fa-118">イベント</span><span class="sxs-lookup"><span data-stu-id="990fa-118">Events</span></span>
  
- [<span data-ttu-id="990fa-119">使用可能なイベントの dispid (Outlook エクスポート Api)</span><span class="sxs-lookup"><span data-stu-id="990fa-119">Available events and their dispids (Outlook exported APIs)</span></span>](available-events-and-their-dispids-outlook-exported-apis.md)
    
<span data-ttu-id="990fa-120">また、ディスパッチ識別子、 **dispidFDirty**および **dispidShowSenderPhoto**を使用して実現できます、次のタスク。</span><span class="sxs-lookup"><span data-stu-id="990fa-120">Additionally, using the dispatch identifiers, **dispidFDirty** and **dispidShowSenderPhoto**, you can achieve the following tasks:</span></span>
  
- [<span data-ttu-id="990fa-121">Outlook アイテムが変更されたが保存されていないかどうかを確認する (Outlook の補助リファレンス)</span><span class="sxs-lookup"><span data-stu-id="990fa-121">Determine whether an Outlook item has been modified but not saved (Outlook Auxiliary Reference)</span></span>](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
    
- [<span data-ttu-id="990fa-122">Outlook (Outlook の補助リファレンス) で、連絡先の画像を表示するかどうかを指定</span><span class="sxs-lookup"><span data-stu-id="990fa-122">Specify whether to display a contact's picture in Outlook (Outlook Auxiliary Reference)</span></span>](https://msdn.microsoft.com/library/office/gg262879.aspx)
    

