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
# <a name="step-1-set-up-the-visual-basic-project"></a><span data-ttu-id="dff32-102">手順 1: Visual Basic プロジェクトを設定する</span><span class="sxs-lookup"><span data-stu-id="dff32-102">Step 1: Set Up the Visual Basic Project</span></span>


<span data-ttu-id="dff32-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="dff32-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="step-1-set-up-the-visual-basic-project"></a><span data-ttu-id="dff32-104">手順 1: Visual Basic プロジェクトを設定する</span><span class="sxs-lookup"><span data-stu-id="dff32-104">Step 1: Set Up the Visual Basic Project</span></span>

<span data-ttu-id="dff32-105">このシナリオでは、システムに Microsoft Visual Basic 6.0 以降、ADO 2.5 以降、および Microsoft OLE DB Provider for Internet Publishing がインストールされていることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="dff32-105">In this scenario, it is assumed that you have Microsoft Visual Basic 6.0 or later, ADO 2.5 or later, and the Microsoft OLE DB Provider for Internet Publishing installed on your system.</span></span>

<span data-ttu-id="dff32-106">**ADO プロジェクトを作成するには**</span><span class="sxs-lookup"><span data-stu-id="dff32-106">**To create an ADO project**</span></span>

1.  <span data-ttu-id="dff32-107">Microsoft Visual Basic で、新規の標準 EXE プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="dff32-107">In Microsoft Visual Basic, create a new Standard EXE project.</span></span>

2.  <span data-ttu-id="dff32-108">**プロジェクト**] メニューの [**参照設定**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dff32-108">From the **Project** menu, choose **References**.</span></span>

3.  <span data-ttu-id="dff32-109">選択 **"Microsoft ActiveX データ オブジェクトの 2.5 ライブラリ**"[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dff32-109">Select **"Microsoft ActiveX Data Objects 2.5 Library**" and click **OK**.</span></span>

<span data-ttu-id="dff32-110">**メイン フォームにコントロールを挿入するには**</span><span class="sxs-lookup"><span data-stu-id="dff32-110">**To insert controls on the main form**</span></span>

1.  <span data-ttu-id="dff32-p101">Form1 に ListBox コントロールを追加します。その **Name** プロパティを lstMain に設定します。</span><span class="sxs-lookup"><span data-stu-id="dff32-p101">Add a ListBox control to Form1. Set its **Name** property to lstMain.</span></span>

2.  <span data-ttu-id="dff32-p102">Form1 にもう 1 つの ListBox コントロールを追加します。その **Name** プロパティを lstDetails に設定します。</span><span class="sxs-lookup"><span data-stu-id="dff32-p102">Add another ListBox control to Form1. Set its **Name** property to lstDetails.</span></span>

3.  <span data-ttu-id="dff32-p103">Form1 に TextBox コントロールを追加します。その **Name** プロパティを txtDetails に設定します。</span><span class="sxs-lookup"><span data-stu-id="dff32-p103">Add a TextBox control to Form1. Set its **Name** property to txtDetails.</span></span>

