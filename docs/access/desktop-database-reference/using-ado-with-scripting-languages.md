---
title: スクリプト言語で ADO を使用する
TOCTitle: Using ADO with Scripting Languages
ms:assetid: 2e163ffb-22fe-36f5-9960-8f6bcb148183
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249074(v=office.15)
ms:contentKeyID: 48543985
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1ab0615d1c16900e86a844635fad4ac9a90751a4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698863"
---
# <a name="using-ado-with-scripting-languages"></a><span data-ttu-id="0d299-102">スクリプトの言語での ADO の使用</span><span class="sxs-lookup"><span data-stu-id="0d299-102">Using ADO with scripting languages</span></span>


<span data-ttu-id="0d299-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="0d299-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0d299-104">スクリプト環境では、ADO を使用することで、サーバー側スクリプトによりデータを公開できます。</span><span class="sxs-lookup"><span data-stu-id="0d299-104">Within a scripting environment, ADO allows you to expose data by way of server-side scripting.</span></span> <span data-ttu-id="0d299-105">このシナリオでは、ADO、ADO が利用する基盤の OLE DB プロバイダー、および特定のデータ ストアを参照するために必要な他のコンポーネントが、インターネット インフォメーション サービス (IIS) を実行するサーバーにインストールされます。</span><span class="sxs-lookup"><span data-stu-id="0d299-105">In this scenario, ADO, the underlying OLE DB provider that it utilizes, and any other components needed to reference a given data store are installed on a server running Internet Information Services (IIS).</span></span> <span data-ttu-id="0d299-106">たとえば、Active Server Pages (ASP) を使用する場合、ADO は HTML を生成できるスクリプトで参照されるコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="0d299-106">Using Active Server Pages (ASP), ADO is a component referenced in a script that can generate HTML, for example.</span></span> <span data-ttu-id="0d299-107">この HTML コンテンツは、HTTP 経由でクライアントの web ブラウザーに渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="0d299-107">This HTML content can be passed via HTTP to a client web browser.</span></span> <span data-ttu-id="0d299-108">スクリプトを使用する web ページは、更新、移動、および特定のデータを表示することを許可する、サーバー側スクリプトにアクションを送信できます。</span><span class="sxs-lookup"><span data-stu-id="0d299-108">Through the use of scripting, the webpage can send actions back to the server-side script, allowing you to update, traverse, or view specific data.</span></span>

## <a name="odbc-data-sources"></a><span data-ttu-id="0d299-109">ODBC データ ソース</span><span class="sxs-lookup"><span data-stu-id="0d299-109">ODBC Data Sources</span></span>

<span data-ttu-id="0d299-p102">スクリプト ADO コードと非スクリプト ADO コードの大きな違いの 1 つは、ODBC データ ソースです (使用した場合)。非スクリプト アプリケーションの場合、ODBC データ ソース アドミニストレーターでユーザー DSN を作成できます。IIS で実行するスクリプトの場合は、システム DSN を作成する必要があります。システム DSN を作成しないと、スクリプトは作成したデータ ソースを認識できません。このことは、Microsoft IIS を通して Microsoft OLE DB Provider for ODBC を使用するすべての ADO スクリプト アプリケーションに当てはまります。</span><span class="sxs-lookup"><span data-stu-id="0d299-p102">One notable difference between scripting and non-scripting ADO code is the ODBC Data Source, if used. For non-scripting applications, you can create a User DSN in the ODBC Data Source Administrator. For scripts that are running under IIS, you must create a System DSN; otherwise your scripts won't recognize the data source you created. This applies to any ADO scripting application using the Microsoft OLE DB Provider for ODBC through Microsoft IIS.</span></span>

## <a name="referencing-the-ado-library"></a><span data-ttu-id="0d299-114">ADO ライブラリの参照</span><span class="sxs-lookup"><span data-stu-id="0d299-114">Referencing the ADO Library</span></span>

<span data-ttu-id="0d299-115">スクリプト言語では使用できません。</span><span class="sxs-lookup"><span data-stu-id="0d299-115">N/A with scripting languages.</span></span>

## <a name="handling-events"></a><span data-ttu-id="0d299-116">イベントの処理</span><span class="sxs-lookup"><span data-stu-id="0d299-116">Handling events</span></span>

<span data-ttu-id="0d299-117">スクリプト言語では使用できません。</span><span class="sxs-lookup"><span data-stu-id="0d299-117">N/A with scripting languages.</span></span>

<span data-ttu-id="0d299-118">以下のトピックでは、スクリプト言語で ADO を使用する方法を詳細に説明しています。</span><span class="sxs-lookup"><span data-stu-id="0d299-118">The following topics contain more specific information about using ADO with scripting languages:</span></span>

- [<span data-ttu-id="0d299-119">JScript での ADO プログラミング</span><span class="sxs-lookup"><span data-stu-id="0d299-119">JScript ADO Programming</span></span>](jscript-ado-programming.md)

- [<span data-ttu-id="0d299-120">VBScript での ADO プログラミング</span><span class="sxs-lookup"><span data-stu-id="0d299-120">VBScript ADO Programming</span></span>](vbscript-ado-programming.md)
