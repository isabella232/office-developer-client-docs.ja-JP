---
title: "\"MinimizeWindow/ウィンドウの最小化\" マクロ アクション"
TOCTitle: MinimizeWindow Macro Action
ms:assetid: 3a92b654-15ce-1ed1-63e0-eed927dbe26c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192648(v=office.15)
ms:contentKeyID: 48544265
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm174420
f1_categories:
- Office.Version=v15
ms.openlocfilehash: fd70c3fb41b65ae9c21b1651a6af64912b9c3c7c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2018
ms.locfileid: "25890891"
---
# <a name="minimizewindow-macro-action"></a>"MinimizeWindow/ウィンドウの最小化" マクロ アクション


**適用されます**Access 2013、Office 2013。

タブ付きドキュメントを使用せずにウィンドウを重ねて使用するように Access が構成されている場合、" **MinimizeWindow/ウィンドウの最小化** " アクションを使用してアクティブ ウィンドウを縮小し、Access ウィンドウの下部に小さなタイトル バーとして表示することができます。


> [!NOTE]
> <P>[!メモ] このアクションは、Visual Basic Editor のコード ウィンドウには適用できません。コード ウィンドウへの影響の詳細については、 <STRONG>WindowState</STRONG> プロパティのトピックを参照してください。</P>



## <a name="setting"></a>設定値

**MinimizeWindow**アクション引数はありません。

## <a name="remarks"></a>解説

オブジェクトを開いたまま、ウィンドウを画面から削除するのには、このアクションを使用できます。 オブジェクトを開くウィンドウを表示せずにこの操作を使用することもできます。 オブジェクトを表示するには、 **MaximizeWindow**または**RestoreWindow**のいずれかのアクションに**SelectObject**アクションを使用します。 **RestoreWindow**アクションは、元のサイズを最小化したウィンドウを復元します。

**MinimizeWindow**アクションは、ウィンドウの右上隅の [**最小化**] ボタンをクリックするか、**コントロール**] メニューの [**最小化**] をクリックと同じです。

**ヒント**

  - 最初必要があります作業中のウィンドウ以外のウィンドウを最小化したい場合は、 **SelectObject**アクションを使用します。

  - ナビゲーション ウィンドウを非表示にするには、ナビゲーション ウィンドウに引数が **[はい]** に設定し、 **MinimizeWindow**アクションを使用して**SelectObject**アクションを使用します。 **SelectObject**アクションで選択したオブジェクトは、データベース内のオブジェクトにできます。

  - アクティブ ウィンドウを非表示にするには、[ **表示**] メニューの [ **このウィンドウの管理**] をクリックし、[ **表示しない**] をクリックします。この場合、ウィンドウは最小化されるのではなく、非表示になります。同じく [ **表示**] メニューの [ **再表示**] をクリックすると、ウィンドウを再度表示できます。これらのコマンドをマクロから実行するには、"RunMenuCommand/メニューコマンドの実行" アクションを使用します。

  - フォームのウィンドウを表示または非表示に、フォームの**Visible**プロパティを設定するのには **、アクション**を使用することもできます。

Visual Basic for Applications (VBA) モジュールに**MinimizeWindow**アクションを実行するには、 **DoCmd**オブジェクトの**最小化**の方法を使用します。

