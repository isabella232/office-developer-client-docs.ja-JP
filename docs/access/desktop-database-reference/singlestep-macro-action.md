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
# <a name="singlestep-macro-action"></a>SingleStep マクロ アクション


**適用されます**Access 2013、Office 2013。

**SingleStep** アクションを使用すると、マクロの実行を一時中断して [ **マクロのシングル ステップ**] ダイアログ ボックスを表示できます。

## <a name="setting"></a>設定

**SingleStep** アクションには、引数はありません。

## <a name="remarks"></a>解説

  - **SingleStep** アクションは、正しく動作していないマクロのトラブルシューティングに使用します。マクロ内で問題の原因と考えられるアクションの直前に **SingleStep** アクションを追加できます。このアクションにより、マクロの実行は一時中断され、[ **マクロのシングル ステップ**] ダイアログ ボックスが表示されます。このダイアログ ボックスでは、マクロ名、指定されている条件、アクション名、引数、エラー番号 (該当する場合) などの現在のマクロ アクションに関する情報が表示されます。このダイアログ ボックスでは、次のマクロ アクションへ進むには [ **ステップ**]、現在のマクロおよびその他の実行中のマクロを停止するには [ **すべてのマクロを停止**]、シングル ステップ実行を終了してマクロの通常の処理を再開するには [ **続行**] をクリックします。

  - **SingleStep** アクションの動作は、マクロ ビルダーの [ **デザイン**] タブの [ **ツール**] で [ **シングル ステップ**] をクリックした場合と似ています。この操作を行う場合と **SingleStep** アクションを実行する場合の違いは、このアクションでは、マクロ内でシングル ステップを開始する場所に直接アクションを配置できる点です。そのため、検証するステップより前にあるすべてのアクションを 1 つずつ処理する必要がありません。一方、マクロ ビルダーの [ **シングル ステップ**] をクリックする場合は、マクロを実行する前にクリックする必要があります。その場合、シングル ステップは、マクロの最初のアクションから開始されます。


> [!NOTE]
> <P>[!メモ] [ <STRONG>続行</STRONG>] をクリックせずにマクロの末尾までシングル ステップで実行した場合、マクロが終了してもシングル ステップは有効なままとなります。後続のマクロの実行は、シングル ステップ モードで開始されます。シングル ステップを無効にするには、[ <STRONG>マクロのシングル ステップ</STRONG>] ダイアログ ボックスの [ <STRONG>続行</STRONG>] をクリックするか、デザイン ビューでマクロを開いた状態で [ <STRONG>デザイン</STRONG>] タブの [ <STRONG>ツール</STRONG>] で [ <STRONG>シングル ステップ</STRONG>] をクリックして選択を解除します。</P>


