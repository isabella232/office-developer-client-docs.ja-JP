---
title: CreateObject メソッド (RDS)
TOCTitle: CreateObject method (RDS)
ms:assetid: 130debe5-31cf-4ab0-5f78-9adaec7d7126
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248905(v=office.15)
ms:contentKeyID: 48543360
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 47ad61495bcc96b3099af6273796626e9442cbf0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295374"
---
# <a name="createobject-method-rds"></a><span data-ttu-id="be473-102">CreateObject メソッド (RDS)</span><span class="sxs-lookup"><span data-stu-id="be473-102">CreateObject method (RDS)</span></span>

<span data-ttu-id="be473-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="be473-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="be473-p101">目的のビジネス オブジェクトのプロキシを作成し、そのポインターを返します。プロキシは、インターネット上で要求やデータを送信するビジネス オブジェクトと交信するために、データをパッケージ化し、サーバー側スタブにマーシャリングします。インプロセス コンポーネント オブジェクトでは、プロキシは使用されず、オブジェクトへのポインターのみが返されます。</span><span class="sxs-lookup"><span data-stu-id="be473-p101">Creates the proxy for the target business object and returns a pointer to it. The proxy packages and marshals data to the server-side stub for communications with the business object to send requests and data over the Internet. For in-process component objects, no proxies are used, just a pointer to the object is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="be473-107">構文</span><span class="sxs-lookup"><span data-stu-id="be473-107">Syntax</span></span>

<span data-ttu-id="be473-108">RDS は、HTTP、HTTPS (HTTP over Secure Socket Layer)、DCOM、およびインプロセスのプロトコルをサポートします。</span><span class="sxs-lookup"><span data-stu-id="be473-108">Remote Data Service supports the following protocols: HTTP, HTTPS (HTTP over Secure Socket Layer), DCOM, and in-process.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="be473-109">プロトコル</span><span class="sxs-lookup"><span data-stu-id="be473-109">Protocol</span></span></p></th>
<th><p><span data-ttu-id="be473-110">構文</span><span class="sxs-lookup"><span data-stu-id="be473-110">Syntax</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be473-111">プロトコル</span><span class="sxs-lookup"><span data-stu-id="be473-111">HTTP</span></span></p></td>
<td><p><span data-ttu-id="be473-112"><em>オブジェクト</em> = の<em>スペース</em>を設定します。CreateObject (&quot;<em>ProgId</em>&quot; &quot; <em>https://awebsrvr</em>, &quot;)</span><span class="sxs-lookup"><span data-stu-id="be473-112">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be473-113">HTTPS</span><span class="sxs-lookup"><span data-stu-id="be473-113">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="be473-114"><em>オブジェクト</em> = の<em>スペース</em>を設定します。CreateObject (&quot;<em>ProgId</em>&quot; &quot; <em>https://awebsrvr</em>, &quot;)</span><span class="sxs-lookup"><span data-stu-id="be473-114">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be473-115">DCOM</span><span class="sxs-lookup"><span data-stu-id="be473-115">DCOM</span></span></p></td>
<td><p><span data-ttu-id="be473-116"><em>オブジェクト</em> = の<em>スペース</em>を設定します。CreateObject (&quot;<em>ProgId</em>&quot;、 &quot; <em>computername</em>&quot;)</span><span class="sxs-lookup"><span data-stu-id="be473-116">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>computername</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be473-117">インプロセス</span><span class="sxs-lookup"><span data-stu-id="be473-117">In-process</span></span></p></td>
<td><p><span data-ttu-id="be473-118"><em>オブジェクト</em> = の<em>スペース</em>を設定します。CreateObject (&quot;<em>ProgId</em>&quot;, &quot; &quot;)</span><span class="sxs-lookup"><span data-stu-id="be473-118">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot; &quot;)</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="parameters"></a><span data-ttu-id="be473-119">パラメーター</span><span class="sxs-lookup"><span data-stu-id="be473-119">Parameters</span></span>

|<span data-ttu-id="be473-120">パラメーター</span><span class="sxs-lookup"><span data-stu-id="be473-120">Parameter</span></span>|<span data-ttu-id="be473-121">説明</span><span class="sxs-lookup"><span data-stu-id="be473-121">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="be473-122">*Object*</span><span class="sxs-lookup"><span data-stu-id="be473-122">*Object*</span></span> |<span data-ttu-id="be473-123">*ProgID* に指定された種類のオブジェクトに評価されるオブジェクト変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="be473-123">An object variable that evaluates to an object that is the type specified in *ProgID*.</span></span>|
|<span data-ttu-id="be473-124">*DataSpace*</span><span class="sxs-lookup"><span data-stu-id="be473-124">*DataSpace*</span></span> |<span data-ttu-id="be473-125">新規オブジェクトのインスタンスの作成に使用される [RDS.DataSpace](dataspace-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="be473-125">An object variable that represents an [RDS.DataSpace](dataspace-object-rds.md) object used to create an instance of the new object.</span></span>|
|<span data-ttu-id="be473-126">*ProgID*</span><span class="sxs-lookup"><span data-stu-id="be473-126">*ProgID*</span></span> |<span data-ttu-id="be473-127">アプリケーションのビジネス ルールを適用する、サーバー側のビジネス オブジェクトを指定するプログラム ID を含む文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="be473-127">A **String** value that contains the programmatic identifier specifying a server-side business object that implements your application's business rules.</span></span>|
|<span data-ttu-id="be473-128">*awebsrvr* または *computername*</span><span class="sxs-lookup"><span data-stu-id="be473-128">*awebsrvr* or *computername*</span></span> |<span data-ttu-id="be473-129">サーバービジネスオブジェクトのインスタンスが作成されるインターネットインフォメーションサービス (IIS) web サーバーを識別する URL を表す**文字列型 (String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="be473-129">A **String** value that represents a URL identifying the Internet Information Services (IIS) web server where an instance of the server business object is created.</span></span>|

## <a name="remarks"></a><span data-ttu-id="be473-130">注釈</span><span class="sxs-lookup"><span data-stu-id="be473-130">Remarks</span></span>

<span data-ttu-id="be473-131">*HTTP プロトコル*は標準の web プロトコルです。*HTTPS*はセキュリティで保護された web プロトコルです。</span><span class="sxs-lookup"><span data-stu-id="be473-131">The *HTTP protocol* is the standard web protocol; *HTTPS* is a secure web protocol.</span></span> <span data-ttu-id="be473-132">HTTP を使用せずにローカルエリアネットワークを実行している場合は、 *DCOM プロトコル*を使用します。</span><span class="sxs-lookup"><span data-stu-id="be473-132">Use the *DCOM protocol* when running a local-area network without HTTP.</span></span> <span data-ttu-id="be473-133">*インプロセス*プロトコルは、ローカルのダイナミックリンクライブラリ (DLL) です。ネットワークを使用しません。</span><span class="sxs-lookup"><span data-stu-id="be473-133">The *in-process* protocol is a local dynamic-link library (DLL); it does not use a network.</span></span>

