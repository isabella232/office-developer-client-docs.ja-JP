---
title: LockNavigationPane マクロ アクション
TOCTitle: LockNavigationPane macro action
ms:assetid: abf7a989-c7cf-3efa-8df4-3c5b075d0e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821487(v=office.15)
ms:contentKeyID: 48546986
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm172454
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7f6ee19edaf2efdc03301e98e709db6dd69f101a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289872"
---
# <a name="locknavigationpane-macro-action"></a><span data-ttu-id="a666a-102">LockNavigationPane マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="a666a-102">LockNavigationPane macro action</span></span>


<span data-ttu-id="a666a-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="a666a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a666a-104">" **LockNavigationPane** /ナビゲーションウィンドウのロック" アクションを使用すると、ナビゲーション ウィンドウに表示されているデータベース オブジェクトをユーザーが削除できないように設定できます。</span><span class="sxs-lookup"><span data-stu-id="a666a-104">You can use the **LockNavigationPane** action to prevent users from deleting database objects that are displayed in the Navigation Pane.</span></span>

## <a name="setting"></a><span data-ttu-id="a666a-105">Setting</span><span class="sxs-lookup"><span data-stu-id="a666a-105">Setting</span></span>

<span data-ttu-id="a666a-106">"LockNavigationPane/ナビゲーションウィンドウのロック" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="a666a-106">The **LockNavigationPane** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a666a-107">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="a666a-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="a666a-108">説明</span><span class="sxs-lookup"><span data-stu-id="a666a-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a666a-109"><strong>Lock</strong></span><span class="sxs-lookup"><span data-stu-id="a666a-109"><strong>Lock</strong></span></span></p></td>
<td><p><span data-ttu-id="a666a-110">ナビゲーションウィンドウをロックするには [<strong>はい</strong>] を、ナビゲーションウィンドウのロックを解除するには [<strong>いいえ</strong>] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a666a-110">Select <strong>Yes</strong> to lock the Navigation Pane, or <strong>No</strong> to unlock the Navigation Pane.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a666a-111">注釈</span><span class="sxs-lookup"><span data-stu-id="a666a-111">Remarks</span></span>

<span data-ttu-id="a666a-112">Locking the Navigation Pane prevents you from deleting database objects or cutting database objects to the clipboard.</span><span class="sxs-lookup"><span data-stu-id="a666a-112">Locking the Navigation Pane prevents you from deleting database objects or cutting database objects to the clipboard.</span></span> <span data-ttu-id="a666a-113">次の操作のいずれかを実行することはでき*ません*。</span><span class="sxs-lookup"><span data-stu-id="a666a-113">It does *not* prevent you from performing any of the following operations:</span></span>

  - <span data-ttu-id="a666a-114">データベース オブジェクトをクリップボードにコピーする</span><span class="sxs-lookup"><span data-stu-id="a666a-114">Copying database objects to the clipboard</span></span>

  - <span data-ttu-id="a666a-115">クリップボードからデータベース オブジェクトを貼り付ける</span><span class="sxs-lookup"><span data-stu-id="a666a-115">Pasting database objects from the clipboard</span></span>

  - <span data-ttu-id="a666a-116">ナビゲーション ウィンドウの表示と非表示を切り替える</span><span class="sxs-lookup"><span data-stu-id="a666a-116">Displaying or hiding the Navigation Pane</span></span>

  - <span data-ttu-id="a666a-117">ナビゲーション ウィンドウのレイアウトを変更する</span><span class="sxs-lookup"><span data-stu-id="a666a-117">Selecting different Navigation Pane organization schemes</span></span>

  - <span data-ttu-id="a666a-118">ナビゲーション ウィンドウのセクションの表示と非表示を切り替える</span><span class="sxs-lookup"><span data-stu-id="a666a-118">Showing or hiding sections of the Navigation Pane</span></span>

<span data-ttu-id="a666a-119">To run the **LockNavigationPane** action in a VBA module, use the **LockNavigationPane** method of the **DoCmd** object.</span><span class="sxs-lookup"><span data-stu-id="a666a-119">To run the **LockNavigationPane** action in a VBA module, use the **LockNavigationPane** method of the **DoCmd** object.</span></span>

