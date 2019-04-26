---
title: Recordset メソッド (DAO)
TOCTitle: Methods
ms:assetid: 8b713eda-b076-4190-b2f5-ff1ce522e2bf
ms:mtpsurl: https://msdn.microsoft.com/library/Dn125237(v=office.15)
ms:contentKeyID: 52073361
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: bf064212e71019f303b6fa7e9bb9360306dfa3c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300484"
---
# <a name="recordset-methods-dao"></a><span data-ttu-id="db5de-102">Recordset メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="db5de-102">Recordset Methods (DAO)</span></span>

<span data-ttu-id="db5de-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="db5de-103">**Applies to**: Access 2013, Office 2013</span></span>

- [<span data-ttu-id="db5de-104">Recordset.AddNew メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="db5de-104">Recordset.AddNew Method (DAO)</span></span>](recordset-addnew-method-dao.md)
- [<span data-ttu-id="db5de-105">Recordset.Cancel メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="db5de-105">Recordset.Cancel Method (DAO)</span></span>](recordset-cancel-method-dao.md)
- [<span data-ttu-id="db5de-106">Recordset.CancelUpdate メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="db5de-106">Recordset.CancelUpdate Method (DAO)</span></span>](recordset-cancelupdate-method-dao.md)
- [<span data-ttu-id="db5de-107">Recordset.Clone メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="db5de-107">Recordset.Clone Method (DAO)</span></span>](recordset-clone-method-dao.md)
- [<span data-ttu-id="db5de-108">Recordset.Close メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="db5de-108">Recordset.Close Method (DAO)</span></span>](recordset-close-method-dao.md)
- [<span data-ttu-id="db5de-109">Recordset.CopyQueryDef メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="db5de-109">Recordset.CopyQueryDef Method (DAO)</span></span>](recordset-copyquerydef-method-dao.md)
- [<span data-ttu-id="db5de-110">Recordset.Delete メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="db5de-110">Recordset.Delete Method (DAO)</span></span>](recordset-delete-method-dao.md)
- [<span data-ttu-id="db5de-111">Recordset.Edit メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="db5de-111">Recordset.Edit Method (DAO)</span></span>](recordset-edit-method-dao.md)
- [<span data-ttu-id="db5de-112">Recordset.FillCache メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="db5de-112">Recordset.FillCache Method (DAO)</span></span>](recordset-fillcache-method-dao.md)
- [<span data-ttu-id="db5de-113">Recordset.FindFirst メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="db5de-113">Recordset.FindFirst Method (DAO)</span></span>](recordset-findfirst-method-dao.md)
- [<span data-ttu-id="db5de-114">Recordset.FindLast メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="db5de-114">Recordset.FindLast method (DAO)</span></span>](recordset-findlast-method-dao.md)
- [<span data-ttu-id="db5de-115">Recordset.FindNext メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="db5de-115">Recordset.FindNext Method (DAO)</span></span>](recordset-findnext-method-dao.md)
- [<span data-ttu-id="db5de-116">Recordset.FindPrevious メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="db5de-116">Recordset.FindPrevious Method (DAO)</span></span>](recordset-findprevious-method-dao.md)
- [<span data-ttu-id="db5de-117">Recordset.GetRows メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="db5de-117">Recordset.GetRows Method (DAO)</span></span>](recordset-getrows-method-dao.md)
- <span data-ttu-id="db5de-118">[Recordset.Move メソッド (DAO)](recordset-move-method-dao.md)</span><span class="sxs-lookup"><span data-stu-id="db5de-118">[](recordset-move-method-dao.md)Recordset.Move Method (DAO)</span></span>
- <span data-ttu-id="db5de-119">[Recordset.MoveFirst メソッド (DAO)](recordset-movefirst-method-dao.md)</span><span class="sxs-lookup"><span data-stu-id="db5de-119">[](recordset-movefirst-method-dao.md)Recordset.MoveFirst Method (DAO)</span></span>
- <span data-ttu-id="db5de-120">[Recordset.MoveLast メソッド (DAO)](recordset-movelast-method-dao.md)</span><span class="sxs-lookup"><span data-stu-id="db5de-120">[](recordset-movelast-method-dao.md)Recordset.MoveLast Method (DAO)</span></span>
- <span data-ttu-id="db5de-121">[ Recordset.MoveNext メソッド (DAO)](recordset-movenext-method-dao.md)</span><span class="sxs-lookup"><span data-stu-id="db5de-121">[](recordset-movenext-method-dao.md)Recordset.MoveNext Method (DAO)</span></span>
- <span data-ttu-id="db5de-122">[Recordset.MovePrevious メソッド (DAO)](recordset-moveprevious-method-dao.md)</span><span class="sxs-lookup"><span data-stu-id="db5de-122">[](recordset-moveprevious-method-dao.md)Recordset.MovePrevious Method (DAO)</span></span>
- <span data-ttu-id="db5de-123">[Recordset.NextRecordset メソッド (DAO)](recordset-nextrecordset-method-dao.md)</span><span class="sxs-lookup"><span data-stu-id="db5de-123">[](recordset-nextrecordset-method-dao.md)Recordset.NextRecordset Method (DAO)</span></span>
- <span data-ttu-id="db5de-124">[Recordset.OpenRecordset メソッド (DAO)](recordset-openrecordset-method-dao.md)</span><span class="sxs-lookup"><span data-stu-id="db5de-124">[](recordset-openrecordset-method-dao.md)Recordset.OpenRecordset Method (DAO)</span></span>
- <span data-ttu-id="db5de-125">[Recordset.Requery メソッド (DAO)](recordset-requery-method-dao.md)</span><span class="sxs-lookup"><span data-stu-id="db5de-125">[](recordset-requery-method-dao.md)Recordset.Requery Method (DAO)</span></span>
- [<span data-ttu-id="db5de-126">Recordset.Seek メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="db5de-126">Recordset.Seek Method (DAO)</span></span>](recordset-seek-method-dao.md)
- [<span data-ttu-id="db5de-127">Recordset.Update メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="db5de-127">Recordset.Update Method (DAO)</span></span>](recordset-update-method-dao.md)


