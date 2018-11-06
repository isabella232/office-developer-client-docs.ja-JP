---
title: SingleStep マクロ アクション
TOCTitle: SingleStep macro action
ms:assetid: 2836fe1d-fb9b-6b42-acfd-c52e468161d4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191989(v=office.15)
ms:contentKeyID: 48543855
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm47687
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b50fe7e37cfe79a54574e54e720cbad2ef84a14e
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998253"
---
# <a name="singlestep-macro-action"></a><span data-ttu-id="d8270-102">SingleStep マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="d8270-102">SingleStep macro action</span></span>

<span data-ttu-id="d8270-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="d8270-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d8270-104">**SingleStep** アクションを使用すると、マクロの実行を一時中断して [ **マクロのシングル ステップ**] ダイアログ ボックスを表示できます。</span><span class="sxs-lookup"><span data-stu-id="d8270-104">You can use the **SingleStep** action to pause macro execution and open the **Macro Single Step** dialog box.</span></span>

## <a name="setting"></a><span data-ttu-id="d8270-105">設定</span><span class="sxs-lookup"><span data-stu-id="d8270-105">Setting</span></span>

<span data-ttu-id="d8270-106">**SingleStep** アクションには、引数はありません。</span><span class="sxs-lookup"><span data-stu-id="d8270-106">The **SingleStep** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8270-107">解説</span><span class="sxs-lookup"><span data-stu-id="d8270-107">Remarks</span></span>

- <span data-ttu-id="d8270-p101">**SingleStep** アクションは、正しく動作していないマクロのトラブルシューティングに使用します。マクロ内で問題の原因と考えられるアクションの直前に **SingleStep** アクションを追加できます。このアクションにより、マクロの実行は一時中断され、[ **マクロのシングル ステップ**] ダイアログ ボックスが表示されます。このダイアログ ボックスでは、マクロ名、指定されている条件、アクション名、引数、エラー番号 (該当する場合) などの現在のマクロ アクションに関する情報が表示されます。このダイアログ ボックスでは、次のマクロ アクションへ進むには [ **ステップ**]、現在のマクロおよびその他の実行中のマクロを停止するには [ **すべてのマクロを停止**]、シングル ステップ実行を終了してマクロの通常の処理を再開するには [ **続行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d8270-p101">Use the **SingleStep** action to troubleshoot a macro that is not working properly. You can add the **SingleStep** action to a macro just before an action that you suspect may be the cause of the problem. The action pauses the macro and opens the **Macro Single Step** dialog box. This dialog box displays information about the current macro action, such as the macro name, any specified conditions, the action name, arguments, and the error number, if applicable. In the dialog box, you can click **Step** to advance to the next macro action, **Stop All Macros** to stop the current macro and any other macros that are running, or **Continue** to stop single stepping and resume normal operation of the macro.</span></span>

- <span data-ttu-id="d8270-p102">**SingleStep** アクションの動作は、マクロ ビルダーの [ **デザイン**] タブの [ **ツール**] で [ **シングル ステップ**] をクリックした場合と似ています。この操作を行う場合と **SingleStep** アクションを実行する場合の違いは、このアクションでは、マクロ内でシングル ステップを開始する場所に直接アクションを配置できる点です。そのため、検証するステップより前にあるすべてのアクションを 1 つずつ処理する必要がありません。一方、マクロ ビルダーの [ **シングル ステップ**] をクリックする場合は、マクロを実行する前にクリックする必要があります。その場合、シングル ステップは、マクロの最初のアクションから開始されます。</span><span class="sxs-lookup"><span data-stu-id="d8270-p102">The **SingleStep** action has a similar effect to clicking **Single Step** in the **Tools** group on the **Design** tab of the Macro Builder. The difference between doing this and running the **SingleStep** action is that by running the action, you can place the action in the macro exactly where you want single stepping to begin. That way, you don't have to step through all the previous actions to get to the one you want to examine. On the other hand, when you click **Single Step** in the Macro Builder, you must do so before running the macro. In that case, single stepping begins at the first action in the macro.</span></span>

> [!NOTE]
> <span data-ttu-id="d8270-p103">[!メモ] [ **続行**] をクリックせずにマクロの末尾までシングル ステップで実行した場合、マクロが終了してもシングル ステップは有効なままとなります。後続のマクロの実行は、シングル ステップ モードで開始されます。シングル ステップを無効にするには、[ **マクロのシングル ステップ**] ダイアログ ボックスの [ **続行**] をクリックするか、デザイン ビューでマクロを開いた状態で [ **デザイン**] タブの [ **ツール**] で [ **シングル ステップ**] をクリックして選択を解除します。</span><span class="sxs-lookup"><span data-stu-id="d8270-p103">If you single-step all the way to the end of a macro without clicking **Continue**, single stepping will still be in effect when the macro ends. Any subsequent macro you run will start in single step mode. To turn off single stepping, either click **Continue** in the **Macro Single Step** dialog box, or, with a macro open in Design view, on the **Design** tab, in the **Tools** group, click **Single Step** so that it is no longer selected.</span></span>