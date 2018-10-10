---
title: "'LockNavigationPane/ナビゲーションウィンドウのロック' マクロ アクション"
TOCTitle: LockNavigationPane Macro Action
ms:assetid: abf7a989-c7cf-3efa-8df4-3c5b075d0e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821487(v=office.15)
ms:contentKeyID: 48546986
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm172454
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4e18b17c5d00095b61323511c20b95a355819eab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478825"
---
# <a name="locknavigationpane-macro-action"></a><span data-ttu-id="de7f1-102">"LockNavigationPane/ナビゲーションウィンドウのロック" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="de7f1-102">LockNavigationPane Macro Action</span></span>


<span data-ttu-id="de7f1-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="de7f1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="de7f1-104">" **LockNavigationPane** /ナビゲーションウィンドウのロック" アクションを使用すると、ナビゲーション ウィンドウに表示されているデータベース オブジェクトをユーザーが削除できないように設定できます。</span><span class="sxs-lookup"><span data-stu-id="de7f1-104">You can use the **LockNavigationPane** action to prevent users from deleting database objects that are displayed in the Navigation Pane.</span></span>

## <a name="setting"></a><span data-ttu-id="de7f1-105">設定値</span><span class="sxs-lookup"><span data-stu-id="de7f1-105">Setting</span></span>

<span data-ttu-id="de7f1-106">**LockNavigationPane**アクションには、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="de7f1-106">The **LockNavigationPane** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="de7f1-107">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="de7f1-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="de7f1-108">説明</span><span class="sxs-lookup"><span data-stu-id="de7f1-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="de7f1-109"><strong>Lock</strong></span><span class="sxs-lookup"><span data-stu-id="de7f1-109"><strong>Lock</strong></span></span></p></td>
<td><p><span data-ttu-id="de7f1-110"><strong>はい</strong>ナビゲーション ウィンドウ] または [<strong>いいえ</strong>ナビゲーション ウィンドウのロックを解除をロックするを選択します。</span><span class="sxs-lookup"><span data-stu-id="de7f1-110">Select <strong>Yes</strong> to lock the Navigation Pane, or <strong>No</strong> to unlock the Navigation Pane.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="de7f1-111">解説</span><span class="sxs-lookup"><span data-stu-id="de7f1-111">Remarks</span></span>

<span data-ttu-id="de7f1-112">ナビゲーション ウィンドウをロックすると、データベース オブジェクトまたはデータベース オブジェクトを切り取ってクリップボードを削除できなくなります。</span><span class="sxs-lookup"><span data-stu-id="de7f1-112">Locking the Navigation Pane prevents you from deleting database objects or cutting database objects to the clipboard.</span></span> <span data-ttu-id="de7f1-113">*ない*次の操作のいずれかの操作を実行することを防ぐ。</span><span class="sxs-lookup"><span data-stu-id="de7f1-113">It does *not* prevent you from performing any of the following operations:</span></span>

  - <span data-ttu-id="de7f1-114">データベース オブジェクトをクリップボードにコピーする</span><span class="sxs-lookup"><span data-stu-id="de7f1-114">Copying database objects to the clipboard</span></span>

  - <span data-ttu-id="de7f1-115">クリップボードからデータベース オブジェクトを貼り付ける</span><span class="sxs-lookup"><span data-stu-id="de7f1-115">Pasting database objects from the clipboard</span></span>

  - <span data-ttu-id="de7f1-116">ナビゲーション ウィンドウの表示と非表示を切り替える</span><span class="sxs-lookup"><span data-stu-id="de7f1-116">Displaying or hiding the Navigation Pane</span></span>

  - <span data-ttu-id="de7f1-117">ナビゲーション ウィンドウのレイアウトを変更する</span><span class="sxs-lookup"><span data-stu-id="de7f1-117">Selecting different Navigation Pane organization schemes</span></span>

  - <span data-ttu-id="de7f1-118">ナビゲーション ウィンドウのセクションの表示と非表示を切り替える</span><span class="sxs-lookup"><span data-stu-id="de7f1-118">Showing or hiding sections of the Navigation Pane</span></span>

<span data-ttu-id="de7f1-119">**LockNavigationPane**アクションは、VBA モジュールで実行するには、 **DoCmd**オブジェクトの**LockNavigationPane**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="de7f1-119">To run the **LockNavigationPane** action in a VBA module, use the **LockNavigationPane** method of the **DoCmd** object.</span></span>

