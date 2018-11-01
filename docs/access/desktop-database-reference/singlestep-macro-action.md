---
title: SingleStep マクロ アクション
TOCTitle: SingleStep Macro Action
ms:assetid: 2836fe1d-fb9b-6b42-acfd-c52e468161d4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191989(v=office.15)
ms:contentKeyID: 48543855
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm47687
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7bee12bb26c4ed3799fce2481e7d9329aa5d1e61
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868960"
---
# <a name="singlestep-macro-action"></a><span data-ttu-id="623d4-102">SingleStep マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="623d4-102">SingleStep Macro Action</span></span>


<span data-ttu-id="623d4-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="623d4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="623d4-104">**SingleStep** アクションを使用すると、マクロの実行を一時中断して [ **マクロのシングル ステップ**] ダイアログ ボックスを表示できます。</span><span class="sxs-lookup"><span data-stu-id="623d4-104">You can use the **SingleStep** action to pause macro execution and open the **Macro Single Step** dialog box.</span></span>

## <a name="setting"></a><span data-ttu-id="623d4-105">設定</span><span class="sxs-lookup"><span data-stu-id="623d4-105">Setting</span></span>

<span data-ttu-id="623d4-106">**SingleStep** アクションには、引数はありません。</span><span class="sxs-lookup"><span data-stu-id="623d4-106">The **SingleStep** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="623d4-107">解説</span><span class="sxs-lookup"><span data-stu-id="623d4-107">Remarks</span></span>

  - <span data-ttu-id="623d4-p101">**SingleStep** アクションは、正しく動作していないマクロのトラブルシューティングに使用します。マクロ内で問題の原因と考えられるアクションの直前に **SingleStep** アクションを追加できます。このアクションにより、マクロの実行は一時中断され、[ **マクロのシングル ステップ**] ダイアログ ボックスが表示されます。このダイアログ ボックスでは、マクロ名、指定されている条件、アクション名、引数、エラー番号 (該当する場合) などの現在のマクロ アクションに関する情報が表示されます。このダイアログ ボックスでは、次のマクロ アクションへ進むには [ **ステップ**]、現在のマクロおよびその他の実行中のマクロを停止するには [ **すべてのマクロを停止**]、シングル ステップ実行を終了してマクロの通常の処理を再開するには [ **続行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="623d4-p101">Use the **SingleStep** action to troubleshoot a macro that is not working properly. You can add the **SingleStep** action to a macro just before an action that you suspect may be the cause of the problem. The action pauses the macro and opens the **Macro Single Step** dialog box. This dialog box displays information about the current macro action, such as the macro name, any specified conditions, the action name, arguments, and the error number, if applicable. In the dialog box, you can click **Step** to advance to the next macro action, **Stop All Macros** to stop the current macro and any other macros that are running, or **Continue** to stop single stepping and resume normal operation of the macro.</span></span>

  - <span data-ttu-id="623d4-p102">**SingleStep** アクションの動作は、マクロ ビルダーの [ **デザイン**] タブの [ **ツール**] で [ **シングル ステップ**] をクリックした場合と似ています。この操作を行う場合と **SingleStep** アクションを実行する場合の違いは、このアクションでは、マクロ内でシングル ステップを開始する場所に直接アクションを配置できる点です。そのため、検証するステップより前にあるすべてのアクションを 1 つずつ処理する必要がありません。一方、マクロ ビルダーの [ **シングル ステップ**] をクリックする場合は、マクロを実行する前にクリックする必要があります。その場合、シングル ステップは、マクロの最初のアクションから開始されます。</span><span class="sxs-lookup"><span data-stu-id="623d4-p102">The **SingleStep** action has a similar effect to clicking **Single Step** in the **Tools** group on the **Design** tab of the Macro Builder. The difference between doing this and running the **SingleStep** action is that by running the action, you can place the action in the macro exactly where you want single stepping to begin. That way, you don't have to step through all the previous actions to get to the one you want to examine. On the other hand, when you click **Single Step** in the Macro Builder, you must do so before running the macro. In that case, single stepping begins at the first action in the macro.</span></span>


> [!NOTE]
> <P><span data-ttu-id="623d4-p103">[!メモ] [ <STRONG>続行</STRONG>] をクリックせずにマクロの末尾までシングル ステップで実行した場合、マクロが終了してもシングル ステップは有効なままとなります。後続のマクロの実行は、シングル ステップ モードで開始されます。シングル ステップを無効にするには、[ <STRONG>マクロのシングル ステップ</STRONG>] ダイアログ ボックスの [ <STRONG>続行</STRONG>] をクリックするか、デザイン ビューでマクロを開いた状態で [ <STRONG>デザイン</STRONG>] タブの [ <STRONG>ツール</STRONG>] で [ <STRONG>シングル ステップ</STRONG>] をクリックして選択を解除します。</span><span class="sxs-lookup"><span data-stu-id="623d4-p103">If you single-step all the way to the end of a macro without clicking <STRONG>Continue</STRONG>, single stepping will still be in effect when the macro ends. Any subsequent macro you run will start in single step mode. To turn off single stepping, either click <STRONG>Continue</STRONG> in the <STRONG>Macro Single Step</STRONG> dialog box, or, with a macro open in Design view, on the <STRONG>Design</STRONG> tab, in the <STRONG>Tools</STRONG> group, click <STRONG>Single Step</STRONG> so that it is no longer selected.</span></span></P>


