---
title: "\"MaximizeWindow/ウィンドウの最大化\" マクロ アクション"
TOCTitle: MaximizeWindow Macro Action
ms:assetid: 79c9e430-07a7-02b2-ff5a-c6b9ec32c5b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196171(v=office.15)
ms:contentKeyID: 48545778
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm196948
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b612d050d6c523ae836b21aa27826ff180e8f977
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477688"
---
# <a name="maximizewindow-macro-action"></a>"MaximizeWindow/ウィンドウの最大化" マクロ アクション


**適用されます**Access 2013 |。Office 2013

タブ付きドキュメントではなく重ねて表示されるウィンドウを使用するアクセスを構成する場合は、Access ウィンドウ全体に表示されるので、作業中のウィンドウを拡大する**MaximizeWindow**アクションを使用できます。 このアクションを使用すると、アクティブ ウィンドウ内でのオブジェクトの表示範囲を拡大できます。


> [!NOTE]
> <P>[!メモ] このアクションは、Visual Basic Editor のコード ウィンドウには適用できません。コード ウィンドウへの影響の詳細については、 <STRONG>WindowState</STRONG> プロパティのトピックを参照してください。</P>



## <a name="setting"></a>設定値

**MaximizeWindow**アクション引数はありません。

## <a name="remarks"></a>解説

このアクションは、ウィンドウの右上隅の [**最大化**] ボタンをクリックするか、[**コントロール**] メニューのウィンドウの**最大化**をクリックすると同じです。

**RestoreWindow**アクションを使用すると、元のサイズを最大化したウィンドウを復元します。

**ヒント**

  - アクティブ ウィンドウ以外のウィンドウを最大化したい場合は、 **SelectObject**アクションを使用する必要があります。

  - Access で 1 つのウィンドウを最大化すると、その他のウィンドウを開くときやその他のウィンドウに切り替えたときにも、それらのウィンドウはすべて最大化されます。 ただし、ポップアップ フォームは最大化されません。 他のウィンドウが最大化されたときにそのサイズを維持するためにフォームを実行する場合に、 **[はい]** に、[ **PopUp** ] プロパティを設定します。

モジュールの Visual Basic for Applications の**MaximizeWindow**アクションを実行するには、 **DoCmd**オブジェクトの**最大化**の方法を使用します。

