---
title: OpenDiagram マクロ アクション
TOCTitle: OpenDiagram macro action
ms:assetid: 408e7224-02bb-335a-b1b9-cbccbf6e36ec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192875(v=office.15)
ms:contentKeyID: 48544427
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm154095
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f4273d6858ad98b723d66ba32fe3b9aa7c902d31
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719625"
---
# <a name="opendiagram-macro-action"></a><span data-ttu-id="b961c-102">OpenDiagram マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="b961c-102">OpenDiagram macro action</span></span>

<span data-ttu-id="b961c-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="b961c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b961c-104">Access プロジェクトで、デザイン ビューでデータベース ダイアグラムを開く**OpenDiagram**アクションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="b961c-104">In an Access project, you can use the **OpenDiagram** action to open a database diagram in Design view.</span></span>

> [!NOTE]
> <span data-ttu-id="b961c-105">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。</span><span class="sxs-lookup"><span data-stu-id="b961c-105">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="b961c-106">設定値</span><span class="sxs-lookup"><span data-stu-id="b961c-106">Setting</span></span>

<span data-ttu-id="b961c-107">**OpenDiagram**アクションには、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="b961c-107">The **OpenDiagram** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b961c-108">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="b961c-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="b961c-109">説明</span><span class="sxs-lookup"><span data-stu-id="b961c-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b961c-110"><strong>Diagram Name/ダイアグラム名</strong></span><span class="sxs-lookup"><span data-stu-id="b961c-110"><strong>Diagram Name</strong></span></span></p></td>
<td><p><span data-ttu-id="b961c-111">開くデータベース ダイアグラムの名前です。</span><span class="sxs-lookup"><span data-stu-id="b961c-111">The name of the database diagram to open.</span></span> <span data-ttu-id="b961c-112">マクロ ビルダー] ウィンドウの [<strong>ダイアグラム名</strong>] ボックス、[<strong>アクションの引数</strong>] セクションでは、現在のデータベースのすべてのデータベース ダイアグラムを示しています。</span><span class="sxs-lookup"><span data-stu-id="b961c-112">The <strong>Diagram Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all database diagrams in the current database.</span></span> <span data-ttu-id="b961c-113">この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="b961c-113">This is a required argument.</span></span> <span data-ttu-id="b961c-114">ライブラリ データベースで<strong>OpenDiagram</strong>アクションを含むマクロを実行すると、Microsoft Access は最初にライブラリ データベースで、し、[現在のデータベース内にこの名前のダイアグラムを検索します。</span><span class="sxs-lookup"><span data-stu-id="b961c-114">If you run a macro containing the <strong>OpenDiagram</strong> action in a library database, Microsoft Access first looks for the diagram with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="b961c-115">解説</span><span class="sxs-lookup"><span data-stu-id="b961c-115">Remarks</span></span>

<span data-ttu-id="b961c-116">このアクションの動作は、ナビゲーション ウィンドウでデータベース ダイアグラムをダブルクリックした場合や、ナビゲーション ウィンドウでデータベース ダイアグラムを右クリックして [ **デザイン ビュー**] をクリックした場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="b961c-116">This action is similar to double-clicking a database diagram in the Navigation Pane, or right-clicking the database diagram in the Navigation Pane and then clicking **Design View**.</span></span>

> [!TIP]
> <span data-ttu-id="b961c-117">ナビゲーション ウィンドウからマクロのアクション行にデータベース ダイアグラムをドラッグできます。</span><span class="sxs-lookup"><span data-stu-id="b961c-117">You can drag a database diagram from the Navigation Pane to a macro action row.</span></span> <span data-ttu-id="b961c-118">**OpenDiagram**操作デザイン ビューでデータベース ダイアグラムを開くことが自動的に作成します。</span><span class="sxs-lookup"><span data-stu-id="b961c-118">This automatically creates an **OpenDiagram** action that opens the database diagram in Design view.</span></span>

<span data-ttu-id="b961c-119">**OpenDiagram**アクションを Visual Basic for Applications (VBA) のモジュールで実行するには、 **DoCmd**オブジェクトの**OpenDiagram**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="b961c-119">To run the **OpenDiagram** action in a Visual Basic for Applications (VBA) module, use the **OpenDiagram** method of the **DoCmd** object.</span></span>

