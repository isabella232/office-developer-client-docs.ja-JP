---
title: MaximizeWindow マクロ アクション
TOCTitle: MaximizeWindow macro action
ms:assetid: 79c9e430-07a7-02b2-ff5a-c6b9ec32c5b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196171(v=office.15)
ms:contentKeyID: 48545778
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm196948
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 262e6781b61018cec3d52dbb930f380d3ff5bd85
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715950"
---
# <a name="maximizewindow-macro-action"></a>MaximizeWindow マクロ アクション

**適用されます**Access 2013、Office 2013。

タブ付きドキュメントではなく重ねて表示されるウィンドウを使用するアクセスを構成する場合は、Access ウィンドウ全体に表示されるので、作業中のウィンドウを拡大する**MaximizeWindow**アクションを使用できます。 このアクションを使用すると、アクティブ ウィンドウ内でのオブジェクトの表示範囲を拡大できます。

> [!NOTE]
> [!メモ] このアクションは、Visual Basic Editor のコード ウィンドウには適用できません。コード ウィンドウへの影響の詳細については、 **WindowState** プロパティのトピックを参照してください。

## <a name="setting"></a>設定値

**MaximizeWindow**アクション引数はありません。

## <a name="remarks"></a>解説

このアクションは、ウィンドウの右上隅の [**最大化**] ボタンをクリックするか、[**コントロール**] メニューのウィンドウの**最大化**をクリックすると同じです。

**RestoreWindow**アクションを使用すると、元のサイズを最大化したウィンドウを復元します。

> [!TIP]
> - アクティブ ウィンドウ以外のウィンドウを最大化したい場合は、 **SelectObject**アクションを使用する必要があります。
> - Access で 1 つのウィンドウを最大化すると、その他のウィンドウを開くときやその他のウィンドウに切り替えたときにも、それらのウィンドウはすべて最大化されます。 ただし、ポップアップ フォームは最大化されません。 他のウィンドウが最大化されたときにそのサイズを維持するためにフォームを実行する場合に、 **[はい]** に、[ **PopUp** ] プロパティを設定します。

モジュールの Visual Basic for Applications の**MaximizeWindow**アクションを実行するには、 **DoCmd**オブジェクトの**最大化**の方法を使用します。

