---
title: スクリプト言語で ADO を使用する
TOCTitle: Using ADO with Scripting Languages
ms:assetid: 2e163ffb-22fe-36f5-9960-8f6bcb148183
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249074(v=office.15)
ms:contentKeyID: 48543985
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2de5cd9507ede3308a207b078a5bc66a4917e267
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479541"
---
# <a name="using-ado-with-scripting-languages"></a><span data-ttu-id="62d6f-102">スクリプト言語で ADO を使用する</span><span class="sxs-lookup"><span data-stu-id="62d6f-102">Using ADO with Scripting Languages</span></span>


<span data-ttu-id="62d6f-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="62d6f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="62d6f-p101">スクリプト環境では、ADO を使用することで、サーバー側スクリプトによりデータを公開できます。このシナリオでは、ADO、ADO が利用する基盤の OLE DB プロバイダー、および特定のデータ ストアを参照するために必要な他のコンポーネントが、インターネット インフォメーション サービス (IIS) を実行するサーバーにインストールされます。たとえば、Active Server Pages (ASP) を使用する場合、ADO は HTML を生成できるスクリプトで参照されるコンポーネントです。この HTML コンテンツは、HTTP を介してクライアントの Web ブラウザーに渡すことができます。スクリプトを使用すると、Web ページからサーバー側スクリプトにアクションを戻して、特定のデータを更新、移動、および表示することができます。</span><span class="sxs-lookup"><span data-stu-id="62d6f-p101">Within a scripting environment, ADO allows you to expose data by way of server-side scripting. In this scenario, ADO, the underlying OLE DB provider that it utilizes, and any other components needed to reference a given data store are installed on a server running Internet Information Services (IIS). Using Active Server Pages (ASP), ADO is a component referenced in a script that can generate HTML, for example. This HTML content can be passed via HTTP to a client Web browser. Through the use of scripting, the Web page can send actions back to the server-side script, allowing you to update, traverse, or view specific data.</span></span>

## <a name="odbc-data-sources"></a><span data-ttu-id="62d6f-109">ODBC データ ソース</span><span class="sxs-lookup"><span data-stu-id="62d6f-109">ODBC Data Sources</span></span>

<span data-ttu-id="62d6f-p102">スクリプト ADO コードと非スクリプト ADO コードの大きな違いの 1 つは、ODBC データ ソースです (使用した場合)。非スクリプト アプリケーションの場合、ODBC データ ソース アドミニストレーターでユーザー DSN を作成できます。IIS で実行するスクリプトの場合は、システム DSN を作成する必要があります。システム DSN を作成しないと、スクリプトは作成したデータ ソースを認識できません。このことは、Microsoft IIS を通して Microsoft OLE DB Provider for ODBC を使用するすべての ADO スクリプト アプリケーションに当てはまります。</span><span class="sxs-lookup"><span data-stu-id="62d6f-p102">One notable difference between scripting and non-scripting ADO code is the ODBC Data Source, if used. For non-scripting applications, you can create a User DSN in the ODBC Data Source Administrator. For scripts that are running under IIS, you must create a System DSN; otherwise your scripts won't recognize the data source you created. This applies to any ADO scripting application using the Microsoft OLE DB Provider for ODBC through Microsoft IIS.</span></span>

## <a name="referencing-the-ado-library"></a><span data-ttu-id="62d6f-114">ADO ライブラリの参照</span><span class="sxs-lookup"><span data-stu-id="62d6f-114">Referencing the ADO Library</span></span>

<span data-ttu-id="62d6f-115">スクリプト言語では使用できません。</span><span class="sxs-lookup"><span data-stu-id="62d6f-115">N/A with scripting languages.</span></span>

## <a name="handling-events"></a><span data-ttu-id="62d6f-116">イベントの処理</span><span class="sxs-lookup"><span data-stu-id="62d6f-116">Handling events</span></span>

<span data-ttu-id="62d6f-117">スクリプト言語では使用できません。</span><span class="sxs-lookup"><span data-stu-id="62d6f-117">N/A with scripting languages.</span></span>

<span data-ttu-id="62d6f-118">以下のトピックでは、スクリプト言語で ADO を使用する方法を詳細に説明しています。</span><span class="sxs-lookup"><span data-stu-id="62d6f-118">The following topics contain more specific information about using ADO with scripting languages:</span></span>

  - [<span data-ttu-id="62d6f-119">VBScript での ADO プログラミング</span><span class="sxs-lookup"><span data-stu-id="62d6f-119">ADO in VBScript</span></span>](vbscript-ado-programming.md)

  - [<span data-ttu-id="62d6f-120">JScript での ADO プログラミング</span><span class="sxs-lookup"><span data-stu-id="62d6f-120">ADO in JScript</span></span>](jscript-ado-programming.md)

