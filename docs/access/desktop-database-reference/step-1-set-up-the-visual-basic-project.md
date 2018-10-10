---
title: '手順 1: Visual Basic プロジェクトを設定する'
TOCTitle: 'Step 1: Set Up the Visual Basic Project'
ms:assetid: 1b8195c9-60c8-18a2-3fa2-ffdeed370748
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248954(v=office.15)
ms:contentKeyID: 48543544
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f608d0dadb44a6ddea7a60123d2d6950bc9627cb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477075"
---
# <a name="step-1-set-up-the-visual-basic-project"></a>手順 1: Visual Basic プロジェクトを設定する


**適用されます**Access 2013 |。Office 2013

## <a name="step-1-set-up-the-visual-basic-project"></a>手順 1: Visual Basic プロジェクトを設定する

このシナリオでは、システムに Microsoft Visual Basic 6.0 以降、ADO 2.5 以降、および Microsoft OLE DB Provider for Internet Publishing がインストールされていることを前提としています。

**ADO プロジェクトを作成するには**

1.  Microsoft Visual Basic で、新規の標準 EXE プロジェクトを作成します。

2.  **プロジェクト**] メニューの [**参照設定**] をクリックします。

3.  選択 **"Microsoft ActiveX データ オブジェクトの 2.5 ライブラリ**"[ **OK**] をクリックします。

**メイン フォームにコントロールを挿入するには**

1.  Form1 に ListBox コントロールを追加します。その **Name** プロパティを lstMain に設定します。

2.  Form1 にもう 1 つの ListBox コントロールを追加します。その **Name** プロパティを lstDetails に設定します。

3.  Form1 に TextBox コントロールを追加します。その **Name** プロパティを txtDetails に設定します。

