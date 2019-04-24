---
title: ADO を使って行える操作
TOCTitle: What You Can Do With ADO
ms:assetid: 98246cb0-aec6-6a77-c953-85895ad83a5d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249681(v=office.15)
ms:contentKeyID: 48546483
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5b7d0bab179cd7ec658bc04cee05f486947f38c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306021"
---
# <a name="what-you-can-do-with-ado"></a><span data-ttu-id="298b3-102">ADO でできること</span><span class="sxs-lookup"><span data-stu-id="298b3-102">What you can do with ADO</span></span>


<span data-ttu-id="298b3-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="298b3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="298b3-p101">ADO は、強力で論理的なオブジェクト モデルを開発者に提供し、OLE DB システムを介したさまざまなデータ ソースへのアクセス、編集および更新をプログラムによって実行できるようにします。ADO の最も一般的な使用方法には、リレーショナル データベースのテーブルの照会、アプリケーションでの結果の取得と表示、ユーザーによるデータの変更と保存を可能にすることなどがあります。ADO を使用してプログラムで実行できるその他の処理には、次のような処理があります。</span><span class="sxs-lookup"><span data-stu-id="298b3-p101">ADO is designed to provide developers with a powerful, logical object model for programmatically accessing, editing, and updating a wide variety of data sources through OLE DB system interfaces. The most common usage of ADO is to query a table or tables in a relational database, retrieve and display the results in an application, and perhaps allow users to make and save changes to the data. Other things that can be done programmatically with ADO include:</span></span>

- <span data-ttu-id="298b3-107">SQL を使用してデータベースを照会し、結果を表示します。</span><span class="sxs-lookup"><span data-stu-id="298b3-107">Querying a database using SQL and displaying the results.</span></span>

- <span data-ttu-id="298b3-108">インターネットでファイル ストア内の情報にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="298b3-108">Accessing information in a file store over the Internet.</span></span>

- <span data-ttu-id="298b3-109">電子メールシステム内のメッセージとフォルダーを操作します。</span><span class="sxs-lookup"><span data-stu-id="298b3-109">Manipulating messages and folders in an email system.</span></span>

- <span data-ttu-id="298b3-110">データベースのデータを XML ファイルに保存します。</span><span class="sxs-lookup"><span data-stu-id="298b3-110">Saving data from a database into an XML file.</span></span>

- <span data-ttu-id="298b3-111">ユーザーがデータベース テーブル内のデータを確認および変更できるようにします。</span><span class="sxs-lookup"><span data-stu-id="298b3-111">Allowing a user to review and make changes to data in database tables.</span></span>

- <span data-ttu-id="298b3-112">パラメーター化されたデータベース コマンドを作成して再利用します。</span><span class="sxs-lookup"><span data-stu-id="298b3-112">Creating and reusing parameterized database commands.</span></span>

- <span data-ttu-id="298b3-113">ストアド プロシージャを実行します。</span><span class="sxs-lookup"><span data-stu-id="298b3-113">Executing stored procedures.</span></span>

- <span data-ttu-id="298b3-114">**Recordset** と呼ばれる柔軟な構造を動的に作成して、データを保持、移動、および操作します。</span><span class="sxs-lookup"><span data-stu-id="298b3-114">Dynamically creating a flexible structure, called a **Recordset**, to hold, navigate, and manipulate data.</span></span>

- <span data-ttu-id="298b3-115">トランザクションによるデータベース操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="298b3-115">Performing transactional database operations.</span></span>

- <span data-ttu-id="298b3-116">実行時の基準に基づいて、データベース情報のローカル コピーをフィルター処理し、並べ替えます。</span><span class="sxs-lookup"><span data-stu-id="298b3-116">Filtering and sorting local copies of database information based on run-time criteria.</span></span>

- <span data-ttu-id="298b3-117">データベースから階層構造の結果を作成して操作します。</span><span class="sxs-lookup"><span data-stu-id="298b3-117">Creating and manipulating hierarchical results from databases.</span></span>

- <span data-ttu-id="298b3-118">データベース フィールドをデータを認識するコンポーネントにバインドします。</span><span class="sxs-lookup"><span data-stu-id="298b3-118">Binding database fields to data-aware components.</span></span>

- <span data-ttu-id="298b3-119">リモートの非接続 **Recordset** を作成します。</span><span class="sxs-lookup"><span data-stu-id="298b3-119">Creating remote, disconnected **Recordsets**.</span></span>

<span data-ttu-id="298b3-p102">このような柔軟性を提供するために、ADO は広範なオプションや設定を公開する必要があります。したがって、アプリケーションでの ADO の使用方法を系統立てて習得し、各目標を対処可能な要素に分割することが重要です。</span><span class="sxs-lookup"><span data-stu-id="298b3-p102">ADO must expose a wide variety of options and settings in order to provide such flexibility. Therefore it's important to take a methodical approach to learning how to use ADO in an application, breaking down each of your goals into manageable pieces.</span></span>

<span data-ttu-id="298b3-p103">ほとんどの ADO プログラムには、データの取得、検査、編集、および更新の 4 つの主要な操作があります。次からの 4 つの章では、これらの操作について詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="298b3-p103">Four primary operations are involved in most ADO programs: getting data, examining data, editing data, and updating data. The next four chapters examine each of these operations in more detail.</span></span>

<span data-ttu-id="298b3-p104">次に進む前に、ADO のオブジェクト モデルのオブジェクトに精通しておく必要があります。次に、「[HelloData: 単純な ADO アプリケーション](hellodata-a-simple-ado-application.md)」を確認してください。このアプリケーションは Visual Basic で記述されており、4 つの主要な各 ADO 操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="298b3-p104">Before proceeding, familiarize yourself with the objects in the ADO Object Model. Then review [HelloData: A Simple ADO Application](hellodata-a-simple-ado-application.md). This application is written in Visual Basic and performs each of the four primary ADO operations.</span></span>

