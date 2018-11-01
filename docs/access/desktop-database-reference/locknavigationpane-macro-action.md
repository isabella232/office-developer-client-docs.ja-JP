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
ms.openlocfilehash: 2db34ee9ea56c5fcb4c5aff6afa57c3f59d1f17c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870332"
---
# <a name="locknavigationpane-macro-action"></a><span data-ttu-id="6bcc2-102">"LockNavigationPane/ナビゲーションウィンドウのロック" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="6bcc2-102">LockNavigationPane Macro Action</span></span>


<span data-ttu-id="6bcc2-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="6bcc2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6bcc2-104">" **LockNavigationPane** /ナビゲーションウィンドウのロック" アクションを使用すると、ナビゲーション ウィンドウに表示されているデータベース オブジェクトをユーザーが削除できないように設定できます。</span><span class="sxs-lookup"><span data-stu-id="6bcc2-104">You can use the **LockNavigationPane** action to prevent users from deleting database objects that are displayed in the Navigation Pane.</span></span>

## <a name="setting"></a><span data-ttu-id="6bcc2-105">設定値</span><span class="sxs-lookup"><span data-stu-id="6bcc2-105">Setting</span></span>

<span data-ttu-id="6bcc2-106">**LockNavigationPane**アクションには、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="6bcc2-106">The **LockNavigationPane** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6bcc2-107">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="6bcc2-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="6bcc2-108">説明</span><span class="sxs-lookup"><span data-stu-id="6bcc2-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6bcc2-109"><strong>Lock</strong></span><span class="sxs-lookup"><span data-stu-id="6bcc2-109"><strong>Lock</strong></span></span></p></td>
<td><p><span data-ttu-id="6bcc2-110"><strong>はい</strong>ナビゲーション ウィンドウ] または [<strong>いいえ</strong>ナビゲーション ウィンドウのロックを解除をロックするを選択します。</span><span class="sxs-lookup"><span data-stu-id="6bcc2-110">Select <strong>Yes</strong> to lock the Navigation Pane, or <strong>No</strong> to unlock the Navigation Pane.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6bcc2-111">解説</span><span class="sxs-lookup"><span data-stu-id="6bcc2-111">Remarks</span></span>

<span data-ttu-id="6bcc2-112">ナビゲーション ウィンドウをロックすると、データベース オブジェクトまたはデータベース オブジェクトを切り取ってクリップボードを削除できなくなります。</span><span class="sxs-lookup"><span data-stu-id="6bcc2-112">Locking the Navigation Pane prevents you from deleting database objects or cutting database objects to the clipboard.</span></span> <span data-ttu-id="6bcc2-113">*ない*次の操作のいずれかの操作を実行することを防ぐ。</span><span class="sxs-lookup"><span data-stu-id="6bcc2-113">It does *not* prevent you from performing any of the following operations:</span></span>

  - <span data-ttu-id="6bcc2-114">データベース オブジェクトをクリップボードにコピーする</span><span class="sxs-lookup"><span data-stu-id="6bcc2-114">Copying database objects to the clipboard</span></span>

  - <span data-ttu-id="6bcc2-115">クリップボードからデータベース オブジェクトを貼り付ける</span><span class="sxs-lookup"><span data-stu-id="6bcc2-115">Pasting database objects from the clipboard</span></span>

  - <span data-ttu-id="6bcc2-116">ナビゲーション ウィンドウの表示と非表示を切り替える</span><span class="sxs-lookup"><span data-stu-id="6bcc2-116">Displaying or hiding the Navigation Pane</span></span>

  - <span data-ttu-id="6bcc2-117">ナビゲーション ウィンドウのレイアウトを変更する</span><span class="sxs-lookup"><span data-stu-id="6bcc2-117">Selecting different Navigation Pane organization schemes</span></span>

  - <span data-ttu-id="6bcc2-118">ナビゲーション ウィンドウのセクションの表示と非表示を切り替える</span><span class="sxs-lookup"><span data-stu-id="6bcc2-118">Showing or hiding sections of the Navigation Pane</span></span>

<span data-ttu-id="6bcc2-119">**LockNavigationPane**アクションは、VBA モジュールで実行するには、 **DoCmd**オブジェクトの**LockNavigationPane**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="6bcc2-119">To run the **LockNavigationPane** action in a VBA module, use the **LockNavigationPane** method of the **DoCmd** object.</span></span>

