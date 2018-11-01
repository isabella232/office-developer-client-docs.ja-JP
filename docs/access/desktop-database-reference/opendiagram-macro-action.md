---
title: "'OpenDiagram/ダイアグラムを開く' マクロ アクション"
TOCTitle: OpenDiagram Macro Action
ms:assetid: 408e7224-02bb-335a-b1b9-cbccbf6e36ec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192875(v=office.15)
ms:contentKeyID: 48544427
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm154095
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 3118c2a6b85d400b4b797c4b9b711e5f5a512c62
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869240"
---
# <a name="opendiagram-macro-action"></a><span data-ttu-id="d776d-102">"OpenDiagram/ダイアグラムを開く" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="d776d-102">OpenDiagram Macro Action</span></span>


<span data-ttu-id="d776d-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="d776d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d776d-104">Access プロジェクトで、デザイン ビューでデータベース ダイアグラムを開く**OpenDiagram**アクションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d776d-104">In an Access project, you can use the **OpenDiagram** action to open a database diagram in Design view.</span></span>


> [!NOTE]
> <P><span data-ttu-id="d776d-p101">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。マクロの有効化の詳細については、この記事の「 See Also」セクションのリンクを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d776d-p101">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="d776d-107">設定値</span><span class="sxs-lookup"><span data-stu-id="d776d-107">Setting</span></span>

<span data-ttu-id="d776d-108">**OpenDiagram**アクションには、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="d776d-108">The **OpenDiagram** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d776d-109">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="d776d-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="d776d-110">説明</span><span class="sxs-lookup"><span data-stu-id="d776d-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d776d-111"><strong>Diagram Name/ダイアグラム名</strong></span><span class="sxs-lookup"><span data-stu-id="d776d-111"><strong>Diagram Name</strong></span></span></p></td>
<td><p><span data-ttu-id="d776d-112">開くデータベース ダイアグラムの名前です。</span><span class="sxs-lookup"><span data-stu-id="d776d-112">The name of the database diagram to open.</span></span> <span data-ttu-id="d776d-113">マクロ ビルダー] ウィンドウの [<strong>ダイアグラム名</strong>] ボックス、[<strong>アクションの引数</strong>] セクションでは、現在のデータベースのすべてのデータベース ダイアグラムを示しています。</span><span class="sxs-lookup"><span data-stu-id="d776d-113">The <strong>Diagram Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all database diagrams in the current database.</span></span> <span data-ttu-id="d776d-114">この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="d776d-114">This is a required argument.</span></span> <span data-ttu-id="d776d-115">ライブラリ データベースで<strong>OpenDiagram</strong>アクションを含むマクロを実行すると、Microsoft Access は最初にライブラリ データベースで、し、[現在のデータベース内にこの名前のダイアグラムを検索します。</span><span class="sxs-lookup"><span data-stu-id="d776d-115">If you run a macro containing the <strong>OpenDiagram</strong> action in a library database, Microsoft Access first looks for the diagram with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d776d-116">解説</span><span class="sxs-lookup"><span data-stu-id="d776d-116">Remarks</span></span>

<span data-ttu-id="d776d-117">このアクションの動作は、ナビゲーション ウィンドウでデータベース ダイアグラムをダブルクリックした場合や、ナビゲーション ウィンドウでデータベース ダイアグラムを右クリックして [ **デザイン ビュー**] をクリックした場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="d776d-117">This action is similar to double-clicking a database diagram in the Navigation Pane, or right-clicking the database diagram in the Navigation Pane and then clicking **Design View**.</span></span>


> [!TIP]
> <P><span data-ttu-id="d776d-118">ナビゲーション ウィンドウからマクロのアクション行にデータベース ダイアグラムをドラッグできます。</span><span class="sxs-lookup"><span data-stu-id="d776d-118">You can drag a database diagram from the Navigation Pane to a macro action row.</span></span> <span data-ttu-id="d776d-119"><STRONG>OpenDiagram</STRONG>操作デザイン ビューでデータベース ダイアグラムを開くことが自動的に作成します。</span><span class="sxs-lookup"><span data-stu-id="d776d-119">This automatically creates an <STRONG>OpenDiagram</STRONG> action that opens the database diagram in Design view.</span></span></P>



<span data-ttu-id="d776d-120">**OpenDiagram**アクションを Visual Basic for Applications (VBA) のモジュールで実行するには、 **DoCmd**オブジェクトの**OpenDiagram**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d776d-120">To run the **OpenDiagram** action in a Visual Basic for Applications (VBA) module, use the **OpenDiagram** method of the **DoCmd** object.</span></span>

