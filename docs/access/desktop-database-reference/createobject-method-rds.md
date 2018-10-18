---
title: CreateObject メソッド (RDS)
TOCTitle: CreateObject Method (RDS)
ms:assetid: 130debe5-31cf-4ab0-5f78-9adaec7d7126
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248905(v=office.15)
ms:contentKeyID: 48543360
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d2ff2381626e8cf81aa95ee9d49f9396bd4b0316
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602721"
---
# <a name="createobject-method-rds"></a><span data-ttu-id="e7ee8-102">CreateObject メソッド (RDS)</span><span class="sxs-lookup"><span data-stu-id="e7ee8-102">CreateObject Method (RDS)</span></span>


<span data-ttu-id="e7ee8-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="e7ee8-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="e7ee8-p101">目的のビジネス オブジェクトのプロキシを作成し、そのポインターを返します。プロキシは、インターネット上で要求やデータを送信するビジネス オブジェクトと交信するために、データをパッケージ化し、サーバー側スタブにマーシャリングします。インプロセス コンポーネント オブジェクトでは、プロキシは使用されず、オブジェクトへのポインターのみが返されます。</span><span class="sxs-lookup"><span data-stu-id="e7ee8-p101">Creates the proxy for the target business object and returns a pointer to it. The proxy packages and marshals data to the server-side stub for communications with the business object to send requests and data over the Internet. For in-process component objects, no proxies are used, just a pointer to the object is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7ee8-107">構文</span><span class="sxs-lookup"><span data-stu-id="e7ee8-107">Syntax</span></span>

<span data-ttu-id="e7ee8-108">RDS は、HTTP、HTTPS (HTTP over Secure Socket Layer)、DCOM、およびインプロセスのプロトコルをサポートします。</span><span class="sxs-lookup"><span data-stu-id="e7ee8-108">Remote Data Service supports the following protocols: HTTP, HTTPS (HTTP over Secure Socket Layer), DCOM, and in-process.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e7ee8-109">プロトコル</span><span class="sxs-lookup"><span data-stu-id="e7ee8-109">Protocol</span></span></p></th>
<th><p><span data-ttu-id="e7ee8-110">構文</span><span class="sxs-lookup"><span data-stu-id="e7ee8-110">Syntax</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e7ee8-111">HTTP</span><span class="sxs-lookup"><span data-stu-id="e7ee8-111">HTTP</span></span></p></td>
<td><p><span data-ttu-id="e7ee8-112"><em>オブジェクト</em>を設定する = <em>インスタンス</em>。CreateObject (&quot;<em>ProgId</em>&quot;、 &quot; <em>https://awebsrvr</em> &quot;)</span><span class="sxs-lookup"><span data-stu-id="e7ee8-112">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7ee8-113">HTTPS</span><span class="sxs-lookup"><span data-stu-id="e7ee8-113">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="e7ee8-114"><em>オブジェクト</em>を設定する = <em>インスタンス</em>。CreateObject (&quot;<em>ProgId</em>&quot;、 &quot; <em>https://awebsrvr</em> &quot;)</span><span class="sxs-lookup"><span data-stu-id="e7ee8-114">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7ee8-115">DCOM</span><span class="sxs-lookup"><span data-stu-id="e7ee8-115">DCOM</span></span></p></td>
<td><p><span data-ttu-id="e7ee8-116"><em>オブジェクト</em>を設定する = <em>インスタンス</em>。CreateObject (&quot;<em>ProgId</em>&quot;、 &quot;<em>コンピューター名</em>&quot;)</span><span class="sxs-lookup"><span data-stu-id="e7ee8-116">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>computername</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7ee8-117">インプロセス</span><span class="sxs-lookup"><span data-stu-id="e7ee8-117">In-process</span></span></p></td>
<td><p><span data-ttu-id="e7ee8-118"><em>オブジェクト</em>を設定する = <em>インスタンス</em>。CreateObject (&quot;<em>ProgId</em>&quot;、 &quot; &quot;)</span><span class="sxs-lookup"><span data-stu-id="e7ee8-118">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot; &quot;)</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="parameters"></a><span data-ttu-id="e7ee8-119">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e7ee8-119">Parameters</span></span>

  - <span data-ttu-id="e7ee8-120">*Object*</span><span class="sxs-lookup"><span data-stu-id="e7ee8-120">*Object*</span></span>

  - <span data-ttu-id="e7ee8-121">*ProgID* に指定された種類のオブジェクトに評価されるオブジェクト変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="e7ee8-121">An object variable that evaluates to an object that is the type specified in *ProgID*.</span></span>

  - <span data-ttu-id="e7ee8-122">*インスタンス*</span><span class="sxs-lookup"><span data-stu-id="e7ee8-122">*DataSpace*</span></span>

  - <span data-ttu-id="e7ee8-123">新規オブジェクトのインスタンスの作成に使用される [RDS.DataSpace](dataspace-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="e7ee8-123">An object variable that represents an [RDS.DataSpace](dataspace-object-rds.md) object used to create an instance of the new object.</span></span>

  - <span data-ttu-id="e7ee8-124">*ProgID*</span><span class="sxs-lookup"><span data-stu-id="e7ee8-124">*ProgID*</span></span>

  - <span data-ttu-id="e7ee8-125">アプリケーションのビジネス ルールを適用する、サーバー側のビジネス オブジェクトを指定するプログラム ID を含む文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="e7ee8-125">A **String** value that contains the programmatic identifier specifying a server-side business object that implements your application's business rules.</span></span>

  - <span data-ttu-id="e7ee8-126">*awebsrvr*または*コンピューター名*</span><span class="sxs-lookup"><span data-stu-id="e7ee8-126">*awebsrvr* or *computername*</span></span>

<span data-ttu-id="e7ee8-127"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="e7ee8-127"><<<<<<< HEAD</span></span>
  - <span data-ttu-id="e7ee8-128">サーバー ビジネス オブジェクトのインスタンスが作成される、インターネット インフォメーション サービス (IIS) Web サーバーを識別する URL を表す文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="e7ee8-128">A **String** value that represents a URL identifying the Internet Information Services (IIS) Web server where an instance of the server business object is created.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7ee8-129">解説</span><span class="sxs-lookup"><span data-stu-id="e7ee8-129">Remarks</span></span>

<a name="the-http-protocol-is-the-standard-web-protocol-https-is-a-secure-web-protocol-use-the-dcom-protocol-when-running-a-local-area-network-without-http-the-in-process-protocol-is-a-local-dynamic-link-library-dll-it-does-not-use-a-network"></a><span data-ttu-id="e7ee8-130">*HTTP プロトコル*は、標準の Web プロトコルです。*HTTPS*は、セキュリティで保護された Web プロトコルです。</span><span class="sxs-lookup"><span data-stu-id="e7ee8-130">The *HTTP protocol* is the standard Web protocol; *HTTPS* is a secure Web protocol.</span></span> <span data-ttu-id="e7ee8-131">HTTP なしのローカル ・ エリア ・ ネットワークを実行している場合は、 *DCOM プロトコル*を使用します。</span><span class="sxs-lookup"><span data-stu-id="e7ee8-131">Use the *DCOM protocol* when running a local-area network without HTTP.</span></span> <span data-ttu-id="e7ee8-132">*プロセス内*のプロトコルは、ローカルのダイナミック リンク ライブラリ (DLL) です。ネットワークを使用しません。</span><span class="sxs-lookup"><span data-stu-id="e7ee8-132">The *in-process* protocol is a local dynamic-link library (DLL); it does not use a network.</span></span>
=======
  - <span data-ttu-id="e7ee8-133">サーバー ビジネス オブジェクトのインスタンスを作成する、インターネット インフォメーション サービス (IIS) web サーバーを識別する URL を表す**文字列**値。</span><span class="sxs-lookup"><span data-stu-id="e7ee8-133">A **String** value that represents a URL identifying the Internet Information Services (IIS) web server where an instance of the server business object is created.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7ee8-134">備考</span><span class="sxs-lookup"><span data-stu-id="e7ee8-134">Remarks</span></span>

<span data-ttu-id="e7ee8-135">*HTTP プロトコル*は、標準の web プロトコルです。*HTTPS*は、セキュリティで保護された web プロトコルです。</span><span class="sxs-lookup"><span data-stu-id="e7ee8-135">The *HTTP protocol* is the standard web protocol; *HTTPS* is a secure web protocol.</span></span> <span data-ttu-id="e7ee8-136">HTTP なしのローカル ・ エリア ・ ネットワークを実行している場合は、 *DCOM プロトコル*を使用します。</span><span class="sxs-lookup"><span data-stu-id="e7ee8-136">Use the *DCOM protocol* when running a local-area network without HTTP.</span></span> <span data-ttu-id="e7ee8-137">*プロセス内*のプロトコルは、ローカルのダイナミック リンク ライブラリ (DLL) です。ネットワークを使用しません。</span><span class="sxs-lookup"><span data-stu-id="e7ee8-137">The *in-process* protocol is a local dynamic-link library (DLL); it does not use a network.</span></span>
>>>>>>> <span data-ttu-id="e7ee8-138">master</span><span class="sxs-lookup"><span data-stu-id="e7ee8-138">master</span></span>

