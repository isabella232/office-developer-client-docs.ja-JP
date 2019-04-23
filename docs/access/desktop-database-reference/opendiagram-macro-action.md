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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288358"
---
# <a name="opendiagram-macro-action"></a><span data-ttu-id="f1f66-102">OpenDiagram マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="f1f66-102">OpenDiagram macro action</span></span>

<span data-ttu-id="f1f66-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="f1f66-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f1f66-104">In an Access project, you can use the **OpenDiagram** action to open a database diagram in Design view.</span><span class="sxs-lookup"><span data-stu-id="f1f66-104">In an Access project, you can use the **OpenDiagram** action to open a database diagram in Design view.</span></span>

> [!NOTE]
> <span data-ttu-id="f1f66-105">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。</span><span class="sxs-lookup"><span data-stu-id="f1f66-105">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="f1f66-106">設定値</span><span class="sxs-lookup"><span data-stu-id="f1f66-106">Setting</span></span>

<span data-ttu-id="f1f66-107">"OpenDiagram/ダイアグラムを開く" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f1f66-107">The **OpenDiagram** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f1f66-108">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="f1f66-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="f1f66-109">説明</span><span class="sxs-lookup"><span data-stu-id="f1f66-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1f66-110"><strong>Diagram Name/ダイアグラム名</strong></span><span class="sxs-lookup"><span data-stu-id="f1f66-110"><strong>Diagram Name</strong></span></span></p></td>
<td><p><span data-ttu-id="f1f66-111">開くデータベース ダイアグラムの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="f1f66-111">The name of the database diagram to open.</span></span> <span data-ttu-id="f1f66-112">[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>ダイアグラム名</strong>] ボックスには、カレント データベース内のデータベース ダイアグラムがすべて表示されます。</span><span class="sxs-lookup"><span data-stu-id="f1f66-112">The <strong>Diagram Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all database diagrams in the current database.</span></span> <span data-ttu-id="f1f66-113">この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="f1f66-113">This is a required argument.</span></span> <span data-ttu-id="f1f66-114">ライブラリ データベースで "OpenDiagram/ダイアグラムを開く" アクションが定義されているマクロを実行すると、この名前のダイアグラムが、最初にライブラリ データベースで検索され、次にカレント データベースで検索されます。</span><span class="sxs-lookup"><span data-stu-id="f1f66-114">If you run a macro containing the <strong>OpenDiagram</strong> action in a library database, Microsoft Access first looks for the diagram with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="f1f66-115">注釈</span><span class="sxs-lookup"><span data-stu-id="f1f66-115">Remarks</span></span>

<span data-ttu-id="f1f66-116">このアクションの動作は、ナビゲーション ウィンドウでデータベース ダイアグラムをダブルクリックした場合や、ナビゲーション ウィンドウでデータベース ダイアグラムを右クリックして [**デザイン ビュー**] をクリックした場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="f1f66-116">This action is similar to double-clicking a database diagram in the Navigation Pane, or right-clicking the database diagram in the Navigation Pane and then clicking **Design View**.</span></span>

> [!TIP]
> <span data-ttu-id="f1f66-p102">You can drag a database diagram from the Navigation Pane to a macro action row. This automatically creates an **OpenDiagram** action that opens the database diagram in Design view.</span><span class="sxs-lookup"><span data-stu-id="f1f66-p102">You can drag a database diagram from the Navigation Pane to a macro action row. This automatically creates an **OpenDiagram** action that opens the database diagram in Design view.</span></span>

<span data-ttu-id="f1f66-119">To run the **OpenDiagram** action in a Visual Basic for Applications (VBA) module, use the **OpenDiagram** method of the **DoCmd** object.</span><span class="sxs-lookup"><span data-stu-id="f1f66-119">To run the **OpenDiagram** action in a Visual Basic for Applications (VBA) module, use the **OpenDiagram** method of the **DoCmd** object.</span></span>

