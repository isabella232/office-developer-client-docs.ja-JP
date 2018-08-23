---
title: Outlook にエクスポート Api について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 7b251308-70ff-a1ec-e968-9d5993909505
description: 次の定義、データ構造体、関数、およびインターフェイスの内部使用のために設計された当初は一般公開されますを outlook にエクスポートします。
ms.openlocfilehash: 888a1d7f828b463dc17c03353d693d3df3544e53
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799289"
---
# <a name="about-apis-exported-by-outlook"></a><span data-ttu-id="f2049-103">Outlook にエクスポート Api について</span><span class="sxs-lookup"><span data-stu-id="f2049-103">About APIs exported by Outlook</span></span>

<span data-ttu-id="f2049-104">次の定義、データ構造体、関数、およびインターフェイスの内部使用のために設計された当初は一般公開されますを outlook にエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="f2049-104">Outlook exports the following definitions, data structures, functions, and interfaces that were originally designed for internal use but are now exposed for public consumption.</span></span>
  
### <a name="definitions"></a><span data-ttu-id="f2049-105">定義</span><span class="sxs-lookup"><span data-stu-id="f2049-105">Definitions</span></span>
  
- [<span data-ttu-id="f2049-106">(Outlook エクスポート Api) 定数</span><span class="sxs-lookup"><span data-stu-id="f2049-106">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
    
### <a name="data-structures"></a><span data-ttu-id="f2049-107">データ構造体</span><span class="sxs-lookup"><span data-stu-id="f2049-107">Data structures</span></span>
  
- [<span data-ttu-id="f2049-108">TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="f2049-108">TZDEFINITION</span></span>](tzdefinition.md)
    
- [<span data-ttu-id="f2049-109">TZREG</span><span class="sxs-lookup"><span data-stu-id="f2049-109">TZREG</span></span>](tzreg.md)
    
- [<span data-ttu-id="f2049-110">TZRULE</span><span class="sxs-lookup"><span data-stu-id="f2049-110">TZRULE</span></span>](tzrule.md)
    
### <a name="functions"></a><span data-ttu-id="f2049-111">関数</span><span class="sxs-lookup"><span data-stu-id="f2049-111">Functions</span></span>
  
- [<span data-ttu-id="f2049-112">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="f2049-112">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)
    
- [<span data-ttu-id="f2049-113">HrProcessConvActionForSentItem</span><span class="sxs-lookup"><span data-stu-id="f2049-113">HrProcessConvActionForSentItem</span></span>](hrprocessconvactionforsentitem.md)
    
- [<span data-ttu-id="f2049-114">RebaseTaskComplete</span><span class="sxs-lookup"><span data-stu-id="f2049-114">RebaseTaskComplete</span></span>](rebasetaskcomplete.md)
    
- [<span data-ttu-id="f2049-115">RebaseTaskProgress</span><span class="sxs-lookup"><span data-stu-id="f2049-115">RebaseTaskProgress</span></span>](rebasetaskprogress.md)
    
### <a name="interfaces"></a><span data-ttu-id="f2049-116">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="f2049-116">Interfaces</span></span>
  
- [<span data-ttu-id="f2049-117">IOlkApptRebaser</span><span class="sxs-lookup"><span data-stu-id="f2049-117">IOlkApptRebaser</span></span>](iolkapptrebaser.md)
    
### <a name="events"></a><span data-ttu-id="f2049-118">イベント</span><span class="sxs-lookup"><span data-stu-id="f2049-118">Events</span></span>
  
- [<span data-ttu-id="f2049-119">使用可能なイベントの dispid (Outlook エクスポート Api)</span><span class="sxs-lookup"><span data-stu-id="f2049-119">Available events and their dispids (Outlook exported APIs)</span></span>](available-events-and-their-dispids-outlook-exported-apis.md)
    
<span data-ttu-id="f2049-120">また、ディスパッチ識別子、 **dispidFDirty**および **dispidShowSenderPhoto**を使用して実現できます、次のタスク。</span><span class="sxs-lookup"><span data-stu-id="f2049-120">Additionally, using the dispatch identifiers, **dispidFDirty** and **dispidShowSenderPhoto**, you can achieve the following tasks:</span></span>
  
- [<span data-ttu-id="f2049-121">Outlook アイテムが変更されたが保存されていないかどうかを確認する (Outlook の補助リファレンス)</span><span class="sxs-lookup"><span data-stu-id="f2049-121">Determine whether an Outlook item has been modified but not saved (Outlook Auxiliary Reference)</span></span>](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
    
- [<span data-ttu-id="f2049-122">Outlook (Outlook の補助リファレンス) で、連絡先の画像を表示するかどうかを指定</span><span class="sxs-lookup"><span data-stu-id="f2049-122">Specify whether to display a contact's picture in Outlook (Outlook Auxiliary Reference)</span></span>](https://msdn.microsoft.com/en-us/library/office/gg262879.aspx)
    

