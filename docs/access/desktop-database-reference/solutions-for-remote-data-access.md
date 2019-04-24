---
title: リモート データ アクセスのソリューション
TOCTitle: Solutions for Remote Data Access
ms:assetid: ae84c05a-cf9b-2b4c-4d7a-e6c9dcd120c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249825(v=office.15)
ms:contentKeyID: 48547072
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b64ed19c268874e0e52a87bc2e05aacb6083422
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306903"
---
# <a name="solutions-for-remote-data-access"></a><span data-ttu-id="d33dd-102">リモート データ アクセスのソリューション</span><span class="sxs-lookup"><span data-stu-id="d33dd-102">Solutions for Remote Data Access</span></span>

<span data-ttu-id="d33dd-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="d33dd-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="the-issue"></a><span data-ttu-id="d33dd-104">問題</span><span class="sxs-lookup"><span data-stu-id="d33dd-104">The issue</span></span>

<span data-ttu-id="d33dd-p101">ADO では、アプリケーションからデータ ソースに直接アクセスし、データ ソースを変更することができます。これは 2 層システムとも呼ばれます。たとえば、使用するデータが格納されているデータ ソースへの接続は、2 層システムによる直接的な接続です。</span><span class="sxs-lookup"><span data-stu-id="d33dd-p101">ADO enables your application to directly gain access to and modify data sources (sometimes called a two-tier system). For example, if your connection is to the data source that contains your data, that is a direct connection in a two-tier system.</span></span>

<span data-ttu-id="d33dd-107">ただし、Microsoft インターネットインフォメーションサービス (IIS) などの仲介によって間接的にデータソースにアクセスする必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="d33dd-107">However, you may want to access data sources indirectly through an intermediary such as Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="d33dd-108">この構成は、3 層システムとも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="d33dd-108">This arrangement is sometimes called a three-tier system.</span></span> <span data-ttu-id="d33dd-109">IIS は、ローカル (クライアント) アプリケーションからインターネットまたはイントラネットを介してリモート (サーバー) プログラムを効率的に呼び出すことができるようにするためのクライアント/サーバー システムです。</span><span class="sxs-lookup"><span data-stu-id="d33dd-109">IIS is a client/server system that provides an efficient way for a local, or client, application to invoke a remote, or server, program across the Internet or an intranet.</span></span> <span data-ttu-id="d33dd-110">サーバー プログラムからデータ ソースにアクセスし、取得したデータを処理することもできます。</span><span class="sxs-lookup"><span data-stu-id="d33dd-110">The server program gains access to the data source and optionally processes the acquired data.</span></span>

<span data-ttu-id="d33dd-111">たとえば、イントラネット web ページには、Microsoft Visual Basic Scripting Edition (VBScript) で記述されたアプリケーションが含まれています。これは IIS に接続します。</span><span class="sxs-lookup"><span data-stu-id="d33dd-111">For example, your intranet webpage contains an application written in Microsoft Visual Basic Scripting Edition (VBScript), which connects to IIS.</span></span> <span data-ttu-id="d33dd-112">この場合、IIS が実際のデータ ソースに接続してデータを取得し、必要な処理を行って、処理済みの情報をアプリケーションに返します。</span><span class="sxs-lookup"><span data-stu-id="d33dd-112">IIS in turn connects to the actual data source, retrieves the data, processes it in some way, and then returns the processed information to your application.</span></span>

<span data-ttu-id="d33dd-113">この例では、アプリケーションがデータ ソースに直接接続することはなく、データ ソースへの接続は IIS が行います。</span><span class="sxs-lookup"><span data-stu-id="d33dd-113">In this example, your application never directly connected to the data source; IIS did.</span></span> <span data-ttu-id="d33dd-114">また、IIS は ADO を使用してデータにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="d33dd-114">And IIS accessed the data by means of ADO.</span></span>

> [!NOTE]
> <span data-ttu-id="d33dd-115">クライアント/サーバーアプリケーションは、インターネットまたはイントラネット (つまり web ベース) に基づいている必要はありません。これは、ローカルエリアネットワーク上のコンパイル済みプログラムだけで構成されている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d33dd-115">The client/server application does not have to be based on the Internet or an intranet (that is, web-based)—it could consist solely of compiled programs on a local area network.</span></span> <span data-ttu-id="d33dd-116">ただし、一般的なケースは web ベースのアプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="d33dd-116">However, the typical case is a web-based application.</span></span>

<span data-ttu-id="d33dd-117">グリッド、チェック ボックス、リストなど、ビジュアル コントロールの中には返される情報を使用するものがあるため、返される情報は、ビジュアル コントロールで容易に使用できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="d33dd-117">Because some visual control, such as a grid, check box, or list, may use the returned information, the returned information must be easily used by a visual control.</span></span>

<span data-ttu-id="d33dd-p106">3 層システムをサポートし、2 層システムで取得する場合と同じように簡単に情報を返す、シンプルで効率の良いアプリケーション プログラミング インターフェイスが望まれます。リモート データ サービス (RDS) が、これに該当するインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="d33dd-p106">You want a simple and efficient application-programming interface that supports three-tier systems, and returns information as easily as if it had been retrieved on a two-tier system. Remote Data Service (RDS) is this interface.</span></span>

## <a name="the-solution"></a><span data-ttu-id="d33dd-120">ソリューション</span><span class="sxs-lookup"><span data-stu-id="d33dd-120">The solution</span></span>

<span data-ttu-id="d33dd-121">RDS は、インターネットインフォメーションサービス (IIS) などの仲介を経由してデータにアクセスするために必要な一連のアクティビティであるプログラミングモデル (データソースへのアクセスと更新) を定義します。</span><span class="sxs-lookup"><span data-stu-id="d33dd-121">RDS defines a programming model—the sequence of activities necessary to gain access to and update a data source — to gain access to data through an intermediary, such as Internet Information Services (IIS).</span></span> <span data-ttu-id="d33dd-122">プログラミングモデルは、RDS の機能全体を要約しています。</span><span class="sxs-lookup"><span data-stu-id="d33dd-122">The programming model summarizes the entire functionality of RDS.</span></span>

