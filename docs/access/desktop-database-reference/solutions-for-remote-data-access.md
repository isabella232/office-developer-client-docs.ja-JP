---
title: リモート データ アクセスのソリューション
TOCTitle: Solutions for Remote Data Access
ms:assetid: ae84c05a-cf9b-2b4c-4d7a-e6c9dcd120c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249825(v=office.15)
ms:contentKeyID: 48547072
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 45164401bbab5cc9134fa7a354fde54bbb02fa37
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604786"
---
# <a name="solutions-for-remote-data-access"></a><span data-ttu-id="a57cc-102">リモート データ アクセスのソリューション</span><span class="sxs-lookup"><span data-stu-id="a57cc-102">Solutions for Remote Data Access</span></span>


<span data-ttu-id="a57cc-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="a57cc-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="the-issue"></a><span data-ttu-id="a57cc-104">問題</span><span class="sxs-lookup"><span data-stu-id="a57cc-104">The Issue</span></span>

<span data-ttu-id="a57cc-p101">ADO では、アプリケーションからデータ ソースに直接アクセスし、データ ソースを変更することができます。これは 2 層システムとも呼ばれます。たとえば、使用するデータが格納されているデータ ソースへの接続は、2 層システムによる直接的な接続です。</span><span class="sxs-lookup"><span data-stu-id="a57cc-p101">ADO enables your application to directly gain access to and modify data sources (sometimes called a two-tier system). For example, if your connection is to the data source that contains your data, that is a direct connection in a two-tier system.</span></span>

<span data-ttu-id="a57cc-p102">一方、Microsoft® インターネット インフォメーション サービス (IIS) などを中継して、データ ソースに間接的にアクセスすることが必要になる場合もあります。この構成は、3 層システムとも呼ばれます。IIS は、ローカル (クライアント) アプリケーションからインターネットまたはイントラネットを介してリモート (サーバー) プログラムを効率的に呼び出すことができるようにするためのクライアント/サーバー システムです。サーバー プログラムからデータ ソースにアクセスし、取得したデータを処理することもできます。</span><span class="sxs-lookup"><span data-stu-id="a57cc-p102">However, you may want to access data sources indirectly through an intermediary such as Microsoft® Internet Information Services (IIS). This arrangement is sometimes called a three-tier system. IIS is a client/server system that provides an efficient way for a local, or client, application to invoke a remote, or server, program across the Internet or an intranet. The server program gains access to the data source and optionally processes the acquired data.</span></span>

<span data-ttu-id="a57cc-111"><<<<<<< ヘッドの例では、イントラネットの Web ページに Microsoft® Visual Basic Scripting Edition (VBScript)、IIS に接続するで作成したアプリケーションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="a57cc-111"><<<<<<< HEAD For example, your intranet Web page contains an application written in Microsoft® Visual Basic Scripting Edition (VBScript), which connects to IIS.</span></span> <span data-ttu-id="a57cc-112">この場合、IIS が実際のデータ ソースに接続してデータを取得し、必要な処理を行って、処理済みの情報をアプリケーションに返します。</span><span class="sxs-lookup"><span data-stu-id="a57cc-112">IIS in turn connects to the actual data source, retrieves the data, processes it in some way, and then returns the processed information to your application.</span></span>
<span data-ttu-id="a57cc-113">=== など、イントラネットの web ページには、Microsoft® Visual Basic Scripting Edition (VBScript)、IIS に接続するで作成したアプリケーションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="a57cc-113">======= For example, your intranet webpage contains an application written in Microsoft® Visual Basic Scripting Edition (VBScript), which connects to IIS.</span></span> <span data-ttu-id="a57cc-114">この場合、IIS が実際のデータ ソースに接続してデータを取得し、必要な処理を行って、処理済みの情報をアプリケーションに返します。</span><span class="sxs-lookup"><span data-stu-id="a57cc-114">IIS in turn connects to the actual data source, retrieves the data, processes it in some way, and then returns the processed information to your application.</span></span>
>>>>>>> <span data-ttu-id="a57cc-115">master</span><span class="sxs-lookup"><span data-stu-id="a57cc-115">master</span></span>

<span data-ttu-id="a57cc-p104">この例では、アプリケーションがデータ ソースに直接接続することはなく、データ ソースへの接続は IIS が行います。また、IIS は ADO を使用してデータにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="a57cc-p104">In this example, your application never directly connected to the data source; IIS did. And IIS accessed the data by means of ADO.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a57cc-p105">[!メモ] クライアント/サーバー アプリケーションは、インターネットまたはイントラネットを基にする (つまり、Web ベースである) 必要はなく、ローカル エリア ネットワーク上のコンパイル済みのプログラムだけで構成される場合もあります。ただし、一般的には Web ベースのアプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="a57cc-p105">The client/server application does not have to be based on the Internet or an intranet (that is, Web-based) — it could consist solely of compiled programs on a local area network. However, the typical case is a Web-based application.</span></span></P>



<span data-ttu-id="a57cc-120">グリッド、チェック ボックス、リストなど、ビジュアル コントロールの中には返される情報を使用するものがあるため、返される情報は、ビジュアル コントロールで容易に使用できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="a57cc-120">Because some visual control, such as a grid, check box, or list, may use the returned information, the returned information must be easily used by a visual control.</span></span>

<span data-ttu-id="a57cc-p106">3 層システムをサポートし、2 層システムで取得する場合と同じように簡単に情報を返す、シンプルで効率の良いアプリケーション プログラミング インターフェイスが望まれます。リモート データ サービス (RDS) が、これに該当するインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="a57cc-p106">You want a simple and efficient application-programming interface that supports three-tier systems, and returns information as easily as if it had been retrieved on a two-tier system. Remote Data Service (RDS) is this interface.</span></span>

## <a name="the-solution"></a><span data-ttu-id="a57cc-123">ソリューション</span><span class="sxs-lookup"><span data-stu-id="a57cc-123">The Solution</span></span>

<span data-ttu-id="a57cc-p107">RDS では、IIS などを中継してデータにアクセスするためのプログラミング モデルが定義されています。このプログラミング モデルは、データ ソースに対するアクセスおよび更新に必要な一連の操作をまとめたものです。プログラミング モデルは、RDS の機能全体の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="a57cc-p107">RDS defines a programming model — the sequence of activities necessary to gain access to and update a data source — to gain access to data through an intermediary, such as Internet Information Services (IIS). The programming model summarizes the entire functionality of RDS.</span></span>

