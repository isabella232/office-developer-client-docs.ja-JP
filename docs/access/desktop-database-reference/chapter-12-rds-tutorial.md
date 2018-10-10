---
title: '12 章: RDS チュートリアル'
TOCTitle: 'Chapter 12: RDS Tutorial'
ms:assetid: fa44a5e8-e4df-dfdd-d7a1-a870ec3cabdd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250277(v=office.15)
ms:contentKeyID: 48548837
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a482da49bb78a74cc68f589c928ffe13dd4a54ad
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479076"
---
# <a name="chapter-12-rds-tutorial"></a><span data-ttu-id="b176d-102">12 章: RDS チュートリアル</span><span class="sxs-lookup"><span data-stu-id="b176d-102">Chapter 12: RDS Tutorial</span></span>


<span data-ttu-id="b176d-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="b176d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b176d-p101">このチュートリアルでは、RDS プログラミング モデルを使用してデータ ソースのクエリおよび更新を行う方法について説明します。最初に、このタスクの実行に必要な手順を説明します。次に、Microsoft® Visual Basic Scripting Edition でのチュートリアル、および、Windows Foundation Classes 用の ADO (ADO/WFC) を使用した Microsoft® Visual J++#174; でのチュートリアルを示します。</span><span class="sxs-lookup"><span data-stu-id="b176d-p101">This tutorial illustrates using the RDS programming model to query and update a data source. First, it describes the steps necessary to accomplish this task. Then the tutorial is repeated in Microsoft® Visual Basic Scripting Edition and Microsoft® Visual J++®, featuring ADO for Windows Foundation Classes (ADO/WFC).</span></span>

<span data-ttu-id="b176d-107">このチュートリアルは、次の 2 つの理由から、複数の言語でコーディングされています。</span><span class="sxs-lookup"><span data-stu-id="b176d-107">This tutorial is coded in different languages for two reasons:</span></span>

  - <span data-ttu-id="b176d-p102">RDS の文書は、Visual Basic でのコーディングを前提にしています。そのため、Visual Basic のプログラマには便利ですが、他の言語を使用するプログラマには不便な場合があります。</span><span class="sxs-lookup"><span data-stu-id="b176d-p102">The documentation for RDS assumes the reader codes in Visual Basic. This makes the documentation convenient for Visual Basic programmers, but less useful for programmers who use other languages.</span></span>

  - <span data-ttu-id="b176d-110">RDS の特定の機能についてわからない場合に、他の言語について多少の知識があれば、他の言語で記述された同じ機能を参照することによって問題を解決できる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b176d-110">If you are uncertain about a particular RDS feature and you know a little of another language, you might be able to resolve your question by looking for the same feature expressed in another language.</span></span>

## <a name="how-the-tutorial-is-presented"></a><span data-ttu-id="b176d-111">このチュートリアルの構成</span><span class="sxs-lookup"><span data-stu-id="b176d-111">How the Tutorial is Presented</span></span>

<span data-ttu-id="b176d-p103">このチュートリアルは、RDS プログラミング モデルに基づいています。プログラミング モデルの各手順を 1 つずつ説明します。さらに、それぞれの手順に Visual Basic コードの一部を示してあります。</span><span class="sxs-lookup"><span data-stu-id="b176d-p103">This tutorial is based on the RDS programming model. It discusses each step of the programming model individually. In addition, it illustrates each step with a fragment of Visual Basic code.</span></span>

<span data-ttu-id="b176d-p104">他の言語についても、コード例を最小限の説明と共に取り上げています。各プログラム言語のチュートリアルの手順には、プログラミング モデルとチュートリアルの説明にある手順に対応する番号が付いています。この手順番号を利用して、対応するチュートリアルの説明を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b176d-p104">The code example is repeated in other languages with minimal discussion. Each step in a given programming language tutorial is marked with the corresponding step in the programming model and descriptive tutorial. Use the number of the step to refer to the discussion in the descriptive tutorial.</span></span>

<span data-ttu-id="b176d-p105">RDS プログラミング モデルについて、次に説明します。チュートリアルを使用するうえでのガイドラインとして使用してください。</span><span class="sxs-lookup"><span data-stu-id="b176d-p105">The RDS programming model is stated below. Use it as a roadmap as you proceed through the tutorial.</span></span>

## <a name="rds-programming-model-with-objects"></a><span data-ttu-id="b176d-120">オブジェクトを使用する RDS プログラミング モデル</span><span class="sxs-lookup"><span data-stu-id="b176d-120">RDS Programming Model with Objects</span></span>

  - <span data-ttu-id="b176d-121">サーバーで呼び出されるプログラムを指定し、クライアントからそのプログラムを参照するための経路 (プロキシ) を取得します。</span><span class="sxs-lookup"><span data-stu-id="b176d-121">Specify the program to be invoked on the server, and obtain a way (proxy) to refer to it from the client.</span></span>

  - <span data-ttu-id="b176d-p106">サーバー プログラムを呼び出します。データ ソースおよび発行するコマンドを識別するためのパラメーターをサーバー プログラムに渡します。</span><span class="sxs-lookup"><span data-stu-id="b176d-p106">Invoke the server program. Pass parameters to the server program that identifies the data source and the command to issue.</span></span>

  - <span data-ttu-id="b176d-p107">サーバー プログラムは、データ ソースから [Recordset](recordset-object-ado.md) オブジェクトを取得します。通常は ADO を使用して取得します。また、サーバー上で **Recordset** オブジェクトを処理することもできます。</span><span class="sxs-lookup"><span data-stu-id="b176d-p107">The server program obtains a [Recordset](recordset-object-ado.md) object from the data source, typically by using ADO. Optionally, the **Recordset** object is processed on the server.</span></span>

  - <span data-ttu-id="b176d-126">サーバー プログラムは、結果の **Recordset** オブジェクトをクライアント アプリケーションに返します。</span><span class="sxs-lookup"><span data-stu-id="b176d-126">The server program returns the final **Recordset** object to the client application.</span></span>

  - <span data-ttu-id="b176d-127">クライアント側では、ビジュアル コントロールを使用すると、必要に応じてフォームに **Recordset** オブジェクトを簡単に配置できます。</span><span class="sxs-lookup"><span data-stu-id="b176d-127">On the client, the **Recordset** object is optionally put into a form that can be easily used by visual controls.</span></span>

  - <span data-ttu-id="b176d-128">**Recordset** オブジェクトに加えられた変更がサーバーに送り返され、その変更がデータ ソースに反映されます。</span><span class="sxs-lookup"><span data-stu-id="b176d-128">Changes to the **Recordset** object are sent back to the server and used to update the data source.</span></span>
